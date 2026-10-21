# AWS EC2 Lifecycle Management & Web Server Deployment

## 📋 Overview
This project provides a comprehensive hands-on implementation of launching, resizing, managing, and monitoring an Amazon Elastic Compute Cloud (Amazon EC2) instance. 

Amazon EC2 is a web service designed to provide resizable compute capacity in the cloud, making web-scale computing accessible for developers. By providing complete control over computing resources within Amazon's proven environment, it reduces server provisioning times to minutes. This enables rapid scaling—both up and down—as infrastructure requirements shift. 

Furthermore, Amazon EC2 optimizes infrastructure economics by operating on a pay-as-you-go model for utilized capacity, while delivering the core tools necessary to build failure-resilient architectures isolated from common failure vectors.

---

## 🛠️ Core Objectives & Implementation Details

### 1. Launch Web Server with Termination Protection Enabled
* **Resource Provisioning:** Deployed a Linux-based EC2 virtual machine designated as **`MyWebServer`** via the AWS Management Console.
* **Data Safeguarding:** Configured explicit termination protection attributes to mitigate the risk of accidental resource deletion.
* **Bootstrap Automation:** Utilized user-data initialization scripts to automate the installation and launching of the web server daemon.

### 2. Security Group Modification & Traffic Routing
* **Firewall Configuration:** Modified the instance's associated stateful AWS Security Group.
* **Inbound Rules:** Added a dedicated rule allowing inbound **HTTP traffic (Port 80)** from any source IP (`0.0.0.0/0`).
* **Deployment Verification:** Successfully validated the deployment by navigating to the instance's Public IPv4 address and viewing the active web page.

### 3. Instance Monitoring & Telemetry
* **Health Metrics:** Observed and verified that both System Status and Instance Status checks successfully cleared.
* **Performance Logs:** Utilized native CloudWatch metrics to monitor real-time infrastructure performance, including CPU utilization, network throughput, and disk I/O operations.

### 4. Infrastructure Scaling & Volume Resizing
* **Compute Scaling:** Successfully stopped the instance to modify the instance type to meet higher resource demands.
* **Storage Optimization:** Expanded the root Elastic Block Store (EBS) volume capacity from **8 GB to 10 GB**, subsequently extending the OS-level file system partition to recognize the newly allocated storage blocks.

### 5. Safeguard Verification & Resource Decommissioning
* **Protection Testing:** Executed an intentional termination command to confirm that the active termination protection block safely rejected the deletion request.
* **Lifecycle Cleanup:** Updated the instance settings to disable termination protection, followed by a final instance **Termination** to efficiently deprecate resources and eliminate ongoing AWS billing cycles.

---

## 📈 Technical Competencies Demonstrated
* **Compute Layer:** Amazon EC2 Instance Lifecycle Management
* **Storage Layer:** Amazon EBS Volume Optimization & Expansion
* **Network Security:** Stateful Firewall (Security Group) Traffic Filtering
* **Monitoring:** CloudWatch Infrastructure Metrics & Health Checks
