<p align="center">
<img width="250" height="200" alt="image" src="https://github.com/user-attachments/assets/a0cbfeb7-3da8-40ff-8cbe-331738fa444c" />
</p>  

# Password-Resetting-and-Account-Unlocking-in-Active-Directory
This project demonstrates common IT Help Desk tasks performed using Microsoft Active Directory Domain Services (AD DS).  The project focuses on managing user accounts and resolving common account-related issues, including password resets, locked user accounts, and disabling user accounts.

# Goal:
* The goal of this project is to gain hands-on experience managing user accounts within a Microsoft Active Directory environment

# Environments and Technologies Used
* Microsoft Active Directory Domain Services (AD DS)
* Active Directory Users and Computers (ADUC)
* Windows Server
* Windows 10/11 Client
* Windows Virtual Machine
* Remote Desktop Protocol (RDP)
* Microsoft Azure Virtual Machines
* Azure Virtual Network
* Command Prompt 

# Operating Systems Used
* Windows Server — Active Directory Domain Controller
* Windows 10/11 — Domain-joined client computer

# High-Level Deployment and Configuration Steps
1. Choose simulated employee from Active Directory domain controller.   
2. Login into the client computer under the user in the domain.
3. Simulate a locked user account.
4. Unlock the user's account using Active Directory Users and Computers.
5. Reset the user's password using Active Directory Users and Computers.
6. Disable the user's account in Active Directory.
7. Re-enable the account and verify that the user can log in again.

# Deployment and Configuration Steps

<p align="center">
<img width="1920" height="1080" alt="20 246 70 236 - Remote Desktop Connection 8_13_2026 3_25_27 AM" src="https://github.com/user-attachments/assets/a314d61b-2f3c-4be9-9894-cd398ef79714" />
</p> 

The first step in our project is to choose the employee located in our Domain Controller that we are going to be helping. In this case shown above, we will be choosing (an employee) or account named (baf.siv). You will find this under Active Directory Users and Computers.

<p align="center">
<img width="608" height="695" alt="Remote Desktop Connection 8_13_2026 3_38_15 AM" src="https://github.com/user-attachments/assets/ee6e09a3-feb2-421c-bc8c-6de71c37cec1" />
</p>

Next, we will attempting to login as the user to verify that the account is properly working. This will then allow us to simulate a future issue resulting in a needed password reset. When logging into the user, you will verify the Public IP Address and username under the domain name followed by the password of the account. 
##### Note: In very common scenarios when users are trying to login and fail, they decide to contact Help Desk because they have forgotten their password. 

<p align="center">
<img width="1501" height="702" alt="image" src="https://github.com/user-attachments/assets/7287458e-42e2-41f4-9307-e6cd2756d70e" />
</p> 

For reference, once you implemented the information to login to the user to verify if everything is correct, you can use the command prompt to further confirm you are now logged in as the correct user.

<p align="center">
<img width="684" height="748" alt="image" src="https://github.com/user-attachments/assets/0b061a5c-e262-4563-ba11-a3165533df7f" />
</p> 

Next, we are going to simulate a password lockout using the users account we verified was properly working using the correct password. Continuously fail the login in order to lock the account. Based off the Group Policy settings, password lockouts can take as many as a couple to possibly over 10 attempts to lockout. 

<p align="center">
<img width="834" height="186" alt="image" src="https://github.com/user-attachments/assets/a7fc9870-6a32-4f5d-8377-f7d0a20542a0" />
</p> 

Once you have successfully locked the account, a notification will be shown to contact support or system administrator because of the amount of failed login attempts. 

<p align="center">
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/96d64b84-312b-4a8a-9020-74facd3d594c" />
</p> 

Next, we will return back to Active Directory on the domain controller computer and find the user who has contacted us explaining they were locked out of their account.    

<p align="center">
<img width="613" height="816" alt="20 246 70 236 - Remote Desktop Connection 8_13_2026 4_20_01 AM" src="https://github.com/user-attachments/assets/5482a6af-4762-4d9e-8ee1-7f81ca728589" />
</p> 

Furthermore, under Account, you will now see a notification stating the account is locked and a box allowing you to confirm whether the account should be unlocked again. After unlocking the account, the simulated user (baf.siv) will be able to attempt more logins.

<p align="center">
<img width="1090" height="872" alt="image" src="https://github.com/user-attachments/assets/81aacf66-0919-4710-9618-962cc93db701" />
</p> 

Next, similar to the previous step we will use the same user to reset their password in case they forgot it and can no longer login. You will return once again to the Active Directory and find the user, instead of clicking on their account you will right-click on the user. There will be a visible option that we will use to reset the user's password. 

<p align="center">
<img width="1103" height="812" alt="20 246 70 236 - Remote Desktop Connection 8_13_2026 4_39_18 AM" src="https://github.com/user-attachments/assets/02bc4a10-0a4e-487d-b53a-a13a45c77fb9" />
</p> 

This will then prompt you to change the password of the user and also unlock the account once again if it was locked out previously. After applying the new password, it will automatically reset and allow (baf.siv) to login using their new password. 






