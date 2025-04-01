## Detailed comments

 * Page #1:
   > Seaduke

   ID: 000

   TOOLS: SEADUKE (S0053)

 * Page #3:
   > The malware hides behind numerous layers of encryption and obfuscation

   ID: 001

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Threat actors use various obfuscation and encryption methods to make it difficult to detect and analyze their tools and techniques.

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #3:
   > is capable of quietly stealing and ex!ltrating sensitive information such as email from the victim's computer.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Seaduke is able to exfiltrate sensitive information such as emails from the victim's machine. 

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #3:
   > Seaduke victims are generally !rst infected with Cozyduke and, if the computer appears to be a target of interest, the operators will install Seaduke

   ID: 003

   TOOLS: COZYDUKE (S0046), SEADUKE (S0053)

   NOTE: first CozyDuke, then if the computer appears to be a target the operators will install Seaduke

 * Page #3:
   > Cozyduke

   ID: 004

   TOOLS: COZYDUKE (S0046)

 * Page #3:
   > Miniduke

   ID: 005

   TOOLS: MINIDUKE (S0051)

 * Page #3:
   > Cosmicduke

   ID: 006

   TOOLS: COSMICDUKE (S0050)

 * Page #3:
   > Cozy Bear

   ID: 007

   TOOLS: COZYBEAR (S0046)

 * Page #3:
   > Cozyduke

   ID: 008

   TOOLS: COZYDUKE (S0046)

 * Page #3:
   > the Duke group began to target victims with "O$ce Monkeys"- and "eFax"-themed emails, booby-trapped with a Cozyduke payload

   ID: 021

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: themed emails were sente with a CozyDuke payload

   TOOLS: -

   NOTE: -

 * Page #4:
   > The attackers control Cozyduke via compromised websites, issuing instructions to infected machines by uploading "tasks" to a database !le

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Attackers control Cozyduke through compromised Web sites by uploading "tasks" to a database file. This technique describes the use of web services for command and control malware.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

 * Page #5:
   > One such task (an encoded PowerShell script) instructed Cozyduke to download and execute Seaduke from a compromised website

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: A task described as a coded PowerShell script that instructs Cozyduke to download and run Seaduke from a compromised website 

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 010

 * Page #5:
   > Seaduke securely communicates with the C&C server over HTTP/HTTPS beneath layers of encoding (Base64) and encryption (RC4, AES).

   ID: 021

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: encoding and encryption layers were used

   TOOLS: -

   NOTE: -

 * Page #5:
   > Seaduke securely communicates with the C&C server over HTTP/HTTPS

   ID: 012

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Use of HTTP/HTTPS as an application layer protocol for communication with the C&C server. 

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #5:
   > They have the ability to retrieve detailed bot/system information

   ID: 013

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Gathering local information from the compromised system, such as operating system details, network configurations, and other information relevant to malware operations.

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #5:
   > self-delete the malware from the system

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ability to self-destruct malware from the compromised system. This can help avoid detection and remove traces of the infection to maintain persistent access.

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #5:
   > upload !les, download !les

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE FILE COPY (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Uploading and downloading files between the compromised system and the C&C server. This may include updating bot configuration, uploading command or script files, and downloading additional payloads.

   TOOLS: SEADUKE (S0053)

   NOTE: -

 * Page #5:
   > Impersonation using Kerberos pass-the-ticket attacks (Mimikatz PowerShell)

   ID: 016

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: STEAL OR FORGE KERBEROS TICKETS (T1558)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Kerberos pass-the-ticket attacks to impersonate legitimate users and gain unauthorized access to systems.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

   ---

   ID: 022

   SOURCE: TEXT 

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Mimikatz was used

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #5:
   > Email extraction from the MS Exchange Server using compromised credentials

   ID: 017

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: EMAIL COLLECTION (T1114)

   SUB-TECHNIQUE: -

   DESCRIPTION: Extracting email from MS Exchange servers using compromised credentials.

   TOOLS: -

   NOTE: -

   ---

   ID: 023

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: compromised credentials were used

   TOOLS: -

   NOTE: -

 * Page #5:
   > Archiving sensitive information

   ID: 018

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: Storage of sensitive information collected for exfiltration or later use.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Data ex!ltration via legitimate cloud services

   ID: 019

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER WEB SERVICE (T1567)

   SUB-TECHNIQUE: -

   DESCRIPTION: Data exfiltration through legitimate cloud services to camouflage malicious traffic.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Secure !le deletion

   ID: 020

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DISK WIPE (T1561)

   SUB-TECHNIQUE: -

   DESCRIPTION: Secure file deletion to remove traces of malicious activity.

   TOOLS: -

   NOTE: -

