# findadoc

## Cassandra database initalize

**use cassandra 3x and python 2.7 java 8**

> C:\apache-cassandra-4.0-rc1\bin>cassandra
> C:\apache-cassandra-4.0-rc1\bin>cqlsh

> CREATE KEYSPACE findadoc WITH replication = {'class': 'SimpleStrategy', 'replication_factor' : 3} AND durable_writes = true;
>> DESCRIBE KEYSPACE findadoc;
>> DROP KEYSPACE findadoc;
> DESCRIBE keyspaces; // show all keyspaces

> USE findadoc;
> CREATE TABLE doctors (doc_id uuid,full_name text,category text,practice_name text,street_address text,city text,state text,new_patients boolean,graduation_year int,PRIMARY KEY (doc_id,full_name,category,city,state));
>> DESCRIBE doctors;
>> DESCRIBE table doctors;
>> CREATE INDEX ON doctors (state);

> create table categories(cat_id uuid PRIMARY KEY);

> insert into doctors(doc_id,full_name ,category,practice_name,street_address ,city ,state ,new_patients ,graduation_year)values(now(),'Bravi Dang','IT','neurologist','Truong Trinh Street','namdinh','Y Yen',true,1992);
> insert into doctors(doc_id,full_name ,category,practice_name,street_address ,city ,state ,new_patients ,graduation_year)values(now(),'Dang Ban','General','Southern Medical','Truong Trinh Street','namdinh','hai hau',true,1993);
>> select * from doctors;

> DESC tables; // show all tables.

> drop table doctors;


