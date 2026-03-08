## Nmap Scan Analysis

The reconnaissance scan revealed multiple exposed services on the target host. These services provide insight into the system's potential attack surface and overall security posture.

---

### Legacy Protocol Exposure

Legacy protocols were identified including:

- **FTP (Port 21)**
- **Telnet (Port 23)**
- **POP3 (Port 110)**

These protocols transmit data in **plaintext**, meaning sensitive information such as usernames and passwords could potentially be intercepted by attackers using packet sniffing techniques.

---

### Remote Access Services

Remote access services detected during the scan include:

- **Telnet**
- **Remote Desktop Protocol (RDP)**

Publicly accessible remote administration services significantly increase the likelihood of **brute-force authentication attacks** and unauthorized system access if proper security controls are not implemented.

---

### Database Exposure

Two database services were discovered:

- **MySQL (Port 3306)**
- **PostgreSQL (Port 5432)**

Exposed database services increase the risk of:

- Unauthorized data access
- Data exfiltration
- Database exploitation if misconfigurations or weak credentials exist.

---

### Web Services

Two web services were detected:

- **HTTP (Port 80)**
- **HTTPS (Port 443)**

Public web servers increase exposure to potential **web application vulnerabilities**, such as:

- SQL Injection
- Cross-Site Scripting (XSS)
- Misconfigured web services

---

### Conclusion

The scan results demonstrate that the target system exposes multiple network services, including administrative protocols, database services, and web applications.

Reducing the number of publicly exposed services and implementing stronger access controls would significantly improve the system’s **overall security posture and attack surface reduction**.
