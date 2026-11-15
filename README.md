# aminbiography Browser 2.0

A developer-focused desktop browser starter project for Windows, built with Python, PySide6, and Qt WebEngine (Chromium).

## Included features

- Chromium-based HTML, CSS, and JavaScript rendering
- Multiple tabs and tab context menu
- Address bar with Google search fallback
- Back, forward, reload, and home navigation
- Persistent Chromium profile, cookies, and cache
- Local bookmarks with a manager dialog
- Browsing history with clear-history option
- Download manager with progress and completion states
- Developer Tools (Chromium DevTools)
- Find text on page
- Zoom controls
- Clear cache, cookies, and saved history
- Keyboard shortcuts

## 64-bit Windows setup

Use **64-bit Python** on 64-bit Windows. PySide6 wheels are selected to match the Python interpreter architecture. This project is source code; it is not a precompiled executable.

Check Python architecture:

```powershell
py -c "import struct; print(struct.calcsize('P') * 8, 'bit')"
```

Expected output: `64 bit`.

Install and run:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python main.py
```

If PowerShell blocks virtual-environment activation, run:

```powershell
py -m pip install -r requirements.txt
py main.py
```

## Build a 64-bit Windows executable

Run these commands from 64-bit Python:

```powershell
py -m pip install pyinstaller
py -m PyInstaller --noconfirm --windowed --name "aminbiography Browser" --collect-all PySide6 main.py
```

PyInstaller writes the packaged application under `dist`. Test it on the target Windows machine before distributing it. A one-folder build is generally easier to troubleshoot for Qt WebEngine than a one-file build.

## Useful shortcuts

| Shortcut | Action |
|---|---|
| Ctrl+L | Focus address bar |
| Ctrl+T | New tab |
| Ctrl+W | Close tab |
| Ctrl+H | Browsing history |
| Ctrl+J | Downloads |
| Ctrl+D | Bookmark page |
| Ctrl+Shift+I | Developer tools |
| Ctrl+Shift+Delete | Clear browsing data |
| Ctrl+F | Find on page |
| Ctrl+Plus / Ctrl+Minus | Zoom |
| Ctrl+0 | Reset zoom |

## Project files

- `main.py` — complete browser application source; major sections are commented.
- `requirements.txt` — Python dependencies.
- `run_windows.bat` — quick Windows launcher.
- `BUILD_WINDOWS_64BIT.bat` — build a 64-bit executable with PyInstaller.
- `README.md` — setup and usage instructions.

## Important limitations and security notes

This project embeds Qt WebEngine/Chromium. It does not implement a browser engine from scratch. It is a functional learning/development browser, not a hardened production browser. It does not currently include Safe Browsing, automatic security updates, password management, sync, extension support, private/incognito mode, or a full permission UI. Avoid relying on it for sensitive browsing until it has undergone security review and additional testing.


## Build the branded Windows executable automatically

This project includes a GitHub Actions workflow at
`.github/workflows/build-windows-exe.yml`.

1. Create a GitHub repository and upload all files in this project.
2. Open the repository's **Actions** tab.
3. Run **Build aminbiography Windows EXE** (or push to the `main` branch).
4. Download the workflow artifact named `aminbiography-windows-x64`.
5. Extract it and run `aminbiography.exe`.

The workflow builds on Windows x64. The output is a portable PyInstaller
one-folder application: keep the `aminbiography.exe` and its companion
`_internal` folder together. Qt WebEngine needs its bundled runtime files.

The app window and executable are branded `aminbiography`. The Windows taskbar
and executable use the generated branded icon where supported.
