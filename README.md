# my_project_docs
# GitHub & Server Access Documentation

## Overview
This document outlines the steps performed to access a remote Ubuntu server via SSH, switch between user accounts, and interact with PostgreSQL and CSV data files.

<img width="425" height="231" alt="du" src="https://github.com/user-attachments/assets/6e14a1a1-7f40-4c15-8604-abc477603967" />

<img width="461" height="235" alt="finding cardata on desktop" src="https://github.com/user-attachments/assets/386882b0-ced5-462b-831b-67b52c55390d" />

<img width="221" height="140" alt="list of schemas" src="https://github.com/user-attachments/assets/aaa9db6f-816d-4905-bbfd-11e78ee3dd35" />

<img width="419" height="392" alt="quit and logging out from pstgres" src="https://github.com/user-attachments/assets/6eaef72a-6156-446f-a660-e7afd2a4f59d" />

<img width="877" height="195" alt="Screenshot 2026-06-07 222439" src="https://github.com/user-attachments/assets/a462527a-6dcb-4d4e-ad4f-3a92aab4e0e8" />

<img width="441" height="281" alt="Screenshot 2026-06-07 223020" src="https://github.com/user-attachments/assets/61dcc7d2-df69-4394-9d0a-a1bd51a030ab" />

<img width="571" height="139" alt="Screenshot 2026-06-07 223455" src="https://github.com/user-attachments/assets/0441e1b7-d808-42b0-8835-78fdf71d4e01" />

<img width="276" height="125" alt="view table data in lucya" src="https://github.com/user-attachments/assets/620072fa-b64f-4cba-9015-3a7d40deeb3e" />

<img width="286" height="70" alt="exiting from postgres" src="https://github.com/user-attachments/assets/721da80a-b41b-4df0-abc7-f4b769f408dc" />

<img width="436" height="68" alt="from postgres to user lucya" src="https://github.com/user-attachments/assets/a7fd9c0e-613c-4b96-bff7-4f7f9a351c6d" />
<img width="439" height="98" alt="listing of folders ls" src="https://github.com/user-attachments/assets/a4bb5f23-1979-45cd-802f-504f218e331e" />

(Listing folders jusing the ls command)
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
<img width="441" height="281" alt="Screenshot 2026-06-07 223020" src="https://github.com/user-attachments/assets/3a714a7d-5971-4cd1-ba42-4dffa13f35bb" />


### 6. View CSV Data File
Displayed the contents of `cardata.csv` containing car dealership information.
<img width="276" height="125" alt="view table data in lucya" src="https://github.com/user-attachments/assets/61b02f52-2704-4a2c-96f8-d70cb66694f2" />

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

## Conclusion
Successfully accessed the remote server, navigated the file system, switched between user accounts, verified PostgreSQL installation, and examined CSV data. using scp.  The server is running Ubuntu 24.04 with PostgreSQL 16.14 ready for database operations.
