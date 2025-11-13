# OPEN-SOURCE-EX-4
# NAME:SOUNDARYA J
# REG NO:212223220108
 # Aim

To create a collaborative directory /common/admin with restricted access, group ownership assigned to admin, and automatic group inheritance for new files in Red Hat Enterprise Linux.

# Algorithm
<h2>Step 1:</h2>
Start the Terminal as Root.
Open the terminal and switch to the root user or use administrative privileges.
<h2>Step 2</h2>
Create the Directory Structure.
Create the directory /common/admin (use the -p option to create any missing parent directories).
<h3>Step 3</h3>
Set Group Ownership.
Change the group ownership of /common/admin to the group admin.
<h2>Step 4:</h2>
Set Appropriate Permissions.
Assign permissions so that only users who are members of admin can read, write, and access the directory, while others have no access.
<h2>Step 5:</h2>
Enable the Setgid Bit.
Apply the setgid (2) permission bit on the directory so that all new files and subdirectories created inside automatically inherit the admin group ownership.
<h2>Step 6:</h2>
Verify Permissions.
List directory details to confirm ownership, permissions, and the presence of the setgid bit.
<h2>Step 7:</h2>
Confirm User Group Membership.
Check that users such as harry are part of the admin group to ensure they can access the directory.

# Steps Involved
```
STEP 1 : sudo mkdir -p /common/admin
STEP 2 : sudo chown root:admin /common/admin
STEP 3 : sudo chmod 2770 /common/admin
STEP 4 : ls -ld /common/admin

# Expected Output:
# drwxrws--- 2 root admin ... /common/admin
STEP 5 : groups harry
```
# Output
<img width="916" height="619" alt="image" src="https://github.com/user-attachments/assets/b7909c77-3b47-4b27-9d50-21e6ab563c8d" />



# Result

Thus, the collaborative directory /common/admin was successfully created with group ownership admin, restricted access to non-members, and automatic group ownership inheritance in Red Hat Enterprise Linux.
