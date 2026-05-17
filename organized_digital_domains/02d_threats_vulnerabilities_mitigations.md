# Threats, Vulnerabilities, and Mitigations

## 2.1 - Threat Vectors and Attack Surfaces 

### Threat Actors 

- A <b>threat actor</b> is any individual, group, or entity responsible for actions that negatively impact the confidentiality, integrity, or availability of systems or data. Threat actors are also commonly referred to as <b>malicious actors</b>.

<b>Internal vs External</b>

- <b>Internal threat actors</b> operate from within an organization.
- Examples include:
    - Employees
    - Contractors
    - Former staff members
- <b>External threat actors</b> operate outside the organization and attempt to gain unauthorized access.

<b>Resources and Funding</b>
- Some attackers possess:
    - Significant funding
    - Advanced infrastructure
    - Specialized tools
    - Other attackers may have very limited resources and capabilities.

<b>Level of Sophistication/Capability</b>
- Threat actors vary in technical skill levels.
- Some create custom malware and advanced exploits.
- Others rely on publicly available attack tools and scripts.

### Threat Actor Motivations 

- <b>Data Exfiltration:</b> Stealing sensitive data from systems or networks.
- <b>Espionage:</b> Gathering intelligence or confidential information. Common among governments and competitors.
- <b>Service Disruption:</b> Interrupting operations or making services unavailable. Often associated with `DoS` or `DDoS` attacks.
- <b>Blackmail:</b> Threatening to leak or destroy data unless demands are met.
- <b>Financial Gain:</b> Attackers seeking money through fraud, ransomware, or theft.
- <b>Political or Philosophical Beliefs:</b> Attacks driven by ideology or activism.
- <b>Ethical Reasons:</b> Some individuals may attack systems believing they are exposing wrongdoing.
- <b>Revenge:</b> Retaliation against organizations or individuals.
- <b>Chaos or Disruption:</b> Attackers motivated simply by causing destruction or instability.
- <b>War</b>: Cyberattacks conducted as part of military or geopolitical conflicts.

### Types of Threat Actors 

<b>Nation-State</b>
- Threat actors sponsored or supported by governments.
- Extremely sophisticated and well-funded.
- Capable of targeting:
    - Financial systems
    - Utilities
    - Critical infrastructure
    - Military systems

<b>Unskilled Attackers</b>
- Often called:
    - Script kiddies
    - Usually rely on prebuilt tools and publicly available exploits.
    - Limited technical understanding.

<b>Hacktivists</b>
- Attackers motivated by political or social causes.
- Often attempt to spread messages or disrupt organizations they oppose.

<b>Insider Threats</b>
- Threats originating from within an organization.
- May involve:
    - Employees
    - Contractors
    - Business partners
- Dangerous because insiders may already have legitimate access.

<b>Organized Crime</b>
- Professional criminal groups conducting cybercrime for profit.
- May perform:
    - Ransomware attacks
    - Fraud
    - Data theft
    - Extortion

<b>Shadow IT</b>
- Unauthorized technology or services used within an organization without IT approval.
- Examples:
    - Unauthorized SaaS applications
    - Personal cloud storage
    - Unapproved devices
- Can create:
    - Compliance risks
    - Data exposure
    - Security blind spots
<hr>

## 2.1 - Threat Vectors and Attack Surfaces 

A <b>threat vector</b> is the path or method an attacker uses to gain access to a system.

An <b>attack surface</b> refers to all possible entry points attackers could exploit.

### Message-Based Threat Vectors

<b>Email</b>
- One of the most common attack vectors.
- Often used for:
    - Phishing
    - Malware delivery
    - Credential theft

<b>SMS (Short Message Service)</b>
- Used in <b>smishing</b> attacks.
- Attackers send malicious links through text messages.

<b>Instant Messaging (IM)</b>
- Messaging platforms (such as Whatsapp) may be used to deliver malicious links or malware.

### Other Types 

<b>Image-Based Threat Vectors</b>
- Malicious code or hidden data may be embedded inside images.
- Often associated with:
    - <b>Steganography</b>  
    - Malicious SVG/XML files

<b>File-Based Threat Vectors</b>
- Malware delivered through downloadable files.
- Common file types:
    - ZIP files
    - Executables
    - Office documents with macros

<b>Voice Call Threat Vectors</b>
- <b>Vishing</b>
    - Voice phishing conducted over phone calls.
    - Attackers impersonate trusted individuals or organizations.

<b>Removable Device Threat Vectors</b>
- Devices such as USB drives may contain malware.
- Attackers may intentionally leave infected USB drives in public locations.

