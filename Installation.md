# OWASP Juice Shop Installation Guide

## Overview

This guide explains how to install and run OWASP Juice Shop on both Kali Linux and Windows 10 virtual machines.

OWASP Juice Shop is a deliberately vulnerable web application used for learning web application security, penetration testing, and ethical hacking.

---

# System Requirements

## Minimum Requirements

* 2 GB RAM
* 20 GB Disk Space
* Internet Connection
* Virtual Machine Software

  * VMware Workstation
  * Oracle VirtualBox

---

# Installation on Kali Linux Virtual Box

## Step 1: Update Kali Linux

Open Terminal and run:

```bash
sudo apt update && sudo apt upgrade -y
```

---

## Step 2: Install Node.js

Install Node.js and npm:

```bash
sudo apt install nodejs npm -y
```

Verify installation:

```bash
node -v
npm -v
```

---

## Step 3: Install Git

```bash
sudo apt install git -y
```

Verify installation:

```bash
git --version
```

---

## Step 4: Clone OWASP Juice Shop Repository

```bash
git clone https://github.com/juice-shop/juice-shop.git
```

Move into the directory:

```bash
cd juice-shop
```

---

## Step 5: Install Dependencies

```bash
npm install
```

This may take several minutes.

---

## Step 6: Start Juice Shop

```bash
npm start
```

You should see output similar to:

```text
Listening on port 3000
```

---

## Step 7: Access the Application

Open a browser and navigate to:

```text
http://localhost:3000
```

or

```text
http://127.0.0.1:3000
```

---

# Installation on Windows 10 Virtual Box

## Step 1: Install Node.js

Download and install Node.js LTS version.

After installation, open Command Prompt and verify:

```cmd
node -v
npm -v
```

---

## Step 2: Install Git

Download and install Git for Windows.

Verify installation:

```cmd
git --version
```

---

## Step 3: Clone Juice Shop Repository

Open Command Prompt:

```cmd
git clone https://github.com/juice-shop/juice-shop.git
```

Move to the project directory:

```cmd
cd juice-shop
```

---

## Step 4: Install Dependencies

```cmd
npm install
```

Wait for installation to complete.

---

## Step 5: Start Juice Shop

```cmd
npm start
```

You should see:

```text
Listening on port 3000
```

---

## Step 6: Access Juice Shop

Open your browser and visit:

```text
http://localhost:3000
```

---

# Alternative Installation Using Docker

## Install Docker

Verify Docker installation:

```bash
docker --version
```

---

## Download Juice Shop Docker Image

```bash
docker pull bkimminich/juice-shop
```

---

## Run Juice Shop Container

```bash
docker run -d -p 3000:3000 bkimminich/juice-shop
```

---

## Access Application

```text
http://localhost:3000
```

---

# Troubleshooting

## Port 3000 Already in Use

Find the process:

### Linux

```bash
sudo lsof -i :3000
```

### Windows

```cmd
netstat -ano | findstr :3000
```

Terminate the process and restart Juice Shop.

---

## Node.js Version Issues

Verify:

```bash
node -v
```

Use the latest LTS release if installation errors occur.

---

## Missing Dependencies

Remove old packages and reinstall:

```bash
rm -rf node_modules
npm install
```

Windows:

```cmd
rmdir /s node_modules
npm install
```

---
---

# Useful Commands

Start Application:

```bash
npm start
```

Stop Application:

```text
CTRL + C
```

Update Repository:

```bash
git pull
```

Install Dependencies:

```bash
npm install
```

---

# References

* OWASP Juice Shop Official Documentation
* OWASP Top 10
* PortSwigger Web Security Academy
* OWASP Testing Guide

---

