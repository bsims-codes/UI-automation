# UI-automation
Use this script with AutoHotKey to automate keystrokes for whatever purpose you see fit

# Warning 
This script sends repeated keystrokes to whatever window is active.
Do not run it against third-party apps, chat clients, or services you do not control. Running it against online services can lead to account suspension or other consequences. 

## Prerequisites

* Windows 10 or 11
* AutoHotkey **v1** installed (v1.1.x)
  [https://www.autohotkey.com/](https://www.autohotkey.com/)


## Save the script

1. Open **Notepad** or another plain-text editor.

2. Paste the **Required header** above, then your script:

   ```ahk
   ^d::

   Loop, 100
   {
       send, {Space}
       sleep, 100
       send, {BS}
       send, {Up}
       sleep, 200
       send, ^a
       sleep, 100
       send, {BS}
       sleep, 200
       send, {Enter}
       sleep, 100
       send, {Enter}
       sleep, 1000
   }
   Return

   Esc::ExitApp
   ```

3. Save the file as **`UI-automation.ahk`**

   * In Notepad: *File → Save As…* → **Save as type:** *All Files* → Name: `UI-automation.ahk`
   * Save it somewhere accessible like your Desktop

---

## Run the script

1. Double-click `UI-automation.ahk`.

   * You should see the green AutoHotkey “H” icon appear in the system tray.
2. Focus the window that should receive the keystrokes.
3. Press **Ctrl + D** to start the loop (triggered by `^d::`).

---

## Stop the script

* **ESCAPE key**
  
* **From system tray:** Right-click the AutoHotkey icon → **Exit**.
* **From Task Manager:**

  1. Press **Ctrl + Shift + Esc**
  2. Find **AutoHotkey** in the list
  3. Select → **End task**

> 💡 *Tip:* Add this line to the end of your file for a quick emergency stop:
>
> ```ahk
> Esc::ExitApp
> ```

---

## Modify the script

* Change how many times it runs → edit `Loop, 100` (e.g., `Loop, 10`).
* Change the hotkey → edit `^d::`

  * Example: `^+d::` = Ctrl + Shift + D, `!d::` = Alt + D

---

## Troubleshooting

* Script doesn’t run: Reinstall AutoHotkey v1 and ensure `.ahk` files open with AutoHotkey.
* Hotkey doesn’t trigger: Make sure the AutoHotkey tray icon is visible and the target window is active.
* Wrong window receives input: Stop the script immediately (tray → Exit or Task Manager).
