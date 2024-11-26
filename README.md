This repo is merged MWCrashFix with MWFixes since they fix the common stack of issues in NFS Most Wanted.

# MWFixes  
A set of code-injected fixes and improvements to NFS Most Wanted stability. Grab the most recent release from [Releases page](https://github.com/GrimMaple/mwfixes/releases)

* Timebug
* Memory fittnes checks
* Attrib::StringToLowerCaseKey null-pointer dereference fix
* Roadblock spawn problem (pure virtual function call)
* Null-pointer dereference @ 0057D105
* Purecall handler trap to generate dump files


# MWCrashFix
https://github.com/x0reaxeax/MWCrashFix

## Description
 Fixes Debug Error: R6025 - pure virtual function call crash in Need for Speed Most Wanted 2005 1.3 BE.
 
 A widely used fix for this crash is implemented in @GrimMaple's mwfixes project, however, MWCrashFix (this mod) takes on a different approach for fixing this error, and that is by replacing the erroneous event with a different one, which should in theory not affect the spawn amount of pursuit events.
 
 This mod CAN be used along with the mwfixes project, however, the 'Roadblock spawn problem fix' in mwfixes will become obsolete.
 
 Usage
 Copy MWCrashFix.asi to scripts folder, which is located inside the main Need For Speed Most Wanted Black Edition game folder.
 
 You can grab the compiled ASI file from the Releases page, or compile it on your own.
 
 Troubleshooting
 Instruction Check error when starting the game:
 You're using an unsupported version of NFS MW. This mod was made for v1.3 RELOADED patch only.
 Additional information
 All instances of offending MOV r/m32, imm32 instruction in speed.exe, where imm32 is the erroneous address 0x00890970, are replaced with a MOV r/m32, 0x8aa828, with 0x8aa828 being an address of a non-offending pursuit event.
 
 Possible improvements
 Add more non-offending event addresses to provide a variety in pursuit event spawning.

