# Department Transfer — Active Directory & NTFS Permissions

## Scenario

Denise Carter transferred from the Accounting department to Human Resources. The request was to update her access so that she could access HR resources while no longer having access to Accounting departmental files.

## Environment

- Windows Server 2022
- Windows 11
- Active Directory Domain Services
- LAB.local domain
- Active Directory Users and Computers (ADUC)
- NTFS permissions
- Windows file shares
- Spiceworks Help Desk
- VirtualBox

## Tasks Performed

- Reviewed Denise Carter's existing Active Directory group membership.
- Removed Denise from the Accounting security group.
- Added Denise to the HR security group.
- Verified her updated group membership in Active Directory.
- Tested access to departmental network shares from her Windows 11 workstation.
- Confirmed Denise could access the HR mapped drive.
- Discovered that Denise could still access Accounting resources after being removed from the Accounting group.
- Investigated the Accounting folder's NTFS permissions.
- Identified overly broad permissions that allowed continued access.
- Corrected the Accounting folder permissions so access was restricted to the appropriate security group.
- Retested Denise's access after correcting the permissions.

## Issue Discovered

Removing Denise from the Accounting security group did not initially prevent her from accessing the Accounting shared folder.

During troubleshooting, I found that the folder's NTFS permissions were too broad. This meant access was still being granted independently of Denise's Accounting group membership.

I corrected the permissions so that access to the Accounting folder was controlled by the appropriate security group.

## Verification

After correcting the permissions:

- Denise successfully accessed the HR shared drive.
- Denise could access the HR Forms and Resumes folders.
- Denise was denied access to the Accounting shared folder.
- Her Active Directory group membership matched her new HR role.

## Key Takeaway

This lab demonstrated that Active Directory group membership and file permissions work together.

Adding or removing a user from a security group does not automatically guarantee the expected file access if the underlying NTFS permissions are configured incorrectly.

Using security groups to assign permissions also makes access easier to manage because permissions can be assigned to the group instead of individually configuring every user.

## Ticket Resolution

Updated Denise Carter's Active Directory group membership following her transfer from Accounting to HR. Removed Accounting membership and added HR membership. During verification, identified overly broad NTFS permissions that continued to allow access to the Accounting share. Corrected the Accounting folder permissions to restrict access to the appropriate security group. Verified Denise could no longer access Accounting resources and successfully accessed the HR mapped drive.
