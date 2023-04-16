# ErrorHandling
Error Dumps

# 1 Library already installed, but the error still persists
& : File C:\Users\pc\Documents\python\venv\Scripts\Activate.ps1 cannot be loaded because running scripts is 
    disabled on this system. For more information, see about_Execution_Policies at 
    https:/go.microsoft.com/fwlink/?LinkID=135170.
    At line:1 char:3
    + & c:/Users/pc/Documents/python/venv/Scripts/Activate.ps1
    +   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
        + CategoryInfo          : SecurityError: (:) [], PSSecurityException       
        + FullyQualifiedErrorId : UnauthorizedAccessenter code here

Solution :

This is because the user your running the script as has a undefined ExecutionPolicy You could fix this by running the following in powershell:

Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted

after this you will see an "(env)" written before your code file path e.g:
(env) PS C:\Users\AKASH YADAV\Desktop\Codes\stts-Whisper> pip uninstall pyttsx3

then install all the dependencies.

