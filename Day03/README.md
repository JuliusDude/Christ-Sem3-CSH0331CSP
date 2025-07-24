## 🧾 Linux Commands

* `ls` – List directory contents
* `cd` – Change directory
* `touch` – Create a new empty file
* `echo` – Display a line of text
* `man` – Manual pages/help for commands
* `ls -lh` – List contents in human-readable format
* `cp` – Copy files or directories
* `mv` – Move/rename files or directories
* `chmod` – Change file permissions

---

## 🦠 Malware Analysis

* **Static** – Constant (no execution)
* **Dynamic** – Varying, observed during runtime (runtime analysis)

### Other Terms

* **Ata Software** – Advanced Threat Analytics; used to detect suspicious activities in a network.
* **Prompt Injection** – A method to manipulate language models by injecting malicious input to alter responses.
* **Bash** – Unix shell and command language, used to execute commands in Linux.
* **Villain Framework** – A tool for reverse shell handling and payload delivery, used in post-exploitation.
* **AV Scans** – Antivirus scans may detect malware in OS but **not in memory**.

---

## 🔁 Git Usage

* How to clone from Git:

  ```bash
  git clone <https>
  ```
* Check repository status:

  ```bash
  git status
  ```
* Add changes to staging:

  ```bash
  git add .
  ```
* Commit changes:

  ```bash
  git commit -m "Your message"
  ```
* Push to remote:

  ```bash
  git push
  ```
---
### chmod
<img width="794" height="397" alt="image" src="https://github.com/user-attachments/assets/3eb26ee2-af46-4a77-9ebb-35827b890f1e" />

---
# How to Upgrade Kali Linux

This guide explains how to safely upgrade your Kali Linux system using APT package manager.

---

## 1. Check Your APT Sources

First, verify that your APT sources are correctly configured.

```bash
cat /etc/apt/sources.list
```

You should see:

```plaintext
deb http://http.kali.org/kali kali-rolling main non-free contrib
```

If it's missing or incorrect, edit the file:

```bash
sudo nano /etc/apt/sources.list
```

Add the correct line, save and exit.

---

## 2. Update the Package List

Update the list of available packages and their versions:

```bash
sudo apt update
```

---

## 3. Perform a Full Upgrade

This will upgrade all installed packages to the latest versions, including the kernel and major system components:

```bash
sudo apt full-upgrade -y
```

---

## 4. Clean Up Unnecessary Packages

Remove unused packages:

```bash
sudo apt autoremove
```

Clean up cached files:

```bash
sudo apt autoclean
```

---

## 5. Reboot the System

After the upgrade is complete, reboot your system:

```bash
sudo reboot
```

---

## ✅ Done!

Your Kali Linux system is now fully upgraded and ready to use.

---
# How to Install Visual Studio Code on Kali Linux

Follow these steps to download and install VS Code on Kali Linux using the official `.deb` package.

---

## 1. Download the VS Code `.deb` Package

Use `wget` to download the latest stable version:

```bash
wget "https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64" -O vscode.deb
```

---

## 2. Install the Package

Once downloaded, install the `.deb` package using `apt`:

```bash
sudo apt install ./vscode.deb
```

This command will handle all dependencies and complete the installation.

---

## ✅ Done!

You can now launch Visual Studio Code from the application menu or by typing `code` in the terminal.

If prompted, allow the installer to add the Microsoft repository for future updates.


