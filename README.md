# oracle_pdb_ass_II_27685_Jibu
2nd Assignment – Oracle 21c PDB Management & OEM Dashboard
 Overview

This assignment demonstrates practical administration tasks in Oracle Database 21c, focusing on:

Accessing and verifying Oracle Enterprise Manager (OEM)

Creating a Pluggable Database (PDB)
NAME OF PDB: Ji_pdb_27685

Managing and opening a PDB

Deleting a PDB properly and completely

All steps are supported with screenshots organized into structured folders.

 Project Structure
2nd Assignment/
│
├── OEM Dashboard/
│   ├── Accessing OEM.png
│   ├── Checking for listener.png
│   └── OEM Dashboard.png
│
├── PDB Creation/
│   ├── Creation of PDB.png
│   ├── Displaying PDB.png
│   ├── Open PDB.png
│   ├── Saving PDB.png
│   └── Switching to PDB.png
│
└── PDB Deletion/
    ├── Creating Temp PDB.png
    ├── Opening Temp PDB.png
    ├── Saving Temp PDB.png
    ├── Showing availability of Temp PDB.png
    └── Deletion of Temp PDB.png

 Part 1: Oracle Enterprise Manager (OEM) Dashboard
 Objective

To verify the database listener and successfully access the Oracle Enterprise Manager web interface.

Steps Performed

Checked Listener Status

Verified that the Oracle listener service is running.

Ensured port 1521 is active.

Accessed OEM

Opened browser and accessed:

https://localhost:5500/em


Logged in using administrative credentials.

Verified OEM Dashboard

Confirmed database status and system health.

Observed monitoring metrics.

 Part 2: Pluggable Database (PDB) Creation
 Objective

To create and configure a new Pluggable Database within a Container Database (CDB).

Steps Performed

Created a New PDB

Used CREATE PLUGGABLE DATABASE statement.

Assigned admin user and password.

Configured file location using FILE_NAME_CONVERT.

Displayed Available PDBs

SHOW PDBS;


Opened the PDB

ALTER PLUGGABLE DATABASE Ji_pdb_27685 OPEN;


Saved the PDB State

ALTER PLUGGABLE DATABASE Ji_pdb_27685 SAVE STATE;


Switched Session to the PDB

ALTER SESSION SET CONTAINER = Ji_pdb_27685;

 Part 3: Pluggable Database (PDB) Deletion
Objective

To properly remove a PDB from the Container Database.

Steps Performed

Created a Temporary PDB

Used for deletion demonstration.

Opened the Temporary PDB

ALTER PLUGGABLE DATABASE Ji_to_delete_pdb_27685 OPEN;


Saved State of Temporary PDB

ALTER PLUGGABLE DATABASE Ji_to_delete_pdb_2768 SAVE STATE;


Verified Availability

SHOW PDBS;


Deleted the Temporary PDB

DROP PLUGGABLE DATABASE Ji_to_delete_pdb_2768 INCLUDING DATAFILES;

 Requirements

Oracle Database 21c installed

Oracle Listener configured and running

SQL*Plus or SQL Developer

Web browser for OEM access

Administrative privileges (SYSDBA)

Learning Outcomes

By completing this assignment, the following skills were demonstrated:

Managing Oracle Multitenant Architecture

Creating and deleting Pluggable Databases

Navigating Oracle Enterprise Manager

Executing administrative SQL commands

Understanding PDB lifecycle management

 Author

Student Name: Jibu Joyau Joseph
Issues Encountered: NO
Course: Database Development with PL/SQL
Assignment: 2nd Assignment – Oracle 21c PDB Management
