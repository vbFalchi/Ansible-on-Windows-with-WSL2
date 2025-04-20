# Using Ansible with Linux on Windows (WSL 2) - Beginner Tutorial

## ✅ What You Will Learn
- How to install WSL 2 on Windows.
- How to install Ubuntu Linux inside WSL.
- How to install Ansible inside Ubuntu.
- How to run Ansible commands from your Windows PC.

---

## 🧰 Step 1: Enable WSL and Virtual Machine on Windows

### 1.1 Open PowerShell as Administrator
Click the **Start menu**, type `powershell`, then right-click and choose **"Run as Administrator"**.

### 1.2 Run These Commands One by One:
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
- Turns on Windows Subsystem for Linux (WSL).

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
- Enables virtual machine support for WSL 2.

### 1.3 Restart Your Computer
You must **restart** Windows to finish enabling WSL and Virtual Machine Platform.

---

## 🧰 Step 2: Install WSL 2 and Ubuntu

### 2.1 Install WSL 2 from the Command Line
Open **PowerShell as Administrator** again and run:
```powershell
wsl --install
```
- Installs WSL 2 and Ubuntu LTS.

### 2.2 Wait for Ubuntu Setup
After the install, Ubuntu will open in a new window. It may take a few minutes the first time.

You will be asked to:
- Create a **Linux username**
- Create a **Linux password**

This user will be the main user for your Linux system.

---

## 🧰 Step 3: Update Linux and Install Ansible

### 3.1 Open Ubuntu (WSL) from the Start Menu

### 3.2 Update Ubuntu
```bash
sudo apt update && sudo apt upgrade -y
```
- Updates the list of software and installs all latest updates.

### 3.3 Install Ansible
```bash
sudo apt install ansible -y
```
- Installs Ansible, a tool that helps you automate tasks.

### 3.4 Check the Version
```bash
ansible --version
```
- Confirms Ansible is installed correctly.

---

## 💡 Bonus: Where are Your Files?

WSL (Ubuntu) can access your Windows files.

From inside Ubuntu, use:
```bash
cd /mnt/c
ls
```
- This takes you to your **C:\** drive.

You can move files between Ubuntu and Windows easily using the `/mnt/` path.

---

## 🧹 Summary

| Step | What You Did |
|------|--------------|
| 1 | Enabled WSL and Virtual Machine Platform |
| 2 | Installed Ubuntu using WSL 2 |
| 3 | Updated Ubuntu and installed Ansible |
| Bonus | Learned how to access Windows files from Linux |
