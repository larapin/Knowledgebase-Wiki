# Errors and fixes

## Buffer overrun
Possible causes include:
- Program name too long
- Bad program end marker
- Multiple programs running besides THM
- `plchist.thm` corruption
- Running files from a network location instead of the control

## Invalid system configuration
If the control reboots with invalid configuration data, check CMOS settings.

## THM.EXE runtime and entry point errors
Possible causes:
- Corrupt Toolman file
- Read-only file attributes
- Bad hard drive
- Bad SIO board

## Spindle not starting
- Check that spindle speed is specified before the tool call
- Check the active tool life left
- Check the frequency converter reset

## Tool change and program issues
- `plchist.thm` or `tool-in-use.thm` may need to be deleted after a missed toolchange
- Invalid actuator errors may require replacing `Toolman.thm` with a backup
- Some label errors are caused by label limits in older OS/2 versions

## PLC and motion errors
- Error 6100: axis motion inhibited by PLC
- Error 19 on boot: check updated software or restore media
- PLC.EXE and MSU missing errors often point to corrupt system files or board issues

## File access and startup issues
- If THM does not start automatically, check user/password settings
- If files are not visible, verify file paths and run disk checks as needed

## Other known issues
- Cmarker values resetting on reboot
- Machine moving but screen still scrolling
- Program misses toolchange
- Circular cuts become odd shapes when arc decimal precision is inconsistent
- User-only access can cause crashes in some XP control setups
