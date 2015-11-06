<head><title>AccessPlatform 4.2.1</title></head>

# DataNucleus AccessPlatform 4.2.1

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.2.1 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_2_1.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__6th November 2015__ - DataNucleus AccessPlatform 4.2.1 ("Planck") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-970'>NUCRDBMS-970</a>] -         SQLStatement needs a way of generation where we don't use table aliases, and just use table names
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-977'>NUCRDBMS-977</a>] -         Support persisting a Collection/Map using a TypeConverter for the whole field
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-971'>NUCRDBMS-971</a>] -         SQLite doesn't provide explicit support for putting nulls last, but can use &quot;{col} IS NULL, {col}&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-972'>NUCRDBMS-972</a>] -         View creation : skip any token that is a &quot;comment&quot; since some RDBMS don't handle that
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-973'>NUCRDBMS-973</a>] -         Delete tables processing : goes off and calls DatabaseMetaData.getColumns for detection of table existence but could just get table type (quicker!)
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-322'>NUCJPA-322</a>] -         Support AttributeConverter on a collection field to be for the whole field not just the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-975'>NUCRDBMS-975</a>] -         Provide access to RDBMSQueryCompilation, and to the SQLStatement(s) that the compilation is made up of.
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1355'>NUCCORE-1355</a>] -         JPQLSingleStringParser has missing trimRight handling (typo in trimLeft)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1356'>NUCCORE-1356</a>] -         Metadata processing moves ColumnMetaData to ElementMetaData is not embedded/serialised but should also allow for full field type converter case
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-112'>NUCAPIJDO-112</a>] -         @Convert specified on field doesn't always get processed. Works fine when using @Persistent(converter=...)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-974'>NUCRDBMS-974</a>] -         Oracle, Firebird require that when using GROUP BY, all non-aggregate SELECT components are in the GROUP BY clause
</li>
</ul>

