# Ex. No: 6 PL/SQL program using Cursor 
### DATE: 
### AIM: To create PL/SQL program to display the customer table 

### Steps:
1. Declare the variable  in Declare section.
2. Fetch the variable with datatype similar to data type in cursor 
3. Create a cursor to select all rows from customers table.
4. Display the result 
5. End the begin section.

### Program:
```
create table customers(ID int,NAME varchar(20),AGE int,ADDRESS varchar(20),salary int);
insert into customers values( 1,'Ramesh',32,'Ahmedabad',2000);
insert into customers values( 1,'Khilan',25,'Delhi',1500);
insert into customers values( 1,'kaushik ',23,'Kota',2000);
DECLARE  
   total_rows number(2); 
BEGIN 
   UPDATE customers 
   SET salary = salary + 500; 
   IF sql%notfound THEN 
      dbms_output.put_line('no customers selected'); 
   ELSIF sql%found THEN 
      total_rows := sql%rowcount;
      dbms_output.put_line( total_rows || ' customers selected '); 
   END IF;  
END; 
/
```
### Output:
![Screenshot 2024-04-03 104606](https://github.com/22003197/DBMS/assets/124332243/d0cef464-d247-4968-a926-6f68983f5fda)

### Result:
Thust the program was performed sucessfully.
