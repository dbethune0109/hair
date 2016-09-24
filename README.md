#Hair Salon

#### August 22nd, 2016

#### By David Bethune

## Description

This application is a representation of a hair salon to showcase week 3 of Java, using postgresql databases.


## Set up

In PSQL:
CREATE DATABASE hair_salon;
CREATE DATABASE hair_salon_test WITH TEMPLATE hair_salon
CREATE TABLE stylists (id serial PRIMARY KEY, name varchar, stylist_id int);
CREATE TABLE clients (id serial PRIMARY KEY, name varchar, clients_id int);


## How To Use

*make a pull request use the hair_salon.sql file to populate the tables connect to the database and here you go.

OR:

* Fork this repository from GitHub and rename it

## Technologies Used

Java, Spark, JUnit, FluentLenium, Velocity, Bootstrap, Database
