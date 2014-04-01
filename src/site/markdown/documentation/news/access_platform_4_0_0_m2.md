<head><title>AccessPlatform 4.0.0.M2</title></head>

# DataNucleus AccessPlatform 4.0.0.M2

<div id="dzone_vote_widget" style="float: left; margin-right: 8px;">
    <script type="text/javascript">var dzone_title = 'DataNucleus AccessPlatform 4.0.0.M2 Released';</script>
    <script type="text/javascript">var dzone_url = 'http://www.datanucleus.org/documentation/news/access_platform_4_0_0_m2.html';</script>
    <script type="text/javascript" language="javascript" src="http://widgets.dzone.com/widgets/zoneit.js"></script>
</div>

__1st April 2014__ - DataNucleus AccessPlatform 4.0.0.M2 ("Einstein") is released.
DataNucleus Access Platform provides persistence and retrieval of Java objects to/from a wide range of datastores including RDBMS, Neo4j, MongoDB, LDAP, XML, and Excel.
This release is available under the [Apache 2 license](http://www.datanucleus.org/documentation/license.html) from our [download page](http://www.datanucleus.org/download.html) 
This release includes the following changes over the previous release


## New Feature

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1147'>NUCCORE-1147</a>] -         Extend datanucleus.readOnlyDatastore so that it can be specified on a PM
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1154'>NUCCORE-1154</a>] -         Add TypeConverter extension for converting object to multiple components, from java type to multiple datastore types
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1160'>NUCCORE-1160</a>] -         Support javax.validation annotations @Size, @NotNull to imply metadata and avoid the need to duplicate that information with JDO/JPA annotations
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1163'>NUCCORE-1163</a>] -         Allow a TypeConverter to define the default length limit of a String column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-3'>NUCCASSANDRA-3</a>] -         Support optimistic versioning
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-18'>NUCCASSANDRA-18</a>] -         Support non-PC collections, maps
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-28'>NUCCASSANDRA-28</a>] -         Support members (fields/properties) mapped to more than 1 column
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-29'>NUCCASSANDRA-29</a>] -         Default to Session per PMF/EMF, but allow persistence property to set it
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-35'>NUCCASSANDRA-35</a>] -         Support compound identity
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-36'>NUCCASSANDRA-36</a>] -         Support user-defined TypeConverter on field/property
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-37'>NUCCASSANDRA-37</a>] -         Support TypeConverter &quot;autoApply&quot; so user can define default handling for a java type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-27'>NUCJSON-27</a>] -         Support embedded 1-1 fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-771'>NUCRDBMS-771</a>] -         Support HikariCP connection pool
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCECLIPSE-6'>NUCACCECLIPSE-6</a>] -         DataNucleus Context Menu does not appear in Project Explorer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-7'>NUCJAVAEIGHT-7</a>] -         Add support for Duration, Period, Year, Month, DayOfWeek, YearMonth, MonthDay, ZoneId, Instant, OffsetTime, OffsetDateTime, ZonedDateTime
</li>
</ul>


