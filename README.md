Download Link: https://assignmentchef.com/product/solved-cind110-assignment2-hollywood
<br>
Create a database ’Hollywood’ and create the below tables with the constraints listed below:

Movie(mID int, title text, year int, director text ); Reviewer(rID int, name text);

Rating(rID int, mID int, stars int, ratingDate date);

Enforce the following constraints on the above database:

<ol>

 <li>Movie and Reviewer should have primary key constraints on the respective id columns.</li>

 <li>Place auto increment on the ’mID’ and ’rID’ columns in the Movie and Reviewer tables.</li>

 <li>Rating table columns ’rID’ and ’mID’ should refer to the respective columns in the parent tables</li>

</ol>

i.e. Movie and Reviewer.

<ol start="4">

 <li>The default value of the ’ratingDate’ column in the Rating table should be the current date.</li>

 <li>The ’year’ column in the Movie table should not be greater than 2016.</li>

</ol>




<h1>                   Question 2</h1>

Execute the following script first and then work on questions given below.

DROP DATABASE IF EXISTS cind110A2Script1;

CREATE SCHEMA cind110A2Script1;

USE cind110A2Script1;

CREATE TABLE hiking ( trail CHAR (50),

area CHAR (50), distance FLOAT, est time FLOAT);

SHOW TABLES;

SHOW COLUMNS FROM hiking;

<h2>INSERT INTO hiking VALUES</h2>

( ‘Cedar Creek Falls’, ‘Upper San Diego’,4.5,2.5);




INSERT INTO hiking(trail, area) VALUES

( ‘East Mesa Loop’, ‘Cuyamaca Mountains’);

SELECT ∗ FROM hiking;




SET SQL SAFE UPDATES = 0;




<h2>UPDATE hiking</h2>

SET distance = 10.5, est time = 5.5 WHERE trail = ‘East Mesa Loop’;

USE cind110A2Script1;

DELETE FROM hiking WHERE trail = ‘Cedar Creek Falls’;

<h2>SELECT ∗ FROM hiking;</h2>




<ol>

 <li>Write the SQL statements to insert the following values into the hiking table:               (3)</li>

</ol>

<table width="427">

 <tbody>

  <tr>

   <td width="420">


    <table width="419">

     <tbody>

      <tr>

       <td width="128">trail</td>

       <td width="164">area</td>

       <td width="71">distance</td>

       <td width="55">est time</td>

      </tr>

      <tr>

       <td width="128">East Mesa Loop</td>

       <td width="164">Cuyamaca Mountains</td>

       <td width="71">10.50</td>

       <td width="55">10.50</td>

      </tr>

      <tr>

       <td width="128">Oak Canyon</td>

       <td width="164">NULL</td>

       <td width="71">3.00</td>

       <td width="55">NULL</td>

      </tr>

     </tbody>

    </table></td>

   <td width="6"></td>

  </tr>

 </tbody>

</table>




<ol start="2">

 <li>Write the SQL statements to update the entry for the ’Oak Canyon’ trail. Set the area to ’Mission Trails Regional Park’ and the estimated time (est time) to 2 hours. Y<u>o</u>ur table should then look like the following:</li>

</ol>




<table width="476">

 <tbody>

  <tr>

   <td width="469">


    <table width="468">

     <tbody>

      <tr>

       <td width="128">trail</td>

       <td width="213">area</td>

       <td width="71">distance</td>

       <td width="55">est time</td>

      </tr>

      <tr>

       <td width="128">East Mesa Loop</td>

       <td width="213">Cuyamaca Mountains</td>

       <td width="71">10.50</td>

       <td width="55">10.50</td>

      </tr>

      <tr>

       <td width="128">Oak Canyon</td>

       <td width="213">Mission Trails Regional Park</td>

       <td width="71">3.00</td>

       <td width="55">2.00</td>

      </tr>

     </tbody>

    </table></td>

   <td width="6"></td>

  </tr>

 </tbody>

</table>




<ol start="3">

 <li>Write the SQL statement to delete trails with a distance greater than 5 miles.</li>

 <li>Write the SQL statement to create a table called ’rating’. This table rates the difficulty of a hiking trail. It will have two columns: the trail name, ’trail’ and the difficulty, ’difficulty’. The tail name is a string of no more than 50 characters and the difficulty is an integer (INT).</li>

 <li>Write the command to add another column to the hiking table called ’trailID’ with Primary key constraint.</li>

 <li>Add another column called ’trailID’ in the ’rating’ table, which should be the foreign key with the table referring to the hiking table.</li>

 <li>What is the command to delete the rating table?</li>

