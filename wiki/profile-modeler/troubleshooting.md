# Troubleshooting

## Default group contains no tools
If Profile Modeler says the default group contains no tools:
- Open Regedit.
- Go to `current_user\software\thermwood\Profile_modeler\App_properties\tool_group`.
- Reset the value to `Generic`.
- Restart Profile Modeler.

## Install or DLL issues
If you get `couldn't find installable ISAM` or Operator error 4260:
- Verify the installer.
- Put the correct DLL in the Profile Modeler directory.

## Control Nesting and Profile Modeler link issues
If Control Nesting with Profile Modeler is not working correctly:
- Make sure system minimums are met.
- Check for the `rnestwithPF.dll` file in the Profile Modeler directory.
- Run the latest Control Nesting update and choose Repair or install.
