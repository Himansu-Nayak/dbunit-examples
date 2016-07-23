DbUnit is a JUnit extension (also usable with Ant) targeted at database-driven projects that, among other things, puts your database into a known state between test runs. This is an excellent way to avoid the myriad of problems that can occur when one test case corrupts the database and causes subsequent tests to fail or exacerbate the damage.

DbUnit has the ability to export and import your database data to and from XML datasets. Since version 2.0, DbUnit can also work with very large datasets when used in streaming mode. DbUnit can also help you to verify that your database data match an expected set of values.

If you develop applications that access relational data, you need to verify that your application code works with the data, as designed. When using Hibernate, for example, you should confirm that your mappings direct Hibernate to store and retrieve data correctly. I implement 

these kind of tests using JUnit. Some testing purists argue that testing against a database belies unit-testing, but no one can refute that testing against a live database is critical -- there is no better way to verify your mappings.

  
But testing against the database requires that the data be in a known initial state. You can load the database manually before you run your test, but that becomes monotonous and error-prone. [DBUnit](http://dbunit.sourceforge.net/) solves this problem. It can pre-load the database for each test based on an XML data set. The data set format is easy to understand; here's a small data set 

taken from three tables of a MySQL database. Element names match table names and the attribute names match columns.