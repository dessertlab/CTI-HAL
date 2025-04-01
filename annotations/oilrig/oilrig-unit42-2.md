## Detailed comments

 * Page #2:
   > Stolen credentials

   ID: 001

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTAIL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: This involves extracting account login information from operating systems and software, such as username-password pairs, hashes, or other forms of authentication credentials.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Deployed webshell URLs

   ID: 002

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: WEB SHELL (T1505.003)

   DESCRIPTION: This involves installing a web shell on a compromised web server to gain persistent access to the server. 

   TOOLS: -

   NOTE: -

 * Page #2:
   > Backdoor tools

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Backdoors are tools that allow attackers to gain unauthorized access to systems, often bypassing security controls.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The credentials appear to have been stolen via multiple techniques, including using post-exploition password recovery tools such as MimiKatz or its variant ZhuMimiKatz

   ID: 004

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: The act of extracting credentials from a compromised system.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #5:
   > we believe OilRig attackers obtained credentials through, bruteforcing, SQL injections, and using traditional credential harvesting toolkits

   ID: 030

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: BRUTE FORCE (T1110)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use brute force techniques to gain access to accounts when passwords are unknown or when password hashes are obtained.

   TOOLS: -

   NOTE: -

   ---

   ID: 031

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATIONS (T1190)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to exploit a weakness in an Internet-facing host or system to initially access a network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > we had internally postulated the OilRig group likely had a propensity to immediately attempt to escalate privileges once they have their initial compromise

   ID: 032

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: EXPLOITATION FOR PRIVILEGE ESCALATION (T1068)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit software vulnerabilities in an attempt to elevate privileges.

   TOOLS: -

   NOTE: -

 * Page #5:
   > then try to move laterally into the local Microsoft Exchange server where they would then able to harvest more credentials

   ID: 005

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Once on the Exchange server, OilRig extracts credentials, which can be used to further compromise additional systems within the network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > implant additional tools such as webshells

   ID: 006

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: WEB SHELL (T1505.003)

   DESCRIPTION: To maintain persistence, OilRig deploys web shells on compromised servers. Web shells allow remote access and command execution, facilitating ongoing control over the compromised server.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Ruler is an open-source penetration testing toolkit which is predicated on being able to access Outlook Web Access (OWA) or OWA via stolen credentials,

   ID: 007

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: EMAIL COLLECTION (T1114)

   SUB-TECHNIQUE: REMOTE EMAIL COLLECTION (T1114.002)

   DESCRIPTION: Ruler is an open-source tool used by OilRig to exploit OWA by setting malicious rules, retrieving the Global Address List, and executing code remotely. This tool leverages the built-in functionalities of Microsoft Exchange to maintain stealth and efficiency in their operations.

   TOOLS: -

   NOTE: -

 * Page #5:
   > performing remote code execution

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Ruler, OilRig can execute arbitrary commands on the Exchange server. This includes retrieving data, executing scripts, and deploying additional malware.

   TOOLS: -

   NOTE: -

 * Page #6:
   > BONDUPDATER tool used DNS tunneling to communicate with its C2, specifically using TXT queries to receive information from the C2 server

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: The malware communicates with its C2 server using DNS queries, specifically leveraging DNS TXT records.

   TOOLS: -

   NOTE: -

   ---

   ID: 033

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Alternate protocols include FTP, SMTP, HTTP/S, DNS, SMB, or any other network protocol not being used as the main command and control channel.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Powershell scripts meant to run on compromised systems.

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries use PowerShell to run malicious scripts, download additional payloads, or execute commands directly.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Command and control server that communicates via DNS tunneling

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: This technique involves using DNS queries and responses to communicate between the C2 server and the compromised system. DNS tunneling allows data to be hidden within DNS traffic, which can bypass traditional network defenses.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Graphical User Interface that allows actors to issue commands, upload and download files to Agents via the Server

   ID: 012

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves transferring tools or files to a compromised system. A GUI that allows file uploads and downloads is directly related to this technique, enabling operators to manage files on the compromised system through the C2 server.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Glimpse is a PowerShell script

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: -

   TOOLS: -

   NOTE: -

 * Page #6:
   > The panel allows the actors to issue commands in addition to uploading files to and downloading files from the compromised endpoints.

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The panel allows file uploads and downloads is directly related to this technique, enabling operators to manage files on the compromised system through the C2 server.

   TOOLS: -

   NOTE: -

 * Page #7:
   > The server portion of Glimpse works in unison with the panel by acting as a DNS server, which is written in JavaScript and runs in the Node.js runtime.

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves using application layer protocols for C2 communication. The Glimpse server's role as a DNS server to handle commands and responses fits within this technique, where DNS is used as an application layer protocol.

   TOOLS: -

   NOTE: -

 * Page #9:
   > The Poison Frog server handles both the HTTP and DNS tunneling channels used by thehUpdater.ps1anddUpdater.ps1scripts.

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTCOLS (T1071.001)

   DESCRIPTION: The Poison Frog server uses HTTP for command and control (C2) communication. This technique involves using web protocols to send and receive data between the compromised system and the C2 server.

   TOOLS: -

   NOTE: -

 * Page #11:
   > The initial TwoFace loader samples decrypted an embedded webshell using an actor provided key, which was modified by using simple arithmetic operators ("+" or "-" specifically) and a salt string embedded within the loader webshell, whose result decrypts an embedded payload using simple arithmetic operators (again, "+" or "-" specifically)

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: This process is designed to obscure the true nature of the payload, requiring decryption before it can be analyzed.

   TOOLS: -

   NOTE: -

 * Page #11:
   > the TwoFace++ loader used the 3DES cipher and a SHA256 hash of a string provided by the actor and used as a key, so we were unable to extract the embedded webshells as we were unable to determine the actor provided key

   ID: 018

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: This encryption method enhances security but also complicates efforts to analyze the malware without the correct decryption key.

   TOOLS: -

   NOTE: -

 * Page #11:
   > Append a string to the password that acts as a salt

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: BINARY PADDING (T1027.001)

   DESCRIPTION: The use of a salt appended to the password before generating the SHA1 hash adds an extra layer of obfuscation, making it more challenging to brute force or predict the hash.

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #11:
   > Obtain the SHA1 hash of the resulting string containing the password and salt Base64 encode the SHA1 hash Compare the encoded hash with hardcoded base64 string

   ID: 020

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006), DEFENSE EVASION (TA0005), PERSISTENCE (TA0003)

   TECHNIQUE: MODIFY AUTHENTICATION PROCESS (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: The TwoFace++ loader modifies the authentication process by requiring a password and a salt to generate a hash. This hash is then compared against a hardcoded string to authenticate the inbound request. This modification in the authentication mechanism is a technique used to control access to the embedded 

   TOOLS: -

   NOTE: -

   LINK: 019, 021

 * Page #11:
   > Base64 encodes the SHA256 hash and uses the first 24 characters as a key

   ID: 021

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: The process of using the 3DES cipher and a derived 24-character key (from the SHA256 hash) to decrypt the embedded webshell indicates an advanced encryption technique aimed at protecting the payload from unauthorized access.

   TOOLS: -

   NOTE: -

   LINK: 020, 022

 * Page #11:
   > Uses 24-character key and the 3DES cipher to decrypt the embedded webshell

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: The steps to decode and decrypt the embedded webshell demonstrate the use of sophisticated decryption routines that must be followed to retrieve and execute the payload.

   TOOLS: -

   NOTE: -

 * Page #15:
   > The webshell will use the 7za module to archive files from the Explorer tab

   ID: 023

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: ARCHIVE VIA UTILITY (T1560.001)

   DESCRIPTION: The webshell uses the 7za module (7-Zip), a well-known file archiving utility, to compress and archive files from the Explorer tab.

   TOOLS: -

   NOTE: -

 * Page #15:
   > the nbtscan module allows the webshell to scan the network for systems to build an IP list of system it can interact with.

   ID: 024

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE DISCOVERY (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: The nbtscan module is employed by the webshell to scan the network and create a list of IP addresses for systems it can interact with. This type of scanning is typically used to identify potential targets within a network.

   TOOLS: -

   NOTE: -

 * Page #15:
   > To use this functionality, the actor must provide information within the "Target Computer" portion of the webshell, specifically a network administrator username and password, as well as a list of IP addresses of remote systems added in the "Select Computer" drop down

   ID: 025

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005),  PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: The webshell uses valid credentials (network administrator username and password) to authenticate and access remote systems. This aligns with using stolen or compromised credentials to gain unauthorized access to network resources.

   TOOLS: -

   NOTE: -

 * Page #16:
   > to determine if it has more than 30 GB of free space. If the server has less than 30 GB of free space the webshell will not perform the activity, which indicates that the developer of the webshell expects a high volume of data downloaded from the victim network

   ID: 026

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: DATA TRANSFER SIZE LIMITS (T1030)

   SUB-TECHNIQUE: -

   DESCRIPTION: The webshell checks for available storage space (ensuring more than 30 GB is free) before initiating the network download. This could be associated with techniques that avoid triggering alarms or detections related to large data transfers by ensuring the operation has sufficient space to proceed.

   TOOLS: -

   NOTE: -

 * Page #16:
   > The Network Downloader function will gather all the files in these folders and use 7-Zip to compress and archive the files.

   ID: 027

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of 7-Zip to compress and archive files before exfiltration is a classic example of this technique. Attackers often compress data to reduce its size, facilitate transfer, or obscure its contents.

   TOOLS: -

   NOTE: -

 * Page #16:
   > The webshell will save the archives locally to the server in theC:\Users\Public\Libraries\Recorded\Filesfolder,

   ID: 028

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA STAGED (T1074)

   SUB-TECHNIQUE: LOCAL DATA STAGIN (T1074.001)

   DESCRIPTION: Storing the compressed archives in the `C:\Users\Public\Libraries\Recorded\Files` folder for later exfiltration corresponds to staging data locally. This is a preparatory step before transferring the data out of the compromised environment.

   TOOLS: -

   NOTE: -

 * Page #18:
   > remote desktop (RDP) sessions showing the Glimpse panel

   ID: 029

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: The use of RDP sessions to access and operate the Glimpse panel indicates the use of remote desktop services to control and manage compromised systems.

   TOOLS: -

   NOTE: -

