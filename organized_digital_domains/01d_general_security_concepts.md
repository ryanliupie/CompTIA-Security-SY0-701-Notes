# General Security Concepts 

## 1.1 - Security Controls 

<b>1. Technical Controls</b> → also known as logical controls, are mechanisms that rely on technology (hardware or software) to protect systems, data and networks. For example, we can have firewalls, IDS/IPS, encryption, antivirus software etc..

<b>2. Managerial Controls</b> → also known as administrative controls, focus on policies, procedures, and planning activities that govern an organizations security practices. This includes explaining to people the best way to secure these things and know how to interpret a potential attack

<b>3. Operational controls</b> → refer to securing a system on a day-to-day basis which are often hands on activities. This can include incident response, backups of data, monitoring, security guards

<b>4. Physical controls</b> → focus on securing the physical aspects of an organizations IT infrastructure. It includes protecting hardware, facilities and people from physical threats we can use badge readers access control vestibule/mantrap.

### Several Control Types 

- <b>Preventive</b> refers to blocking access to a resource. This can include firewall rules, security policy, guard shack, door locks.

- <b>Deterrent</b> discourages a person from doing something. Making that attacker think twice even though they can still commit the action as it does not directly prevent access. For instance warning sign like at Grimsby beach front reception desks, threat of dismissal.

- <b>Detective</b> identifies and logs an intrusion attempt and may not prevent access. For example, the action of collecting and reviewing system logs, motion detectors like a PIR, regularly patrolling the area, IDS.

- <b>Corrective</b> designed to fix security incidents after they have happened, to try and restore system functionality and limit damages. This can include getting rid of malware, creating processes for reporting security issues, contacting law enforcement to get rid of criminals, using a fire extinguisher.

- <b>Compensating</b> is simply a temporary fix as it is not sufficient enough to be a complete overall fix. Includes having a generator to use after a power outage, an application having a security vulnerability so using a firewall so no one can exploit it, implement a separation of duties, using many security guards.

- <b>Directive</b> set out expectations and provide guidance on how to act in specific situations. We can do this by storing sensitive files in a protected folder, creating compliance policies and procedures, training users on security policies, using an “authorized personnel only” sign.
<hr>

## 1.2 - Security Controls 

### The CIA Triad

The CIA Triad are the fundamentals of IT security, which include three components:

1. <b>Confidentiality:</b> refers to preventing specific information from falling into the hands of unauthorized users or systems. We can achieve this by: 

    - Encryption (encoding messages so only select people can see them)
    - Restricting access to resources (e.g., private files)
    - Implementing multi-factor authentication (2FA)

2. <b>Integrity:</b> refers to data being 100% accurate and ensuring no modifications have been made to that data. Methods to ensure integrity include:

    - <b>Hashing:</b> The sender sends a hash (a special code) with the data. The receiver checks if their computed hash matches to determine if the data has been tampered with.
    - <b>Digital Signatures:</b> Used to verify that a document was sent by a specific sender and has not been changed.
    - <b>Certificates:</b> Act like ID cards for websites or people. They prove authenticity and are issued by a Certificate Authority (CA).

3. <b>Availability:</b> refers to having access to information and resources at any given moment. Key concepts include:

    - <b>Redundancy:</b> Systems are always available through backups.
    - <b>Fault Tolerance:</b> Systems continue running even if a failure occurs.

### Non-Repudiation

<b>Non-repudiation</b> is a security concept that ensures someone cannot deny their actions (e.g., sending a message, making a purchase, or signing a document). It provides <b>accountability</b> by making actions traceable back to the individual who performed them. Non-repudiation is a form of <b>"proof of integrity"</b>.

We can use a <b>hash</b> with data so that:

If the data changes → the hash changes. 
However, a hash alone does <b>not identify who changed the data</b>. 

For example: 

    Original Hash → 17ACBD80eff3
    Modified Hash → 3D4efvb4385

If the hashes are different, it means someone changed a character in the file. A hash proves that data <b>was or was not modified</b>. It does <b>NOT prove identity</b>. 

To fully achieve non-repudiation, we use tools that provide <b>proof of origin</b>. 
- <b>Digital Signatures</b> prove who sent the message.
- <b>Certificates</b> verify identity and are issued by a Certificate Authority (CA).

### Authentication, Authorization, Accounting (AAA)

