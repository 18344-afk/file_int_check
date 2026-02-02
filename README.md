# File Integrity Checker

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![GUI](https://img.shields.io/badge/Interface-Tkinter-green?style=flat-square)

A lightweight, Python-based GUI application designed to validate the integrity of your files. It monitors specific files for unauthorized changes, corruption, or deletion by comparing current SHA-256 hashes against a stored baseline.

## 📋 Features

### GUI Interface:
Built with tkinter, featuring a clean, column-based layout to view file paths, hash fragments, timestamps, and status.


### SHA-256 Hashing:
Uses robust SHA-256 encryption to generate unique digital signatures for every file monitored.


### Visual Status Indicators:
Color-coded feedback for quick analysis:

🟢 Green: File is intact (OK).

🔴 Red: File content has been modified.

🟡 Yellow: File is missing/deleted.


### Persistent Storage:
Saves your file baseline to baseline_hashes.json, allowing you to close and reopen the app without losing your tracking data.


### Timestamping:
Records exactly when a file was added to the monitoring list.

## 🛠️ Prerequisites

#### Python 3.x 

#### Tkinter: Included with most standard Python installations.

#### Linux users: You may need to install it manually (e.g., sudo apt-get install python3-tk).

# 🚀 Installation & Usage

### Clone the repository:

```bash
git clone https://github.com/yourusername/file-integrity-monitor.git
cd file-integrity-monitor
```
### Run the application:

```bash
python file_int.py
```
### Using the App:

### Add File:
Click + Add File to Monitor to select a file from your system. This calculates the initial hash and adds it to the baseline.

### Run Check:
Click Run Integrity Check to compare the current state of files against the saved baseline. The status column will update immediately.

### Remove File:
Select a row and click Remove Selected to stop monitoring that file.

# ⚙️ Technical Details
### The Baseline
The application creates a local file named baseline_hashes.json in the same directory as the script. This file stores the "known good" state of your files.

### Data Structure:
The application supports storing metadata including the full file path, the calculated hash, and the timestamp of when it was added.

### Hashing Logic:
The program reads files in 4096-byte chunks to ensure memory efficiency, even when hashing larger files, and generates a hexadecimal digest using the hashlib library.

# 🔮 Future Improvements:
Add recursive directory monitoring (currently monitors single selected files).

Add ability to "Update Baseline" for files that were intentionally modified.

Export reports to CSV/PDF.

Real-time background monitoring.
