# Security and access control

## Windows security on Thermwood controls
Windows file and directory permissions can be used to limit machine operator access.
This should only be done by an experienced IT person.

## General approach
1. Log on as Administrator.
2. Open Explorer and locate the data or part directory.
3. Open Properties and go to the Security tab.
4. Add the Administrator user and grant Full Control.
5. Use Advanced settings and disable inheritance if needed.
6. Remove the Administrators group only after Administrator has been added.
7. Do not remove the SYSTEM account.
8. Add Thermwood and operator users with the desired permissions.

## Notes
- If the Administrator sets a directory to Read only, it will stay that way.
- Improper security changes can cause major problems, including the need for a hard disk rebuild.
