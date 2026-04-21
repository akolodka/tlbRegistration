# VBA Subroutines for Registering C# DLLs Without Admin Rights

When you create custom class libraries in C# and want to use them in VBA, you must register them using `regasm.exe`. 
Unlike native C++ DLLs, you cannot simply add a direct file reference in the VBA editor.

The main caveat is that running `regasm.exe` from the command line typically requires administrator privileges. These subroutines provide a workaround to register and unregister DLLs using only standard user permissions.



## Registration
1. Copy the contents of `Register.txt` into any module in your VBA project.
2. Run the `RegisterDLL` sub, passing the full path to your DLL as an argument.

## Unregistration
1. Copy the contents of `Unregister.txt` into any module in your VBA project.
2. Run the `UnregisterDLL` sub, passing the full path to your DLL as an argument.

> 💡 **Note:** This approach was inspired by a Stack Overflow solution. The original link is no longer available, but full credit goes to the SO community.
