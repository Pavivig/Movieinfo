#Movieinfo

#create a new sqlite database 

sqlite3 movieinfo.db 

#connect to the sqlite database
  
import sqlite3  
  
conn = sqlite3.connect('movieinfo.db')  
  
print "Opened database successfully";


#creating a new table (movies) using
  
import sqlite3  
  
conn = sqlite3.connect('movieinfo.db')  
print "Opened database successfully";  
  
conn.execute('''''CREATE TABLE movie
       (ID INT PRIMARY KEY     NOT NULL, 
       NAME           TEXT    NOT NULL, 
       ACTOR          TEXT    NOT NULL, 
       ACTRESS         TEXT   NOT NULL, 
       DIRECTOR        TEXT    NOT NULL, 
       YEAR OR RELEASED     INT );''')  
print "Table created successfully";  
  
conn.close()


#insert data into movies table
  
import sqlite3  
  
conn = sqlite3.connect('movieinfo.db')  
print "Opened database successfully";  
  
conn.execute("INSERT INTO movie (ID,NAME,ACTOR,ACTRESS,DIRTECTOR,YEAR OF RELEASED) \  
      VALUES (1, 'city hunter', 'Jackie chan', 'joey wong', 'wong jing', 1993 )");  
  
conn.execute("INSERT INTO movie (ID,NAME,ACTOR,ACTRESS,DIRTECTOR,YEAR OF RELEASED) \  
      VALUES (2, 'viswasam', 'ajithkumar', 'nayanthara', 'siva', 2019 )");  
  
conn.execute("INSERT INTO movie (ID,NAME,ACTOR,ACTRESS,DIRTECTOR,YEAR OF RELEASED) \  
      VALUES (3, 'baahubali', 'prabhas' , 'anushka shetty', 's.s.rajamouli', 2015 )");  
  
conn.execute("INSERT INTO movie (ID,NAME,ACTOR,ACTRESS,DIRTECTOR,YEAR OF RELEASED) \  
      VALUES (4, 'tenet', 'John david washington' , 'elizebeth debicki', 'Christopher nolan', 2020 )");  
  
conn.commit()  
print "Records inserted successfully";  
conn.close()  


#querying data from movies table 
  
import sqlite3  
  
conn = sqlite3.connect('movieinfo.db')  
  
data = conn.execute("select * from movie");  
  
for row in data:  
   print "ID = ", row[0]  
   print "NAME = ", row[1]  
   print "ACTOR = ", row[2] 
   print "ACTRESS = ", row[3]
   print "DIRTECTOR = ", row[4]
   print "YEAR OF RELEASED =", row[5], "\n"  
  
conn.close();  


