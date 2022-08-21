# Reading Mongo and Mongoose

## nosql vs sql

1. Fill in the chart below with five differences between SQL and NoSQL databases:

| SQL    | NoSQL   |
| ------ | ------- |
|        |         |
|        |         |
|        |         |
|        |         |

1. What kind of data is a good fit for an SQL database?
“SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data. While you can use NoSQL for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.”

2. Give a real world example.
SQL allows you to define data, manipulate data, and retrieve data from data bases(number of sales for this month for example).

3. What kind of data is a good fit a NoSQL database?
“NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.”

4. Give a real world example.
“NoSQL is used for Big data and real-time web apps. For example, companies like Twitter, Facebook and Google collect terabytes of user data every single day.” - “https://www.guru99.com/nosql-tutorial.html"

5. Which type of database is best for hierarchical data storage?
“SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

6. Which type of database is best for scalability?
“In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.”

## sql vs nosql (Video)

1. What does SQL stand for?
Structured query language

2. What is a relational database?
“A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables.” -“https://www.oracle.com/in/database/what-is-a-relational-database/"

3. What type of structure does a relational database work with?
“The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure.”

4. What is a ‘schema’?
“We define SQL Schema as a logical collection of database objects. A user owns that owns the schema is known as schema owner. It is a useful mechanism to segregate database objects for different applications, access rights, managing the security administration of databases. We do not have any restrictions on the number of objects in a schema.” - “https://www.sqlshack.com/a-walkthrough-of-sql-schema/"

5. What is a NoSQL database?
“NoSQL databases store data in documents rather than relational tables. Accordingly, we classify them as "not only SQL" and subdivide them by a variety of flexible data models. Types of NoSQL databases include pure document databases, key-value stores, wide-column databases, and graph databases. NoSQL databases are built from the ground up to store and process vast amounts of data at scale and support a growing number of modern businesses.” -“https://www.couchbase.com/resources/why-nosql"

6. How does it work?
“NoSQL database technology stores information in JSON documents instead of columns and rows used by relational databases.”

7. What is inside of a Mongo database?
“The following are some of MongoDB benefits and strengths:
Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.
Scalability: It is horizontally scalable i.e. you can reduce the workload by increasing the number of servers in your resource pool instead of relying on a stand alone resource.
Manageable: It is easy to use for both developers and administrators. This also gives the ability to shard database
Dynamic Schema: Its gives you the flexibility to evolve your data schema without modifying the existing data”

8. Which is more flexible - SQL or MongoDB? and why.
MongoDB because “It gives you the flexibility to evolve your data schema without modifying the existing data.”

9. What is the disadvantage of a NoSQL database?

“Disadvantages of NoSQL databases
Not all NoSQL databases contemplate the atomicity of instructions and the integrity of the data. They withstand what’s know as eventual consistence.
Compatibility issues with SQL instructions. New databases use their own characteristics in the query language and they’re not yet 100% compatible with the SQL used in relational databases. Support for work query issues in a NoSQL database is more complicated.
Lack of standardizing. There are many NoSQL databases and there is still no standard like the ones that exist in relational databases. An uncertain future is predicted for these databases.
Cross-platform support. There are still many improvements to be made on some systems so that they can run on non-Linux operating systems.
They usually have not-really-useful management tools or console access.” -“https://pandorafms.com/blog/nosql-vs-sql-key-differences/"

## Things I want to know more about
  This is the section on SQL and NoSql and what is the differences in both of them and how they work. Also the disadvantages and advantages in both.
## Bookmark and Review

[nosql vs sql. by The Geek Stuff](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool),
[sql vs nosql . by Academind](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y),
[mongoose api. by mongoose](https://mongoosejs.com/docs/api.html#Model),
[React Router. by REMIX / REACT ROUTER](https://v5.reactrouter.com/web/api/BrowserRouter),
