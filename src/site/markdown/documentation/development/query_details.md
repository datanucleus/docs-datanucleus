<head><title>Query Process Details</title></head>

# Section : [Documentation](../index.html) > [Development](index.html)

## Query Compilation and Evaluation

DataNucleus provides a _generic_ query processing engine. It provides for compilation of __string-based query languages__. 
Additionally it allows _in-memory evaluation_ of these queries. This is very useful when providing support for new datastores which either
don't have a native query language and so the only alternative is for DataNucleus to evaluate the queries, or where it will take some time 
to map the compiled query to the equivalent query in the native language of the datastore.

### Input Processing

When a user invokes a query, using the JDO/JPA APIs, they are providing either

* A single-string query made up of keywords and clauses
* A query object that has the clauses specified directly

The first step is to convert these two forms into the constituent clauses. It is assumed that a string-based query is of the form

	SELECT {resultClause} FROM {fromClause} WHERE {filterClause}
	GROUP BY {groupingClause} HAVING {havingClause}
	ORDER BY {orderClause}]]></source>

The two primary supported query languages have helper classes to provide this migration from the _single-string query form_ into the individual clauses. 
These can be found in _org.datanucleus.query.JDOQLSingleStringParser_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/JDOQLSingleStringParser.html)
and _org.datanucleus.query.JPQLSingleStringParser_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/JPQLSingleStringParser.html).

### Compilation

So we have a series of clauses and we want to compile them. So what does this mean? Well, in simple terms, we are going to convert the individual clauses 
from above into expression tree(s) so that they can be evaluated. The end result of a compilation is a _org.datanucleus.query.compiler.QueryCompilation_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/compiler/QueryCompilation.html).

So if you think about a typical query you may have

	SELECT field1, field2 FROM MyClass

This has 2 result expressions - field1, and field2 (where they are each a "PrimaryExpression" meaning a representation of a field).
The query compilation of a particular clauses has 2 stages

1. Compilation into a Node tree, with operations between the nodes
2. Compilation of the Node tree into an Expression tree of supported expressions

and compilation is performed by a JavaQueryCompiler, so look at _org.datanucleus.query.compiler.JDOQLCompiler_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/compiler/JDOQLCompiler.html)
and _org.datanucleus.query.compiler.JPQLCompiler_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/compiler/JPQLCompiler.html).
These each have a Parser that performs the extraction of the different components of the clauses and generation of the Node tree. 
Once a Node tree is generated it can then be converted into the compiled Expression tree; this is handled inside the JavaQueryCompiler.

The other part of a query compilation is the _org.datanucleus.query.symbol.SymbolTable_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/symbol/SymbolTable.html)
which is a lookup table (map) of identifiers and their value. So, for example, an input parameter will have a name, so has an entry in 
the table, and its value is stored there. This is then used during evaluation.

### Evaluation : In-datastore

Intuitively it is more efficient to evaluate a query within the datastore since it means that fewer actual result objects need 
instantiating in order to determine the result objects. To evaluate a compiled query in the datastore there needs to be a compiler 
for taking the generic expression compilation and converting it into a native query. Additionally it should be noted that you aren't 
forced to evaluate the whole of the query in the datastore, maybe just the filter clause. This would be done where the datastore 
native language maybe only provides a limited amount of query capabilities. For example with db4o we evaluated the _filter_ and 
_ordering_ in the datastore, using their SODA query language. The remaining clauses can be evaluated on the resultant objects 
_in-memory_ (see below). Obviously for a datastore like RDBMS it should be possible to evaluate the whole query in-datastore.

### Evaluation : In-memory

Evaluation of queries in-memory assumes that we have a series of "candidate" objects. These are either user-input to the query itself, 
or retrieved from the datastore. We then use the in-memory evaluator _org.datanucleus.query.evaluator.memory.InMemoryExpressionEvaluator_
[![Javadoc](../../images/javadoc.gif)](http://www.datanucleus.org/javadocs/core/latest/org/datanucleus/query/evaluator/memory/InMemoryExpressionEvaluator.html).
This takes in each candidate object one-by-one and evaluates whichever of the query clauses are desired to be evaluated. 
For example we could just evaluate the filter clause. Evaluation makes use of the values of the fields of the candidate objects 
(and related objects) and uses the SymbolTable for values of parameters etc. Where a candidate fails a particular clause 
in the filter then it is excluded from the results.

### Results

There are two primary ways to return results to the user.

* Instantiate all into memory and return a (java.util.)List. This is the simplest, but obviously can impact on memory footprint.
* Return a wrapper to a List, and intercept calls so that you can load objects as they are accessed. This is more complex, 
but has the advantage of not imposing a large footprint on the application.

To make use of the second route, consider extending the class _org.datanucleus.store.query.AbstractQueryResult_ and implement the key methods.
Also, for the iterator, you can extend _org.datanucleus.store.query.AbstractQueryResultIterator_.
