# 🧾 Cybersecurity Incident Report  
**Incident Type:** Brute Force Attack on Web Server Credentials  
**Analyst:** Raaid Ali  
**Protocols Involved:** DNS (Port 53), HTTP (Port 80)  
**Date:** 8/5/2024

---

## 🧠 Section 1: Network Protocols Involved
During the attack, both **Port 53 (DNS)** and **Port 80 (HTTP)** were involved.

The browser first initiated a **DNS request** to resolve the domain name `yummyrecipesforme.com` into its corresponding IP address. Once the DNS server responded with the correct IP, the browser used **HTTP** on port 80 to establish a connection with the web server and request the webpage content.

This sequence demonstrates how normal web browsing traffic was later exploited once the attacker gained unauthorized access to the web host.

---

## 🔍 Section 2: Incident Documentation
Investigation revealed that a **malicious actor performed a brute force attack** against the website’s administrative login.  
The web server was using **default credentials**, which allowed the attacker to **successfully gain access** after repeated login attempts.

After obtaining admin privileges, the attacker **modified the website’s source code**, embedding malicious scripts that forced any connecting user to **download malware**.  

This compromise caused:
- User systems to slow down due to malware execution.  
- Redirection of the legitimate domain `yummyrecipesforme.com` to a fake site, `greatrecipesforme.com`.  
- Contamination of web traffic and degradation of client trust.  

The incident highlights the dangers of weak or default passwords and the ease with which attackers can exploit them to compromise web infrastructure.

---

## 🛡️ Section 3: Recommended Remediation
### Primary Recommendation: **Change Default Passwords Immediately**
Never retain default administrative credentials on production servers. Default passwords are easily guessable and are one of the first targets during brute force attacks.

### Additional Recommendations:
1. **Implement a Strong Password Policy**  
   Require passwords that include uppercase, lowercase, numeric, and special characters. Enforce minimum length and periodic rotation.  

2. **Enable Account Lockout Policies**  
   Restrict login attempts by temporarily disabling accounts after a set number of failed attempts to deter brute forcing.  

3. **Use Multi-Factor Authentication (MFA)**  
   Add a second layer of verification to significantly reduce credential abuse risk.  

4. **Monitor Authentication Logs**  
   Continuously review login attempts to detect abnormal patterns and block suspicious IP addresses early.  

---

## 🧩 Lessons Learned
- Default credentials are one of the most common security oversights leading to compromise.  
- Regular credential audits and access reviews are essential for web server protection.  
- Implementing MFA and account lockout policies greatly mitigates brute force risk.  
- Keeping strong password policies and consistent monitoring ensures a secure authentication environment.

---

*This report is a simulated example created for educational and portfolio purposes. No real client or organization data is included.*
