# PANDORA Installation Guide 🧬🔮🐳

## 🔮Introduction to PANDORA

**PANDORA** is a powerful software designed for performing machine learning (ML) analysis, including both unsupervised and supervised techniques, as well as automated ML approaches. In **Module 4**, we will use PANDORA as our primary software to explore ML methods and apply them to real-world datasets. This will help you gain hands-on experience with ML techniques, from clustering and dimensionality reduction to predictive modeling. By the end of the module, you'll be familiar with a range of ML tools and workflows used in modern research.

You can learn more about **PANDORA** on its official GitHub page: [PANDORA GitHub Repository](https://github.com/genular/pandora).

To start using PANDORA, follow the steps below to install it using **Docker**.

---

## 📋 Pre-requisites

Before installing PANDORA, you need to install **Docker** on your system. Make sure you meet the following system requirements:

- **Windows**: Version 10 or 11 (64-bit), version 21H2 or higher
- **macOS**: Latest version or the previous two releases
- Minimum **4GB RAM**
- **WSL 2** enabled on Windows (for Linux containers)
- Hardware virtualization enabled in BIOS (for both platforms)

---

## 🛠️🐳 Docker Installation

### Windows 🪟

1. **Download Docker Desktop**:  
   👉 [Download Docker for Windows](https://desktop.docker.com/win/stable/Docker%20Desktop%20Installer.exe)

2. **Install Docker**:  
   - Double-click the downloaded `Docker Desktop Installer.exe` to launch the installer.
   - On the installation screen, **select the option to use WSL 2** instead of Hyper-V. This ensures compatibility with Linux containers (recommended for our setup).
   - Follow the prompts to complete the installation. Docker may ask you to restart your computer if necessary.

3. **Start Docker**:  
   - After the installation is complete, open **Docker Desktop** from the Windows search bar.
   - When Docker starts for the first time, accept the **Subscription Agreement** to continue.

4. **Enable WSL 2 Feature**:  
   If you didn’t enable WSL 2 during installation, Docker will prompt you to enable it. Follow the on-screen instructions to install and enable **WSL 2**.

### macOS 🍏

1. **Download Docker Desktop** based on your chip type:  
   - **Apple silicon (M1/M2)**: [Download Docker for Apple Silicon](https://desktop.docker.com/mac/stable/arm64/Docker.dmg)  
   - **Intel chip**: [Download Docker for Intel Chip](https://desktop.docker.com/mac/stable/Docker.dmg)

2. **Install Docker**:  
   - Double-click the `Docker.dmg` file, then drag the Docker icon to the **Applications** folder.
   - Launch Docker from your **Applications** folder.

3. **Start Docker**:  
   - Accept the **Subscription Agreement** when Docker starts for the first time.

For more detailed instructions on Docker installation and installation instructions on Linux, visit the official guide 👉 [Docker Installation Guide](https://docs.docker.com/engine/install/).

---

## 🚀 Running PANDORA

After Docker is installed, you can pull and run the PANDORA Docker image.

1. **Open Terminal or PowerShell**:  
   - **Windows**: Open **PowerShell**.  
   - **macOS**: Open the **Terminal**.

2. **Pull the PANDORA Docker Image**:  
   Run the following command in the terminal to download and start PANDORA:

   ```bash
   docker run --rm --detach --name pandora --tty --interactive --env IS_DOCKER='true' --env TZ=America/New_York --volume pandora_data_master:/mnt/usrdata --publish 3010:3010 --publish 3011:3011 --publish 3012:3012 --publish 3013:3013 genular/pandora:latest

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

If you encounter any issues or need more details, check the official [Docker installation guide](https://docs.docker.com/engine/install/) or contact Adriana Tomic for support.

Happy analyzing with PANDORA! 🎉
