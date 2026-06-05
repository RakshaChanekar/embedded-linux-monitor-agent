# Embedded Linux Monitoring Agent 🚀

## 📌 Overview
This project is a lightweight **Embedded Linux System Monitoring Agent** developed in C++. It continuously monitors system performance by collecting real-time CPU, RAM, and Disk usage using Linux kernel interfaces and system files.

The agent simulates real-world embedded device behavior such as IoT gateways, routers, and industrial monitoring systems.

---

## 🎯 Key Features

- 📊 CPU Usage monitoring using `/proc/stat`
- 🧠 RAM usage monitoring using `/proc/meminfo`
- 💾 Disk usage monitoring using `statvfs()`
- 🔁 Continuous system monitoring (daemon-like behavior)
- 📝 Automatic log generation (`monitor.log`)
- 📂 Process monitoring using Linux `ps` command
- ☁️ AWS S3 integration for log upload (via Bash script)
- 🐳 Docker containerization for portable execution

---

## 🛠️ Tech Stack

- **Programming Language:** C++
- **Operating System:** Linux (Ubuntu / WSL)
- **Embedded Concepts:** Linux system programming, `/proc` filesystem
- **Scripting:** Bash
- **Cloud:** AWS S3
- **DevOps Tools:** Docker, Git
- **System Tools:** statvfs(), ps, /proc filesystem

---

## 🧠 System Architecture

<img width="1247" height="826" alt="image" src="https://github.com/user-attachments/assets/de5de476-4d2c-40d0-b772-71515bdc825f" />

## 📂 Project Structure


embedded-monitor-agent/
│
├── src/
│ └── monitor.cpp
│
├── scripts/
│ └── upload_logs.sh
│
├── monitor.log
├── Dockerfile
└── README.md


---

## ⚙️ How to Build & Run

### 1️⃣ Compile the project
```bash
g++ src/monitor.cpp -o monitor
2️⃣ Run monitoring agent
./monitor

Stop execution:

CTRL + C
3️⃣ View logs
cat monitor.log
☁️ AWS S3 Log Upload
Step 1: Configure AWS CLI
aws configure
Step 2: Upload logs
bash scripts/upload_logs.sh
🐳 Docker Support
Build Docker Image
docker build -t embedded-linux-monitor .
Run Container
docker run -it embedded-linux-monitor
📈 Learning Outcomes

This project demonstrates:

Embedded Linux system understanding
Linux kernel interfaces (/proc, system calls)
Real-time system monitoring
C++ system programming
Bash scripting automation
Cloud integration using AWS S3
Containerization using Docker
💼 Use Case

This project simulates real-world systems such as:

IoT monitoring devices
Edge computing systems
Industrial control systems
Network routers and embedded gateways
👩‍💻 Author

Raksha M Chanekar
Pune, India
Aspiring Embedded Linux / DevOps Engineer

🚀 Future Improvements
Add CPU graph visualization (Grafana integration)
Real-time alert system using email/SNS
MQTT-based IoT communication
Web dashboard for monitoring
Cross-platform embedded deployment (ARM/Raspberry Pi)
