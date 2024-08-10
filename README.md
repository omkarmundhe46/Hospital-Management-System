In this project I am going to explain about How can we develop Hospital Management System.
Here a complete Hospital Management System Project using Java and JDBC. 

For developing this project I am going to use Core Java and Basic Functionality of it like 
 . How to take input from user (String, int, Long, Double etc..)
 . How to take input from console.
 . Use of while loop, if block, switch case etc
 . Class/Object Creation, Calling Methods from One class to Another
 . As a database I am going to use MySQL.
 . For connecting with Database I am going to use Plain JDBC. 
 
Features for Hospital Management System
 . Adding Patient
 . Adding Doctor
 . View Patient
 . View Doctor
 . Book Appointment

Database table which are used for Hospital Management Project
 1. patient
 2. doctor
 3. appointment

Here,  
=== Table Creation SQL ===

CREATE DATABASE HOSPITALMANAGEMNET;

CREATE TABLE patients (
  id MEDIUMINT(8) NOT NULL AUTO_INCREMENT,
  NAME VARCHAR(100) NOT NULL,
  age VARCHAR(3) NOT NULL,
  gender VARCHAR(7) NOT NULL,
  PRIMARY KEY (id)  
);

CREATE TABLE doctors (
  id MEDIUMINT(8) NOT NULL AUTO_INCREMENT,
  NAME VARCHAR(255) NOT NULL,
  department VARCHAR(100) NOT NULL,
  PRIMARY KEY (id)
);

CREATE TABLE appointments (
  id MEDIUMINT(8) NOT NULL AUTO_INCREMENT,
  patient_id MEDIUMINT(8) NOT NULL,
  doctor_id MEDIUMINT(8) NOT NULL,
  appointment_date DATE NOT NULL,
  PRIMARY KEY (id),
  FOREIGN KEY (patient_id) REFERENCES patients (id),
  FOREIGN KEY (doctor_id) REFERENCES doctors (id)
);

select * from patients;

select * from doctors;

select * from appointments;
