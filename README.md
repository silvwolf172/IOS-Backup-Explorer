💎 IOS Backup Explorer (IBE) 
IOS Backup Explorer is a cutting-edge Windows desktop application designed to navigate, explore, and edit iOS/iPadOS backups (iOS 10+). Built with a focus on speed, security, and a premium user experience.

🚀 Tech Stack
Framework: Electron + React

Build System: Vite

Database: better-sqlite3 (native bindings for Manifest.db parsing)

Plist Engines: plist (XML) & bplist-parser (Binary)

UI & Icons: Vanilla CSS (Premium Dark Theme) + Lucide Icons

✨ Features Implemented
📱 Backup Discovery
Auto-detection: Automatically scans iTunes/Finder backups from:

%APPDATA%\Apple Computer\MobileSync\Backup

%APPDATA%\Apple\MobileSync\Backup

Metadata Display: Shows device name, product model, iOS version, last backup date, and encryption status.

Manual Selector: Support for backups located in non-standard folders via a manual directory picker.

🗂️ Virtual File System Explorer
Recursive Navigation: Explore domain subfolders (e.g., Media/DCIM/100APPLE).

Smart Sidebar Categories: Data is grouped for faster discovery:

Communications: Photos, WhatsApp, Messages.

Browsing: Safari History & Data.

System: Notes, Contacts, Call History, Keychains, Preferences.

Breadcrumb Navigation: Clickable segments for seamless folder switching.

✏️ Plist Editor
Interactive Tree Editor: Supports both XML and Binary .plist files.

Inline Editing: Click any value to edit strings, numbers, or booleans directly.

Data Consistency: Saves changes to the physical file and automatically updates the Manifest.db to keep the backup valid.

🌎 Settings & Localization
Full i18n: Complete support for both English and French languages.

Settings Panel: Centralized modal to switch themes and languages with persistent storage.

Dynamic Themes: Toggle between Dark, Light, and OLED modes with intuitive Sun/Moon icons.

🖼️ Preview & Export
Image Preview: Inline support for HEIC, JPEG, and PNG files directly in the detail panel.

Native Export: Export any file to disk via the standard Windows Save dialog.

🔒 Security & Technical Notes
Encryption Support
Detection: The application correctly identifies if a backup is encrypted via Manifest.plist.

[!WARNING]
Note: Encrypted backups are not supported at this time. A clear message is displayed if encryption is detected.

Architecture
UI/UX: Frameless custom titlebar with integrated breadcrumbs and window controls.

Visuals: Custom dark theme featuring glassmorphism elements, using Inter and Fira Code fonts.

Branding: Features the official IBE Logo for the application icon and interface.

📦 Executables
Located in the release/ folder:

File	Type	Size
IOS Backup Explorer 0.0.0.exe	Portable (no install needed)	~84 MB
IOS Backup Explorer Setup 0.0.0.exe	NSIS Installer (with shortcuts)	~84 MB
