# PANDORA Installation Guide 🧬🐳

Welcome to the PANDORA installation guide! Follow these simple steps to get PANDORA up and running on your machine.

---

## 📋 Pre-requisites

Before installing PANDORA, you need to install **Docker** on your system. Make sure you meet the following system requirements:

- **Windows**: Version 10 or 11 (64-bit), version 21H2 or higher
- **macOS**: Latest version or the previous two releases
- Minimum **4GB RAM**
- **WSL 2** enabled on Windows (for Linux containers)
- Hardware virtualization enabled in BIOS (for both platforms)

---

## 🛠️ Docker Installation

### Windows 🪟

1. **Download Docker Desktop**:  
   👉 [Download Docker for Windows](https://desktop.docker.com/win/stable/Docker%20Desktop%20Installer.exe)

2. **Install Docker**:  
   Double-click the downloaded `Docker Desktop Installer.exe` and follow the instructions.  
   - When prompted, select **WSL 2** as the backend.  
   - Launch Docker after installation is complete.

3. **Start Docker**:  
   Open Docker Desktop and accept the **Subscription Agreement** to continue.

### macOS 🍏

1. **Download Docker Desktop** based on your chip type:  
   - **Apple silicon (M1/M2)**: [Download Docker for Apple Silicon](https://desktop.docker.com/mac/stable/arm64/Docker.dmg)  
   - **Intel chip**: [Download Docker for Intel Chip](https://desktop.docker.com/mac/stable/Docker.dmg)

2. **Install Docker**:  
   Double-click the `Docker.dmg` file, then drag the Docker icon to the **Applications** folder.  
   Launch Docker from your **Applications** folder.

3. **Start Docker**:  
   Accept the **Subscription Agreement** when Docker starts for the first time.

For detailed instructions on Docker installation, visit the official guide 👉 [Docker Installation Guide](https://docs.docker.com/engine/install/).

---

## 🚀 Running PANDORA

After Docker is installed, you can pull and run the PANDORA Docker image.

1. **Open Terminal or PowerShell**:  
   - **Windows**: Open **PowerShell**.  
   - **macOS**: Open the **Terminal**.

2. **Pull the PANDORA Docker Image**:  
   Run the following command in the terminal to download and start PANDORA:

   ```bash
   docker run --rm --detach --name pandora --tty --interactive --env IS_DOCKER='true' --env TZ=Europe/London --volume pandora_data_master:/mnt/usrdata --publish 3010:3010 --publish 3011:3011 --publish 3012:3012 --publish 3013:3013 genular/pandora:latest
---
This command will:

- Pull the **PANDORA** image from DockerHub
- Set up the environment variables, ports, and volumes

---

## 🌐 Accessing PANDORA

Once PANDORA is running, follow these steps to access it:

1. **Open Your Browser** (we recommend **Firefox** or **Chrome**).
2. Go to `http://localhost:3010` to access the PANDORA interface.
3. Create your administrator account and start exploring!

---

## 📚 Further Assistance

If you encounter any issues or need more details, check the official [Docker installation guide](https://docs.docker.com/engine/install/) or contact us for support.

Happy analyzing with PANDORA! 🎉
