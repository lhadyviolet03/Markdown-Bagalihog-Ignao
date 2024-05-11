# Markdown-Bagalihog-Ignao

#### Ethical Hacking Engagement Report: PhilHealth
**Client:** PhilHealth
**Date:** April 10, 2024  
**Prepared by:** Joy C. Bagalihog and Criselle B. Ignao  

**Executive Summary:**

This report details the results of an ethical hacking engagement aimed at uncovering potential security vulnerabilities within PhilHealth's systems and infrastructure. Through automated scans and manual tests, critical vulnerabilities across various areas like web applications, databases, and physical security were discovered. Recommendations to address these issues include implementing secure coding practices, enhancing authentication mechanisms, and improving physical security measures. While the findings are hypothetical, addressing these vulnerabilities can bolster PhilHealth's cybersecurity defenses and safeguard patient data privacy.

**Vulnerability Summary:**

1. **Unsecured API Endpoints:** APIs designed to manage patient data or healthcare claims might be accessible without proper authentication or authorization, allowing unauthorized access to sensitive information.
   - **Critical:** The PhilHealth company's web application is vulnerable to SQL injection attacks, potentially allowing attackers to manipulate database queries and access or modify sensitive information stored in the database.
   - **High:** APIs designed to manage patient data or healthcare claims might be accessible without proper authentication or authorization, allowing unauthorized access to sensitive information.

2. **Data Leakage Through Misconfigured Databases:** Improper database configurations could expose patient data, such as names, addresses, or medical records, in case of a breach.
   - **Critical:** The PhilHealth company's web application may have insecure direct object references (IDOR) that allow unauthorized users to access and manipulate patient records by directly referencing object identifiers (e.g., patient IDs) in URLs or parameters.
   - **High:** Improper database configurations could expose patient data, such as names, addresses, or medical records, in case of a breach.

3. **Insecure File Transfer Practices:** Sending or storing sensitive patient information through unsecured channels could be vulnerable to interception by attackers.
   - **Critical:** The PhilHealth company's Electronic Health Records (EHR) system may have weak access controls, allowing unauthorized users to view, modify, or delete patient records.
   - **High:** Sending or storing sensitive patient information through unsecured channels could be vulnerable to interception by attackers. This vulnerability could occur when employees transmit patient data via unencrypted email attachments or use insecure file-sharing platforms without proper encryption or access controls.
4. **Weak Encryption for Sensitive Data:** Patient data at rest or in transit might be inadequately encrypted, making it easier to decrypt if stolen.
    - **Critical:** The PhilHealth company's patient management system may be vulnerable to SQL injection attacks, allowing attackers to manipulate database queries and access or modify sensitive patient data.
    - **High:** Patient data at rest or in transit might be inadequately encrypted, making it easier to decrypt if stolen. Weak encryption algorithms or improperly implemented encryption mechanisms could expose sensitive patient information to unauthorized access or theft.
5. **Insider Threat Potential:** Privileged access granted to healthcare providers or PhilHealth staff could be misused for unauthorized access, data manipulation, or fraud.
   - **Critical:** The patient portal used by PhilHealth may employ weak authentication mechanisms, such as simple passwords or lack of multi-factor authentication, making it susceptible to unauthorized access by attackers.
   - **High:** Privileged access granted to healthcare providers or PhilHealth staff could be misused for unauthorized access, data manipulation, or fraud. This vulnerability poses a significant risk as insiders with legitimate access to sensitive systems and data may abuse their privileges intentionally or unintentionally, resulting in data breaches, unauthorized disclosures, or financial losses.
6. **Denial-of-Service (DoS) Vulnerabilities in Claims Processing Systems:** Critical PhilHealth systems responsible for processing health insurance claims might be susceptible to DoS attacks, causing delays or service disruption.
   - **Critical:** The claims database of PhilHealth may be vulnerable to unauthorized access, allowing attackers to view, modify, or delete sensitive information related to health insurance claims.
   - **High:** Critical PhilHealth systems responsible for processing health insurance claims might be susceptible to DoS attacks, causing delays or service disruption. Attackers could exploit vulnerabilities in the infrastructure, such as network or application-layer weaknesses, to overwhelm the systems with malicious traffic, leading to downtime or degradation of services.
7. **Insufficient Logging and Auditing of User Activity:** Lack of comprehensive logging and auditing of user activity on PhilHealth's systems could make it difficult to detect and investigate suspicious behavior.
   - **Critical:** PhilHealth's systems may have weak password policies and practices, such as the use of easily guessable passwords, password sharing, or lack of password expiration policies, making them vulnerable to unauthorized access and credential-based attacks.
   - **High:** Lack of comprehensive logging and auditing of user activity on PhilHealth's systems could make it difficult to detect and investigate suspicious behavior. Insufficient logging may result in gaps in the organization's ability to track and monitor user actions, including unauthorized access attempts, data breaches, or system misuse.
