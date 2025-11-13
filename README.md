# Lab 3: Active Directory — User, OU, and Group Management 
**Created by:** Terrence Edwards 
--- 
## 🧩 Overview 

In this lab, we’ll build on what we learned in **Lab 2** and dive deeper into managing users, groups, and permissions within **Active Directory (AD)**

You’ll learn how to: 
> ➕ Add new users

> 👥 Add users to groups with different permissions

> 📋 Copy a user

> 🔐 Reset a password

> 🔓 Unlock an account

> 🔁 Move users between OUs

> 🧭 Search for users

> ⚙️ Understand **Security Groups vs Distribution Lists**

  
> This lab focuses on hands-on Active Directory user and group management — all within a Windows Server Domain Controller hosted in Azure.


---


## Step 1: Recap — Creating Organizational Units (OUs) and Users
   - Before managing accounts and permissions, let’s quickly recap how to create OUs and users. This ensures your directory structure is clean and organized.


### 🧱 Create Organizational Units (OUs) 
1. Open **Active Directory Users and Computers (ADUC)**.
2. Right-click your **domain name** → **New → Organizational Unit**.
3. Name the OU (example: Branch1) → Click **OK**.
4. Screenshots below for reference:
5. ![Create OU](https://github.com/user-attachments/assets/b65f085e-c815-4e3a-b0ee-5069afce7883)
6. ![Branch1 OU](https://github.com/user-attachments/assets/39fcc5ea-baf9-4699-ad65-d71c56c75b11) 

7. Repeat this process to create additional OUs such as:
   - Users
     
   - Computers
     
   - Groups

   
> 🧠 **Why OUs Matter:**
   > Organizational Units allow you to group similar objects (like users or computers) and apply specific **Group Policies** to them.

   > OUs provide logical structure and control. They allow administrators to:

      > Delegate control to department heads or junior admins.
      
      > Keep the domain organized for easier maintenance and security.
      
      > Think of OUs as *folders* that help you manage and secure AD resources more efficiently.

   
   ---


### 👤 Create a User in Active Directory

   1. Right-click on your **Users OU** (for example, Branch1 → Users).
   2. Select **New → User**. ![Create User](https://github.com/user-attachments/assets/d5b52fbc-096d-447c-a066-5ece45d1150b)
   3. Fill out the user details (First name, Last name, User logon name) → Click **Next**. ![User Info](https://github.com/user-attachments/assets/4e3a4f6f-1301-4c26-9d89-caf51620e170)
   4. Set the password and configure account options (like “User must change password at next logon”). ![Password Setup](https://github.com/user-attachments/assets/52bbed9f-cebd-4481-87f5-325482ed9e9e)
   5. Click **Finish** — your new user (e.g., *Tez Dough*) should now appear under your OU. ![First User](https://github.com/user-attachments/assets/e183b16d-0099-45ce-8ead-ac3632255b73)


## Step 2: Managing Users and Groups (Coming Next) 

In the next section, we’ll cover: 
> Adding users to groups

> Creating **Security Groups vs Distribution Lists**

> Copying and resetting users

> Unlocking accounts

> Moving users between OUs

> Searching for specific users efficiently

>  ⚙️ Each of these actions helps keep your Active Directory environment organized, secure, and easy to manage — especially in large organizations or hybrid setups.


 ---

 
➕ Adding Users to a Security Group

> Adding users to a group ensures they automatically inherit all permissions assigned to that group.

> Open Active Directory Users and Computers (ADUC).

> Navigate to your Groups OU and locate the group (example: IT_Admins).

> Right-click the group → Select Properties.

> Go to the Members tab → Click Add.

> Enter the username(s) of the users you want to add → Click Check Names → Click OK.

> The selected user(s) will now appear in the group’s Members list.

🧠 Importance:
   > Adding users to groups allows administrators to:

   > Grant access to shared resources efficiently

   > Maintain consistent permissions across multiple users

   > Simplify auditing and compliance checks

      > Example: Instead of giving individual access to a shared folder for 10 users, you give access to IT_Admins, and everyone in the group automatically inherits it. Groups reduce administrative overhead,             ensure consistent permissions, and make auditing easier.


---


📋 Copying a User

   > Copying a user allows you to duplicate an existing user account, inheriting the same properties and group memberships.

   > Right-click on an existing user → Select Copy.

   > Enter the new user’s details (e.g., First Name, Last Name, Username).

   > Click Finish.

🧠 Why Copy Users:
   > Saves time when onboarding new employees with similar roles, ensuring consistent permissions without re-entering all data manually.


---


🔐 Resetting a Password

   > If a user forgets their password or their account is locked:

   > Right-click on the user account → Reset Password.

   > Enter the new password → Click OK.

   > Optionally, select User must change password at next logon. -> **Great Security Practice**

🧠 Importance:
Resets keep accounts secure and allow users to regain access quickly without exposing administrative credentials.


---


🔓 Unlocking an Account

   > Accounts can lock after multiple failed login attempts. To unlock:

   > Right-click the user → Properties → Account tab.

   > Check Unlock account → Click Apply.

🧠 Why:
Unlocking accounts restores productivity while maintaining security, avoiding unnecessary downtime.

---


🚚 Moving Users Between OUs

   > Moving users helps keep your AD organized and ensures the correct policies are applied.

   > Right-click on the user → Select Move.

   > Choose the destination OU → Click OK.

🧠 Importance:
Proper OU placement allows policies to apply correctly (e.g., security settings, login scripts) and keeps the directory clean.


---


🔍 Searching for a User

   > Efficient user management requires quickly finding accounts:

   > Right-click your domain → Find.

   > Enter the username → Click Find Now.

   > The results appear below.

🧠 Why Searching Matters:
With large organizations, manually locating users is time-consuming. Search ensures quick access for management and troubleshooting.


---


### 🧾 Security Groups vs Distribution Lists

| Type               | Purpose                        | Assign Permissions? | Email Use? |
|-------------------|--------------------------------|-------------------|------------|
| **Security Group** | Manage access to shared resources | ✅ Yes            | ❌ No      |
| **Distribution List** | Send email to multiple users      | ❌ No             | ✅ Yes     |

💡 **Tip:**  
- Use **Security Groups** to manage access to resources like folders or printers.  
- Use **Distribution Lists** for communication via email.

---


Step 3: Key Takeaways

   > Organize users into OUs for structure and policy application.

   > Use Security Groups to efficiently manage permissions.

   > Copying users streamlines onboarding.

   > Resetting and unlocking accounts keeps your AD environment secure and functional.

   > Moving users ensures policies apply correctly.

   > Searching simplifies management in large environments.


⚙️ With these steps, your Active Directory environment will be organized, secure, and manageable, even in large or hybrid setups.


---


## ⚙️ Sneak Peek: Lab 4 — Group Policy Management (GPOs)

Get ready to level up your Active Directory skills! In **Lab 4**, we’ll dive into **Group Policy Objects (GPOs)** and learn how to control your domain like a pro.

### Hands-On Exercises You’ll Do:
- **Create and link GPOs** to specific OUs for targeted control  
- **Enforce security settings** automatically across users and computers  
- **Deploy login scripts** that run on multiple machines  
- **Customize desktop environments** for different groups of users  
- **Manage passwords and account policies** at scale  

> 🧠 **Why it matters:**  
> GPOs let administrators **automate and enforce rules** across an entire domain — keeping your network secure, compliant, and efficient.  
> By mastering GPOs, you’ll be able to **control settings for hundreds or thousands of users at once**, a crucial skill in enterprise IT environments.

