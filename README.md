SmartSystemMenu
=============

SmartSystemMenu extends system menu of all windows in the system. It appends next custom items to menu:

* **Information.** Shows a dialog with information of the current window and process: the window handle, the window caption, the window style, the window class, the process name, the process id, the path to the process.
* **Always On Top.** Allows the current window to stay on top of all other windows.
* **Save Window Screenshot.** Allows to save the current window screenshot on a disk.
* **Resize.** Allows to change the size of the current window.
* **Alignment.** Allows the current window to be aligned with any of the 9 positions on the desktop.
* **Transparency.** Allows to change the transparency of the current window.
* **Priority.** Allows to change the current window's program priority.
* **System Tray.** Allows to minimize the current window to the system tray.

Screenshots
------------------

![alt tag](https://cloud.githubusercontent.com/assets/8102586/24604537/c89a60be-186d-11e7-9a2c-d9ee7663b5e6.png)
![alt tag](https://cloud.githubusercontent.com/assets/8102586/24604539/ccae8252-186d-11e7-9244-59f8c2fc5299.png)

Requirements
--------------------

* OS Windows XP SP3 and later. Supports x86 and x64 systems.
* .NET Framework 4.0

Files
--------------------

* SmartSystemMenu.exe
* SmartSystemMenu64.exe (located in resources of SmartSystemMenu.exe module)
* SmartSystemMenuHook.dll
* SmartSystemMenuHook64.dll

Files
--------------------

This program has SmartSystemMenu.exe and SmartSystemMenuHook.dll modules for x86 processes, SmartSystemMenu64.exe and SmartSystemMenuHook64.dll modules for x64 processes. When you run SmartSystemMenu.exe, it also runs SmartSystemMenu64.exe. These two executable modules load hooks (SmartSystemMenuHook.dll and SmartSystemMenuHook64.dll) to all processes. When you select an item in the system menu, the hook sends a message to the executable module. After that, the module performs the selected action: changes the transparency of the window, changes the size of the window, etc.

Limitations
--------------------

This tool can't work properly with a window whose system menu is managed by its own process, for example IE9 and later, Chrome 29 and later, etc. Also the tool doesn't work correctly with windows of delphi processes, because delphi window has a parent TApplication window.

Tips
--------------------

Run SmartSystemMenu.exe process. If your OS has enabled UAC, the system will display a UAC dialog. You do not need to worry because the program needs elevated privileges. After the program has been executed, in all system menus of all windows you can see custom items.