<head><title>AccessPlatform 4.0.0.M4</title></head>

# DataNucleus AccessPlatform 4.0.0.M4

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.0.M4 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_0_m4.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__29th May 2014__ - DataNucleus AccessPlatform 4.0.0.M4 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1216'>NUCCORE-1216</a>] -         Allow option of Query results being closed when ExecutionContext is closed
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-49'>NUCCASSANDRA-49</a>] -         Support schema creation &quot;USING&quot; options via metadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-11'>NUCJAVAEIGHT-11</a>] -         Add support for Instant persisted as Long (numeric)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-12'>NUCJAVAEIGHT-12</a>] -         Support for OffsetTime, OffsetDateTime
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1203'>NUCCORE-1203</a>] -         Logging around transactional cache enlist/evict is far from optimum and can just show evictions
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1208'>NUCCORE-1208</a>] -         Transaction cache cpu improvement
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1209'>NUCCORE-1209</a>] -         Constructor cache in IdentityManagerImpl
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1210'>NUCCORE-1210</a>] -         Configuration.getManagerOverrideableProperties() costs quite a lot of cpu during ExecutionContext creation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1212'>NUCCORE-1212</a>] -         Change Localisation sub-system to allow each plugin to register its bundle, and specify language/errorCodes via System properties
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1213'>NUCCORE-1213</a>] -         Cache frequently accessed properties in fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1214'>NUCCORE-1214</a>] -         Cache populated ClassMetadata
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1215'>NUCCORE-1215</a>] -         org.datanucleus.store.types.SCO should be genericised with the java type it represents
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1217'>NUCCORE-1217</a>] -         Refactor ExecutionContext callback handler method names to make clearer their usage
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1219'>NUCCORE-1219</a>] -         Add method to AbstractJavaQuery to compile the query to get just the generic compilation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-75'>NUCAPIJDO-75</a>] -         Decrease lock contention during PersistenceManager.close()
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1195'>NUCCORE-1195</a>] -         Upgrade ASM to 5.0.2
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1196'>NUCCORE-1196</a>] -         Make StoreManager.getStrategyForNative public
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1197'>NUCCORE-1197</a>] -         Various ApiAdapter methods are now no longer needed since we use a DataNucleus-centric enhancement contract
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1198'>NUCCORE-1198</a>] -         Drop org.datanucleus.metadata.PersistenceFlags, now part of Persistable interface
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1200'>NUCCORE-1200</a>] -         ExecutionContext.newQuery is not needed and all queries should be instantiated via QueryManager
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1201'>NUCCORE-1201</a>] -         Move query language name conversion to JDO API layer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1205'>NUCCORE-1205</a>] -         Add accessor for the StoreManager for the managed object
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1206'>NUCCORE-1206</a>] -         Add TypeConverter for Calendar to (millis, timezone)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1207'>NUCCORE-1207</a>] -         Collection wrappers (with backing store) should likely throw IllegalXXXException when add() fails in the datastore
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1211'>NUCCORE-1211</a>] -         Change QueryManager to be interface, with default implementation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1218'>NUCCORE-1218</a>] -         org.datanucleus.metadata.FieldRole should be enum to give type safety
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-271'>NUCJPA-271</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-273'>NUCJPA-273</a>] -         JPAAnnotationReader has line which sets jdbcType of all boolean fields to SMALLINT. No reason why we need this so disable
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCAPIJDO-74'>NUCAPIJDO-74</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-794'>NUCRDBMS-794</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-796'>NUCRDBMS-796</a>] -         Change default Calendar persistence to single column (timestamp)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-798'>NUCRDBMS-798</a>] -         PostgreSQL : support OFFSET/FETCH for ranges
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-799'>NUCRDBMS-799</a>] -         PostgreSQL : add dummy BOOLEAN JDBC type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-801'>NUCRDBMS-801</a>] -         PostgreSQL : add dummy TINYINT JDBC type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCNEODATIS-30'>NUCNEODATIS-30</a>] -         Support NUCCORE-1197 removing methods from ApiAdapter
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCESS-128'>NUCACCESS-128</a>] -         Migrate projects to standard maven 2 layout
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCESS-129'>NUCACCESS-129</a>] -         Release own version of javax.persistence jar and remove use of EclipseLink JPA API jar
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1199'>NUCCORE-1199</a>] -         Improve logic for transient id handling to check for null
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1202'>NUCCORE-1202</a>] -         Missing release resource in non-tx handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-270'>NUCJPA-270</a>] -         JPA spec 2.10.3.1 requires a unique constraint on a OneToOne unidir relation by default
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJPA-272'>NUCJPA-272</a>] -         Query.getParameter methods using position return that parameter is not found for JPQL
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-795'>NUCRDBMS-795</a>] -         Query with aggreg.function on single-column calendar field doesn't work due to wrong metadata handling
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-797'>NUCRDBMS-797</a>] -         MSSQL OFFSET is not optional when using FETCH
</li>
</ul>

