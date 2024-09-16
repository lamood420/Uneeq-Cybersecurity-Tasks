
# **Network Traffic Analysis**

---
### **Man-in-the-Middle Attack**

---

#### **Objective:**

Demonstrate how to capture and analyze HTTP login credentials using Wireshark during a MITM attack.

---

### **Tools Needed:**

- **Wireshark**: A network protocol analyzer to capture and inspect traffic.
- **A Web Browser**: To visit a website that uses HTTP.
- **HTTP Website**: An unencrypted website that uses HTTP (no HTTPS) for login.
- **Network Setup**: The attacker must have the capability to intercept traffic between the target (client) and the web server.

---
### **Step-by-Step Process:**

**Opened Wireshark:**

- Launched Wireshark on my computer.
- Selected the appropriate network interface (Wi-Fi adapter in this case).
- Started capturing live network traffic by clicking the blue shark fin button.

**Navigated to an HTTP Website:**

- Opened a web browser and accessed a website that uses the HTTP protocol.
- Verified the website was not encrypted by confirming the URL started with http://.

**Logged into the Website:**

- On the HTTP login page, entered the following credentials:
	- Username: example_user
	- Password: example_password
- Submitted the login form while Wireshark continued capturing traffic in the background.

**Filtered and Analyzed Traffic in Wireshark:**

- Switched back to Wireshark to analyze the captured traffic.
- Applied the HTTP filter by typing http in the filter bar and hitting Enter.
- Scrolled through the HTTP traffic and found the POST request containing the login form data.

**Extracted the Username and Password:**

- Selected the packet with the POST request.
- Expanded the Hypertext Transfer Protocol (HTTP) section in the packet details.
- Located the login credentials sent in plain text:
	- username=example_user
	- password=example_password

---

### **Conclusion:**

- This process demonstrates how easy it is to intercept unencrypted HTTP traffic and steal login credentials during a MITM attack.
- To mitigate such attacks, always use

---
#### **Task Summary:**

Performed a network traffic analysis using Wireshark to capture login credentials over an unencrypted HTTP connection.

---
