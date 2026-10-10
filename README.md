# 🦅 Dead Canary: Your Reliable LAN Watchdog

![Dead Canary Logo](https://img.shields.io/badge/Dead%20Canary-v1.0.0-blue.svg)  
[![Release](https://img.shields.io/badge/Release-v1.0.0-orange.svg)](https://github.com/emebetberhe12/dead-canary/releases)

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Introduction

Welcome to **Dead Canary**, a LAN watchdog designed to monitor your network and gracefully shut down a NAS via an ESP32 device. This project aims to provide a reliable solution for ensuring your network's health and managing your NAS efficiently. 

You can find the latest releases [here](https://github.com/emebetberhe12/dead-canary/releases). Please download and execute the necessary files to get started.

---

## Features

- **Network Monitoring**: Keep an eye on your LAN for any issues.
- **Graceful Shutdown**: Automatically shut down your NAS to prevent data loss.
- **ESP32 Integration**: Utilize the power of ESP32 for effective monitoring.
- **User-Friendly**: Easy setup and configuration process.
- **Lightweight**: Minimal resource usage on your network.

---

## Installation

To install Dead Canary, follow these steps:

1. **Clone the Repository**:
   Open your terminal and run:
   ```bash
   git clone https://github.com/emebetberhe12/dead-canary.git
   ```

2. **Navigate to the Directory**:
   Change to the project directory:
   ```bash
   cd dead-canary
   ```

3. **Download Required Files**:
   You can find the latest releases [here](https://github.com/emebetberhe12/dead-canary/releases). Download and execute the necessary files.

4. **Install Dependencies**:
   Ensure you have the required libraries installed. Use the following command:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

Once you have installed Dead Canary, you can start using it right away.

1. **Connect Your ESP32**:
   Make sure your ESP32 is connected to your network.

2. **Run the Watchdog**:
   Start the watchdog by executing:
   ```bash
   python main.py
   ```

3. **Monitor Your Network**:
   The application will now monitor your LAN for any issues. If it detects a problem, it will initiate a graceful shutdown of your NAS.

---

## Configuration

You can configure Dead Canary to suit your needs. The configuration file is located in the `config` directory.

1. **Edit the Configuration File**:
   Open `config/settings.json` in your preferred text editor.

2. **Modify Parameters**:
   Adjust the parameters as needed. Key settings include:
   - `nas_ip`: The IP address of your NAS.
   - `monitor_interval`: How often to check the network (in seconds).
   - `shutdown_command`: The command to execute for shutting down the NAS.

3. **Save Changes**:
   After editing, save the configuration file.

---

## How It Works

Dead Canary operates by continuously monitoring your LAN. It checks the connectivity of devices at regular intervals. If it detects a failure, it triggers a graceful shutdown of the NAS to prevent data corruption or loss.

### Monitoring Process

1. **Ping Devices**: The watchdog sends ping requests to all configured devices.
2. **Analyze Responses**: It waits for responses and records any failures.
3. **Trigger Shutdown**: If a device fails to respond, the shutdown command is executed.

### ESP32 Role

The ESP32 serves as the central monitoring unit. It connects to your network and communicates with the NAS to manage shutdown commands.

---

## Contributing

We welcome contributions to Dead Canary! If you'd like to help improve the project, please follow these steps:

1. **Fork the Repository**: Click on the "Fork" button at the top right of the page.
2. **Create a New Branch**: Use a descriptive name for your branch.
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. **Make Changes**: Implement your changes and commit them.
   ```bash
   git commit -m "Add your message here"
   ```
4. **Push to Your Fork**:
   ```bash
   git push origin feature/YourFeatureName
   ```
5. **Create a Pull Request**: Go to the original repository and click "New Pull Request."

---

## License

Dead Canary is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact

For questions or suggestions, feel free to reach out:

- **Email**: emebetberhe12@example.com
- **GitHub**: [emebetberhe12](https://github.com/emebetberhe12)

---

Thank you for using Dead Canary! We hope it enhances your network management experience. Don't forget to check the [Releases](https://github.com/emebetberhe12/dead-canary/releases) section for updates and new features.