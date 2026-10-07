# Individual Assignment II: Oracle Pluggable Databases (PDB) Management

**Course:** Database Development with PL/SQL (INSY 8311)  
**Student Name:** Kacyeye Jane Igihozo  
**Student ID:** 20251SEN127  
**Assignment:** Individual Assignment II – Oracle Pluggable Databases (PDB) Management  
**Assignment Date:** September 17, 2026  
**Instructor:** Eric Maniraguha  
**Teaching Assistant:** Afanyu Emmanuel  

---

## 1. Overview

This repository contains my work for Individual Assignment II on Oracle Pluggable Database (PDB) Management.

The assignment required four main areas of work:

1. Create a new Pluggable Database (PDB).
2. Create, verify, and completely delete a temporary PDB.
3. Access and demonstrate Oracle Enterprise Manager (OEM).
4. Document the work professionally and provide evidence through screenshots.

The screenshots in this README are the evidence of the work performed. Each screenshot is matched to the corresponding assignment requirement.

> **Evidence note:** The PDB name shown in my execution evidence is `JA_PDB_20251SEN127`, and the temporary PDB is `JA_TO_DELETE_PDB_20251SEN127`. The README records the names exactly as they appear in my submitted execution evidence.

---

## 2. Oracle Environment

The Oracle environment shown in the evidence was:

- **Oracle Database:** Oracle Database 21c Enterprise Edition
- **Oracle Version:** 21.3.0.0.0
- **Platform:** Microsoft Windows x86 64-bit
- **Database instance:** ORCL
- **PDB created:** `JA_PDB_20251SEN127`
- **Temporary PDB:** `JA_TO_DELETE_PDB_20251SEN127`
- **PDB administrator used during creation:** `pdbadmin`
- **Application/class user created:** `jane_plsqlauca_20251SEN127`

---

# 3. Task 1 — Create a New Pluggable Database

### Assignment requirement

The assignment required:

- Create the PDB successfully.
- Use the required PDB naming convention.
- Open the PDB and verify its state.
- Create a user inside the PDB.
- Provide screenshots showing the PDB creation, open state, and user creation.

### 3.1 PDB creation

The PDB was created as:

`JA_PDB_20251SEN127`

The command shown in the evidence creates the PDB and defines the PDB administrator `pdbadmin`.

### Evidence — PDB creation command

<img width="841" height="159" alt="01_pdb_creation_command" src="https://github.com/user-attachments/assets/6e18e423-c2d6-49b0-a917-776239a612e4" />


**Screenshot 1 — Task 1: PDB creation command and successful creation message.**

The screenshot shows the `CREATE PLUGGABLE DATABASE` command and the message:

`Pluggable database created.`

This proves that the PDB creation command completed successfully.

---

### 3.2 Open and verify the PDB

After creation, the PDB was opened using:

`ALTER PLUGGABLE DATABASE ja_pdb_20251SEN127 OPEN;`

The PDB state was then saved using:

`ALTER PLUGGABLE DATABASE ja_pdb_20251SEN127 SAVE STATE;`

### Evidence — PDB open state

<img width="473" height="211" alt="02_pdb_open_state" src="https://github.com/user-attachments/assets/e884101d-f66f-4f8e-9572-308882966ca6" />


**Screenshot 2 — Task 1: PDB opened and saved in its open state.**

The screenshot shows the successful execution of the `OPEN` and `SAVE STATE` commands and the PDB list confirming the environment.

---

# 4. Task 2 — Create and Delete a Temporary PDB

### Assignment requirement

The assignment required:

- Create a temporary PDB.
- Verify that the temporary PDB exists.
- Delete the temporary PDB completely.
- Provide evidence of the creation and deletion.

The temporary PDB used in my work was:

`JA_TO_DELETE_PDB_20251SEN127`

---

## 4.1 Create the temporary PDB

### Evidence — Temporary PDB creation

<img width="458" height="171" alt="01_temporary_pdb_creation" src="https://github.com/user-attachments/assets/6832ff51-6af1-4e3a-a807-0a8c3ceb0531" />



**Screenshot 3 — Task 2: Temporary PDB creation command.**

The screenshot shows the `CREATE PLUGGABLE DATABASE` command for:

`JA_TO_DELETE_PDB_20251SEN127`

and the successful result:

`Pluggable database created.`

---

## 4.2 Verify that the temporary PDB exists

After creation, `SHOW PDBS;` was used to verify the PDB.

### Evidence — Temporary PDB exists

<img width="472" height="32" alt="02_temporary_pdb_exists" src="https://github.com/user-attachments/assets/f998f042-7c00-4788-9f1a-afe3a177be6c" />


## 4.3 Delete the temporary PDB

The temporary PDB was deleted with:

`DROP PLUGGABLE DATABASE ja_to_delete_pdb_20251SEN127 INCLUDING DATAFILES;`

### Evidence — Temporary PDB deletion

<img width="469" height="63" alt="03_temporary_pdb_deleted" src="https://github.com/user-attachments/assets/9a95a771-101d-44c7-87f2-ac0b44bf0cea" />


**Screenshot 5 — Task 2: Temporary PDB deleted successfully.**

The screenshot shows the `DROP PLUGGABLE DATABASE ... INCLUDING DATAFILES` command and the successful result:

`Pluggable database dropped.`

Using `INCLUDING DATAFILES` demonstrates that the PDB was removed together with its associated datafiles.

---

# 5. Task 3 — Oracle Enterprise Manager (OEM)

### Assignment requirement

The assignment required:

