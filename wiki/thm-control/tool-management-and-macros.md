# Tool management and macros

## Ghost macros
When tool management was introduced, Thermwood used ghost macros to handle different tool change paths.

### How they work
- A `T` call tells the PLC a tool change is needed.
- The PLC determines the tool change type.
- The PLC starts the appropriate macro.
- THM temporarily inserts the ghost macro and a `M00` into the program.
- Once the macro finishes, THM removes the ghost macro and resumes the part program.

### Notes
- Ghost macros are most likely to remain if an interruption happens right during the tool change.
- GEN II controls have a shorter communication window, so the issue is less likely.

## Universal PLC macros written on the fly
- Starting with THM V7.3, the Universal PLC writes most macros each time they are called.
- Custom macros remain untouched.

## Multiple MSU files
Some controls use multiple MSU files, such as rotary and non-rotary versions.
- Files reside in `C:\MSUFMT`
- At boot, the selected MSU BIN is copied into `C:\System`

## Tangency factor note
- Tangency Factor behavior changed in some GEN II versions
- Older values may not act the same after later updates