1. <b>Authentication:</b> 

    The process of verifying <b>who someone is</b>. This is the first step before access is granted. Examples include logging in with a username and password or using multi-factor authentication (2FA). This answers: <b>"Are you really who you claim to be?"</b>. 

2. <b>Authorization:</b> 

    Determines <b>what a user is allowed to do</b> after they are authenticated. Examples include access to files or permissions such as read, write, and execute. This answers: <b>"What can you do?"</b>. This follows the concept of <b>least privilege</b>, where users are only given the minimum level of access required to perform their tasks.

    There are two main ideas regarding authentication:

    - `Authenticating People` → This involves verifying the identity of a user before granting access to a system.

        In a typical network setup, a user connects through the internet and may pass through components like a firewall or VPN concentrator before reaching an internal file server. A <b>firewall</b> does not have knowledge of authentication factors like usernames or passwords. Because of this, authentication is handled by a separate system such as an <b>AAA server</b>. The AAA server communicates with the system (e.g., file server) to determine whether the user should be granted access.

    - `Authentication of Systems` → This refers to verifying whether a device is allowed to be on a network. Since devices cannot always be physically verified, systems use digital methods to confirm identity.

        One common method is using a <b>digitally signed certificate</b> installed on the device. During the connection process, the certificate is checked to confirm authenticity. These certificates are issued by a <b>Certificate Authority (CA)</b>, which is a trusted organization. Because the certificate is signed by the CA, it can be traced back and verified, ensuring the device is legitimate.

3. <b>Accounting:</b> 

    Tracks and logs <b>what a user does</b> within a system. Examples include login logs, file access history, and audit trails. This answers: <b>"What did you do?"</b>. 

### Gap Analysis

<b>Gap Analysis</b> is the process of comparing where you are now versus where you want to be. It often involves research over weeks or months to gather data and determine which security measures will be needed in the future. The goal is to identify what gaps exist and how to address them.

<b>Frameworks & Standards</b>

To perform a gap analysis, organizations compare their current state against established frameworks or sets of questions. Common examples include:

- NIST Special Publication 800-171 Revision 2
- ISO/IEC 27001
- Custom frameworks tailored to the organization 

To systematically identify and address gaps, the process is divided into the following stages:

1. <b>Evaluate People and Processes</b>
    - Assess employee experience and expertise
    - Review current training programs
    - Evaluate knowledge of security policies and procedures
2. <b>Compare Against Controls</b>
    - Evaluate existing systems
    - Identify weaknesses
    - Examine broad security categories and break them down into smaller components
        - <b>Example: Account Management</b>
            
            1. Registration/de-registration
            2. User access provisioning 
            3. Review of user access rights 
3. <b>Analysis and Reporting</b>
    - Define baseline (desired state vs current state)
    - Identify the path to improvement (time, money, and achievable controls)
    - Produce a Gap Analysis Report (formal documentation of findings and recommendations)

### Zero Trust

In networking, <b>Zero Trust</b> is a security concept based on the principle <i>never trust, always verify</i>. 

Instead of assuming users or devices inside a network are safe, every access request must be continuously validated. This is similar to, but more strict than, traditional models like SSO, often requiring multi-factor authentication (MFA) and strict policy enforcement.

Zero architecture is typically divided into two main components: 

1. <b>Control Plane:</b> This is responsible for making policy decisions. It determines:
    - How traffic should be handled (e.g., routing, NAT, packet forwarding)
    - Whether a user or service should be granted access
    - What criteria must be met before access is allowed

    The core concepts in the control plane are:

    - <b>Adaptive Identity</b> (Access decisions are dynamically adjusted based on user behaviour)
        - If a user behaves outside normal patterns, additional verification may be required
        - Example: logging in from a new location triggers MFA 

    - <b>Threat Scope Reduction</b> (Limits how much of the system a user can access)
        - Users only get access to what is necessary (`least privilege`)
        - Reduces the impact of a potential breach
        - Example: restricting access to a small network segment instead of the entire system
    
    - <b>Policy-Driven Access Control</b> (Policies define how access decisions are made)
        - Evaluates requests against policies
        - Grants or denies access in real time
    
    - <b>Policy Administrator</b> (Executes decisions made by the policy engine)
        - Evaluates requests against policies
        - Grants or denies access in real time
    
    - <b>Policy Engine</b> (Responsible for making access decisions)
        - Evaluates identity, device, behavior, and context  
        - Determines whether to allow, deny, or require additional verification  
        - Continuously monitors for changes in behaviour  
        - Triggers re-evaluation of access when anomalies are detected 
    
