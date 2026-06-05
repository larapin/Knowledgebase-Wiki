# Windows and OS/2 troubleshooting

## OS/2 multiple file transfer issue
If multiple files fail to copy from an OS/2 SuperControl machine, it may be due to file permissions.
Use Manage Access on the share to apply new file permissions.

## OS/2 hidden folders and drivers
- Some OS/2 systems require the `VMOUSE.SYS` device line to be enabled in `sys.config`
- Some mice are not compatible with OS/2

## Multiple keyboards
OS/2 does not support multiple keyboards unless the machine has a dual circuit installed.

## Hard drive notes
- OS/2 and Windows 2000 systems have specific drive layouts
- Drive cloning should use proper disk-copy software
- Slaving drives is not recommended for recovery because it can corrupt the new drive

## Print screen note
On some Windows 2000 keyboards, Print Screen uses `Fn + Ctrl + PrnScr`