## Improvement

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1144'>NUCCORE-1144</a>] -         Update NamingFactory to take a set of reserved keywords that an identifier has to be quoted to use
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1145'>NUCCORE-1145</a>] -         Provide TypeConverters for byte[], int[], float[], etc to ByteBuffer and clean up TypeConversionHelper type safety
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1157'>NUCCORE-1157</a>] -         Split TypeManager converter helpers out into TypeConverterHelper
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1164'>NUCCORE-1164</a>] -         Add TypeConverters for javax.time LocalDateTime -&gt; Timestamp, LocalTime -&gt; Time, LocalDate -&gt; Date
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1166'>NUCCORE-1166</a>] -         Extend CompleteClassTable to support multiple columns per member
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1172'>NUCCORE-1172</a>] -         Some calls to ObjectProvider.loadUnloadedFields only require relation fields loading
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-25'>NUCCASSANDRA-25</a>] -         Change javaType-datastoreType conversion process to use TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-30'>NUCCASSANDRA-30</a>] -         Support persistence of members of type Locale (or array of Locale)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-42'>NUCCASSANDRA-42</a>] -         Support cascadePersist/cascadeUpdate for reachability
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-43'>NUCCASSANDRA-43</a>] -         Support interface fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-75'>NUCEXCEL-75</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-56'>NUCODF-56</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-46'>NUCJSON-46</a>] -         Adopt Table/Column/CompleteClassTable data structures rather than ad-hoc index/schema control
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-775'>NUCRDBMS-775</a>] -         UUIDMapping, URLMapping, URIMapping can be removed and just fallback to TypeConverterStringMapping to get the same results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-776'>NUCRDBMS-776</a>] -         LocaleMapping, CurrencyMapping, TimeZoneMapping, StringBufferMapping, StringBuilderMapping can be removed and just fallback to TypeConverterStringMapping to get the same results
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-778'>NUCRDBMS-778</a>] -         Update mapping/mappingClass lookup process to allow for TypeConverter specified via jdbcType
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-781'>NUCRDBMS-781</a>] -         Support multi column TypeConverter and wrap them in a XXXMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-18'>NUCJODATIME-18</a>] -         Add TypeConverters for DateTime -&gt; Timestamp, LocalTime -&gt; Time, LocalDate -&gt; Date and maybe also Timestamp
</li>
</ul>


## Task

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1105'>NUCCORE-1105</a>] -         Upgrade repackaged ASM to v5 when it is released
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1142'>NUCCORE-1142</a>] -         Add TypeConverter for Serializable -&gt; java.nio.ByteBuffer
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1143'>NUCCORE-1143</a>] -         Add StoreManager.OPTION_ORM_FOREIGN_KEYS to signify that the store supports FKs
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1146'>NUCCORE-1146</a>] -         Add StoreManager.OPTION_APPLICATION_COMPOSITE_ID to signify that the store supports multiple PK fields
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1148'>NUCCORE-1148</a>] -         Change &quot;datanucleus.identifier.case&quot; 'PreserveCase' to be 'MixedCase' to be match internal namings
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1151'>NUCCORE-1151</a>] -         In-memory query evaluation : improve ordering support so we can process DyadicExpression, InvokeExpression etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1152'>NUCCORE-1152</a>] -         In-memory query evaluation : support for Map.containsEntry(key,val)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1158'>NUCCORE-1158</a>] -         Change TypeManager to be an interface, and have default implementation
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1159'>NUCCORE-1159</a>] -         Fix NamingFactory index generation to respect user-specified names, and add method for datastore-id, discriminator, multitenancy index
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1161'>NUCCORE-1161</a>] -         Add TypeConverter for converting java.sql.Timestamp -&gt; String
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1162'>NUCCORE-1162</a>] -         Fix MultiMap.remove(Object,Object) method to avoid clash with JDK1.8 new Map method
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1165'>NUCCORE-1165</a>] -         Change javax.time default TypeConverter so we persist as Timestamp/Time/Date wherever possible (hence queryable)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1168'>NUCCORE-1168</a>] -         Remove default TypeConverter for java.util.Date/java.sql.Date/java.sql.Time/java.sql.Timestamp/BigDecimal/BigInteger since persistable natively
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1169'>NUCCORE-1169</a>] -         Remove references to javax.time now that we use a separate plugin for JDK 1.8 time
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1170'>NUCCORE-1170</a>] -         Store Column &quot;jdbcType&quot; with org.datanucleus.store.schema.table.Column so store plugin don't need to do lookups
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1171'>NUCCORE-1171</a>] -         Add JdbcType enum and change ColumnMetaData.jdbcType to be of that type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-10'>NUCCASSANDRA-10</a>] -         Support quoted table/column identifiers (i.e case sensitive)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-23'>NUCCASSANDRA-23</a>] -         Add internal table/column definition, to avoid continual column naming lookups
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-32'>NUCCASSANDRA-32</a>] -         Add list of reserved keywords and prohibit use of them as identifiers
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-33'>NUCCASSANDRA-33</a>] -         Support persistence of Collection&lt;Enum&gt; etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-40'>NUCCASSANDRA-40</a>] -         Map BigDecimal to Cassandra &quot;decimal&quot; type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-41'>NUCCASSANDRA-41</a>] -         Support java.util.Queue as Cassandra &quot;list&quot; type
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-45'>NUCCASSANDRA-45</a>] -         Support null elements in Collection&lt;PC&gt; and null keys in Map&lt;?, PC&gt;
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-46'>NUCCASSANDRA-46</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-90'>NUCHBASE-90</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCHBASE-91'>NUCHBASE-91</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMONGODB-143'>NUCMONGODB-143</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-72'>NUCEXCEL-72</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCEXCEL-73'>NUCEXCEL-73</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-53'>NUCODF-53</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCODF-54'>NUCODF-54</a>] -         Optimistic version handling should use VersionHelper to get next version, and only use isVersioned for determining whether to do checks
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJSON-45'>NUCJSON-45</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-769'>NUCRDBMS-769</a>] -         Adopt NamingCase instead of IdentifierCase so we have commonality across all store plugin
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-772'>NUCRDBMS-772</a>] -         Support NUCCORE-1157 (TypeConverterHelper)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-773'>NUCRDBMS-773</a>] -         Support DBCP2 as connection pool (changed class names from DBCP v1.x)
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-774'>NUCRDBMS-774</a>] -         Support NUCCORE-1162, avoid JDK 1.8 naming clash
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-777'>NUCRDBMS-777</a>] -         Drop ObjectAsXXXMapping
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-780'>NUCRDBMS-780</a>] -         Drop javax.time Mapping/Expression/Literal classes now that we have TypeConverters
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJODATIME-19'>NUCJODATIME-19</a>] -         Drop Mapping/Expression/Literal classes for LocalDate, LocalTime, DateTime since we have TypeConverters now
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCJAVAEIGHT-1'>NUCJAVAEIGHT-1</a>] -         Update java.time support to reflect packaging in &quot;Java 8&quot;
</li>
</ul>