<b>Vulnerable Software</b>
- Unpatched or insecure software can be exploited.
- `Client-Based`: The vulnerable software runs on the user’s device, such as a browser, email client, PDF reader, or installed application.
- `Agentless`: The system is accessed or managed without installing a local agent, often through network-based scanning, APIs, or remote connections.
- Vulnerabilities may allow:
    - Remote code execution
    - Privilege escalation
    - Data theft

<b>Unsupported Systems and Applications</b>
- Older systems may no longer receive security updates.
- Creates major security risks due to unpatched vulnerabilities.

<b>Wireless Networks</b>
- Weak wireless security can allow unauthorized access.
- Modern networks should use:
    - <b>WPA2</b>
    - <b>WPA3</b>

<b>Wired Networks</b>
- Wired environments should use security controls like:
    - <b>802.1X authentication</b>   

<b>Bluetooth</b>
- Bluetooth can introduce risks such as unauthorized pairing or data interception.

<b>Open Service Ports</b>
- Open ports expose services to the network.
- Attackers scan for open ports to identify running services and vulnerabilities.

<b>Default Credentials</b>
- Many devices ship with default usernames and passwords.
- Attackers frequently attempt these credentials first.

<b>Supply Chain Attacks</b>

- A <b>supply chain attack</b> targets trusted vendors, suppliers, or service providers.

    <b>Managed Service Providers (MSPs)</b>
    - MSPs provide outsourced IT services.
    - Compromising an MSP can provide access to multiple customers.

    <b>Vendors</b>
    - Software or hardware vendors may unintentionally distribute compromised products.

    <b>Suppliers</b>
    - Suppliers may introduce risks through compromised materials or systems.

### Social Engineering Threats 

- <b>Phishing:</b> Fraudulent attempts to steal information by pretending to be a trusted entity.
- <b>Business Email Compromise (BEC):</b> Attackers impersonate executives or trusted contacts to manipulate victims into sending money or sensitive information.
- <b>Typosquatting:</b> Registering fake domains that closely resemble legitimate websites to trick users.
- <b>Pretexting:</b> Creating a fabricated story or scenario to manipulate victims into revealing sensitive information.
- <b>Smishing:</b> Phishing attacks conducted through SMS text messages.
<b>Impersonation:</b> Pretending to be another person or organization in order to gain trust.
- <b>Brand Impersonation:</b> Attackers pretending to represent well-known companies or brands.
- <b>Watering Hole Attacks:</b> Compromising websites frequently visited by targeted victims in order to infect them with malware.
- <b>Misinformation and Disinformation:</b> Intentionally spreading false or misleading information to manipulate people or create confusion.
<hr>

## 2.3 - Types of Vulnerabilities 

### Memory Injection 

- Attackers inject malicious code into a running process’s memory space.
- Often used to bypass security protections or avoid detection.

### Buffer Overflow

- A <b>buffer overflow</b> occurs when more data is written into memory than the allocated buffer can handle.
- Can overwrite adjacent memory locations.
- May allow:   
    - Arbitrary code execution
    - Privilege escalation
    - Application crashes

### Race Conditions 

- A <b>race condition</b> occurs when multiple processes access shared resources simultaneously in unintended ways.

    | <b>TOC (Time of Check)</b> | <b>TOU (Time of Use)</b> |
    | -------------------------- | ----------------------- |
    |The system checks a condition or permission | The system later uses the resource or performs the action. Attackers may exploit the gap between TOC and TOU.

### Malicious Updates 

- Attackers distribute malware disguised as legitimate software updates.
- Systems should only install updates from trusted sources.

### Operating System (OS) - based

- Operating systems contain millions of lines of code and may contain vulnerabilities.
- Regular patching and updates are critical.

### SQL Injection (SQLi)

- A <b>SQL injection</b> attack occurs when malicious SQL code is inserted into application input fields.
- Example payload = `' OR '1'='1`
- Potential impacts:
    - Unauthorized database access
    - Data leakage
    - Authentication bypass

### Cross-Site Scripting (XSS)

- A <b>Cross-Site Scripting (XSS)</b> attack injects malicious JavaScript into web applications.

|<b>Non-Persistent XSS</b> | <b>Persistent XSS</b> |
| ----------------------- | --------------------- |
|Malicious script is reflected temporarily | Malicious script is permanently stored on the server or application. | 

### Hardware Vulnerabilities 

