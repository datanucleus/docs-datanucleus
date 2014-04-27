<head><title>AccessPlatform 4.0.0.M3</title></head>

# DataNucleus AccessPlatform 4.0.0.M3

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.0.M3 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_0_m3.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__27th April 2014__ - DataNucleus AccessPlatform 4.0.0.M3 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-74'>NUCEXCEL-74</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-7'>NUCCASSANDRA-7</a>] -         Support in-datastore querying of primary JDOQL/JPQL operations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-47'>NUCCASSANDRA-47</a>] -         Support schema evolution (new columns, delete columns)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-47'>NUCJSON-47</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-50'>NUCJSON-50</a>] -         Supported embedded 1-1 fields stored as nested in the JSON object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-55'>NUCODF-55</a>] -         Support multicolumn TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-9'>NUCJAVAEIGHT-9</a>] -         Support LocalTime, LocalDate, LocalDateTime getSecond, getMinute, getHour, getDayOfMonth, getMonth, getYear in in-memory query evaluation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-10'>NUCJAVAEIGHT-10</a>] -         Support getHour, getMinute, getSecond, getYear, getMonthValue, getDayOfMonth method invocation on LocalXXX classes with RDBMS
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-922'>NUCCORE-922</a>] -         JPA : Enhance classes to implement org.datanucleus.enhancer.Persistable to avoid dependency on JDO
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1097'>NUCCORE-1097</a>] -         Genericise ExecutionContext/ObjectProvider interfaces
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1175'>NUCCORE-1175</a>] -         Rename &quot;org.datanucleus.store.types.simple&quot; to &quot;org.datanucleus.store.types.wrappers&quot;, and &quot;org.datanucleus.store.types.backed&quot; to &quot;org.datanucleus.store.types.wrappers.backed&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1176'>NUCCORE-1176</a>] -         Add TypeConverters for converting Boolean to &quot;Y&quot;/&quot;N&quot; and 1,0
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1181'>NUCCORE-1181</a>] -         JDOQL/JPQL : add compiler checks for use of aggregate in result clause with incorrect arguments
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1186'>NUCCORE-1186</a>] -         ValueGeneration class is pointless and should be removed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-73'>NUCAPIJDO-73</a>] -         Support NUCCORE-922 (change bytecode enhancement contract)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-269'>NUCJPA-269</a>] -         Support NUCCORE-922 (change bytecode enhancement contract)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-48'>NUCJSON-48</a>] -         javadoc improvements according to JDK1.8 warning and errors
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-782'>NUCRDBMS-782</a>] -         Add Expression/Literal for handling TypeConverterMapping so we can avoid having to create Expression/Literal (and hence XXXMapping) for more types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-8'>NUCJAVAEIGHT-8</a>] -         Refactor so that root package is org.datanucleus.store.types.java8
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-20'>NUCJODATIME-20</a>] -         Refactor so that root package is org.datanucleus.store.types.jodatime
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-8'>NUCGUAVA-8</a>] -         Refactor so that root package is org.datanucleus.store.types.guava
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-934'>NUCCORE-934</a>] -         Restrict all references to PersistenceCapable/Detachable to isolated packages
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1173'>NUCCORE-1173</a>] -         Remove checks on &quot;stackmapFrames&quot; since we are using JDK 1.7+ now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1174'>NUCCORE-1174</a>] -         Upgrade to javax.cache v1.0.0 now that final is out
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1177'>NUCCORE-1177</a>] -         Rename &quot;org.datanucleus.query.evaluator.memory&quot; to &quot;org.datanucleus.query.inmemory&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1178'>NUCCORE-1178</a>] -         Names of in-memory query evaluators are too verbose
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1180'>NUCCORE-1180</a>] -         Add StoreManager.OPTION_ORM_EMBEDDED_PC_NESTED to signify that the store supports embedding an object nested in the owner object (like JSON)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1182'>NUCCORE-1182</a>] -         Split runReachability out of ObjectProvider so that ReachabilityFieldManager is the only place we provide the pbr-at-commit process
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1183'>NUCCORE-1183</a>] -         Move NullCallbackHandler to org.datanucleus.state
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1184'>NUCCORE-1184</a>] -         Move ObjectProvider.nullifyFields() to ExecutionContextImpl reachability at commit code
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1185'>NUCCORE-1185</a>] -         org.datanucleus.query.node adds no value and should be merged into org.datanucleus.query.compiler
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1187'>NUCCORE-1187</a>] -         ExecutionContext newObjectProviderForEmbedded are simply relays and should be removed; use ObjectProviderFactory direct
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1190'>NUCCORE-1190</a>] -         Change bytecode enhancement of copyKeyFieldsToObjectId to avoid use of JDOHelper
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1191'>NUCCORE-1191</a>] -         Remove EclipsePluginRegistry
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1194'>NUCCORE-1194</a>] -         Drop support for &lt;extension vendor-name=&quot;jpox&quot; ...&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-76'>NUCEXCEL-76</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-50'>NUCCASSANDRA-50</a>] -         If user specified jdbc-type of &quot;char&quot;, override with &quot;varchar&quot; internally (since there is no &quot;char&quot; in Cassandra)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-51'>NUCCASSANDRA-51</a>] -         IncrementGenerator should use key as &quot;sequence-name&quot; if provided (user input), otherwise &quot;field-name&quot; if for a field, otherwise &quot;root-class-name&quot;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-52'>NUCCASSANDRA-52</a>] -         Detect members using TypeConverter with datastore type of subclass of java.util.Date, and change to converter with datastoreType=java.util.Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-53'>NUCCASSANDRA-53</a>] -         Move to Datastax Cassandra driver v2.0.1
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-54'>NUCCASSANDRA-54</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-92'>NUCHBASE-92</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-49'>NUCJSON-49</a>] -         Use Base64 under org.datanucleus.util instead of own copy
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-51'>NUCJSON-51</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCLDAP-62'>NUCLDAP-62</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-144'>NUCMONGODB-144</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEOFORJ-48'>NUCNEOFORJ-48</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-57'>NUCODF-57</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-785'>NUCRDBMS-785</a>] -         Support NUCCORE-1175
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-787'>NUCRDBMS-787</a>] -         SQLMethod method should have signature getExpression(SQLExpression, List&lt;SQLExpression&gt;) i.e include generics
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-789'>NUCRDBMS-789</a>] -         Support NUCCORE-1197
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-791'>NUCRDBMS-791</a>] -         Drop use of &quot;java-version&quot; on java types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-51'>NUCSPATIAL-51</a>] -         Add TypeConverter for Rectangle -&gt; x,y,width,height  and fix Point -&gt; x,y to use int
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-52'>NUCSPATIAL-52</a>] -         Add multicolumn TypeConverter for Point2D.Double and Point2D.Float
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-7'>NUCGUAVA-7</a>] -         Support NUCCORE-1175
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCGUAVA-9'>NUCGUAVA-9</a>] -         Support NUCCORE-1197
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1188'>NUCCORE-1188</a>] -         PersistenceUnit &quot;exclude-unlisted-classes&quot; is processed incorrectly ignoring the value in the element
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1193'>NUCCORE-1193</a>] -         Bad code in JavaUtils.initialiseJREVersion() [in general] // fails on Android [in concrete]
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-268'>NUCJPA-268</a>] -         inconsistent property name: javax.persistence.sql.load-script-source
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-783'>NUCRDBMS-783</a>] -         AVG on integral number drops decimals on some databases
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-784'>NUCRDBMS-784</a>] -         MapSizeMethod uses wrapper Map rather than java.util.Map!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-786'>NUCRDBMS-786</a>] -         Catch special case SQL method classes (ARRAY etc) to avoid ClassNotResolvedException
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCSPATIAL-49'>NUCSPATIAL-49</a>] -         OSGi manifest is missing some package imports
</li>
</ul>

