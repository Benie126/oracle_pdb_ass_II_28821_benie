# oracle_pdb_ass_II_28821_benie

# Oracle Pluggable Database MANAGEMENT (Assignment II)

**Student Name:** GWIRA UWAMAHORO Benie Kelia  
**Student ID:** 28821  
**Course:** PL/SQL / Database Management   

---

## Overview of Tasks

This assignment demonstrates practical experience with Oracle Pluggable Databases (PDBs) using Oracle 21c and SQL Developer. The following tasks were completed step by step:

1. Task 1 – Creation of a new PDB, verification of its open state, and creation of a student user inside the PDB.  
2. Task 2 – Creation and complete deletion of a temporary PDB.  
3. Task 3 – Verification and monitoring using Oracle Enterprise Manager (OEM) dashboard.  

All tasks include screenshots as evidence for transparency and verification.

---

## Oracle Environment Used

- **Oracle Database Version:** 21c Enterprise Edition  
- **SQL Developer:** Latest installed version (24.3)  
- **Operating System:** Windows 10  
- **Oracle Enterprise Manager (OEM):** https://localhost:5500/em  
- **Oracle Managed Files (OMF):** Enabled for automatic file handling  

---

## Task 1 – Create a New PDB, Open State, and User Creation

### Step 1: Creating the PDB

The first step involved creating the pluggable database `be_pdb_28821`. This allowed us to have a separate container inside the Oracle CDB for coursework. The PDB was successfully created and ready to be opened.  

**Evidence – PDB Creation Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/8cbc92fceb662995fe0b61a8ce1c01ad380f23c9/screenshots/pdb_created.PNG)

---

### Step 2: Verifying the PDB Open State

After creation, it was important to **open the PDB** to make it accessible for connections and operations. Opening the PDB confirms that the database is in a ready-to-use state. This was verified by checking its status in SQL Developer (open mode) which showed read write.

**Evidence – PDB Open State Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/e22259c4904ada0947c45563c4736369b0df6afc/screenshots/pdb-open-mode.PNG)

---

### Step 3: Creating the Student User

Once the PDB was open, we created the student user `benie_plsqlauca_28821` inside the PDB. This user will be used for all course-related tasks. Proper privileges were assigned, and the creation was confirmed by verifying the user’s presence inside the PDB.  

**Evidence – Student User Creation Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/ce38138d30ef9ff5ef251a39e8ddf3f4ffde9377/screenshots/new-user-created.PNG)

---

## Task 2 – Create and Delete a Temporary PDB

### Step 1: Creating the Temporary PDB

To demonstrate database management, a temporary PDB `be_to_delete_pdb_28821` was created. This step mimicked a real-life scenario where a temporary workspace is needed for testing or experimentation.  

**Evidence – Temporary PDB Creation Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/ce38138d30ef9ff5ef251a39e8ddf3f4ffde9377/screenshots/pdb-to-delete-created.PNG
)

---

### Step 2: Deleting the Temporary PDB

After confirming the temporary PDB’s creation, it was **dropped completely** from the system to ensure it no longer existed. This step was essential to show proper cleanup and resource management.  

**Evidence – Temporary PDB Deletion Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/ce38138d30ef9ff5ef251a39e8ddf3f4ffde9377/screenshots/pdb-to-delete-dropped.PNG)

---

## Task 3 – Oracle Enterprise Manager (OEM) Verification

Finally, the Oracle Enterprise Manager dashboard was accessed to **verify and monitor all PDBs**. This included:

- Confirming that the main PDB `be_pdb_28821` is open and ready.  
- Ensuring the temporary PDB `be_to_delete_pdb_28821` was no longer listed.    

This step validates the proper state of the Oracle environment visually.  

**Evidence – OEM Dashboard Screenshot:**  
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/ce38138d30ef9ff5ef251a39e8ddf3f4ffde9377/screenshots/eom1.PNG)
![image alt](https://github.com/Benie126/oracle_pdb_ass_II_28821_benie/blob/ce38138d30ef9ff5ef251a39e8ddf3f4ffde9377/screenshots/eom2.PNG)

---

## Challenges Faced and How They Were Solved

| Challenge | Explanation | Solution |
|-----------|------------|---------|
| File creation conflicts during PDB creation | When creating a new PDB, Oracle was unable to automatically assign file locations for the datafiles, which caused conflicts and errors. This typically happens when Oracle Managed Files (OMF) is not enabled, or the specified directories are not properly set. | Enabled Oracle Managed Files (OMF) by setting `db_create_file_dest` to a valid directory. This allowed Oracle to automatically manage the datafile locations, avoiding naming conflicts and errors. |
| Error when closing an already closed PDB | While attempting to close a temporary PDB, an error occurred because the database was already in a closed state. This can happen if the system assumes the PDB is open when it is not. | Checked the current state of the PDB using system views (`V$PDBS`) before performing any close or drop operations. This ensured safe deletion without unnecessary errors. |
| Displaying student username in OEM | Initially, the student user created inside the PDB did not appear on the OEM dashboard, causing difficulty in providing evidence for task verification. This happens because OEM sometimes requires navigating to the correct PDB container to see user details. | Accessed the correct PDB in OEM and navigated to the **Users/Sessions** section to confirm that the student user `benie_plsqlauca_28821` was properly created and visible on the dashboard. |
| Understanding temporary PDB deletion | Deleting a temporary PDB requires careful handling to ensure that all datafiles are also removed. There was a concern that residual files could remain, taking up space and causing confusion. | Used the “DROP PLUGGABLE DATABASE … INCLUDING DATAFILES” approach to ensure complete removal of the PDB and all associated files, confirming deletion by rechecking the PDB list. |


---

## Integrity Statement

I hereby declare that this work is entirely my own. All tasks were completed personally using Oracle 21c and SQL Developer. No unauthorized assistance or external solutions were used to complete this assignment.  

---

## Final Checklist

- [x] Correct PDB name used: `be_pdb_28821`  
- [x] Student user created inside PDB: `benie_plsqlauca_28821`  
- [x] Temporary PDB created and deleted: `be_to_delete_pdb_28821`  
- [x] OEM dashboard screenshot included  
- [x] GitHub repository is public  
- [x] README is clear and professiona  
- [x] Assignment submission deadline respected