2. <b>Data Plane</b>: It is responsible for processing and handling network traffic, including packets and network data. This includes functions such as packet forwarding, traffic inspection, encryption, and Network Address Translation (NAT). 

    The Data Plane operates under the direction of the Control Plane, which defines the policies and rules. While the Control Plane makes decisions about whether traffic should be allowed or denied, the Data Plane enforces those decisions by allowing or blocking data flows between users and resources. Some key concepts of the Data plane include: 

    1. <b>Removal of Implicit Trust Zones</b> → Traditional networks relied on “trusted zones” (internal vs external).

        - Internal networks were trusted 
        - External networks were not trusted

        `Zero Trust eliminates this model:`
        - Trust is not based on location 
        - Every request must be verified individually
    
    2. <b>Subjects and Systems</b>
        - <b>Subject</b> → User, device, or service requesting access
        - <b>System/Resource</b> → What the subject is trying to access
    
        Key idea: 
        - Subjects may have changing identities (behavior, location, device)
        - Systems are the resources being protected
    
    3. <b>Policy Enforcement Point (PEP)</b> → The PEP acts as a gatekeeper between subjects and resources 
        - It enforces decisions made by the control plane
        - Does NOT make decisions itself
        - Only allows access if policies are satisfied

        Analogy: 
        
        Think of the PEP like a bouncer at a club.
        The manager (policy engine) sets the rules, and the bouncer checks if you meet them before letting you in.
    
### Physical Security
Physical security is very important for day-to-day operations and there are different types including:

- <b>Bollards:</b> are meant to prevent unauthorized vehicle access while still allowing people to walk through. For example, you may see these poles at the front of supermarkets, storefronts, or driveways. Some locations use retractable metal bollards that go up and down to control vehicle access and help prevent vehicle theft or vehicle ramming attacks.

- <b>Access control vestibules (mantraps)</b>: are small access rooms used to control entry into secure areas. Once you enter through the first door using a PIN, ID badge, biometrics, etc., the first door closes before the second door opens. This helps prevent tailgating and piggybacking by ensuring only one person enters at a time.

- <b>Fencing:</b> is very common to prevent unauthorized access to an area such as a house, yard, or restricted facility.

- <b>Video surveillance:</b> means using CCTV (Closed-Circuit Television) cameras to monitor areas and support or replace physical guards. Cameras can detect motion, monitor suspicious activity, and trigger alarms when people enter unauthorized areas.

- <b>Security Guards:</b> provide physical protection and monitoring in an area such as a university or other buildings and facilities.

- <b>Access badges:</b> are authorized identification badges required to enter certain areas for additional security and identity verification.

- <b>Lighting:</b> improves visibility and security since dark areas make it easier for intruders to hide or move around unnoticed. Proper lighting also helps cameras capture clearer facial details and activities.

### Deception and Disruption

There are different security techniques used to create deception and disruptions:

- <b>Honeypots:</b> attract attackers and trap them in a controlled environment so security teams can analyze the techniques being used against them. Attackers may use automated systems, vulnerability scanners, or scripts, while defenders try to make the honeypot appear realistic enough that attackers believe it is real.

- <b>Honeynets:</b> are entire networks of honeypots designed to make the environment even more believable. A honeypot could simulate a server, router, firewall, VPN concentrator, load balancer, or other systems. Multiple honeypots make it harder for attackers to determine what is real or fake.

- <b>Honeyfiles:</b> are files containing fake but seemingly sensitive information designed to attract attackers. For example, creating a file named `passwords.txt`.

- <b>Honeytokens:</b> are pieces of fake data or information placed within databases, documents, email accounts, or other data repositories to detect unauthorized access. For example, fake login credentials or fake API keys may be planted to monitor who attempts to use them.
<hr>

## 1.3 - Change Management

In a corporate environment, making a change such as updating software, patching an application, modifying switch or router configurations, or reconfiguring firewalls and rules can affect many other systems.

