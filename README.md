# ASK-Data-Shield

> A lightweight, automated Python-based data backup utility that performs incremental backups using cryptographic file hashing and creates timestamped zip archives at scheduled intervals.

## 📝 Overview
The ASK Data Shield System is a fully automated backup script designed to protect your important files without relying on heavy or expensive cloud software. It continuously monitors a target directory, identifies new or modified files, backs them up to a safe location, and compresses the backup into a timestamped `.zip` archive on a recurring schedule.

## 🎯 What Problem Does This Solve?
Setting up automated backups often requires complex software that consumes heavy background resources. Manual backups are tedious and easily forgotten. This script provides a simple, terminal-based "set it and forget it" solution. Furthermore, to save processing time and disk space, it uses **incremental backups**—meaning it only copies files that have actually changed since the last scan, rather than copying everything over and over.

## ✨ Features
* **Incremental Backups:** Utilizes cryptographic hashing to compare files. Only newly created or recently modified files are copied to the backup directory.
* **Automated Archiving:** Automatically packages your backed-up files into a clean, timestamped `.zip` file for easy storage and version control.
* **Zero Cloud Dependency:** Everything runs and stays completely local. 
* **Automated Scheduling:** Set a minute interval, and the script handles the continuous backup loop autonomously.
* **Cross-Platform:** Built using standard Python libraries, making it fully compatible with Windows, Linux, and macOS.

---

## 🚀 Getting Started & Installation

### Prerequisites
You need Python 3.x installed on your machine. Almost all the libraries used in this script (`os`, `sys`, `time`, `shutil`, `hashlib`, `zipfile`) are built into Python. 

You only need to install the external `schedule` library:
```bash
pip install schedule
