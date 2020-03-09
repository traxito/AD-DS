# AD-DS
Operacions bàsiques per AD DS

Computer name (server name): Allways with a DC in the name EX: IPDC01
AD DS: active directory domain service ( the role that must be installed on the Windows Server to have AD on it)

Most used actions on AD:

Tools (upper right side) -> Active Directory users and computers

1. Create users: tick the option to enter a new password on next login, or tick "disable account" until the new worker arrives at the office.
2. Inside the user options (double click on user):
    • To use the same desktop on different computers: Profile-> user profile -> profile path: \\server01\roamingprofiles\%username%
    • To add the user to a group: Member of -> Add ->Enter the object name to select-> EX: domain admin -> check names-> ok

 3. Unlock accounts: 
     • Click on the icon upper-mid "Find objects in AD DS"
     • Choose what to find (users, contacts, groups) and where (entire AD or just the DS we are)
     • On "name" put the name of the account and click "Find"
     • If there are 2 ppl with the same name, check the "login name inside Account.
     • Inside Account, check "Unlock account"

4. Password reset and unlock account:
   • Right-click on user -> reset password and chose a new one. Check "unlock    account"

5. Create Group:
• Right-click on the domain-> new-> group:
• Group scope: Global is most used
• Group type: security for most users, Distribution for admins and so
• Move the group the proper organizational unit with right-click -> move
• A group can be a member of another group

6. Delete thing with protection activated: View (upper left) -> advanced features -> right click on the item to delete (like groups)->properties -> object -> uncheck "protect object from accidental delete" 

7. File share / printer share:
• Create the folder where you want-> right click-> properties-> sharing-> share-> put the user, group, or domain users (all the users on the domain)-> add -> Permission level-> read or read/write-> share
• On BAR inside the EXPLORER, type: \\NAMEOFSERVER\ -> press enter and all the share folders are there. Look for the folder to share, double click (open) and on the EXPLORER BAR, copy the path.
• Inside the AD users and computers: right click -> new-> Shared folder -> put a name for the folder-> paste the path of the shared folder-> share.


Description of folders inside Users and Computers:
1. Built-in domains: groups that are essential for the domain to operate.
2. Domain controllers: (The Windows Servers that controls the AD)
3. TYPE: organization unit: you can apply policies (used 9/10), CONTAINER you CANT

Apply policies to groups

GPO: GROUP POLICY OBJECT
OU: ORGANIZATIONAL UNIT

Tools-> Group Policy Management-> Select the forest -> select the domain ->  Starter GPO's to import or export policies or Group Policy objects to create a new one
