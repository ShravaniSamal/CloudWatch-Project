# CloudWatch-Project
This project enables real-time CPU monitoring on an AWS EC2 instance using CloudWatch and SNS alerts. A Python script spikes CPU usage, triggering a CloudWatch Alarm that sends an email notification via SNS when utilization exceeds the threshold. This helps in automated monitoring, proactive alerting, and better system reliability
AWS CloudWatch CPU Utilization Monitoring with SNS Alerts 🚀

This project demonstrates how to monitor CPU utilization using AWS CloudWatch and trigger SNS alerts when CPU usage exceeds a threshold. A Python script is used to spike CPU usage, triggering an alarm that sends a real-time email notification via SNS.

Features
✅ Monitor EC2 CPU utilization with CloudWatch 📊
✅ Automate alerts using CloudWatch Alarms 🚨
✅ Receive real-time notifications via SNS 📩
✅ Python script to simulate high CPU usage ⚡

Architecture 🏗️
1️⃣ EC2 Instance – Hosts the application
2️⃣ Python Script – Generates high CPU utilization
3️⃣ CloudWatch Metrics – Tracks CPU usage
4️⃣ CloudWatch Alarm – Triggers alerts when threshold is exceeded
5️⃣ SNS Topic – Sends notifications via email

Setup Instructions 🔧
1️⃣ Launch an EC2 Instance
Select Ubuntu or Amazon Linux

Allow SSH (port 22) and other required ports

2️⃣ Install Dependencies
Connect to your instance and run:

sh
Copy
Edit
sudo apt update && sudo apt install python3-pip -y
pip3 install boto3
3️⃣ Create and Run the CPU Spike Script
python3 cpu_spike.py &
4️⃣ Set Up CloudWatch Alarm & SNS
Go to AWS CloudWatch > Alarms > Create Alarm

Select EC2 CPUUtilization metric

Set Threshold: >50% for 1 minutes

Create an SNS topic and subscribe via email

Confirm SNS subscription from your email

5️⃣ Trigger the Alarm & Receive Notification
Run the CPU spike script again

Wait for CloudWatch to detect high CPU

