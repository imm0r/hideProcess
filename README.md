<div align="center">
  <img src="assets/hideprocess_logo.png" alt="HideProcess Logo" width="320">

[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Windows-blue.svg)]()
[![Architecture](https://img.shields.io/badge/Architecture-x86%20%7C%20x64-orange.svg)]()
[![Language](https://img.shields.io/badge/Language-AutoHotkey%20%7C%20C%2B%2B-yellow.svg)]()

</div>

---

## 📌 Overview

**HideProcess** is a proof‑of‑concept demonstrating how a process can be hidden from the **Windows Task Manager** on legacy Windows systems (Windows 2000 → Windows 7).

It uses a DLL injected into all running processes via a **CBT hook** (`SetWindowsHookEx`) to intercept specific API calls and prevent the target process from being listed.

> ⚠️ **Educational Use Only**  
> This project is intended for research, debugging, and reverse‑engineering education.  
> It must not be used for malicious purposes.

---

## ✨ Features

- Hide a process from the Windows Task Manager  
- Works on **x86 and x64**, depending on the AutoHotkey version used  
- Injection via:
  - `SetWindowsHookEx(WH_CBT, ...)`
  - Exported `CBTProc` inside the DLL  
- Auto‑injection into all running processes  
- Press **ESC** to stop the script and unload the hook  
- Works with:
  - **AutoHotkey.exe** (if script not compiled)  
  - **Your compiled EXE name** (if compiled)

---

## 🧩 How It Works

The AutoHotkey script loads a DLL that:

1. Installs a **CBT hook** using `SetWindowsHookEx`
2. Injects itself into all running processes
3. Hooks internal APIs responsible for enumerating processes
4. Filters out the target process name
5. Prevents the Task Manager from displaying it

## ⚠️ Disclaimer

> This project is intended for research, debugging, and reverse‑engineering education.  
> It must not be used for malicious purposes.

## 📜 License

This project is licensed under the MIT License.
