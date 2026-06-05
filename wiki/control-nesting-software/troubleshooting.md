# Troubleshooting

## Problem reading INI / machine type
If Control Nesting reports it cannot verify the correct machine type or gets `GetProfString failed for Machine_ID`:
- Run the `delete-XP_upgrade-installer.reg` fix.

## JET database / access conflicts
If the Microsoft JET Database Engine reports access conflicts:
- Close Control Nesting.
- Delete `history.mdb` from `C:\RollingNest\SavedHistory`.
- Delete `history_old.mdb` from `C:\RollingNest`.
- Run the Control Nesting install utility and choose Repair or Remove and install.

## Crystal Reports runtime error
If labels fail to print due to Crystal Reports runtime errors:
- Download and run the Crystal Reports installer package.

## Launching Control Nesting a second time
If Control Nesting crashes on the second launch:
- Delete all Tools files in `C:\RollingNest`.
- Reset up all tooling afterward.

## Syntax error loading multiple MDB files
- Run the current Control Nesting update and choose Repair.

## Nstlib / existing database errors
- Load `.twd` files through Control Nesting, not directly as a part program.
- Shorten long DXF file names.
- Repair the install or remove `N32DLL.DLL` if needed.

## Slow performance
- Run Defrag on the PC.

## No data to nest / invalid bookmark / DAO errors
- Verify files are not corrupt.
- Run the latest update.
- Install DAO components if needed.
- Check printer and report settings.

## Database already exists
- Delete `resultx.mdb` if present.
- Delete `inputx.twd` if present.
- Clear `C:\temp`.

## No current record
- Delete `history.mdb`.
- Reinstall or repair the latest version.
- Check nested direction and angle settings.
- Inspect DXF geometry for broken segments.

## Screen freezes or no labels
- Repair or reinstall Control Nesting.
- Delete `history.mdb` if needed.
- Verify label printer power, roll condition, and printer setup.

## Other known errors
- `RNest.dll` update issues
- `RNest Record is Deleted`
- `couldn't find installable ISAM`
- `CryptAcquire Context` errors
- `Unrecognized database file for input`
- `Too Few Parameters`
- `Invalid database / Get Rows Binding Error`
- `Error 80090016`
- `Label Does Not Exist`
- `Error 6100`
- `Axis motion has been inhibited by PLC`
