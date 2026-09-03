# New Employee Onboarding — Active Directory

## Scenario
A new employee, Marcus Reed, was starting in the Accounting department. The request was to create his domain account, assign the appropriate Accounting access, require a password change at first login, and provide access to the department's shared resources.

## Environment
- Windows Server 2022
- Windows 11
- Active Directory Domain Services
- LAB.local domain
- Spiceworks Help Desk
- VirtualBox
## Tasks Performed

- Created a domain user account for Marcus Reed using Active Directory Users and Computers (ADUC).
- Assigned a temporary password and configured the account to require a password change at first login.
- Added Marcus Reed to the Accounting security group.
- Signed into the domain-joined Windows 11 workstation using Marcus's account.
- Mapped the Accounting departmental shared drive to the workstation.
- Verified that Marcus could successfully access the Accounting department's shared folders.

## Verification

Confirmed that Marcus Reed could authenticate to the LAB.local domain and access the mapped Accounting drive, including the Funding, Invoices, and Payroll departmental folders.

## Ticket Resolution

Documented the completed onboarding work in Spiceworks and closed the ticket after verifying access.
