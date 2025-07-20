# Setting Up Kali Linux in VirtualBox on Windows

Follow these steps to install and run Kali Linux using VirtualBox on your Windows machine.

---

## Step 1: Download VirtualBox

- Go to the official [VirtualBox website](https://www.virtualbox.org).
- Download the Windows installer.
- Run the setup and follow the installation steps.

<img width="1847" height="850" alt="image" src="https://github.com/user-attachments/assets/07d1bc36-a2c9-49c8-84b0-c601e1c02a77" />

---

## Step 2: Download Kali Linux for VirtualBox

- Visit the Kali Linux official page: [Get Kali](https://www.kali.org/get-kali/#kali-virtual-machines).
- Scroll to the **"Virtual Machines"** section.
- Download the **Kali Linux VirtualBox (OVA)** file (approx. 3.3 GB).

<img width="1870" height="696" alt="image" src="https://github.com/user-attachments/assets/792f3a2d-4577-4669-ae39-2bd36561b6b3" />

---

## Step 3: Extract the Kali Linux Files

- After downloading, extract the compressed `.7z` or `.zip` file.
- You will see two important files:
  - **`.vdi` (Virtual Disk Image):** This file contains the virtual hard disk of the Kali OS.
  - **`.vbox` (VirtualBox Machine Definition):** This file stores the VM configuration like hardware settings and disk links.

> Tip: You can double-click the `.vbox` file to automatically load the Kali VM into VirtualBox.

---

## Step 4: Enable Windows Features

Before running the VM, enable the following Windows features:

1. Open **Control Panel → Programs → Turn Windows features on or off**.
2. Enable:
   - **Virtual Machine Platform**
   - **Windows Hypervisor Platform**
3. Click **OK** and **restart your system**.

<img width="400" height="82" alt="image" src="https://github.com/user-attachments/assets/6f4135fd-5456-4164-85d8-95f18e3ffd0f" />

---

## Step 5: Launch and Configure Kali VM

1. Open the extracted Kali Linux folder.
2. Double-click the `.vbox` file to open it in VirtualBox.
<img width="600" height="318" alt="image" src="https://github.com/user-attachments/assets/c17b0b41-4a37-488a-ad92-1c908b78981f" />
<img width="900" height="560" alt="image" src="https://github.com/user-attachments/assets/e1727010-c94e-4c12-9ad1-f0ff6fd8f66d" />
3. In VirtualBox, click **Settings**:
   - Allocate memory (RAM) (e.g., 2048 MB or more).

   <img width="558" height="197" alt="image" src="https://github.com/user-attachments/assets/7071a09e-5398-4ee6-8262-0b7518e067d6" />


   - Assign CPU cores (e.g., 2 or more).

     
   <img width="586" height="200" alt="image" src="https://github.com/user-attachments/assets/264b39f9-2965-47ae-8729-da095fa9abea" />


4. Click **Start** to boot the virtual machine.
5. When prompted, enter:
   - **Username:** `kali`
   - **Password:** `kali`
  <img width="280" height="378" alt="image" src="https://github.com/user-attachments/assets/831ebec2-7b5b-48e6-8e84-79fd970b9398" />

---

## Optional: Prevent File Corruption

- It's recommended to **create a separate volume or drive partition** (e.g., `D:\KaliVM`) and store your Kali VM files there.
- This reduces the chance of corruption due to OS crashes or disk write issues.

---

## Common Errors and Fixes

| Error Message or Issue | Cause | Solution |
|------------------------|-------|----------|
| **VT-x/AMD-V not enabled** | Virtualization is disabled in BIOS | Reboot and enable Virtualization (Intel VT-x / AMD-V) in BIOS settings |
| **Failed to open a session for the virtual machine** | Hyper-V conflict or corrupt VM config | Ensure Hyper-V is off if not using WSL, and re-import the `.vbox` file |
| **No bootable medium found** | Incorrect image file or disk missing | Make sure you're using the `.vbox` file, not just the `.vdi` |
| **Kernel panic** | Misconfigured system resources | Allocate more RAM/cores or re-check downloaded image integrity |
| **Black screen after boot** | Low memory or corrupted files | Increase allocated memory and re-extract the VM files |
| **Stuck on boot logo** | Windows features not enabled | Ensure **Virtual Machine Platform** and **Windows Hypervisor Platform** are both enabled and restart your PC |

---
