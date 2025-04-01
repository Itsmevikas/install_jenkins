# Jenkins Automation Script

## Instructions

### Prerequisites
- This script is designed for **Ubuntu/Debian-based systems**.

### Steps to Run

#### 1️⃣ Download the Script
- **Using GitHub:** Clone the repository:  
  ```bash
  git clone https://github.com/Itsmevikas/install_jenkins.git
  ```
- **Using a ZIP file:** Extract it to a preferred directory.

#### 2️⃣ Navigate to the Script Location
```bash
cd /path/to/your/script
```

#### 3️⃣ Make the Script Executable
```bash
chmod +x install_jenkins.sh
```

#### 4️⃣ Run the Script with sudo
```bash
sudo ./install_jenkins.sh
```

### Post Installation
- To access Jenkins in a web browser:
  - `http://localhost:8000`

---

## Q&A

### Describe the most difficult hurdle you had to overcome in implementing your solution.
One of the hurdles I faced was figuring out how to change Jenkins default server request port to **8000**. To resolve this, I referred to **Stack Overflow** and **Jenkins documentation**, which helped me understand the correct way to modify the port settings. After applying the right configuration, Jenkins successfully started listening on **port 8000** as required. 

Additionally, when deploying my solution on an **EC2 instance**, Jenkins was running, but I couldn’t access it externally due to **incorrect inbound rules** for port **8000** in AWS Security Groups. After updating the security group to allow traffic on port **8000**, Jenkins became accessible as expected.

### Why is it important to ensure automation does not repeat redundant tasks or cause failures?
Ensuring that automation does not repeat redundant tasks or cause failures is **critical**, especially in environments running **business-critical applications**. Unnecessary reinstallation or reconfiguration can lead to **service disruptions, increased downtime, and potential business impact**. 

Additionally, redundant operations consume **system resources unnecessarily** and can lead to unintended issues, such as **multiple configuration downloads**, which may result in **system instability or failures**. An effective automation process should be **efficient, reliable, and minimally disruptive**, applying only the necessary changes while preserving the stability of the existing infrastructure.

### Where did you go to find information to help you?
- **Jenkins Documentation**
- **Docker Hub (Jenkins Image)**
- **Stack Overflow**
- **Peer Review**
- **Gen AI**

### Briefly explain what automation means to you, and why it is important to an organization's infrastructure design strategy.
For me, automation isn’t just about eliminating **repetitive or boring tasks**—it’s about making things **more efficient and even enjoyable**. This exercise was a perfect example of that—turning a manual setup into an **automated process** made it both **fun and rewarding**. 

Automation is **crucial** to an organization’s infrastructure design strategy because it ensures **consistency, efficiency, and scalability**. By automating repetitive tasks like **deployments, configurations, and monitoring**, companies can **reduce human error, minimize downtime, and improve overall system reliability**. 

After all, the **only** task I love doing over and over again is **building LEGO sets**—everything else should be automated! 😄
