#Hair Salon

#### August 22nd, 2016

#### By David Bethune

## Description

This application is a representation of a hair salon to showcase week 3 of Java, using postgresql databases.


## Set up

In PSQL:
CREATE DATABASE hair_salon;
CREATE DATABASE hair_salon_test WITH TEMPLATE hair_salon
CREATE TABLE stylists (name varchar, stylist_id int);
ALTER TABLE clients OWNER TO "Guest";
CREATE SEQUENCE clients_id_seq
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;
    ALTER TABLE clients_id_seq OWNER TO "Guest";
    ALTER SEQUENCE clients_id_seq OWNED BY clients.id;
    CREATE TABLE stylists ( id int, name varchar,);
    ALTER TABLE stylists OWNER TO "Guest";
    CREATE SEQUENCE stylists_id_seq
        START WITH 1
        INCREMENT BY 1
        NO MINVALUE
        NO MAXVALUE
        CACHE 1;
        ALTER TABLE stylists_id_seq OWNER TO "Guest";
        ALTER SEQUENCE stylists_id_seq OWNED BY stylists.id;
        ALTER TABLE ONLY clients ALTER COLUMN id SET DEFAULT nextval('clients_id_seq'::regclass);
        ALTER TABLE ONLY stylists ALTER COLUMN id SET DEFAULT nextval('stylists_id_seq'::regclass);
        SELECT pg_catalog.setval('clients_id_seq', 1, false);
        SELECT pg_catalog.setval('stylists_id_seq', 1, false);
        ALTER TABLE ONLY clients
            ADD CONSTRAINT clients_pkey PRIMARY KEY (id);
            ALTER TABLE ONLY stylists
                ADD CONSTRAINT stylists_pkey PRIMARY KEY (id);
                











## How To Use

*make a pull request use the hair_salon.sql file to populate the tables connect to the database and here you go.

OR:

* Fork this repository from GitHub and rename it

## Technologies Used

Java, Spark, JUnit, FluentLenium, Velocity, Bootstrap, Database
