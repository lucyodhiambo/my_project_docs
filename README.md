# my_project_docs
# GitHub & Server Access Documentation

## Overview
This document outlines the steps performed to access a remote Ubuntu server via SSH, switch between user accounts, and interact with PostgreSQL and CSV data files.

---

## Steps Performed

### 1. SSH into Remote Server as Root
Connected to the Ubuntu server at `159.65.222.96` using the root user.

### 2. Navigate Server Directory Structure
Listed all user directories and project files on the server.

### 3. Switch to LucyA User Account
Used SSH to switch from root to the `LucyA` user account.

### 4. Check PostgreSQL Version
Verified PostgreSQL installation and version.

### 5. Explore User Directories
Navigated through `LucyA`'s home directory and subdirectories.

### 6. View CSV Data File
Displayed the contents of `cardata.csv` containing car dealership information.

---

## Commands Used

```bash
# SSH into server as root
ssh root@159.65.222.96

# Enter password when prompted (first attempt failed, successful on second)

# List all directories and files in root home
ls

# Switch to LucyA user account via SSH
ssh LucyA@159.65.222.96

# Enter LucyA's password

# Check PostgreSQL version
psql --version

# List files in LucyA's home directory
ls

# View contents of app.py (file was empty)
cat app.py

# Check testfile type (found it was a directory)
cat testfile

# Change into testfile directory
cd testfile

# List contents
ls

# Go back to previous directory
cd ..

# Change into folder directory
cd folder

# List contents of folder
ls

# Display CSV file contents

## Explanations

### Why SSH?
SSH (Secure Shell) allows encrypted remote access to the server. The command `ssh root@159.65.222.96` connects to the server at that IP address using the root administrative account.

### Why did the first login fail?
The first attempt failed due to an incorrect password. SSH requires exact password matching for security.

### What is PostgreSQL?
PostgreSQL is an open-source relational database management system. Version 16.14 is installed on this server.

### What is the CSV data?
The `cardata.csv` file contains car listing data with 10 records including make, model, price, mileage, and condition. This could be imported into PostgreSQL for analysis.And also transfered from the local server on my PC to the remote server on my user using the scp.
# SCREENSHOTS
cat cardata.csv<img width="276" height="125" alt="view table data in lucya" src="https://github.com/user-attachments/assets/38e509f2-ec2b-4ba4-97d0-76966d1e79bc" />
<img width="921" height="469" alt="Screenshot 2026-06-08 185202" src="https://github.com/user-attachments/assets/6a04e1d1-e29d-4245-a36b-10053d629639" />
<img width="571" height="139" alt="Screenshot 2026-06-07 223455" src="https://github.com/user-attachments/assets/e6765bd6-d781-4c85-8754-44cfd7bba72d" />
<img width="552" height="250" alt="Screenshot 2026-06-07 223129" src="https://github.com/user-attachments/assets/5cd42f5e-6a7c-4402-aa0b-4157f449bdae" />
<img width="441" height="281" alt="Screenshot 2026-06-07 223020" src="https://github.com/user-attachments/assets/6efe6b2b-cacf-404e-a7e5-bce225dbc57b" />
<img width="871" height="135" alt="Screenshot 2026-06-07 222927" src="https://github.com/user-attachments/assets/01866c00-ed72-4e0d-86f5-d1040dccf59c" />
<img width="877" height="195" alt="Screenshot 2026-06-07 222439" src="https://github.com/user-attachments/assets/a81ce186-de91-4442-8a33-c35980780e56" />
<img width="837" height="784" alt="Screenshot 2026-06-07 221908" src="https://github.com/user-attachments/assets/1d8cadb6-695d-4f54-9722-3e322a41f636" />
<img width="849" height="462" alt="Screenshot 2026-06-07 221726" src="https://github.com/user-attachments/assets/604730e8-52db-41dd-a31d-afbb907b6b13" />
<img width="571" height="140" alt="Screenshot 2026-06-07 221628" src="https://github.com/user-attachments/assets/a237ae5c-ac1b-4e66-b7db-59fc74284ca0" />
<img width="649" height="580" alt="Screenshot 2026-06-07 221600" src="https://github.com/user-attachments/assets/d7ba2219-ec64-401c-9ff7-85b556581125" />
<img width="419" height="392" alt="quit and logging out from pstgres" src="https://github.com/user-attachments/assets/2f5c4ce7-62f8-431d-9453-c088069fdd56" />
<img width="439" height="98" alt="listing of folders ls" src="https://github.com/user-attachments/assets/7b9908dc-0773-4b97-a55d-3f919413585b" />
<img width="221" height="140" alt="list of schemas" src="https://github.com/user-attachments/assets/1758afb8-de7f-482c-976c-6deb5d14ac02" />
<img width="436" height="68" alt="from postgres to user lucya" src="https://github.com/user-attachments/assets/dfa069ee-f71e-4438-a138-2a9ac8aff219" />
<img width="461" height="235" alt="finding cardata on desktop" src="https://github.com/user-attachments/assets/cee6ddb8-d3a6-4342-bc79-cedd19598c26" />
<img width="286" height="70" alt="exiting from postgres" src="https://github.com/user-attachments/assets/ab463b1a-9e5d-402b-bba6-eba298c86b7f" />
<img width="425" height="231" alt="du" src="https://github.com/user-attachments/assets/7290e3a0-4429-41d6-89a9-566a6cdc5981" />

## Conclusion
Successfully accessed the remote server, navigated the file system, switched between user accounts, verified PostgreSQL installation, and examined CSV data. using scp.  The server is running Ubuntu 24.04 with PostgreSQL 16.14 ready for database operations.
