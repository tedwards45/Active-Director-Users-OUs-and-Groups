# Lab 3: Active Directory — User, OU, and Group Management
**Created by:** Terrence Edwards  

---

## 🧩 Overview
In this lab, we’ll build on what we learned in **Lab 2** and dive deeper into managing users, groups, and permissions within **Active Directory (AD)**.

You’ll learn how to:
- ➕ Add new users  
- 👥 Add users to groups with different permissions  
- 📋 Copy a user  
- 🔐 Reset a password  
- 🔓 Unlock an account  
- 🔁 Move users between OUs  
- 🧭 Search for users  
- ⚙️ Understand **Security Groups vs Distribution Lists**

> This lab focuses on hands-on Active Directory user and group management — all within a Windows Server Domain Controller hosted in Azure.

---

## Step 1: Recap — Creating Organizational Units (OUs) and Users
Before managing accounts and permissions, let’s quickly recap how to create OUs and users. This ensures your directory structure is clean and organized.

### 🧱 Create Organizational Units (OUs)
1. Open **Active Directory Users and Computers (ADUC)**.  
2. Right-click your **domain name** → **New → Organizational Unit**.  
3. Name the OU (example: `Branch1`) → Click **OK**.  
   ![Create OU](https://github.com/user-attachments/assets/b65f085e-c815-4e3a-b0ee-5069afce7883)  
   ![Branch1 OU](https://github.com/user-attachments/assets/39fcc5ea-baf9-4699-ad65-d71c56c75b11)

4. Repeat this process to create additional OUs such as:
   - `Users`
   - `Computers`
   - `Groups`

> 🧠 **Why OUs Matter:**  
> Organizational Units allow you to group similar objects (like users or computers) and apply specific **Group Policies** to them.
> OUs provide logical structure and control. They allow administrators to:
   > Delegate control to department heads or junior admins.
   > Keep the domain organized for easier maintenance and security. 
   > Think of OUs as *folders* that help you manage and secure AD resources more efficiently.

---

### 👤 Create a User in Active Directory
1. Right-click on your **Users OU** (for example, `Branch1 → Users`).  
2. Select **New → User**.  
   ![Create User](https://github.com/user-attachments/assets/d5b52fbc-096d-447c-a066-5ece45d1150b)

3. Fill out the user details (First name, Last name, User logon name) → Click **Next**.  
   ![User Info](https://github.com/user-attachments/assets/4e3a4f6f-1301-4c26-9d89-caf51620e170)

4. Set the password and configure account options (like “User must change password at next logon”).  
   ![Password Setup](https://github.com/user-attachments/assets/52bbed9f-cebd-4481-87f5-325482ed9e9e)

5. Click **Finish** — your new user (e.g., *Tez Dough*) should now appear under your OU.  
   ![First User](https://github.com/user-attachments/assets/e183b16d-0099-45ce-8ead-ac3632255b73)


## Step 2: Managing Users and Groups (Coming Next)
In the next section, we’ll cover:
- Adding users to groups  
- Creating security vs distribution groups  
- Copying and resetting users  
- Unlocking accounts  
- Moving users between OUs  
- Searching for specific users efficiently  

> ⚙️ Each of these actions helps keep your Active Directory environment organized, secure, and easy to manage — especially in large organizations or hybrid setups.

---

