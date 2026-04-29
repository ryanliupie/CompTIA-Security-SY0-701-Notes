# General Security Concepts 

## 1.1 Security Controls 

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

## 1.2 Security Controls 

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
    