</ol>

<h1>Question 3</h1>

Consider the following tables for Customer, Salesman and Order entities.




<table width="465">

 <tbody>

  <tr>

   <td colspan="2" width="209">customer id cust name</td>

   <td colspan="2" width="255"></td>

  </tr>

  <tr>

   <td width="96">30023005300130043007300930083003</td>

   <td width="114">Nick RimandoGraham ZusiBrad GuzanFabian JohnsBrad DavisGeoff CameroJulian GreenJozy Altidor</td>

   <td width="135">New York    100California 200LondonParis             300New York    200Berlin 100 London 300 Moscow 200</td>

   <td width="121"> 50015002500550065001 500350025007</td>

  </tr>

  <tr>

   <td width="88"></td>

   <td width="107"></td>

   <td width="150"></td>

   <td width="120"></td>

  </tr>

 </tbody>

</table>







<table width="357">

 <tbody>

  <tr>

   <td width="96">salesman id</td>

   <td width="182">name                city</td>

   <td width="78">commission</td>

  </tr>

  <tr>

   <td width="96">5001</td>

   <td width="182">James Hoog New York</td>

   <td width="78">0.15</td>

  </tr>

  <tr>

   <td width="96">5002</td>

   <td width="182">Nail Knite         Paris</td>

   <td width="78">0.13</td>

  </tr>

  <tr>

   <td width="96">5005</td>

   <td width="182">Pit Alex            London</td>

   <td width="78">0.11</td>

  </tr>

  <tr>

   <td width="96">5006</td>

   <td width="182">Mc Lyon           Paris</td>

   <td width="78">0.14</td>

  </tr>

  <tr>

   <td width="96">5003</td>

   <td width="182">Lauson Hen</td>

   <td width="78">0.12</td>

  </tr>

  <tr>

   <td width="96">5007</td>

   <td width="182">Paul Adam       Rome</td>

   <td width="78">0.13</td>

  </tr>

 </tbody>

</table>




Order No Purch Amt            Ord Date          Customer id salesman id 70<u>0</u>01

150.5               2012-10-05 3005                  5002

70009 270.65 2012-09-10 3001 5005 70002 65.26 2012-10-05 3002 5001

70004            110.5               2012-08-17 3009                  5003

70007 948.5 2012-09-10 3005 5002 70005 2400.6 2012-07-27 3007 5001 70008 5760 2012-09-10 3002 5001

70010 1983.43 2012-10-10 3004 5006 70003 2480.4 2012-10-10 3009 5003

70012 250.45 2012-06-27 3008 5002 70011 75.29 2012-08-17 3003 5007 70013 3045.6 2012-04-25 3002 5001







Instruction:

You are asked to provide the correct SQL scripts for the following questions. You may execute your script using terminal or MySQL workbench to verify your answers. Provide screenshots of only the outputs along with your SQL scripts.




<ol>

 <li>Write an SQL statement to prepare a list with salesman name, customer name and their cities for the salesmen and customer who belong to same city.                                                             (5)</li>

 <li>Write an SQL statement to make a list with order no, purchase amount, customer name and their cities for the orders where order amount is between 500 and 2000. (5)</li>

 <li>Write an SQL statement to find out which salesmen are working for which customer. (5)</li>

 <li>Write an SQL statement to find the list of customers who appointed a salesman for their jobs whose commission is more than 12%. (6)</li>

 <li>Write an SQL statement to find the list of customers who appointed a salesman for their jobs who does not live in same city where the customer lives, and gets a commission above 12%. (6)</li>

 <li>Write an SQL statement to find the details of an order i. e. order number, order date, amount of order, which customer gives the order and which salesman works for that customer and how much</li>

</ol>

commission he gets for an order.                                                                                                       (8)

<ol start="7">

 <li>Write an SQL statement to make a join within the tables salesman, customer and orders such that the same column of each table will appear once and only the related rows will be returned. (5)</li>

</ol>

<h1>Question 4</h1>

Consider the following Relations for a database that keeps track of student enrollment in courses and books adopted for each course.







STUDENT(Ssn, Name, Major, Bdate)

COURSE(Course#, Cname, Dept)

ENROLL(Ssn, Course#, Quarter, Grade)

BOOK ADOPTION(Course#, Quarter, Book isbn) TEXT(Book isbn<span style="text-decoration: line-through;">,</span> Book title<span style="text-decoration: line-through;">,</span> Publisher, Author)







Having that a Relation can have zero or more Foreign keys and each Foreign key can refer to different referenced Relations. Specify all possible Foreign keys for this schema