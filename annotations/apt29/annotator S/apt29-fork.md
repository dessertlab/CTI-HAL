## Detailed comments

 * Page #2:
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

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #3:
   > is capable of quietly stealing and ex!ltrating sensitive information such as email from the victim's computer.

   ID: 002

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: EMAIL COLLECTION (T1114)

   SUB-TECHNIQUE: LOCAL EMAIL COLLECTION (T1114.001)

   DESCRIPTION: Adversaries may target email on local systems to collect sensitive information.

   TOOLS: -

   NOTES: - 

   ID: 003

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an alternative protocol.

   TOOLS: -

   NOTES: -

 * Page #3:
   > Cozyduke

   ID: 020

   TOOLS: COZYDUKE (S0046)

 * Page #3:
   > Miniduke

   ID: 021

   TOOLS: MINIDUKE (S0051)

 * Page #3:
   > Cosmicduke

   ID: 022

   TOOLS: COSMICDUKE (S0050)

 * Page #3:
   > In the months that followed, the Duke group began to target victims with "O$ce Monkeys"- and "eFax"-themed emails, booby-trapped with a Cozyduke payload.

   ID: 017

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may send phishing messages to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #4:
   > The attackers control Cozyduke via compromised websites, issuing instructions to infected machines by uploading "tasks" to a database !le.

   ID: 004

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

    

   TECHNIQUE: WEB SERVICE (T1102)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Attackers control Cozyduke through compromised Web sites by uploading "tasks" to a database file. This technique describes the use of web services for command and control malware.

    

   TOOLS: COZYDUKE (S0046)

    

   NOTE: -

 * Page #5:
   > One such task (an encoded PowerShell script) instructed Cozyduke to download and execute Seaduke from a compromised website.

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands and scripts.

   TOOLS: -

   NOTES: -

 * Page #5:
   > beneath layers of encoding (Base64) and encryption (RC4, AES).

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTES: -

 * Page #5:
   > Seaduke securely communicates with the C&C server over HTTP/HTTPS

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries may communicate using web protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTES: -

 * Page #5:
   > They have the ability to retrieve detailed bot/system information,

   ID: 010

    

   SOURCE: TEXT

    

   TACTIC: COLLECTION (TA0009)

    

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Gathering local information from the compromised system, such as operating system details, network configurations, and other information relevant to malware operations.

    

   TOOLS: SEADUKE (S0053)

    

   NOTE: -

 * Page #5:
   > Impersonation using Kerberos pass-the-ticket attacks (Mimikatz PowerShell)

   ID: 012

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: STEAL OR FORGE KERBEROS TICKETS (T1558)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries use stolen Kerberos tickets to authenticate to systems using Pass-the-Ticket (PtT).

   TOOLS: Mimikatz (S0002)

   NOTES: -

   ---

   ID: 018

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Adversaries may attempt to access credential material stored in the process memory of the LSASS.

   TOOLS: Mimikatz (S0002)

   NOTES: -

 * Page #5:
   > Email extraction from the MS Exchange Server using compromised credentials

   ID: 013

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: EMAIL COLLECTION (T1114)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may target email on local systems to collect sensitive information.

   TOOLS: -

   NOTES: -

   ---

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004), PERSISTENCE (TA0003), INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts 

   TOOLS: -

   NOTES: -

 * Page #5:
   > Archiving sensitive information

   ID: 014

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may compress and/or encrypt data collected prior to exfiltration to reduce the size and/or evade detection.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Data ex!ltration via legitimate cloud services

   ID: 015

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER WEB SERVICE (T1567)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exfiltrate data via direct connections to cloud storage services.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Secure !le deletion

   ID: 016

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DISK WIPE (T1561)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may wipe or corrupt raw disk data on specific systems or in large numbers in a network to interrupt availability to system and network resources. 

   TOOLS: -

   NOTE: -

