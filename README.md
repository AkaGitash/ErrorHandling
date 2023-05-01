# ErrorHandling
Error Dumps in process of Advanced CC project.

# 1 Library already installed, but the error still persists (Solved)
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

# 2 importerror: cannot import name ‘config’ from ‘decouple’ ( Solved )
importerror: cannot import name ‘config’ from ‘decouple’ error mostly occurs because of a simple confusion between decouple and python-decouple package.
Step 1: Uninstall the package decouple – pip uninstall decouple
Step 2: Installing package python-decouple – pip install python-decouple