By having an <b>approval process</b>, we can avoid downtime, confusion, and mistakes.
- Complete the request form
- Determine the purpose of the change
- Identify the scope of the change
- Schedule a date and time for the change
- Determine affected systems and the impact
- Analyze the risks associated with the change
- Get approval from the Change Control Board (CCB)
- Get end-user acceptance once the change is complete

We also identify the risk level (high, medium, low). There is risk if the change is not made (security vulnerabilities, application unavailability) and also risk if the change is made incorrectly, which is why <b>impact analysis</b> is important.

This process starts with determining <b>ownership</b> of the application or system. If a change needs to be made, the owner or administrator responsible for the affected system performs or coordinates the change. For example, if software used by the shipping and receiving department needs to be upgraded, the shipping department may own the process while the IT department performs the technical implementation.

The <b>stakeholders</b> would also be affected by this change, so before implementing it we must review how the change impacts different departments. For example, upgrading shipping software may impact shipping/receiving, accounting, product delivery timelines, customers, and finance.

Before implementing the change in a production environment, we need to <b>test it first</b>. Tests should be done in a development or staging environment to ensure the change works correctly before being moved into production. We should also document rollback or backup plans in case the change causes issues.

The most difficult part of the process is usually the <b>maintenance window</b>. During this time, systems may become unavailable while updates or fixes are applied. Organizations often schedule maintenance during low-usage hours such as late nights or weekends because outages during business hours may affect operations heavily.

A <b>Standard Operating Procedure (SOP)</b> is a document that explains the entire process step-by-step so changes can be completed consistently and correctly. SOPs are updated over time to improve efficiency and reduce mistakes.

### Technical Change Management

We are now looking at the change control process from the technical point of view.

A technician may need to change firewall rules, IDS/IPS signatures, or configurations related to applications and infrastructure. These modifications can introduce vulnerabilities or unintended issues that may affect other systems if not managed properly.

- <b>Restricted activities</b> → are used to limit what a person can change. A technician should only modify the components they are authorized to work on. Even if they have broader permissions, only approved changes should be performed during the maintenance window. This follows the principle of least privilege and helps reduce mistakes.

- <b>Downtime</b> → refers to the maintenance window where services may become partially or completely unavailable while changes are being implemented. Some downtime is planned and expected, but unplanned downtime may occur from unexpected outages or failed changes.

A common thing to do after a change is to perform a <b>service restart</b>. Some services or applications require restarting before new configurations or updates take effect.

On the other hand, an <b>application restart</b> may cause the entire application to go offline. For example, restarting the whole e-commerce platform could make the website inaccessible, preventing browsing, payments, and cart usage.

<b>Legacy applications</b> may have been running for many years and may no longer receive updates or vendor support. Changes involving legacy systems must be planned carefully because modifications could break compatibility or affect other connected systems.

Sometimes before changing System A, you may also need to update System B first. These are called <b>dependencies</b>. Dependencies may not always exist on the same system. For example, upgrading financial management software may require updating database schemas or libraries beforehand.

When managing many changes, <b>documentation</b> becomes very important. Every change should be tracked no matter how small. Examples include:

- <b>Updating diagrams</b> such as modifications to network diagrams 
- <b>Updating policies/procedures</b> such as new systems requiring new policies/procedures

We can also review how code changes over time using systems like GitHub. This is a form of <b>version control</b>, allowing administrators and developers to track revisions, compare versions, and restore previous configurations if necessary. Some devices or operating systems may not include built-in version control features, so additional software may be required. 
<hr>

## 1.4 - Cryptographic Solutions

### Public Key Infrastructure 

<b>Public Key Infrastructure (PKI)</b> is a broad term in cryptography that mainly refers to the use of policies, procedures, hardware, software, and people for creating, distributing, managing, storing, and revoking <b>digital certificates</b>.

PKI is used to associate digital certificates with people, users, organizations, or devices in conjunction with a <b>Certificate Authority (CA)</b>.

A <b>Certificate Authority (CA)</b> is a trusted entity responsible for issuing and validating digital certificates.

### Symmetric Encryption

<b>Symmetric encryption</b> uses the same key for both encryption and decryption. Whenever you are decrypting information, you use the same key that was originally used to encrypt the data.

- It uses a single shared key
- The key must be securely distributed between parties
- It is generally a very fast encryption method

