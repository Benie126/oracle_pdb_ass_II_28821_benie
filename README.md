# oracle_pdb_ass_II_28821_benie

# Oracle Pluggable Database Assignment II

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
![image alt]()

---

### Step 2: Verifying the PDB Open State

After creation, it was important to **open the PDB** to make it accessible for connections and operations. Opening the PDB confirms that the database is in a ready-to-use state. This was verified by checking its status in SQL Developer (open mode) which showed read write.

**Evidence – PDB Open State Screenshot:**  
![PDB Open State](screenshots/task1_pdb_open_state.png)

---

### Step 3: Creating the Student User

Once the PDB was open, we created the student user `benie_plsqlauca_28821` inside the PDB. This user will be used for all course-related tasks. Proper privileges were assigned, and the creation was confirmed by verifying the user’s presence inside the PDB.  

**Evidence – Student User Creation Screenshot:**  
![Student User Creation](screenshots/task1_user_creation.png)

---

## Task 2 – Create and Delete a Temporary PDB

### Step 1: Creating the Temporary PDB

To demonstrate database management, a temporary PDB `be_to_delete_pdb_28821` was created. This step mimicked a real-life scenario where a temporary workspace is needed for testing or experimentation.  

**Evidence – Temporary PDB Creation Screenshot:**  
![Temporary PDB Creation](screenshots/task2_temp_pdb_creation.png)

---

### Step 2: Deleting the Temporary PDB

After confirming the temporary PDB’s creation, it was **dropped completely** from the system to ensure it no longer existed. This step was essential to show proper cleanup and resource management.  

**Evidence – Temporary PDB Deletion Screenshot:**  
![Temporary PDB Deletion](screenshots/task2_temp_pdb_deletion.png)

---

## Task 3 – Oracle Enterprise Manager (OEM) Verification

Finally, the Oracle Enterprise Manager dashboard was accessed to **verify and monitor all PDBs**. This included:

- Confirming that the main PDB `be_pdb_28821` is open and ready.  
- Ensuring the temporary PDB `be_to_delete_pdb_28821` was no longer listed.    

This step validates the proper state of the Oracle environment visually.  

**Evidence – OEM Dashboard Screenshot:**  
![OEM Dashboard](screenshots/task3_oem_dashboard.png)

---

## Challenges Faced and Solutions

| Challenge | Solution |
|-----------|---------|
| File creation conflicts during PDB creation | Enabled Oracle Managed Files (OMF) to automatically handle file storage |
| Error when closing already closed PDB | Verified PDB status using system views before performing deletion |
| Displaying student username in OEM | Navigated to Users/Sessions under the PDB in the dashboard for confirmation |

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
- [x] README is clear, professional, and comprehensive  
- [x] Assignment submission deadline respected




