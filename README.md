Task 4 – Setup and Use a Firewall on Kali Linux

📌 Objective

The objective of this task is to configure and test basic firewall rules on Kali Linux using UFW (Uncomplicated Firewall). This task helps in understanding how firewalls filter network traffic by allowing or blocking specific ports and services.

---

🛠 Tools Used

Operating System: Kali Linux

Firewall Tool: UFW (Uncomplicated Firewall)

---

📚 Key Concepts Covered

Firewall configuration

Inbound and outbound traffic rules

Port-based traffic filtering

Blocking insecure services (Telnet)

Allowing secure services (SSH)

---

🔍 Step-by-Step Implementation

1️⃣ Install UFW

sudo apt update
sudo apt install ufw

---

2️⃣ Check Firewall Status

sudo ufw status verbose

---

3️⃣ Enable the Firewall

sudo ufw enable

---

4️⃣ List Existing Firewall Rules

sudo ufw status numbered

---

5️⃣ Block Inbound Traffic on Port 23 (Telnet)

sudo ufw deny 23

Reason: Telnet is insecure as it transmits data in plain text.

---

6️⃣ Test the Blocked Port

telnet localhost 23

Expected result: Connection should fail, confirming the rule works.

---

7️⃣ Allow SSH (Port 22)

sudo ufw allow 22

This ensures secure remote access to the system.

---

8️⃣ Remove the Test Block Rule

sudo ufw delete <rule_number>

This restores the system to its original state after testing.

---

✅ Outcome

Successfully configured firewall rules using UFW

Understood how firewalls control network traffic

Learned how to block insecure services and allow secure ones



---





