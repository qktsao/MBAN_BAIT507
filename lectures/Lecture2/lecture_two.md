
https://github.ubc.ca/gorings/MBAN_BAIT507

---
title: BAIT507 - Lecture Two
separator: <!--s-->
verticalSeparator: <!--v-->
theme: solarized
revealOptions:
    transition: 'fade'
---

# BAIT507
## All About Databases!

<!--v-->

# Key Concepts

* Servers, DBs, schema, tables
* Relations, indexes and keys
* Managing ACID in databases

<!--v-->

# Class Work

* Your first RMarkdown Document
* Connecting to Postgres with R
* Plot results

<!--s-->

# The Database Ecosystem

<!--v-->

## Servers, DBs, schema, tables

* A server contains databases
* A database contains schema
* A schema contains tables
* A table contains columns
* Individual data "tuples" consist of data from all columns in one table row.

<!--v-->

## The Server

* The server manages access (you log in to the server)
* The server manages transactions
* The server optimizes queries
* The DBMS manages the interaction between agents and the data within the database

<!--v-->

## The Database

* The database provides rules for access and management
* Databases can be structured into **schema**
* Databases use defined language to help the DBMS understand and optimize data access
  - INDEXes, FOREIGN KEYs, CONSTRAINTs

<!--v-->

## Schema

* A schema is a heterogenous set of data within the database
* Often related to other data within the database, but with a set user group and purpose

<!--v-->

## Table

* A table is the atomic unit for sets of records, defining a core set of properties.

Primary Key  | Name  | Group  | Grade
--|---|---|--
1  | A. Cmblm  | Team Super  | A+
2  | T. Hngn  | Team Not Good  |  F

<!--v-->

## Columns

* A unit within a table
* A defined data type that cannot be violated
  - [Postgres Data Types](https://www.postgresql.org/docs/current/datatype.html)
* Can be INDEXed, can be CONSTRAINed (at the Table level)

Primary Key  | **Name**  | Group  | Grade
--|---|---|--
1  | **A. Cmblm**  | Team Super  | A+
2  | **T. Hngn**  | Team Not Good  |  F

<!--v-->

## The Tuple

* A coherent unit of data

Primary Key  | Name  | Group  | Grade
--|---|---|--
**1**  | **A. Cmblm**  | **Team Super**  | **A+**
2  | T. Hngn  | Team Not Good  |  F

* May include CONSTRAINTs (set at the Table level)
<!--v-->

<img src=figures/db_table_schema.png>

<!--s-->

# Organizing Data

<!--v-->

## Organized Data

* Moving from multiple files to logical data strucutures
* Coherent conceptual groups
* Instagram manages information about
  -  users, employees, advertisers

<!--v-->

## Short Exercise

* What data does Instragram manage?
  - How would you organize it?

<!--v-->

<img src=figures/instagram.svg>

<!--s-->

# Break time!

<!--s-->

# Getting to the Database

<!--v-->

## Creating a Database

* Using [AWS RDS (free tier)](https://aws.amazon.com/getting-started/tutorials/create-connect-postgresql-db/)
* Using [PGAdmin4](https://www.pgadmin.org/docs/pgadmin4/development/database_dialog.html)

<!--v-->

## Connecting

<img src=figures/pgadmin_newdb.png>

<!--v-->

## Connecting

* Server:
XXmban-bait.cmy5mce9ahmj.us-east-1.rds.amazonaws.comXX
* Port: 5432

<!--v-->

## Connecting

* RMarkdown:  [Rmarkdown Link](https://github.com/SimonGoring/MBAN_BAIT507/blob/master/lectures/Lecture2/R/mban_lecturetwo_connecting.Rmd) [http://bit.ly/ubcmban]()

* Data: [BC Data Catalogue](https://catalogue.data.gov.bc.ca/dataset?download_audience=Public) [Labour Market Data](https://catalogue.data.gov.bc.ca/dataset/labour-market-outlook/resource/df92bf55-45b2-42a3-b5a8-6d2857df2ffe) [http://bit.ly/2kwWQrI]()
