# SQLite 3

* Python has ibuilt SQL module called as SQLite3 which helps us access SQL DB.
* Databases help us in storing data in a structured manner.

## To create a DB.

```python
import sqlite3
conn = sqlite3.connect('test.db')
print(conn)
print('created successfully')
conn.close()

# o/p --->
# <sqlite3.Connection object at 0x0000017E1A58E110>
# created successfully
```

To access DB:

* install SQLite extention VS Code
* press F1
* type 'Sqlite'
* click on 'open database'
* select ur DB
* on the bottom left corner, SQLite explorer will be present
* make sure u refresh before accessing
* Database is created if it does not exist

## Create a table

```python
import sqlite3
conn = sqlite3.connect('test.db')
print ('Opened database successfully')

conn.execute('''CREATE TABLE COMPANY
         (ID INT PRIMARY KEY     NOT NULL,
         NAME           TEXT    NOT NULL,
         AGE            INT     NOT NULL,
         ADDRESS        CHAR(50),
         SALARY         REAL);''')

print ("Table created successfully")
conn.close()
```

## Insert data to table

```python
import sqlite3
conn = sqlite3.connect('test.db')
print ('Opened database successfully')

conn.execute("INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) VALUES (5, 'Paul', 32, 'California', 20000.00 )");

conn.execute("INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) VALUES (6, 'Allen', 25, 'Texas', 15000.00 )");

conn.execute("INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) VALUES (7, 'Teddy', 23, 'Norway', 20000.00 )");

conn.execute("INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) VALUES (, 'Mark', 25, 'Rich-Mond ', 65000.00 )");

conn.commit()

print ("Data Inserted successfully")
conn.close()
```

## Selecting/Printing content from the DB

```python
import sqlite3
conn = sqlite3.connect('test.db')
print ('Opened database successfully')

cursor = conn.execute("SELECT id, name, address, salary from COMPANY")
print(cursor)
print(dir(cursor))
for row in cursor:
   print ("ID = ", row[0])
   print ("NAME = ", row[1])
   print ("ADDRESS = ", row[2])
   print ("SALARY = ", row[3], "\n")

conn.close()
```