- OEM to be accessible.
- The dashboard to reflect the Oracle environment.
- Evidence of the completed PDB work.
- A clear screenshot of the OEM dashboard.

### Evidence — OEM dashboard


<img width="599" height="253" alt="01_oem_dashboard" src="https://github.com/user-attachments/assets/cd7cf0ac-182b-4061-b3dc-b9e8f1eacd0f" />

**Screenshot 6 — Task 3: Oracle Enterprise Manager dashboard.**

The screenshot shows the Oracle Enterprise Manager Database Home dashboard. It displays information about the Oracle database environment, including:

- Database status
- Oracle Database version
- Platform
- Instance information
- Performance/activity information
- Database resource information

This provides evidence that Oracle Enterprise Manager was accessible and displaying the Oracle environment.

---

# 6. Task 1 — User Creation Inside the PDB

The assignment specifically required a user to be created inside the PDB and stated that the user would be reused for future class work.

The user created in my evidence is:

`jane_plsqlauca_20251SEN127`

## 6.1 Check for the user

Before creating the account, a query was used to check whether the username already existed.

### Evidence — Username check

<img width="445" height="24" alt="01_username_check" src="https://github.com/user-attachments/assets/639c85d1-e5dc-4be5-a8ce-b53f83a6824c" />


**Screenshot 7 — Task 1: Check for the required username.**

This screenshot shows the SQL query checking for:

`jane_plsqlauca_20251SEN127`

This serves as the preliminary verification before user creation.

---

## 6.2 Create the user

The user was then created using:

`CREATE USER jane_plsqlauca_20251SEN127 IDENTIFIED BY ...;`

### Evidence — User successfully created

<img width="470" height="68" alt="02_user_created" src="https://github.com/user-attachments/assets/7537917e-0b09-4e21-b9d6-81bd2c480d1f" />


**Screenshot 8 — Task 1: User created successfully inside the Oracle environment.**

The screenshot shows the `CREATE USER` command and the successful result:

`User created.`

This provides direct evidence that the required user account was created.

---

# 7. Task-to-Evidence Mapping

| Assignment Requirement | Evidence | Screenshot |
|---|---|---|
| Create a new PDB | PDB creation command and successful result | Screenshot 1 |
| Verify/open the PDB | `OPEN`, `SAVE STATE`, and PDB state | Screenshot 2 |
| Create a user inside the PDB | Username check and successful `CREATE USER` | Screenshots 7–8 |
| Create a temporary PDB | Temporary PDB creation command and result | Screenshot 3 |
| Verify temporary PDB exists | `SHOW PDBS` output | Screenshot 4 |
| Delete temporary PDB completely | `DROP PLUGGABLE DATABASE ... INCLUDING DATAFILES` | Screenshot 5 |
| Access Oracle Enterprise Manager | OEM Database Home dashboard | Screenshot 6 |
| Professional documentation | This README and organized evidence folders | Repository |
| Public GitHub repository | To be completed with the repository URL | Submission Details |

---

# 8. Challenges Faced and How They Were Solved

During the practical work, the main challenge was managing the PDB lifecycle correctly: creating the PDB, verifying its state, creating the required user, creating a temporary PDB, and then deleting the temporary PDB.

The work was completed by executing each Oracle command in sequence and checking the result after each operation. The `SHOW PDBS;` command was used to verify PDB states, while the successful Oracle messages such as `Pluggable database created.`, `Pluggable database altered.`, and `Pluggable database dropped.` were used to confirm completion.

---

# 9. Repository Structure

The repository is organized according to the assignment documentation requirements:

```text
oracle_pdb_ass_II_20251SEN127_Kacyeye/
│
├── README.md
│
└── screenshots/
    ├── pdb_creation/
    │   ├── 01_pdb_creation_command.png
    │   └── 02_pdb_open_state.png
    │
    ├── pdb_deletion/
    │   ├── 01_temporary_pdb_creation.png
    │   ├── 02_temporary_pdb_exists.png
    │   └── 03_temporary_pdb_deleted.png
    │
    ├── oem_dashboard/
    │   └── 01_oem_dashboard.png
    │
    └── user_creation/
        ├── 01_username_check.png
        └── 02_user_created.png
```

---

# 10. Integrity Statement

I confirm that the work documented in this repository represents my own practical execution of the Oracle PDB assignment. The screenshots included in this README are the evidence of my work, and the documentation is organized to correspond to the tasks and requirements in the assignment.

---

# 11. Submission Details

**Repository Link:** `[Paste your public GitHub repository URL here]`

**PDB Name Created:** `JA_PDB_20251SEN127`

**Issues Encountered:** Yes

**Student Name:** Kacyeye Jane Igihozo

**Student ID:** 20251SEN127

---

# 12. Final Checklist

- [x] New PDB created.
- [x] PDB open state demonstrated.
- [x] User created.
- [x] Temporary PDB created.
- [x] Temporary PDB verified.
- [x] Temporary PDB deleted.
- [x] OEM dashboard accessed.
- [x] Screenshots included and matched to tasks.
- [x] README documentation prepared.
- [ ] Public GitHub repository URL added.
- [ ] README and screenshots pushed to GitHub.
- [ ] Same submission details entered in the required Google Form.
- [ ] Final submission completed before the deadline.

---

## Professional Note

> “Excellence is never an accident; it is the result of discipline, commitment, and integrity.”

As a future database professional, this work demonstrates practical experience with Oracle Multitenant Architecture, PDB creation and deletion, user management, Oracle Enterprise Manager, and technical documentation.

