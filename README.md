# Aminbiography Browser 2.0  

**No traditional installation required**

Simply download the ZIP file, extract it, and double-click `aminbiography Browser.exe` to launch the browser.

- No separate Python installation required.
- No setup wizard required.
- Portable Windows application.
- Designed for Windows 10/11 (64-bit).
- No additional installation dependencies required for end users.

**Security note:** Download Aminbiography Browser 2.0 only from the official [GitHub Releases page](https://github.com/aminbiography/aminbiography-browser/releases). Windows Defender SmartScreen may display an unfamiliar-app warning because this is a newly published application without an established reputation. Review the warning and verify the download before deciding whether to run it.

**Download:** [aminbiography Browser.exe](https://github.com/aminbiography/aminbiography-browser/releases/download/v2.0/aminbiography-browser.zip) 

**Platform:** Windows 10/11 (64-bit)

**Download Size:** Approximately 211 MB

### ⚠️ Windows SmartScreen Warning

When launching Aminbiography Browser 2.0 for the first time, Windows may display a **"Windows protected your PC"** message through Microsoft Defender SmartScreen.

This can happen because the application is newly published and does not yet have an established Windows reputation or a recognized code-signing certificate.

**If you downloaded the application from the official Aminbiography GitHub Releases page and have verified the download, you can proceed as follows:**

1. Click **More info** in the SmartScreen warning.
2. Review the application information and publisher details.
3. If you trust the downloaded application, select **Run anyway** to continue.

**Important security notice:**

- Only download the application from the official GitHub Releases page.
- Verify the downloaded file before running it.
- Do not bypass warnings if the file came from an unknown or untrusted source.
- SmartScreen warnings do not prove that an application is malicious, but they should not be ignored without checking the source.
  
---

## How to Download, Install, and Run

Follow these steps to install and launch Aminbiography Browser 2.0.

### Step 1 — Download

Click the direct download link:

[**Download aminbiography-browser.zip**](https://github.com/aminbiography/aminbiography-browser/releases/download/v2.0/aminbiography-browser.zip)

### Step 2 — Extract the ZIP File

1. Locate the downloaded `aminbiography-browser.zip` file.
2. Right-click the ZIP file.
3. Select **Extract All**.
4. Choose your preferred destination.

### Step 3 — Keep Application Files Together

After extraction, open the application folder.

Keep the following application components together:

- `aminbiography Browser.exe`
- `_internal` folder
- Other required supporting files.

**Important:** Do not delete, rename, or move the `_internal` folder or required supporting files.

### Step 4 — Launch the Browser

Double-click:

`aminbiography Browser.exe`

Aminbiography Browser 2.0 should launch.

### Installation Notes

- Extract the complete ZIP archive before running the application.
- Do not launch the executable directly from inside the ZIP archive.
- Keep the executable and its supporting files in the same application folder.
- No separate Python installation is required to run the packaged Windows application.

---

# Project Overview

## About Aminbiography Browser 2.0

**Aminbiography Browser 2.0** is a desktop web browser application developed using Python, PySide6, and Chromium-based Qt WebEngine.

Developed by [@aminbiography](https://github.com/aminbiography), this project combines desktop application development with AI-assisted programming.

The browser provides a graphical browsing environment for Windows desktop computers and laptops, supporting modern HTML, CSS, and JavaScript rendering through Qt WebEngine.

It includes essential browsing functionality such as multi-tab navigation, bookmarks, browsing history, download management, persistent browsing profiles, and Chromium Developer Tools.

**Platform:** Windows 10/11 (64-bit).

**Development technologies:**
- Python
- PySide6
- Qt WebEngine
- Chromium

*macOS, Android, and iOS versions are not currently available.*

---

# Software Architecture and Technical Overview

## 1. Application Architecture

Aminbiography Browser 2.0 follows a desktop application architecture built around Python and PySide6, with Qt WebEngine providing the underlying web rendering functionality.

The application connects its graphical user interface with browser navigation, browsing data management, and web content rendering.

### Architecture Components

**Presentation Layer — PySide6**

Responsible for the desktop graphical user interface.

Includes:
- Main browser window
- Tab interface
- Address and search bar
- Navigation controls
- Browser menus and dialogs
- Download and bookmark interfaces

**Application Layer — Python**

Responsible for application-level browser functionality.

Includes:
- Tab management
- Navigation handling
- Browser controls
- Bookmark management
- Browsing history
- Download management
- User interaction and keyboard shortcuts

**Browser Engine Layer — Qt WebEngine / Chromium**

Responsible for web content processing and rendering.

Includes:
- HTML rendering
- CSS processing
- JavaScript execution
- Web page navigation
- Chromium-based browser functionality
- Developer Tools integration

**Data and Storage Layer**

Responsible for persistent browser data through the configured browser profile.

Includes:
- Cookies
- Cache
- Browsing history
- Bookmarks
- Persistent browser profile data

### Conceptual Architecture Diagram

```text
             USER
               |
               v
    +------------------------+
    |    PySide6 Interface   |
    |                        |
    | Tabs | Address Bar     |
    | Menus | Navigation     |
    +------------------------+
               |
               v
    +------------------------+
    |   Python Application   |
    |                        |
    | Tab Management         |
    | Bookmarks              |
    | Browsing History       |
    | Download Management    |
    +------------------------+
               |
               v
    +------------------------+
    | Qt WebEngine / Chromium |
    |                        |
    | HTML | CSS | JavaScript|
    | Web Rendering          |
    | Developer Tools        |
    +------------------------+
               |
               v
    +------------------------+
    |   Browser Profile      |
    |                        |
    | Cookies                |
    | Cache                  |
    | Persistent Data        |
    +------------------------+
```

This is a conceptual representation of the described application architecture, not a verified implementation-level dependency diagram.

## 2. Browser Rendering Architecture

Aminbiography Browser uses Qt WebEngine, which is based on the Chromium browser engine.

The application does not implement its own browser rendering engine.

Qt WebEngine provides the underlying functionality for:

- Processing HTML documents.
- Rendering CSS layouts.
- Executing JavaScript.
- Displaying modern web content.
- Managing browser navigation.
- Integrating Chromium Developer Tools.

This architecture allows the application to provide browser functionality without independently implementing a complete web rendering engine.

## 3. Browser Profile and Data Management

The browser uses a persistent Chromium-based browser profile for supported browsing data.

Depending on the configured profile and storage settings, this includes:

- Cookies
- Cache
- Browsing history
- Bookmarks
- Persistent browsing information

The application also provides controls for clearing selected browsing data.

---

# Security Architecture

## 1. Browser Engine Security

Aminbiography Browser uses Qt WebEngine, based on Chromium, for web content rendering and browser functionality.

The application relies on security mechanisms provided by the underlying Qt WebEngine framework and its Chromium components.

Security capabilities depend on the Qt WebEngine version, configuration, and application implementation.

## 2. Browsing Data and Storage

The browser maintains a persistent browsing profile.

Supported data management functionality includes:

- Persistent browser profile storage.
- Cookie and cache storage through the browser profile.
- Local browsing history.
- Local bookmarks.
- Available controls for clearing cache, cookies, and saved history.

## 3. Download Management

The application includes a download manager with progress and completion states.

Users should:
- Download files from trusted websites.
- Verify downloaded files before opening them.
- Scan downloaded files with appropriate security software.

## 4. Developer Tools

Chromium Developer Tools are available for inspecting web pages, debugging JavaScript, and analyzing browser behavior.

Developer Tools are intended for development and troubleshooting.

## 5. Security Considerations

Aminbiography Browser 2.0 is a learning and development browser project, not a hardened production browser.

The current project does not implement the following features:

- Google Safe Browsing integration.
- Automatic browser security updates.
- Built-in password management.
- Browser synchronization.
- Browser extension support.
- Private/incognito browsing.
- A complete website permission management interface.

Using Chromium-based Qt WebEngine does not automatically mean that every security feature available in Google Chrome is implemented by this application.

## 6. User Security Recommendations

- Keep Windows and the browser's bundled components updated.
- Download the application from the official GitHub Releases page.
- Avoid downloading files from untrusted websites.
- Scan downloaded files before opening them.
- Avoid entering sensitive information until the application has undergone additional security review and testing.

---

# Included Features

## Browsing and Navigation

- Chromium-based HTML, CSS, and JavaScript rendering.
- Multiple tabs and tab context menu.
- Address bar with Google search fallback.
- Back, forward, reload, and home navigation.

## Browser Data Management

- Persistent Chromium profile, cookies, and cache.
- Local bookmarks with a manager dialog.
- Browsing history with clear-history option.
- Clear cache, cookies, and saved browsing history.

## Productivity and Developer Tools

- Download manager with progress and completion states.
- Chromium Developer Tools.
- Find text on page.
- Zoom controls.
- Keyboard shortcuts.

---

# Developer Documentation

Want to explore the source code, modify the application, or build your own version?

**GitHub Repository:**

https://github.com/aminbiography/aminbiography-browser

## 1. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Application programming |
| PySide6 | Desktop graphical interface |
| Qt WebEngine | Web content rendering |
| Chromium | Underlying browser engine |
| PyInstaller | Windows executable packaging |
| GitHub Actions | Automated Windows builds |

## 2. Project Structure

| File or Folder | Description |
|---|---|
| `main.py` | Main browser application source code |
| `requirements.txt` | Python dependencies |
| `run_windows.bat` | Quick Windows launcher |
| `BUILD_WINDOWS_64BIT.bat` | Windows executable build script |
| `aminbiography Browser.spec` | PyInstaller configuration |
| `aminbiography_browser_purple.ico` | Application icon |
| `.github/workflows/` | GitHub Actions automation |
| `.gitignore` | Git ignore configuration |
| `README.md` | Project documentation |

## 3. 64-bit Windows Development Setup

Use **64-bit Python** on 64-bit Windows.

Check Python architecture:

```powershell
py -c "import struct; print(struct.calcsize('P') * 8, 'bit')"
```

Expected output:

```text
64 bit
```

## 4. Install and Run from Source

Clone the repository:

```powershell
git clone https://github.com/aminbiography/aminbiography-browser.git
cd aminbiography-browser
```

Create a virtual environment:

```powershell
py -m venv .venv
```

Activate it:

```powershell
.\.venv\Scripts\Activate.ps1
```

Upgrade pip and install dependencies:

```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Run the application:

```powershell
python main.py
```

### Alternative Without Virtual Environment Activation

If PowerShell blocks virtual-environment activation, use:

```powershell
py -m pip install -r requirements.txt
py main.py
```

## 5. Build a 64-bit Windows Executable

Install PyInstaller:

```powershell
py -m pip install pyinstaller
```

Build the application:

```powershell
py -m PyInstaller --noconfirm --windowed --name "aminbiography Browser" --icon="aminbiography_browser_purple.ico" --collect-all PySide6 main.py
```

PyInstaller generates the packaged application under the `dist` directory.

The output is a one-folder application.

**Important:** Keep `aminbiography Browser.exe` and its companion `_internal` folder together.

Test the generated application on a separate Windows computer before distributing it.

## 6. Automatic Windows Build with GitHub Actions

This project includes a GitHub Actions workflow at:

`.github/workflows/build-windows-exe.yml`

The workflow can automatically build a Windows x64 executable.

1. Open the repository's **Actions** tab.
2. Select **Build aminbiography Windows EXE**.
3. Run the workflow or push changes to the `main` branch.
4. Wait for the workflow to complete successfully.
5. Download the generated `aminbiography-windows-x64` artifact.
6. Extract the artifact and run `aminbiography Browser.exe`.

The output is a portable PyInstaller one-folder application.

Keep the executable and its companion `_internal` folder together.

---

# Useful Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| Ctrl + L | Focus address bar |
| Ctrl + T | New tab |
| Ctrl + W | Close tab |
| Ctrl + H | Browsing history |
| Ctrl + J | Downloads |
| Ctrl + D | Bookmark page |
| Ctrl + Shift + I | Developer Tools |
| Ctrl + Shift + Delete | Clear browsing data |
| Ctrl + F | Find on page |
| Ctrl + Plus | Zoom in |
| Ctrl + Minus | Zoom out |
| Ctrl + 0 | Reset zoom |

---

# ⚠️ Limitations and Project Status

Aminbiography Browser 2.0 is a functional learning and development browser.

It embeds Qt WebEngine/Chromium and does not implement a browser engine from scratch.

The current application does not include:
- Google Safe Browsing integration.
- Automatic browser security updates.
- Password management.
- Browser synchronization.
- Browser extension support.
- Private/incognito mode.
- A complete website permission management interface.

The application has not been presented as a hardened production browser or as having undergone an independent security audit.

**Platform availability:**

- Windows 10/11 (64-bit): Supported.
- macOS: Not currently available.
- Android: Not currently available.
- iOS: Not currently available.

---

# Legal Information, Copyright, Privacy, and Third-Party Notices

## 1. Independent Project and Non-Affiliation

Aminbiography Browser 2.0 is an independently developed desktop web browser created by aminbiography.

This project is not affiliated with, associated with, authorized by, sponsored by, or endorsed by Google LLC, Microsoft Corporation, The Qt Company, or the Chromium project.

Aminbiography Browser is an independent application and does not claim to be Google Chrome or any other officially branded third-party browser.

All third-party trademarks, service marks, product names, and logos belong to their respective owners.

## 2. Google Search and External Website Navigation

Aminbiography Browser provides users with the ability to access Google Search and other external websites through its Chromium-based Qt WebEngine rendering engine.

Google Search is accessed as an external website through normal browser navigation.

Google's website interface, content, branding, footer links, Privacy Policy, Terms of Service, and Settings options are provided and maintained by Google LLC.

Aminbiography Browser does not claim ownership of Google's website, search services, content, or intellectual property.

The appearance of Google Search within Aminbiography Browser does not imply any partnership, authorization, sponsorship, or endorsement by Google.

## 3. Google Privacy Policy and Terms of Service

When users access Google services through Aminbiography Browser, they may interact with Google's official privacy and service policies.

Google's official policy links:

- **Google Privacy Policy:** https://policies.google.com/privacy?hl=en-BD&fg=1
- **Google Terms of Service:** https://policies.google.com/terms?hl=en-BD&fg=1

These policies are published and maintained by Google LLC and govern the applicable Google services.

They are not the privacy policy or software license of Aminbiography Browser.

Users should review the relevant policies of external websites and services they access through the browser.

## 4. Third-Party Software and Open-Source Licenses

Aminbiography Browser incorporates third-party software components and technologies, including:

- Python
- PySide6
- Qt Framework
- Qt WebEngine
- Chromium
- PyInstaller
- Other bundled libraries, dependencies, and supporting components.

These components remain the property of their respective copyright holders and are governed by their applicable licenses.

Their copyright notices, license conditions, redistribution requirements, and other applicable obligations remain in effect independently of the licensing terms of Aminbiography Browser.

The developer does not claim ownership of third-party software.

Applicable third-party license texts, copyright notices, and required source-code information should accompany the distributed application in accordance with the relevant licenses.

## 5. Original Project Copyright and Software Ownership

Copyright © 2026 aminbiography. All rights reserved for original project materials, subject to applicable third-party software licenses.

The original Aminbiography Browser application, its independently developed source code, interface design, project documentation, and original assets are subject to their applicable ownership and licensing terms.

The project's copyright statement does not override, restrict, or replace rights granted under applicable third-party open-source licenses.

Permissions concerning modification, redistribution, and commercial use of the original application are governed by the project's applicable software license.

## 6. Privacy and Browsing Data

Aminbiography Browser uses a persistent browser profile to support browsing functionality.

Depending on the application's configuration and implementation, browsing data may include:

- Cookies
- Browser cache
- Browsing history
- Bookmarks
- Other persistent browsing information.

Websites accessed through the browser may independently collect, process, and store information according to their own privacy policies and applicable terms.

Users should review external website privacy policies before submitting personal or sensitive information.

For information about data collected, stored, or transmitted by Aminbiography Browser itself, users should consult the project's separate Privacy Policy.

## 7. Security and Responsible Use

Aminbiography Browser is an independently developed learning and development browser project.

It uses Qt WebEngine and its underlying Chromium components for web content rendering and browser functionality.

The application is not represented as an officially certified, independently audited, or hardened production browser.

Security capabilities depend on the versions, configurations, and implementation of its underlying components.

Users are responsible for exercising appropriate caution when browsing websites, downloading files, and accessing sensitive online accounts.

## 8. Warranty and Liability Disclaimer

Aminbiography Browser is provided subject to its applicable software license and mandatory rights under applicable law.

To the extent permitted by applicable law, the developer makes no additional warranty regarding uninterrupted availability, compatibility, fitness for a particular purpose, or error-free operation.

Nothing in this notice excludes or limits any liability, warranty, or consumer right that cannot legally be excluded or limited.

## 9. External Services and Intellectual Property

External websites and services accessible through Aminbiography Browser are independently operated by their respective providers.

Their content, policies, trademarks, logos, and intellectual property remain the property of their respective owners.

Aminbiography Browser does not claim ownership of external website content or imply that third-party providers endorse this project.

Users are responsible for complying with applicable terms and policies when accessing external services.

## 10. Contact and Legal Inquiries

For questions concerning Aminbiography Browser, its original source code, project documentation, copyright, or licensing, please contact the developer through the official GitHub repository.

**Official GitHub Repository:**
https://github.com/aminbiography/aminbiography-browser

**GitHub Issues:**
https://github.com/aminbiography/aminbiography-browser/issues

---

**Project:** Aminbiography Browser 2.0

**Developer:** aminbiography

**Copyright:** © 2026 aminbiography. All rights reserved, subject to applicable third-party licenses.

---

# Feedback, Issues, and Contributions

Feedback, suggestions, and contributions are welcome.


- **Download Latest Release:** [v2.0](https://github.com/aminbiography/aminbiography-browser/releases/tag/v2.0)
- **Source Code:** [GitHub Repository](https://github.com/aminbiography/aminbiography-browser)
- **Report Issues:** [GitHub Issues](https://github.com/aminbiography/aminbiography-browser/issues)

If you find this project useful, consider giving the repository a ⭐ Star.

**Thank you for exploring Aminbiography Browser 2.0!**

---

© 2026 aminbiography. All rights reserved.

























# Aminbiography Browser 2.0

**A portable Windows desktop browser — no traditional installation required.**

Aminbiography Browser 2.0 is an independently developed desktop web browser built with Python, PySide6, and Chromium-based Qt WebEngine, with AI assistance throughout the development process.

Download the ZIP archive, extract it, and launch the browser directly from its folder. No separate Python installation or setup wizard is required.

**Platform:** Windows 10/11 (64-bit)

**Developer:** [@aminbiography](https://github.com/aminbiography)

---

## Download Aminbiography Browser 2.0

<details>
<summary><strong>Download and run instructions</strong></summary>

### Download

[**Download Aminbiography Browser 2.0 — Windows x64 (ZIP)**](https://github.com/aminbiography/aminbiography-browser/releases/download/v2.0/aminbiography-browser.zip)

You can also visit the [GitHub Releases page](https://github.com/aminbiography/aminbiography-browser/releases) to explore available releases.

### How to Run

1. Download `aminbiography-browser.zip`.
2. Locate the downloaded ZIP archive.
3. Right-click the file and select **Extract All**.
4. Choose your preferred destination.
5. Open the extracted application folder.
6. Double-click `aminbiography Browser.exe` to launch the browser.

### Important

- Extract the complete ZIP archive before launching the application.
- Do not run the executable directly from inside the ZIP file.
- Keep `aminbiography Browser.exe`, the `_internal` folder, and all supporting files together.
- Do not delete, rename, or move required application files.
- No separate Python installation is required.
- No traditional software installation process is required.

**Application type:** Portable, one-folder Windows application.

</details>

---

## Features

- **Portable application — no installation required:** Extract the ZIP archive, open the application folder, and double-click `aminbiography Browser.exe`.
- **Custom application icon and branding:** A custom visual identity for the browser.
- **Multi-tab browsing:** Open and manage multiple websites in separate tabs.
- **Bookmarks:** Save and manage favorite websites.
- **Browsing history:** Access previously visited pages.
- **Download manager:** Monitor download progress and completion.
- **Developer Tools:** Inspect and debug web pages using Chromium Developer Tools.
- **Page zoom:** Adjust website magnification.
- **Find in Page:** Search for text within the current webpage.
- **Persistent browsing profiles:** Retain supported browsing data between sessions.
- **Google Search:** Search the web through the address bar and homepage.
- **Homepage quick links:** Access useful Google services and websites.

---

# Project Overview

## About the Project

Aminbiography Browser 2.0 is an independent desktop browser application designed for Windows computers and laptops.

The application uses Qt WebEngine, which is based on Chromium, to provide modern web content rendering and JavaScript execution.

It combines a Python-based desktop interface with browser navigation, tab management, bookmarks, browsing history, download management, and persistent browsing profiles.

### Development Technologies

| Technology | Purpose |
|---|---|
| Python | Application programming |
| PySide6 | Desktop graphical user interface |
| Qt WebEngine | Web content rendering |
| Chromium | Underlying browser engine |
| PyInstaller | Windows application packaging |
| GitHub Actions | Automated build workflow |

### Platform Availability

- Windows 10/11 (64-bit): Supported.
- macOS: Not currently available.
- Android: Not currently available.
- iOS: Not currently available.

Mobile and macOS versions are not currently provided.

---

# Software Architecture and Technical Overview

## 1. Application Architecture

Aminbiography Browser 2.0 uses a desktop application architecture built around Python, PySide6, and Qt WebEngine.

The application connects its graphical interface with browser navigation, user interactions, web content rendering, and browsing data management.

### Presentation Layer — PySide6

Responsible for the desktop graphical user interface.

Includes:

- Main browser window
- Tab interface
- Address and search bar
- Navigation controls
- Browser menus and dialogs
- Download and bookmark interfaces

### Application Layer — Python

Responsible for application-level functionality.

Includes:

- Tab management
- Navigation handling
- Browser controls
- Bookmark management
- Browsing history
- Download management
- User interactions and keyboard shortcuts

### Browser Engine Layer — Qt WebEngine / Chromium

Responsible for web content processing and rendering.

Includes:

- HTML rendering
- CSS processing
- JavaScript execution
- Webpage navigation
- Chromium-based browser functionality
- Developer Tools integration

### Data and Storage Layer

Responsible for persistent browser data through the configured browser profile.

Depending on the implementation and settings, this may include:

- Cookies
- Cache
- Browsing history
- Bookmarks
- Other persistent browsing information

## 2. Conceptual Architecture Diagram

```text
                  USER
                    |
                    v
        +--------------------------+
        |     PySide6 Interface    |
        |                          |
        | Tabs | Address Bar       |
        | Menus | Navigation       |
        +--------------------------+
                    |
                    v
        +--------------------------+
        |    Python Application    |
        |                          |
        | Tab Management           |
        | Bookmarks                |
        | Browsing History         |
        | Download Management      |
        +--------------------------+
                    |
                    v
        +--------------------------+
        |   Qt WebEngine/Chromium  |
        |                          |
        | HTML | CSS | JavaScript  |
        | Web Rendering            |
        | Developer Tools          |
        +--------------------------+
                    |
                    v
        +--------------------------+
        |     Browser Profile      |
        |                          |
        | Cookies                  |
        | Cache                    |
        | Persistent Data          |
        +--------------------------+
````

This is a conceptual representation of the application architecture, not a verified implementation-level dependency diagram.

## **3. Browser Rendering Architecture**

Aminbiography Browser uses Qt WebEngine, which is based on the Chromium browser engine.

The application does not implement its own web rendering engine.

Qt WebEngine provides the underlying functionality for:

- Processing HTML documents.
- Rendering CSS layouts.
- Executing JavaScript.
- Displaying modern web content.
- Managing browser navigation.
- Integrating Chromium Developer Tools.

This architecture allows the application to provide browser functionality without independently implementing a complete web rendering engine.

## **4. Browser Profile and Data Management**

The browser uses a persistent Chromium-based browser profile to support browsing data between sessions.

Depending on the configured profile and storage settings, this includes:

- Cookies
- Cache
- Browsing history
- Bookmarks
- Other persistent browsing information

The application also provides controls for clearing selected browsing data.

# **Security Architecture and Considerations**

## **1. Browser Engine Security**

Aminbiography Browser uses Qt WebEngine, based on Chromium, for web content rendering and browser functionality.

The application relies on security mechanisms provided by its underlying Qt WebEngine framework and Chromium components.

Security capabilities depend on the component versions, configuration, and application implementation.

## **2. Browsing Data and Storage**

The browser maintains a persistent browsing profile.

Supported data management functionality includes:

- Persistent browser profile storage.
- Cookie and cache storage through the browser profile.
- Local browsing history.
- Local bookmarks.
- Available controls for clearing selected browsing data.

## **3. Download Management**

The application includes a download manager with progress and completion states.

Users should:

- Download files from trusted websites.
- Verify downloaded files before opening them.
- Scan downloaded files with appropriate security software.

## **4. Developer Tools**

Chromium Developer Tools are available for inspecting webpages, debugging JavaScript, and analyzing browser behavior.

Developer Tools are intended for development and troubleshooting.

## **5. Security Limitations**

Aminbiography Browser 2.0 is an independently developed learning and development browser project. It is not represented as a hardened production browser.

The current project does not implement the following features:

- Google Safe Browsing integration.
- Automatic browser security updates.
- Built-in password management.
- Browser synchronization.
- Browser extension support.
- Private/incognito browsing.
- A complete website permission management interface.

Using Chromium-based Qt WebEngine does not automatically mean that every security feature available in Google Chrome is implemented by this application.

## **6. User Security Recommendations**

- Keep Windows and the browser's bundled components updated.
- Download the application from the official GitHub Releases page.
- Avoid downloading files from untrusted websites.
- Scan downloaded files before opening them.
- Exercise caution when accessing sensitive online accounts.

# **Included Browser Features**

## **Browsing and Navigation**

- Chromium-based HTML, CSS, and JavaScript rendering.
- Multiple tabs and tab context menu.
- Address bar with Google Search fallback.
- Back, forward, reload, and home navigation.

## **Browser Data Management**

- Persistent Chromium profile.
- Cookies and cache storage.
- Local bookmarks with a manager dialog.
- Browsing history with clear-history functionality.
- Available controls for clearing cache, cookies, and saved browsing history.

## **Productivity and Developer Tools**

- Download manager with progress and completion states.
- Chromium Developer Tools.
- Find text on the current webpage.
- Page zoom controls.
- Keyboard shortcuts.

# **Developer Documentation**

Want to explore the source code, modify the application, or build your own version?

**GitHub Repository:**

[https://github.com/aminbiography/aminbiography-browser](https://github.com/aminbiography/aminbiography-browser?utm_source=chatgpt.com)

## **1. Project Structure**

The repository includes the application source code, dependencies, Windows build configuration, and project documentation.

| File or Folder                     | Description                          |
| ---------------------------------- | ------------------------------------ |
| `main.py`                          | Main browser application source code |
| `requirements.txt`                 | Python dependencies                  |
| `run_windows.bat`                  | Windows launcher                     |
| `BUILD_WINDOWS_64BIT.bat`          | Windows executable build script      |
| `aminbiography Browser.spec`       | PyInstaller configuration            |
| `aminbiography_browser_purple.ico` | Application icon                     |
| `.github/workflows/`               | GitHub Actions automation            |
| `.gitignore`                       | Git ignore configuration             |
| `README.md`                        | Project documentation                |

## **2. Development Requirements**

- Windows 10/11 (64-bit).
- 64-bit Python.
- pip.
- Git.
- Required Python dependencies listed in `requirements.txt`.

Check your Python architecture:

```
py -c "import struct; print(struct.calcsize('P') * 8, 'bit')"
```

Expected output:

```
64 bit
```

## **3. Clone the Repository**

```
git clone https://github.com/aminbiography/aminbiography-browser.git
cd aminbiography-browser
```

## **4. Create a Virtual Environment**

```
py -m venv .venv
```

Activate it:

```
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, configure your environment appropriately or use the Python executable inside the virtual environment directly.

## **5. Install Dependencies**

Upgrade pip:

```
python -m pip install --upgrade pip
```

Install the project dependencies:

```
python -m pip install -r requirements.txt
```

## **6. Run from Source**

```
python main.py
```

The browser application should launch using your installed Python environment and dependencies.

## **7. Build the Windows Executable**

Install PyInstaller:

```
python -m pip install pyinstaller
```

Build the application:

```
python -m PyInstaller --noconfirm --clean --windowed --name "aminbiography Browser" --icon="aminbiography_browser_purple.ico" --collect-all PySide6 main.py
```

PyInstaller generates the packaged application under the `dist` directory.

The output is a one-folder Windows application.

### **Important Packaging Notes**

- Keep `aminbiography Browser.exe` and its companion `_internal` folder together.
- Do not distribute only the executable.
- Distribute the complete packaged application.
- Test the generated application on a separate Windows computer before publishing it.

## **8. Automated Windows Build with GitHub Actions**

The project includes a GitHub Actions workflow at:

```
.github/workflows/build-windows-exe.yml
```

The workflow can automatically build a Windows x64 executable.

To use it:

1. Open the repository's **Actions** tab.
2. Select **Build aminbiography Windows EXE**.
3. Run the workflow or push changes to the configured branch.
4. Wait for the workflow to complete successfully.
5. Download the generated `aminbiography-windows-x64` artifact.
6. Extract the artifact and launch `aminbiography Browser.exe`.

The output is a portable PyInstaller one-folder application.

Keep the executable and its companion `_internal` folder together.

# **Keyboard Shortcuts**

| Shortcut              | Action              |
| --------------------- | ------------------- |
| Ctrl + L              | Focus address bar   |
| Ctrl + T              | New tab             |
| Ctrl + W              | Close tab           |
| Ctrl + H              | Browsing history    |
| Ctrl + J              | Downloads           |
| Ctrl + D              | Bookmark page       |
| Ctrl + Shift + I      | Developer Tools     |
| Ctrl + Shift + Delete | Clear browsing data |
| Ctrl + F              | Find on page        |
| Ctrl + Plus           | Zoom in             |
| Ctrl + Minus          | Zoom out            |
| Ctrl + 0              | Reset zoom          |

# **Limitations and Project Status**

Aminbiography Browser 2.0 is a functional learning and development browser.

It embeds Qt WebEngine/Chromium and does not implement a browser engine from scratch.

The current application does not include:

- Google Safe Browsing integration.
- Automatic browser security updates.
- Built-in password management.
- Browser synchronization.
- Browser extension support.
- Private/incognito browsing.
- A complete website permission management interface.

The application is not presented as a hardened production browser or as having undergone an independent security audit.

### **Platform Availability**

| Platform               | Availability            |
| ---------------------- | ----------------------- |
| Windows 10/11 (64-bit) | Supported               |
| macOS                  | Not currently available |
| Android                | Not currently available |
| iOS                    | Not currently available |

# **Legal Information, Copyright, Privacy, and Third-Party Notices**

## **1. Independent Project and Non-Affiliation**

Aminbiography Browser 2.0 is an independently developed desktop web browser created by aminbiography.

This project is not affiliated with, associated with, authorized by, sponsored by, or endorsed by Google LLC, Microsoft Corporation, The Qt Company, or the Chromium project.

Aminbiography Browser is an independent application and does not claim to be Google Chrome or any other officially branded third-party browser.

All third-party trademarks, service marks, product names, and logos belong to their respective owners.

## **2. Google Search and External Website Navigation**

Aminbiography Browser allows users to access Google Search and other external websites through its Chromium-based Qt WebEngine rendering engine.

Google Search is accessed as an external website through normal browser navigation.

Google's website interface, content, branding, Privacy Policy, Terms of Service, and Settings options are provided and maintained by Google LLC.

Aminbiography Browser does not claim ownership of Google's website, search services, content, or intellectual property.

The appearance of Google Search within Aminbiography Browser does not imply any partnership, authorization, sponsorship, or endorsement by Google.

## **3. Third-Party Privacy Policies and Terms**

External websites and services accessed through Aminbiography Browser may have their own privacy policies and terms of service.

For Google services:

- [Google Privacy Policy](https://policies.google.com/privacy?utm_source=chatgpt.com)
- [Google Terms of Service](https://policies.google.com/terms?utm_source=chatgpt.com)

These policies are published and maintained by Google LLC. They are not the privacy policy or software license of Aminbiography Browser.

Users should review the applicable policies of external websites and services they access.

## **4. Third-Party Software and Open-Source Licenses**

Aminbiography Browser incorporates third-party software components and technologies, including:

- Python
- PySide6
- Qt Framework
- Qt WebEngine
- Chromium
- PyInstaller
- Other bundled libraries, dependencies, and supporting components.

These components remain the property of their respective copyright holders and are governed by their applicable licenses.

Their copyright notices, license conditions, redistribution requirements, and other applicable obligations remain in effect independently of the licensing terms of Aminbiography Browser.

The developer does not claim ownership of third-party software.

Applicable third-party license texts, copyright notices, and required source-code information should accompany the distributed application in accordance with the relevant licenses.

## **5. Original Project Copyright and Software Ownership**

Copyright © 2026 aminbiography. All rights reserved for original project materials, subject to applicable third-party software licenses.

The original Aminbiography Browser application, its independently developed source code, interface design, project documentation, and original assets are subject to their applicable ownership and licensing terms.

The project's copyright statement does not override, restrict, or replace rights granted under applicable third-party open-source licenses.

Permissions concerning modification, redistribution, and commercial use of the original application are governed by the project's applicable software license.

## **6. Privacy and Browsing Data**

Aminbiography Browser uses a persistent browser profile to support browsing functionality.

Depending on the application's configuration and implementation, browsing data may include:

- Cookies
- Browser cache
- Browsing history
- Bookmarks
- Other persistent browsing information.

Websites accessed through the browser may independently collect, process, and store information according to their own privacy policies and applicable terms.

Users should review external website privacy policies before submitting personal or sensitive information.

For information about data collected, stored, or transmitted by Aminbiography Browser itself, consult the project's separate Privacy Policy, if provided.

## **7. Security and Responsible Use**

Aminbiography Browser is an independently developed learning and development browser project.

It uses Qt WebEngine and its underlying Chromium components for web content rendering and browser functionality.

The application is not represented as an officially certified, independently audited, or hardened production browser.

Security capabilities depend on the versions, configurations, and implementation of its underlying components.

Users are responsible for exercising appropriate caution when browsing websites, downloading files, and accessing sensitive online accounts.

## **8. Warranty and Liability Disclaimer**

Aminbiography Browser is provided subject to its applicable software license and mandatory rights under applicable law.

To the extent permitted by applicable law, the developer makes no additional warranty regarding uninterrupted availability, compatibility, fitness for a particular purpose, or error-free operation.

Nothing in this notice excludes or limits any liability, warranty, or consumer right that cannot legally be excluded or limited.

## **9. External Services and Intellectual Property**

External websites and services accessible through Aminbiography Browser are independently operated by their respective providers.

Their content, policies, trademarks, logos, and intellectual property remain the property of their respective owners.

Aminbiography Browser does not claim ownership of external website content or imply that third-party providers endorse this project.

Users are responsible for complying with applicable terms and policies when accessing external services.

## **10. Contact and Legal Inquiries**

For questions concerning Aminbiography Browser, its original source code, project documentation, copyright, or licensing, please contact the developer through the official GitHub repository.

- **Official Repository:** [GitHub Repository](https://github.com/aminbiography/aminbiography-browser?utm_source=chatgpt.com)
- **Issues and Feedback:** [GitHub Issues](https://github.com/aminbiography/aminbiography-browser/issues?utm_source=chatgpt.com)

# **Feedback, Issues, and Contributions**

Feedback, suggestions, and contributions are welcome.

If you encounter a bug, experience an issue, or have suggestions for improving Aminbiography Browser, please submit an issue through the GitHub repository.

### **Project Links**

- **Download:** [Download Aminbiography Browser 2.0 — Windows x64](https://github.com/aminbiography/aminbiography-browser/releases/download/v2.0/aminbiography-browser.zip?utm_source=chatgpt.com)
- **Latest Release:** [GitHub Releases — v2.0](https://github.com/aminbiography/aminbiography-browser/releases/tag/v2.0?utm_source=chatgpt.com)
- **Source Code:** [GitHub Repository](https://github.com/aminbiography/aminbiography-browser?utm_source=chatgpt.com)
- **Report Issues:** [GitHub Issues](https://github.com/aminbiography/aminbiography-browser/issues?utm_source=chatgpt.com)

If you find this project useful, consider giving the repository a ⭐ Star.

**Thank you for exploring Aminbiography Browser 2.0!**

**Project:** Aminbiography Browser 2.0\
**Developer:** aminbiography\
**Platform:** Windows 10/11 (64-bit)\
**Copyright:** © 2026 aminbiography. All rights reserved, subject to applicable third-party licenses.

\#AminbiographyBrowser #Python #PySide6 #Chromium #OpenSource #DesktopBrowser #Windows #GitHub

```

**Before publishing, verify these five details against your actual repository and release:**

1. The executable is actually named `aminbiography Browser.exe`.
2. The ZIP contains the executable and `_internal` folder.
3. The workflow filename and workflow name match the README.
4. The keyboard shortcuts listed are implemented.
5. Your repository's `LICENSE` and any separate Privacy Policy match the statements in this README.

One legal point: the copyright notice does not itself establish an open-source license. Choose and publish a license that reflects how you want others to use and redistribute your code.
```
