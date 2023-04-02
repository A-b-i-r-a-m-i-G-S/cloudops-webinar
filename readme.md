# Online Book Store System 📚

## Problem Statement: ❓

People find it difficult to visit a bookstore in-person whenever they require any book. This causes a necessity to design a system that gives an alternative mode of buying the required books from wherever they are.

## Project Justification:

A system to purchase books online and to store the inventory data securely can be built using MySQL inside the AWS environment. This system gives people an alternative mode of buying required books online on a first come first serve basis, rather than visiting the store.

## Project Characteristics and Requirements:📝

-	Secured database
-	Cloud hosted service
-	Easy navigation
-	Integrated payment systems
-	User history tracked

## Project Success Criteria: 

Our main goal is to develop a light software that can serve as a tool for purchasing required books at the ease of the buyer, irrespective of where they are.

## Scope of Work:

The online book store system can be used by people across the world, to purchase the required books. Users who are 12+ years old can handle the software without much difficulty in processing their purchase. The software can be designed in a way to easily adapt updates and additions to its features, thus making it useful in the long term. Since books are purchased online, the cost associated with displaying the books in shops as well as maintenance costs can be cut down.

## Features: 
- Selection of books is done using the system through a simple registration process, wherein a form can be filled by the user provided by the website. This form can be built using MySQL.
- User login is authenticated.
-	Add to cart option for books selected.
-	Easy to use

## Implementation: 🧰

### Installing dependencies
* Install node version manager (nvm).
    ```
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
    ```
* Activate nvm.
    ```
    . ~/.nvm/nvm.sh
    ```
* Install node
    ```
    nvm install node
    ```
* Install git
    ```
    sudo apt-get install git
    ```
* Install nodejs, ejs, express and mysql2 inside the code repository.
    ```
    npm install node
    npm install ejs
    npm install express
    npm install mysql2
    ```
* Install mariadb
    ```
    sudo apt-get update
    sudo apt-get install mariadb-client
    mysql -h <endpoint> -P 3306 -u <mymasteruser> -p
    ```
### Application Frontend:
A full stack web application is created using HTML, CSS, JavaScript, Node.js, Express.js. The frontend is connected to a MySQL database to maintain the inventory of books. 

### MySQL Database:
MySQL is one of the easy to understand and proficient languages available today, and its features can be utilised efficiently to build an online system for storing data related to the books.

#### MySQL commands to be run on the EC2 instance:
* Create the online book store database.
```mysql
create database online_book_store;
use online_book_store;
```
* Create tables users and inventory.
```mysql
create table users(
uid smallint primary key,
uname varchar(100) not null,
password varchar(20) not null,
email varchar(30) not null
);

create table inventory(
idx smallint primary key,
bname varchar(200) not null,
bauth varchar(200) not null,
bprice double(6,2)
);
```
* Insert data into inventory table.
```mysql
 insert into inventory values(1,'Da Vinci Code','Dan Brown',1500.00);     
 insert into inventory values(2,'It Ends with Us','Colleen Hoover',900.00);
 insert into inventory values(3,'Twilight','Stephanie Meyer',1350.00);
 insert into inventory values(4,'The Lord of the Rings','R R J Tolkien',1400.00);  
 insert into inventory values(5,'To Kill a Mockingbird','Harper Lee',1000.00);
 insert into inventory values(6,'The Hunger Games','Suzanne Collins',1100.00);
 insert into inventory values(7,'Pride and Prejudice','Jane Austen',1150.00);
 insert into inventory values(8,'The Book Thief','Markus Zusak',900.00);
 insert into inventory values(9,'The Fault in Our Stars','Margaret Mitchell',1900.00); 
```

### AWS Resources required:
-	Amazon EC2 instance - Virtual machine to host web application
-	Amazon RDS - Backend MySQL database to store book details

## Suggestive Additions to the Project:

*The following features can be added to the project with subsequent updates:*
-	User registration validation.
-	Provision for returning books.
-	Request for books not in list/out of stock.
-	Option to review books.
-	Subscription to auto-deliver newsletters/magazines for every edition.
-	Donate money/new books/used books to help educate underprivileged children.
-	Provide an online sample of a few pages per book, to encourage users to purchase the product.

**Front-end web application by**:*@mohammadshaad*

**Back-end web application by**:*@A-b-i-r-a-m-i-G-S*

**Documentation by**:*@deepthi1129*