Examples include:
- AES
- DES
- ChaCha20

### Asymmetric Encryption

<b>Asymmetric encryption</b> uses two different keys:

- A <b>public key</b>
- A <b>private key</b>

These keys are mathematically related and are generated together.

- The <b>public key</b> is openly shared and available to anyone
- The <b>private key</b> is confidential and only known to the owner

The public key is used to encrypt messages or data, while the private key is used to decrypt the encrypted information. This allows secure communication without needing to share the private key publicly.

Examples include:
- RSA
- ECC (Elliptic Curve Cryptography)

### Public and Private Key Analogy

Think of it like giving someone an open padlock.

- Anyone can place the lock onto the locker and lock it using the <b>public key</b>
- However, only the owner with the correct <b>private key</b> can unlock and open it

This demonstrates how anyone can encrypt data, but only the intended owner can decrypt it.

A public key may look like a long randomized string of characters such as:

    MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8A...

### Key Escrow

<b>Key escrow</b> refers to storing a copy of a private encryption key with a trusted third party known as an <b>escrow agent</b>.

For example:

- A user creates a public and private key pair
- The user encrypts data normally using the public key
- If the private key is lost, the escrow agent may provide the stored backup copy for recovery purposes

This helps prevent permanent data loss if encryption keys are lost.

### Encryption Data

- <b>Full-disk encryption</b> secures the entire storage device, including all partitions and system files.

- <b>Partition encryption</b> secures only a selected partition of a disk.
Examples include <b>BitLocker</b> (Windows), <b>FileVault</b> (macOS), and - <b>LUKS</b> (Linux).

- <b>File encryption</b> protects individual files instead of the whole disk.
Windows can use <b>EFS (Encrypting File System)</b> for file-level encryption.

- <b>Database encryption</b> protects stored database data and the transmission of that data.
Database encryption may encrypt entire tables, columns, or specific records.

- <b>Record encryption</b> occurs when only certain rows or records in a database are encrypted while other data may remain plaintext.

- <b>Transport encryption</b> protects data while it travels across networks.
<b>HTTPS</b> uses <b>TLS</b> over port <b>443</b> to encrypt web traffic.
Organizations may also use <b>VPNs</b> for encrypted communication tunnels.
Common VPN technologies include <b>SSL/TLS VPN</b> and <b>IPSec VPN</b>.

### Encryption Algorithms

| Feature | <b>DES (Digital Encryption Standard)</b> | <b>AES (Advanced Encryption Standard)</b> |
|---|---|---|
| Type | <b>Symmetric encryption</b> algorithm | Modern <b>symmetric encryption</b> algorithm |
| Key Length | <b>56-bit</b> key | <b>128-bit</b>, <b>192-bit</b>, or <b>256-bit</b> keys |
| Block Size | <b>64-bit block cipher</b> | <b>128-bit block size</b> |
| Security | Vulnerable to <b>brute-force attacks</b> due to short key length | Significantly stronger security |
| Performance | Slower and outdated | Faster and more efficient |
| Usage | Considered insecure today | Commonly used with <b>WPA2/WPA3</b> wireless security |
| Recommendation | Not recommended for modern systems | Preferred modern encryption standard |

<b>Key Stretching</b>

- <b>Key stretching</b> increases the work required to crack passwords or hashes.
This can involve repeatedly hashing data many times.
Makes brute-force attacks significantly slower and more difficult.

### Key Exchange 

- <b>Key exchange</b> securely establishes encryption keys between two parties.
Public transmission of symmetric keys is insecure because attackers could intercept them.
- <b>Asymmetric cryptography</b> helps securely exchange symmetric keys.
    - Each user has a <b>public key</b> and a <b>private key</b>.
    - The <b>public key</b> can be shared openly.
    - The <b>private key</b> must remain secret.
    - Asymmetric encryption is commonly used to establish a secure <b>symmetric session key</b>.
- Symmetric encryption is then used for actual communication because it is faster.

### Encryption Technologies 

<b>Trusted Platform Module (TPM)</b>
- A <b>TPM</b> is a hardware chip that performs cryptographic operations.
- Commonly used for <b>full-disk encryption</b> and secure key storage.
- Can securely store system certificates and encryption keys.
Helps verify system integrity during boot processes.

