# oracle-pdb-assignment
## STUDENT INFORMATION :
Names = Ndirima Mutagoma Caleb
id=26974
------------------------------------------------------------------------------------------------------------------------------------------------------
##########Task 1: Create  a PDB "plsql_class2025db"
sql commands  used :
         CREATE PLUGGABLE DATABASE plsql_class2025db
ADMIN USER caleb_plsqlauca_26974 IDENTIFIED BY Mutago123
FILE_NAME_CONVERT = ('pdbseed', 'plsql_class2025db');

<img width="582" height="257" alt="1" src="https://github.com/user-attachments/assets/4ca9df6e-51bb-47c5-ad7e-f7718f939c27" />
-----------------------------------------------------------------------------------------------------------------------------------------------------------
###########Task 2: Create and Delete a PDB
Overview
Created a temporary PDB named ca_to_delete_pdb_26974 and subsequently deleted it as required.

SQL Commands Used :
      CREATE PLUGGABLE DATABASE ca_to_delete_pdb_26974
ADMIN USER ca_admin IDENTIFIED BY Mutagoma
FILE_NAME_CONVERT = ('pdbseed', 'ca_to_delete_pdb_26974');

DROP PLUGGABLE DATABASE ca_to_delete_pdb_26974 INCLUDING DATAFILES;

<img width="772" height="120" alt="3" src="https://github.com/user-attachments/assets/b97e4764-e4d4-4fa9-bd36-2daae47816c2" />
<img width="581" height="336" alt="4" src="https://github.com/user-attachments/assets/c4000bb7-4f4e-40cf-928b-294613032bd2" />
<img width="604" height="130" alt="5" src="https://github.com/user-attachments/assets/8ba74ad7-e33e-4ee5-b380-af5ffdce1f32" />
<img width="602" height="301" alt="6" src="https://github.com/user-attachments/assets/b932bd1d-74f3-473d-9d5c-c1323c719dca" />
---------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 3: Oracle Enterprise Manager (OEM)
Overview
Configured and accessed Oracle Enterprise Manager to monitor and verify the PDB operations. The OEM dashboard provides a graphical interface to manage database components.

Access Steps
Configured HTTP port (if needed)

Accessed via: https://localhost:5500/em

Logged in with privileged credentials

Navigated to database instance and PDB sections

<img width="1345" height="663" alt="7" src="https://github.com/user-attachments/assets/427331b9-a5d7-40eb-a2b6-48cae9759921" />
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
########################3Issues and Solutions
Issue 2: OEM Displaying PDBS Problem
Problem:
  My OEM displays only the number of PDBs i have but it doesn't show  them 

Solution:
I didnot find the solution i think the reason was that am using Oracle express edition and it has limited features .

Issue 2: OEM Not Accessible
Problem: Could not connect to OEM on default port.

Solution:

Checked if OEM is configured: SELECT dbms_xdb_config.gethttpsport FROM dual;

Configured port needed: EXEC DBMS_XDB_CONFIG.SETHTTPSPORT(5500);

Restarted database services

