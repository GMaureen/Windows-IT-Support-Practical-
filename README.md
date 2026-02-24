# Windows-IT-Support-Practical-

# Windows IT Support Practical Task - By Galaletsang Maureen Mokgele

This practical task demonstrates **user management, file management, and software installation** using the Windows command line as an IT support professional. The goal is to practice key IT support skills such as creating users and groups, managing file permissions, and installing software via the command line.

---

## Step 1 — Open Command Prompt as Administrator
**Description:** Opened Command Prompt with administrator privileges to perform system-level tasks. Administrator access is required to create users, groups, and modify permissions.
**Screenshot:** Step1_CMD_Admin.png 

<img width="451" height="141" alt="Step1_CMD_Admin" src="https://github.com/user-attachments/assets/1da1e7aa-4f6f-48a7-a879-4678f7a53d31" />


## Step 2 — Create a New User
**Description:** Created a new user account named `supportuser` using the `net user` command. This simulates adding a new employee to the system.
**Command Used:** `net user supportuser Password123 /add`
**Screenshot:** Step2_CreateUser.png

<img width="526" height="196" alt="Step2_CreateUser" src="https://github.com/user-attachments/assets/c779691f-478d-4216-9608-01f992d58193" />


## Step 3 — Create a New Group
**Description:** Created a local group named `itgroup` using the `net localgroup` command. Groups are used to manage multiple users with similar permissions.
**Command Used:** `net localgroup itgroup /add`
**Screenshot:** Step3_CreateGroup.png

<img width="500" height="150" alt="Step3_CreateGroup" src="https://github.com/user-attachments/assets/8dc6f209-21c0-47d3-9c24-6f7a796f1336" />


## Step 4 — Add User to the Group
**Description:** Added the user `supportuser` to the `itgroup` group using the `net localgroup` command. This ensures the user inherits the permissions assigned to the group.
**Command Used:** `net localgroup itgroup supportuser /add`
**Screenshot:** Step4_AddUserToGroup.png

<img width="542" height="115" alt="Step4_AddUserToGroup" src="https://github.com/user-attachments/assets/bc424736-9592-4082-b392-46f446336020" />


## Step 5 — Create a Folder
**Description:** Created a folder named `C:\ITSupportPractice` using the `mkdir` command. This folder will store files for testing permissions and access control.
**Command Used:** `mkdir C:\ITSupportPractice`
**Screenshot:** Step5_CreateFolder.png

<img width="503" height="132" alt="Step5_CreatoeFolder" src="https://github.com/user-attachments/assets/82de46d8-02b0-4acc-989b-91fdcff396e1" />


## Step 6 — Create a File
**Description:** Created a test file named `report.txt` inside the folder using the `echo` command. This file will be used to demonstrate permissions management.
**Command Used:** `echo This is a test file > C:\ITSupportPractice\report.txt`
**Screenshot:** Step6_CreateFile.png

<img width="670" height="99" alt="Step6_CreateFile" src="https://github.com/user-attachments/assets/3e60d83a-5874-4ecf-8c99-693135d8bcc9" />


## Step 7 — Check File Permissions
**Description:** Checked the current permissions of `report.txt` using the `icacls` command. This shows which users and groups have access and what type of access they have.
**Command Used:** `icacls C:\ITSupportPractice\report.txt`
**Screenshot:** Step7_CheckPermissions.png

<img width="660" height="161" alt="Step7_CheckPermissions" src="https://github.com/user-attachments/assets/03a236a4-92c5-4a33-bd8d-7de44741d197" />


## Step 8 — Grant Group Read Permission
**Description:** Granted read access to the `itgroup` group for the file `report.txt` using the `icacls /grant` command. This demonstrates controlled access for a group of users.
**Command Used:** `icacls C:\ITSupportPractice\report.txt /grant itgroup:R`
**Screenshot:** Step8_GrantPermissions.png

<img width="657" height="89" alt="Step8_GrantPermissions" src="https://github.com/user-attachments/assets/2f92476b-d61d-425d-9728-1b1237694d78" />


## Step 9 — Install Chocolatey
**Description:** Installed Chocolatey, a Windows package manager, to enable software installation via the command line. This simulates IT support software deployment.
**Commands Used:**
1. `Set-ExecutionPolicy Bypass -Scope Process -Force`
2. `@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"`
3. `choco -v`
**Screenshots:** Step9a_ExecutionPolicy.png, Step9b_ChocolateyInstall.png, Step9c_ChocolateyVersion.png

<img width="300" height="67" alt="Step9_ChocoCheck" src="https://github.com/user-attachments/assets/79959ebc-8560-43d4-ac71-ddf12bbfc263" />


## Step 10 — Install Git via Chocolatey
**Description:** Installed Git using Chocolatey. This demonstrates software installation via the command line, a common IT support task.
**Command Used:** `choco install git -y`
**Screenshot:** Step10_ChocoInstall.png

<img width="892" height="472" alt="Step10_ChochInstall" src="https://github.com/user-attachments/assets/5ce30c03-6f10-41ca-bc64-74655160c971" />


## Step 11 — Verify Git Installation
**Description:** Verified that Git was installed successfully by checking its version using the `git --version` command.
**Command Used:** `git --version`
**Screenshot:** Step11_VerifyInstall.png

<img width="816" height="487" alt="Step11_VerifyInstall" src="https://github.com/user-attachments/assets/68cfd901-0a3b-40d2-8e2b-a161b64f5c6c" />


---

### Notes
- Each screenshot corresponds to the step above for clarity.
- This practical task demonstrates key IT support skills: **user & group management, file permissions, and software installation**.

---

**Prepared by:** Galaletsang Maureen Mokgele