8. **Social Engineering Susceptibility of Staff:** PhilHealth staff might be susceptible to social engineering attacks like phishing emails or phone scams, potentially leading to compromised credentials or data breaches.
   - **Critical:** PhilHealth's endpoint devices, such as workstations and laptops used by staff, may lack adequate security controls, making them vulnerable to malware infections, data exfiltration, or unauthorized access
   - **High:** PhilHealth staff might be susceptible to social engineering attacks like phishing emails or phone scams, potentially leading to compromised credentials or data breaches. Social engineering attacks exploit human psychology to manipulate individuals into disclosing sensitive information, clicking on malicious links, or performing actions that compromise security.
9. **Outdated Software on Legacy Systems:** Continued use of outdated software on older PhilHealth systems might introduce vulnerabilities that haven't been addressed through security patches.
   - **Critical:** PhilHealth may lack secure remote access controls for accessing legacy systems, potentially exposing them to unauthorized access or exploitation from external attackers.
   - **High:** Continued use of outdated software on older PhilHealth systems might introduce vulnerabilities that haven't been addressed through security patches. Unsupported or end-of-life software may no longer receive security updates, leaving systems exposed to known vulnerabilities that could be exploited by attackers
10. **Physical Security Weaknesses at Data Centers:** Inadequate physical security measures at data centers storing patient information could increase the risk of unauthorized access.
    - **Critical:**  Insider threats from data center personnel pose a critical risk to the security of patient information stored in data centers. Trusted insiders with physical access to data center facilities may abuse their privileges to access or manipulate sensitive data, potentially leading to data breaches or unauthorized disclosures.
    - **High:** Inadequate physical security measures at data centers storing patient information could increase the risk of unauthorized access. Weaknesses in physical security controls, such as insufficient access controls, lack of surveillance cameras, or ineffective monitoring of entry points, may expose sensitive data to theft, tampering, or destruction.

**Recommendations:**
1. **Unsecured API Endpoints:**
   - Conduct a thorough code review of the web application to identify and sanitize all user inputs to prevent SQL injection attacks. Implement parameterized queries or use Object-Relational Mapping (ORM) frameworks to mitigate the risk of SQL injection vulnerabilities. Regularly scan the application for vulnerabilities and apply security patches promptly to address any newly discovered vulnerabilities. Additionally, implement web application firewalls (WAFs) to provide an additional layer of defense against SQL injection attacks.
   - Implement robust authentication mechanisms such as OAuth 2.0 or JWT tokens for API endpoints. Additionally, enforce proper authorization checks to ensure that only authenticated and authorized users can access sensitive data. Regularly monitor and audit API access logs for any suspicious activity.

2. **Data Leakage Through Misconfigured Databases:**
   - Implement proper authorization mechanisms, such as role-based access control (RBAC) or attribute-based access control (ABAC), to restrict access to patient records based on user roles and permissions. Ensure that sensitive patient data is only accessible to authorized personnel with a legitimate need-to-know. Implement input validation and access controls at the application level to prevent unauthorized access to patient records through IDOR vulnerabilities. Regularly perform security testing, including penetration testing and code review, to identify and remediate IDOR vulnerabilities in the web application.
   - Conduct regular security audits and assessments of the database configurations to ensure that they adhere to industry best practices and compliance standards, such as HIPAA. Implement strict access controls and encryption mechanisms to protect sensitive patient data at rest and in transit. Utilize database security tools and monitoring solutions to detect and alert on any unauthorized access or unusual activities. Develop and enforce data handling policies and procedures to govern the access, storage, and transmission of patient information, and provide comprehensive training to employees on data security best practices and compliance requirements.
3. **Insecure File Transfer Practices:**
    - Strengthen access controls in the EHR system by implementing role-based access control (RBAC) mechanisms to restrict user access based on their roles and responsibilities. Regularly review and update user permissions to ensure that only authorized personnel have access to patient records. Implement audit logging and monitoring capabilities to track user activities and detect any unauthorized access attempts or suspicious behavior. Conduct regular security assessments and penetration testing to identify and remediate vulnerabilities in the EHR system's access controls.
    - Implement secure file transfer protocols such as SFTP (SSH File Transfer Protocol) or FTPS (FTP Secure) for transferring sensitive patient information. Encrypt patient data both in transit and at rest using strong encryption algorithms. Provide training and awareness programs to educate employees about the importance of secure file transfer practices and the risks associated with using unsecured communication channels. Implement data loss prevention (DLP) solutions to monitor and prevent unauthorized transfer of sensitive patient information. Regularly audit and review file transfer practices to ensure compliance with security policies and regulations.