- <b>Firmware Vulnerabilities:</b> Weaknesses within firmware software embedded into hardware devices such as routers, switches, or IoT devices. Firmware updates are usually provided only by the vendor.
- <b>End-of-Life (EOL):</b> A product is no longer sold but may still receive limited updates or support.
- <b>End-of-Service-Life (EOSL):</b> A product no longer receives patches, updates, or vendor support, increasing security risks significantly.
- <b>Legacy Systems:</b> Older systems or applications that remain in use despite outdated security protections and unsupported software.

### Virtualization Vulnerabilities 
- <b>VM Escape:</b> An attacker breaks out of a virtual machine and gains access to the host operating system or other VMs.
- <b>Resource Reuse:</b> Risks caused by shared or overcommitted resources between virtual machines and cloud systems.

### Cloud-Specific Vulnerabilities 
- <b>Cloud Misconfigurations:</b> Improperly configured cloud resources that expose systems or data publicly.
- <b>Weak Authentication:</b> Poor access controls or lack of MFA on cloud applications and services.
- <b>Unpatched Cloud Applications:</b> Vulnerable cloud-hosted applications that attackers may exploit remotely.

### Supply Chain Vulnerabilities 

- <b>Service Provider Risks:</b> Third-party providers may become compromised and expose connected organizations.
- <b>Hardware Provider Risks:</b> Compromised hardware or firmware may introduce malicious functionality into systems.
- <b>Software Provider Risks:</b> Malicious or compromised software updates may distribute malware to customers.

### Misconfiguration Vulnerabilities 

- <b>Weak Passwords:</b> Poor administrator credentials can allow brute-force attacks and unauthorized access.

- <b>Insecure Protocols:</b> Older protocols such as:

    - `Telnet`
    - `FTP`
    - `SMTP`

- <b>Default Credentials:</b> Devices using default usernames and passwords are highly vulnerable to attacks.
- <b>Open Ports:</b> Unnecessary open ports expose services and increase the attack surface.

### Mobile Device Vulnerabilities
- <b>Jailbreaking:</b> Removing manufacturer restrictions on iOS devices to gain deeper system access.
- <b>Rooting:</b> Gaining privileged access on Android devices.
- <b>Sideloading:</b> Installing applications from unofficial or untrusted sources outside the official app store.

### Cryptographic Vulnerabilities 
- <b>Weak Encryption Algorithms:</b> Older encryption methods such as <b>DES</b> are vulnerable due to short key lengths.
- <b>Poor Key Management:</b> Improper storage or handling of encryption keys can compromise encrypted data.
- <b>Zero-Day Vulnerabilities:</b> Newly discovered vulnerabilities with no available patch or fix at the time of discovery.
<hr>

## 2.4 Indicators of Malicious Activity 

### Malware Types 

- <b>Ransomware:</b> Malware that encrypts files or systems and demands payment for decryption.
- <b>Trojan:</b> Malware disguised as legitimate software that grants attackers unauthorized access.
- <b>Worm:</b> Self-replicating malware that spreads across networks automatically.
- <b>Spyware:</b> Malware that secretly monitors user activity and collects sensitive information.
- <b>Bloatware:</b> Unwanted preinstalled software that consumes resources and may introduce vulnerabilities.
- <b>Virus:</b> Malware that attaches itself to files or programs and spreads when executed.
- <b>Keylogger:</b> Malware that records keystrokes to capture usernames, passwords, and sensitive information.
- <b>Logic Bomb:</b> Malicious code triggered when specific conditions or events occur.
- <b>Rootkit:</b> Malware designed to provide attackers with hidden privileged access to a system.

### Physical Attacks 

- <b>Brute Force Attacks:</b> Repeatedly attempting passwords or authentication combinations until access is gained.
- <b>RFID Cloning:</b> Copying RFID badge information to impersonate authorized users.
- <b>Environmental Attacks:</b> Attacks targeting physical infrastructure such as:
    - HVAC systems
    - Power systems
    - Cooling systems

### Network Attacks

| <b>Denial-of-Service (DoS)</b>  | <b>Distributed Denial-of-Service (DDoS) </b> |
| ---------------------------- | ---------------------- |
| Overwhelming a service or system to make it unavailable. | Multiple systems  (`botnet`) attack a target simultaneously to exhaust resources.


| <b>Amplified DDoS</b> | <b>Reflected DDoS</b> |
| --------------------- | --------------------- |
| Attackers send small requests that generate much larger responses toward a victim. | Attackers spoof the victim’s IP address so third-party systems flood the victim with responses. |


<b>DNS Attacks:</b> Manipulating DNS responses to redirect victims to malicious destinations.