## Bug

<ul>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1149'>NUCCORE-1149</a>] -         Initialisation of org.datanucleus.store.types.simple.Properties is incorrect
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1150'>NUCCORE-1150</a>] -         InMemory query evaluation of max/min/avg/sum(arg) when no candidates is returning an integer : should return the type of the arg
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1156'>NUCCORE-1156</a>] -         java.sql.Timestamp SCO wrapper should also preserve nanos when cloning/detaching etc
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCORE-1167'>NUCCORE-1167</a>] -         NamingFactory column namer when embedded metadata has &lt;column&gt; but no name generates null column name!
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-31'>NUCCASSANDRA-31</a>] -         Empty collection fields are being stored as null, and then when read back in are null rather than empty
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-39'>NUCCASSANDRA-39</a>] -         User specified table name for &quot;increment&quot; value generator table is not being respected
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCCASSANDRA-44'>NUCCASSANDRA-44</a>] -         Surrogate version should be long or Timestamp for consistency with RDBMS
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCRDBMS-770'>NUCRDBMS-770</a>] -         Timestamp maximum precision is milliseconds
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCMAVEN-47'>NUCMAVEN-47</a>] -         Exception (Error 87 - commandline too long) when starting the enhancer in forked mode
</li>
<li>[<a href='http://issues.datanucleus.org/browse/NUCACCECLIPSE-11'>NUCACCECLIPSE-11</a>] -         Exception (Error 87 - commandline too long) during the enhancer is called within eclipse (plugin version 3.0.1)
</li>
</ul>