4. **Weak Encryption for Sensitive Data:** 
   - Conduct a thorough code review of the patient management system to identify and remediate SQL injection vulnerabilities. Implement parameterized queries or prepared statements to prevent malicious input from being interpreted as SQL commands. Utilize web application firewalls (WAFs) to detect and block SQL injection attacks in real time. Regularly perform security testing, including automated and manual penetration testing, to identify and mitigate SQL injection vulnerabilities in the patient management system. Keep the patient management system and associated software up-to-date with security patches and updates to address any newly discovered vulnerabilities.
   - Conduct a comprehensive review of encryption protocols and algorithms used to protect sensitive patient data. Ensure that industry-standard encryption algorithms, such as AES (Advanced Encryption Standard), are implemented with strong key management practices. Regularly update encryption protocols and algorithms to mitigate vulnerabilities identified in cryptographic libraries or protocols. Implement data encryption both at rest and in transit using secure protocols such as TLS (Transport Layer Security) for network communications and disk encryption for data storage. Provide training to employees on encryption best practices and the importance of safeguarding sensitive patient information.
5. **Insider Threat Potential:** 
   - Enhance the authentication mechanisms of the patient portal by implementing strong password policies, including minimum length requirements, complexity rules, and periodic password changes. Implement multi-factor authentication (MFA) to add layer of security and verify the identity of users accessing the patient portal. Utilize adaptive authentication techniques to dynamically adjust authentication requirements based on risk factors such as device trustworthiness, location, and user behavior. Regularly monitor and analyze authentication logs for suspicious activity and implement account lockout mechanisms to prevent brute-force attacks. Conduct security testing, including penetration testing and vulnerability assessments, to identify and remediate weaknesses in the authentication mechanisms of the patient portal.
   - Implement a least privilege principle to restrict access to sensitive systems and data only to authorized personnel based on their roles and responsibilities. Conduct regular access reviews and audits to monitor and enforce compliance with access control policies. Implement robust authentication mechanisms such as multi-factor authentication (MFA) to verify the identity of users accessing sensitive systems or data. Provide comprehensive training and awareness programs to educate employees about insider threat risks, the importance of safeguarding sensitive information, and the consequences of unauthorized access or misuse of privileged credentials
6. **Denial-of-Service (DoS) Vulnerabilities in Claims Processing Systems:**
   - Strengthen access controls to the claims database by implementing role-based access control (RBAC) mechanisms to restrict access to authorized personnel based on their roles and responsibilities. Encrypt sensitive data stored in the claims database to protect it from unauthorized access or theft. Monitor and log database access activities to detect and investigate any unauthorized access attempts or suspicious behavior. Conduct regular security assessments and audits to identify and remediate vulnerabilities in the claims database. Implement database activity monitoring (DAM) solutions to continuously monitor database transactions and enforce security policies.
   - Implement robust network security measures, such as firewalls, intrusion detection and prevention systems (IDPS), and rate-limiting mechanisms, to detect and mitigate DoS attacks. Utilize load balancing and failover mechanisms to distribute traffic and ensure high availability of critical claims processing systems. Implement distributed denial-of-service (DDoS) protection solutions and cloud-based scrubbing services to mitigate large-scale DoS attacks. Regularly conduct vulnerability assessments and penetration testing to identify and remediate weaknesses in the infrastructure that could be exploited by DoS attacks. Develop incident response plans and procedures to quickly mitigate the impact of DoS attacks and restore normal operations.
7. **Insufficient Logging and Auditing of User Activity:**
   - Implement and enforce strong password policies, including minimum length requirements, complexity rules, and regular password expiration intervals, to enhance the security of user accounts and credentials. Utilize password management tools and techniques, such as password hashing and salting, to securely store and manage passwords in the system. Enforce multi-factor authentication (MFA) for user accounts to provide an additional layer of security and mitigate the risk of credential-based attacks. Conduct regular password audits and password strength assessments to identify and remediate weak or compromised passwords. Provide security awareness training to employees to educate them about the importance of password security and best practices for creating and managing passwords securely.
   - Implement robust logging and auditing mechanisms across all PhilHealth systems to capture and record user activity, system events, and security-relevant actions. Define and enforce logging policies to ensure that all relevant events are logged with sufficient detail, including user authentication, access control changes, privilege escalations, and critical system activities. Utilize centralized logging solutions to aggregate and analyze log data from various sources, enabling real-time monitoring and proactive threat detection. Regularly review and analyze log data to identify anomalies, security incidents, or policy violations, and respond promptly to mitigate risks. Provide training and awareness programs to educate employees about the importance of logging and auditing practices and their role in maintaining cybersecurity.
