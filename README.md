# Windows-10-Context-Menu-Restorer

A lightweight registry script and guide for Windows 11 to instantly restore the classic Windows 10 right-click context menu, bypassing the condensed "Show more options" layout to speed up file management workflows.

---

## Features

* **Instant Classic Layout:** Modifies the Windows Registry to revert the context menu back to the efficient Windows 10 layout.
* **Fully Reversible:** Includes clean commands to restore the default Windows 11 context menu layout at any time.

---

## Usage & Commands

1. Open Command Prompt as Administrator (`Win + R`, type `cmd`, press `Ctrl + Shift + Enter`).
2. **To enable the classic Windows 10 context menu:**
   `reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve`
3. **To restore the default Windows 11 context menu:**
   `reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f`
4. **Restart Windows Explorer** for changes to take effect:
   `taskkill /f /im explorer.exe & start explorer.exe`
