# How to Register C# DLLs Without Administrator Privileges Using Excel VBA

Unlike native C++ DLLs, you cannot simply add a direct file reference in the VBA editor. 
When you create custom class libraries in C# and want to use them in Excel, you must register them using `regasm.exe`. 

The main caveat is that running `regasm.exe` from the command line typically requires administrator privileges.

This repository provides a workaround to register and unregister C# DLLs without requiring elevated access.

## Registration
1. Copy the contents of `Register.txt` into any module in your VBA project.
2. Run the `RegisterDLL` sub, passing the full path to your DLL as an argument.

## Unregistration
1. Copy the contents of `Unregister.txt` into any module in your VBA project.
2. Run the `UnregisterDLL` sub, passing the full path to your DLL as an argument.

> 💡 **Note:** This approach was inspired by a Stack Overflow solution. The original link is no longer available, but full credit goes to the SO community.