<b>Wireless Attacks:</b> Attacks against wireless communications such as deauthentication attacks or RF jamming.

<b>On-Path Attacks:</b> Attackers intercept and potentially modify communications between two parties.

<b>Credential Replay Attacks:</b> Captured credentials or session tokens are reused to gain unauthorized access.

### Application Attacks 

- <b>Injection Attacks:</b> Injecting malicious input such as SQL, XML, or scripts into applications.
- <b>Buffer Overflow Attacks:</b> Writing excess data into memory buffers to overwrite adjacent memory.
- <b>Replay Attacks:</b> Capturing and retransmitting legitimate communications or authentication data.
- <b>Privilege Escalation:</b> Exploiting vulnerabilities to gain higher-level permissions or administrative access.
- <b>Forgery Attacks:</b> Creating fake requests or transactions pretending to be legitimate users.
- <b>Directory Traversal:</b> Accessing unauthorized files or directories using manipulated file paths.

    | <b>Cross-Site Request Forgery (CSRF)</b> | <b>Server-Side Request Forgery (SSRF) |
    | --- | --- |
    |Tricking authenticated users into performing unwanted actions | Exploiting a server to send unintended requests to internal or external systems. |

### Cryptographic Attacks

- <b>Birthday Attacks:</b> Exploiting hash collision probabilities to find matching hashes.
- <b>Collision Attacks:</b> Attempting to generate two different inputs that produce the same hash value.
- <b>Downgrade Attacks:</b> Forcing systems to use older, weaker cryptographic protocols or algorithms.

### Password Attacks 

- <b>Password Spraying:</b> Attempting common passwords across many accounts to avoid lockouts.
- <b>Brute Force Password Attacks:</b> Trying many password combinations until the correct one is found.

### Indicators of Compromise (IoCs) 

- <b>Account Lockouts:</b> Multiple failed login attempts may indicate brute-force attacks.
- <b>Concurrent Session Usage:</b> The same account appearing active from multiple locations simultaneously.
- <b>Blocked Content:</b> Security systems repeatedly blocking suspicious files or traffic.
- <b>Impossible Travel:</b> Logins appearing from geographically impossible locations within short timeframes.
- <b>Resource Consumption:</b> Unusually high CPU, RAM, disk, or network usage.
- <b>Resource Inaccessibility:</b> Systems, files, or services suddenly becoming unavailable.
- <b>Out-of-Cycle Logging:</b> Logins or activity occurring outside normal business hours.
- <b>Published or Documented Data:</b> Sensitive internal information appearing publicly online.
- <b>Missing Logs:</b> Deleted or missing logs potentially indicating attacker tampering.
<hr>

## 2.5 - Mitigation Techniques 

### Segmentation and Access Control

- <b>Network Segmentation:</b> Separating networks or systems into smaller isolated sections to limit attacker movement.
- <b>Access Control Lists (ACLs):</b> Rules that permit or deny traffic based on IP addresses, ports, or protocols.
- <b>Application Allow Lists:</b> Only approved applications are permitted to run.
- <b>Deny Lists:</b> Explicitly blocking known malicious or unauthorized applications.

### Mitigation Techniques

- <b>Patching:</b> Applying updates and security fixes to remove vulnerabilities.
- <b>Isolation:</b> Separating systems, applications, or processes to prevent spread or interaction.
- <b>Encryption:</b> Protecting data confidentiality both at rest and in transit.
- <b>Monitoring:</b> Continuously analyzing systems, logs, and activity for threats or anomalies.
- <b>Least Privilege:</b> Granting users only the minimum permissions required for their tasks.
- <b>Configuration Enforcement:</b> Ensuring systems follow approved security configurations and baselines.
- <b>Decommissioning:</b> Securely retiring systems and removing sensitive data before disposal.

### Hardening Techniques  

- <b>Endpoint Protection:</b> Installing antivirus, EDR, firewalls, and security controls on devices.
- <b>Host-Based Firewalls:</b> Software firewalls installed directly on endpoints to control inbound and outbound traffic.
- <b>Host-Based Intrusion Prevention Systems (`HIPS`):</b> Detecting and blocking suspicious activity directly on a host.
- <b>Disabling Ports and Protocols:</b> Turning off unnecessary services and ports to reduce attack surfaces.
- <b>Default Password Changes:</b> Replacing vendor default credentials with strong unique passwords.
- <b>Removal of Unnecessary Software:</b> Uninstalling unused applications and services that may introduce vulnerabilities.