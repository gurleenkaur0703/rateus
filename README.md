# RateUs Database
## Database Schema 
### Creating the RateUs Database
```
CREATE DATABASE RateUs;

USE RateUs;
```
### Creating the Organisation Table
```
CREATE TABLE Organisation(
    ID varchar(10) PRIMARY KEY,
    Name varchar(200),
    Owner_id varchar(10),
    Logo varchar(100),
    Address varchar(200),
    Listed_On DATE DEFAULT CURRENT_TIMESTAMP
);
```
### Creating the User Table
```
CREATE TABLE User_(
    ID varchar(10) PRIMARY KEY,
    Name varchar(100),
    Email varchar(200),
    Contact varchar(12),
    Password varchar(300),
    Created_ON DATE DEFAULT CURRENT_TIMESTAMP
);
```
## Database Queries
### Inserting User Details
```
INSERT INTO User_ (ID, Name, Email, Contact, Password) 
VALUES ('enter_id', 'enter_name', 'enter_email', 'enter_contact', 'enter_password');
```
### Inserting Organisation Details
```
INSERT INTO Organisation (ID, Name, Owner_id, address) 
VALUES ('enterOrg_id', 'enterOrg_name', 'enterOrg_owner_id', 'enterOrg_address');
```
### Fetching User Details by Email
```
SELECT ID, Contact, Password 
FROM User_ 
WHERE Email = 'backend_provided';
```
