# 🚀 Tech Stack
- **Framework**: Electron + React
- **Build System**: Vite
- **Database**: better-sqlite3 (native bindings for Manifest.db parsing)
- **Plist Engines**: plist (XML) & bplist-parser (Binary)
- **UI & Icons**: Vanilla CSS (Premium Dark Theme) + Lucide Icons

## 📦 Executables
Located in `release/`:

| File | Type | Size |
|------|------|------|
| IOS Backup Explorer 0.0.0.exe | Portable (no install needed) | ~84 MB |
| IOS Backup Explorer Setup 0.0.0.exe | NSIS Installer (with shortcuts) | ~84 MB |

## ✨ Features Implemented

### 📱 Backup Discovery
- Auto-detects iTunes/Finder backups from `%APPDATA%\Apple Computer\MobileSync\Backup` and the newer `%APPDATA%\Apple\MobileSync\Backup`
- Shows device name, product model, iOS version, last backup date, encryption status
- Manual folder selector for backups not in standard locations

### 🗂️ Virtual File System Explorer
- Recursive navigation through domain subfolders (e.g., Media/DCIM/100APPLE)
- Breadcrumb navigation with clickable segments
- Subfolder icons and "Open Folder" actions in detail panel
- Enhanced Sidebar Categories with smart grouping of data:
  - **Communications**: Photos, WhatsApp, Messages
  - **Browsing**: Safari History & Data
  - **System**: Notes, Contacts, Call History, Keychains, Preferences

### ✏️ Plist Editor
- Full interactive tree editor for both XML and Binary .plist files (using bplist-parser)
- Click any value to edit inline; supports string, number, boolean types
- Saves back to the physical file AND updates Manifest.db to keep the backup consistent

### 🔒 Encryption & Security
- Detection of Encrypted Backups: The application identifies if a backup is encrypted (Manifest.plist) and displays a clear message
- ABI & SQL Fixes: Resolved the "file is not a database" error and the SqliteError by aligning the Electron ABI and fixing the SQL syntax
- Binary Plist Support: Integrated bplist-parser for reading device information and manifest files

### 🌎 Settings & Localization
- Full i18n: Support for both English and French languages
- Settings Panel: Centralized modal to switch themes and languages with persistence
- Dynamic Themes: Dark, Light, and OLED modes with persistent user preference storage

### 🎨 UI & UX
- Custom dark theme with glassmorphism elements
- Inter + Fira Code fonts
- Custom frameless titlebar with breadcrumb navigation and window controls
- Premium Exit Flow: Clicking the close button triggers a beautiful, non-blocking "IBE is closing..." overlay with a glassmorphism effect and a smooth scale-up animation
- Unrecognized File Types: Files of unknown types display a subtle "File with Question Mark" icon instead of a generic folder or file icon
- Strict distinction between folders and files during navigation

### 🖼️ Image Preview
- Inline preview of HEIC, JPEG, PNG images directly in the detail panel

### 📤 Export
- Export any file to disk via native Save dialog