8. **Social Engineering Susceptibility of Staff:**
   - Implement robust endpoint security solutions, including antivirus software, endpoint detection and response (EDR) tools, and host-based intrusion prevention systems (HIPS), to protect against malware threats and unauthorized access. Enforce device encryption and endpoint management policies to secure sensitive data stored on endpoint devices and prevent data breaches in case of device loss or theft. Implement application whitelisting and privilege management to control the installation and execution of software on endpoint devices and minimize the risk of malware infections. Regularly patch and update endpoint software and operating systems to address known vulnerabilities and security flaws. Conduct regular security assessments and penetration testing to identify and remediate weaknesses in endpoint security controls and ensure continuous improvement of security posture.
   - Conduct regular security awareness training programs to educate PhilHealth staff about the tactics and techniques used in social engineering attacks and how to recognize and respond to suspicious emails, phone calls, or other communications. Implement email filtering and anti-phishing solutions to detect and block malicious emails before they reach staff inboxes. Establish clear procedures and protocols for verifying the identity of individuals requesting sensitive information or performing unusual actions, such as changing passwords or accessing confidential data. Encourage a culture of skepticism and caution among staff, emphasizing the importance of verifying requests for information or actions that seem unusual or unexpected.
9. **Outdated Software on Legacy Systems:** 
   - Implement secure remote access solutions, such as virtual private networks (VPNs) or remote desktop gateways, to provide encrypted and authenticated access to legacy systems from external networks. Enforce strong authentication mechanisms, such as multi-factor authentication (MFA) and certificate-based authentication, to verify the identity of remote users and prevent unauthorized access. Implement access controls and session logging mechanisms to monitor and audit remote access activities, and enforce least privilege principles to restrict access to only authorized users and resources. Regularly review and update remote access policies and configurations to align with security best practices and compliance requirements. Conduct regular security assessments and penetration testing to identify and remediate vulnerabilities in remote access controls and ensure continuous improvement of security posture.
   - Develop a comprehensive inventory of all legacy systems and software used within PhilHealth's infrastructure. Prioritize upgrading or replacing legacy systems that are no longer supported by vendors or have reached end-of-life status. Implement a regular patch management process to ensure that all software and systems receive timely security updates and patches. Utilize virtualization or containerization technologies to isolate legacy applications and mitigate the risk of exploitation. Implement network segmentation and access controls to limit exposure of legacy systems to the internal network and reduce the attack surface. Conduct regular vulnerability assessments and penetration testing to identify and remediate vulnerabilities in legacy systems, and develop contingency plans to mitigate risks associated with unsupported software.
10. **Physical Security Weaknesses at Data Centers:** 
    - Implement strict access controls and monitoring mechanisms to prevent unauthorized access and mitigate the risk of insider threats. Conduct thorough background checks and security screenings for data center personnel to verify their trustworthiness and integrity. Implement role-based access controls (RBAC) and least privilege principles to restrict access to sensitive data and systems based on job responsibilities and business needs. Monitor and audit privileged user activities, including system administrators and data center staff, to detect and respond to suspicious behavior or policy violations. Provide regular training and awareness programs to data center personnel on the importance of security policies and procedures, ethical conduct, and the consequences of insider threats.
    - Conduct a comprehensive security assessment of data center facilities to identify and address physical security weaknesses. Implement robust access controls, including biometric authentication, access cards, and security guards, to restrict access to authorized personnel only. Install surveillance cameras and monitoring systems to monitor entry points, server rooms, and critical infrastructure areas. Implement environmental controls, such as temperature and humidity monitoring, to prevent damage to equipment and ensure the integrity of stored data. Develop and implement incident response plans and procedures to respond effectively to physical security breaches or unauthorized access incidents. Provide training and awareness programs to data center staff on security best practices and procedures for maintaining physical security controls.

**Conclusion**: The ethical hacking engagement conducted on PhilHealth's systems revealed significant vulnerabilities that pose a threat to patient data security and privacy. Implementing recommended remediation measures is crucial to enhance PhilHealth's security posture and protect sensitive information from unauthorized access and data breaches. PhilHealth must prioritize cybersecurity initiatives, maintain proactive threat detection, and cultivate a culture of security awareness among its employees. Continued investment in cybersecurity measures, regular assessments, and ongoing training will be essential to safeguard patient data and maintain trust among members. Addressing these cybersecurity risks demonstrates PhilHealth's commitment to protecting healthcare information and delivering quality services to the Filipino population.

**Signature:**
![Ethical Hackers Signature](signature.png)
