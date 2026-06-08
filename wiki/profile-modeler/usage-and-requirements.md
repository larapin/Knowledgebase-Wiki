# Usage and requirements

## Legacy reference
The following information applies to older standalone Profile Modeler workflows and legacy controls.

## Overview
Profile Modeler was previously used for profile-based machining and could be run stand-alone or linked with Control Nesting.

## Legacy requirements
### Stand-alone minimums
- THM V5.05 Build 7 or higher for SIO controls on Windows 2000
- THM V6.0.7.1 or higher for GEN II controls
- Control Nesting V5.10 or higher

### Linked with Control Nesting minimums
- THM V5.05 Build 9 or higher
- THM V6.1.0.4 or higher
- Control Nesting V5.10 or higher

## Notes
- Parts were viewed and written in Imperial code.
- Tooling in the Modeler had to be set up in Imperial.
- The lower-left corner, as viewed in the Modeler, was the program origin.
- Some parts with different profiles could still require toolchanges even if the same tool was used.

## Legacy workflow
1. Start the process in eCab software.
2. Design the tool geometry and save it as a `.tol` file.
3. Save the cabinet or boardstock file.
4. Write the CNC file.
5. Load the `.twd` file into Profile Modeler at the control.
6. Select the part and region.
7. Edit tool cutting parameters if needed.
8. Regenerate the toolpath after changes.
