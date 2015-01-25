# hideProcess
'hideProcess' hides a process from the Task-Manager on Windows2k/Windows7 (x86/x64 bit)! 

Your process can inject it into other processes however you like.  The example uses
SetWindowsHookEx with a CBT hook (the dll  exports a CBTProc) to inject it into all
running processes.

Press Esc to exit the script.

Note: if you do not compile the  script, AutoHotKey.exe gets hidden.  Otherwise the
the name of the .exe gets hidden.

Important: This does only work if you are using a x64 bit OS and the 64 bit version
of AutoHotkey or if you're using a x86 bit OS and the 32 bit version of AutoHotkey.
This does not work if you have a x64 bit OS but use 32 bit AHK (and vice versa) !!!