<b>Hardware Security Module (HSM)</b>
- An <b>HSM</b> is dedicated hardware for managing cryptographic operations.
- Used heavily in enterprise environments and data centers.
- Can perform encryption, decryption, and digital signing.
- Often designed with redundancy and fault tolerance.

<b>Key Management System (KMS)</b>
- A centralized system used to manage cryptographic keys.
- Functions include:
    - Creating keys
    - Rotating keys
    - Associating keys with services or users
    - Logging key usage events

<b>Secure Enclave</b>
- An isolated secure region within a processor.
- Stores highly sensitive information securely.
- Often protects biometric data, encryption keys, and authentication data.

### Obfuscation

- <b>Obfuscation</b> hides information to make it more difficult to understand or interpret.

<b>Steganography</b>
- Hides secret information inside another medium.
- Examples:
    - Images
    - Audio files
    - Videos
    - Network packets

<b>Tokenization</b>
- Replaces sensitive data with non-sensitive placeholder values called <b>tokens</b>.
- Commonly used for:
    - Credit card numbers
    - Payment systems
    - Personal information
- Tokens are not mathematically related to the original value.

<b>Data Masking</b>
- Hides parts of sensitive information.
- Example:
    - Showing only the last 4 digits of a credit card number.
    - Commonly used on receipts and customer-facing systems.

### Hashing and Digital Signatures

<b>Hashing</b>

- <b>Hashing</b> provides:
    - Data integrity
    - Authentication support
    - Hashing converts input data into a fixed-length output.
    - Hashing is a <b>one-way function</b>, meaning it cannot realistically be reversed.

<b>SHA-256</b>
- A common modern hashing algorithm.
- Produces a <b>256-bit hash</b>.
- Represented as <b>64 hexadecimal characters</b>.

<b>Hash Collisions</b>
- A <b>collision</b> occurs when two different inputs generate the same hash value.
Older algorithms such as <b>MD5</b> are vulnerable to collisions and are no longer considered secure.

<b>Password Storage</b>
- Passwords should be stored as <b>salted hashes</b>, not plaintext.

<b>Salting</b>
- <b>Salting</b> adds random data before hashing.
- Prevents attackers from using:
    - Rainbow tables
    - Precomputed hash databases
    - Even identical passwords generate different hashes when unique salts are used.

<b>Digital Signatures</b>
- Provide:
    - Integrity
    - Authentication
    - Non-repudiation
    - Verify that data was not altered during transmission.
    - Created using a sender’s <b>private key</b>.
    - Verified using the sender’s <b>public key</b>.

### Blockchain Technology

- A <b>blockchain</b> is a distributed ledger shared across multiple systems.
- Each participant maintains a copy of the blockchain.
- Blocks are connected using cryptographic hashes.
- If a block changes, the hash changes, alerting the network.

<b>Blockchain Uses</b>
- Payment processing
- Digital identity systems
- Supply chain monitoring
- Digital voting

<b>Open Public Ledger</b>
- A blockchain acts as an <b>open public ledger</b> where transactions are distributed across many systems.

### Certificates and PKI

<b>Certificates</b>
- A digital certificate binds a <b>public key</b> to an identity.

<b>Certificate Authority (CA)</b>
- A trusted third party that validates and signs certificates.
Browsers trust certificates signed by trusted CAs.

<b>Public Key Infrastructure (PKI)</b>
- Framework that manages:
    - Public keys
    - Private keys
    - Certificates
    - Trust relationships

<b>Certificate Signing Request (CSR)</b>
- A request sent to a CA asking for a certificate to be signed.

<b>Self-Signed Certificates</b>
- Certificates signed by the creator instead of a trusted CA.
- Commonly used internally or for testing.
- Browsers usually display security warnings for self-signed certificates.

<b>Wildcard Certificates</b>
- Secure multiple subdomains under one domain.
- `*.example.com` can secure:
    - `mail.example.com`
    - `shop.example.com`
    - `login.example.com`

<b>Certificate Revocation List (CRL)</b>
- A list of revoked certificates maintained by a CA.
- Reasons for revocation may include:
    - Compromised private keys
    - Incorrect certificate issuance
    - Policy violations

<b>Online Certificate Status Protocol (OCSP)</b>
- Allows systems to check certificate validity in real time.

<b>Root of Trust</b>
- Foundational trusted hardware or software components used to establish system security.