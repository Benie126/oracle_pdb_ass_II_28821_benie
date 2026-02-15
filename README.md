# oracle_pdb_ass_II_28821_benie

# Oracle Pluggable Database Assignment II

**Student Name:** GWIRA UWAMAHORO Benie Kelia  
**Student ID:** 28821  
**Course:** PL/SQL / Database Management  
**Date:** 2026-02-09  

---

## Overview of Tasks

This repository demonstrates my work on Oracle Pluggable Databases (PDBs) using Oracle 21c and SQL Developer. The assignment includes:

1. Creating a new PDB and user
2. Creating and deleting a temporary PDB
3. Accessing and verifying tasks through Oracle Enterprise Manager (OEM)

Screenshots are provided to evidence successful completion of each task.

---

## Oracle Environment

- **Oracle Version:** 21c Enterprise Edition  
- **SQL Developer:** Latest installed version  
- **Operating System:** Windows 10  
- **Oracle Enterprise Manager (OEM):** Localhost, default port 5500  
- **OMF (Oracle Managed Files):** Enabled  

---

## Task 1 – Create a New PDB

**PDB Name:** `be_pdb_28821`  
**User inside PDB:** `benie_plsqlauca_28821`  
**Password:** `benie123` (example)

**Steps Taken:**

1. Connected as SYS / SYSDBA in SQL Developer
2. Enabled OMF for automatic file management
3. Created the PDB using:

```sql
CREATE PLUGGABLE DATABASE be_pdb_28821
ADMIN USER pdbadmin IDENTIFIED BY admin123
ROLES = (DBA);

# Screenshot Evidence of PDB Creation

Below is the screenshot showing the successful creation of the Pluggable Database (PDB):

![Screenshot Evidence of PDB Creation](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/main/screenshots/pdb_created.PNG?raw=true)



