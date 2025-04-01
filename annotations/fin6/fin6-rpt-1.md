## Detailed comments

 * Page #4:
   > Email phishing credential theft

   ID: 001

   SOURCE: IMAGE

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Email phishing campaigns aimed to credential theft.

   TOOLS: -

   NOTES: The goal may be to spread Grabnew malware to steal credentials. Threat actors could be different and FIN6 could have bought credentials (cybercrime support ecosystem).

   LINK: 014

 * Page #6:
   > FIN6 used a Metasploit PowerShell module to download and execute shellcode and to set up a local listener that would execute shellcode received over a specific port. Similarly, FIN6 used at least two downloaders called HARDTACK and SHIPBREAD (apparent variations on Metasploit payloads) to establish backdoor access to the compromised environment. Both of these tools are configured to connect to remote command and control (CnC) servers and download and execute shellcode.

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Tools or files may be copied from an external adversary-controlled system to the victim network through the command and control channel.

   TOOLS: -

   NOTES: -

   LINK: 002

   ---

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries can abuse PowerShell commands and scripts for execution.

   TOOLS: METASPLOIT, HARDTACK, SHIPBREAD (Downloader)

   NOTES: A Metasploit Powershell module is used to download and execute shellcode from a CnC server.

   LINK: 007, 008

 * Page #6:
   > FIN6 generally used either registry run keys

   ID: 005

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/STARTUP FOLDER (T1547.001)

   DESCRIPTION: Adversaries may achieve persistence by adding a program to a startup folder or referencing it with a Registry run key.

   TOOLS: -

   NOTES: -

 * Page #6:
   > Windows scheduled tasks in order to establish persistence for these tools.

   ID: 006

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SCHEDULED TASK/JOB  (T1053)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse task scheduling functionality to facilitate initial or recurring execution of malicious code.

   TOOLS: -

   NOTES: -

 * Page #6:
   > or

   ID: T01

   SOURCE: TEXT

   NOTES: OR

   LINK: 005, 006

 * Page #6:
   > FIN6 used additional public utilities such as Windows Credentials Editor for privilege escalation and credential harvesting

   ID: 007

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attemp to dump credentials to obtain account login.

   TOOLS: -

   NOTES: -

   LINK: 004

   ---

   ID: 008

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHINQUE: -

   DESCRIPTION:  Adversaries may obtain credentials of existing accounts.

   TOOLS: -

   NOTES: -

   LINK: 004

 * Page #6:
   > gaining access with valid credentials

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain credentials of existing accounts.

   TOOLS: -

   NOTES: FIN6 may obtain access with valid credentials, stolen by credential stealers.

   LINK: 003

 * Page #6:
   > FIN6 also used Metasploit's PsExec NTDSGRAB module to obtain a copy of the Active Directory database (ntds.dit). Access to this file would allow them to extract password hashes from the file and crack them offline.

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: NTDS (T1003.003)

   DESCRIPTION: Adversaries may attempt to access or create a copy of the Active Directory domain database in order to steal credential information.

   TOOLS: Metasploit's PsExec NTDSGRAB

   NOTES: -

   ---

   ID: 010

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: BRUTEFORCE (T1110)

   SUB-TECHNIQUE: PASSWORD CRACKING (T1110.002)

   DESCRIPTION: Adversaries may use password cracking to attempt to recover usable credentials, such as plaintext passwords, when credential material such as password hashes are obtained.

   TOOLS: -

   NOTES: -

 * Page #7:
   > In addition to collecting credentials, FIN6 used publicly available tools to map the internal network and conduct reconnaissance against Active Directory, Structured Query Language (SQL) servers and NetBIOS.

   ID: 011

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN6 used publicly available tools (including Microsoft's built-in SQL querying tool, osql.exe) to map the internal network and conduct reconnaissance against Active Directory, SQL servers, and NetBIOS.

   TOOLS: AdFind (S0552), osql.exe

   NOTES: -

 * Page #7:
   > gathered information on systems running SQL instances, dumping schemas for multiple databases and SQL user accounts

   ID: 022

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: gathered information on systems running SQL instances

   TOOLS: -

   NOTE: -

 * Page #7:
   > using credentials stolen from various systems on which they gathered usernames and password hashes

   ID: 012

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: -

   NOTES: Adversaries cracked the hashes outside the target's network.

 * Page #7:
   > remote command execution tools such as PsExec and Remote Command Executor (RemCom) throughout the rest of the lateral movement phase.

   ID: 013

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: SOFTWARE DEPLOYMENT TOOLS (T1072)

   SUB-TECHINQUE: -

   DESCRIPTION: Adversaries may gain access to and use centralized software suites installed within an enterprise to execute commands and move laterally through the network.

   TOOLS: PsExec (S0029), RemCom

   NOTES: -

 * Page #7:
   > FIN6 leveraged the publicly available Plink command-line utility (part of the PuTTY SSH and Telnet suite) to create SSH tunnels to CnC servers under their control

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: PROTOCOL TUNNELING  (T1572)

   SUB-TECHINQUE: -

   DESCRIPTION: Adversaries perform SSH tunneling.

   TOOLS: Plink

   NOTES: -

   LINK: 001, 019, 020

 * Page #7:
   > they used these SSH tunnels to route Remote Desktop Protocol (RDP) traffic and allow for interactive RDP sessions with systems in the target network.

   ID: 015

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES  (T1021)

   SUB-TECHINQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Adversaries may use Valid Accounts to log into a computer using the Remote Desktop Protocol (RDP). The adversary may then perform actions as the logged-on user.

   TOOLS: -

   NOTES: -

 * Page #7:
   > Once the malware identifies track data, it copies and encodes it to a local file in a subdirectory of the c:\windows\ directory while attempting to conceal these files with .dll or .chm extensions.

   ID: 016

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may target and collect data from local system sources.

   TOOLS: -

   NOTES: -

   ---

   ID: 017

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTES: -

 * Page #7:
   > The malware encodes the data with a simple substitution cipher and single-byte XOR using the OxAA key.

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILE (T1027.013)

   DESCRIPTION: Encrypting and/or encoding file content aims to conceal malicious artifacts within a file used in an intrusion.

   TOOLS: -

   NOTES: -

 * Page #7:
   > to move the stolen payment card data out of the environment, FIN6 used a script to systematically iterate through a list of compromised POS systems, copying the harvested track data files to a numbered "log" file before removing the original data files. They then compressed the log files into a ZIP archive and moved the archive through the environment to an intermediary system and then to a staging system.

   ID: 021

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN6 used a script to systematically iterate through a list of compromised POS systems, copying the harvested track data files. They then compressed into a ZIP archive.

   TOOLS: Framework POS (S0503)

   NOTE: -

   LINK: 024

   --- 

   ID: 024

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: AUTOMATED EXFILTRATION (T1020)

   SUB-TECHNIQUE: -

   DESCRIPTION: they used a script to systematically iterate through a list of compromiserd POS system.

   TOOLS: -

   NOTE: -

   LINK: 021

 * Page #7:
   > they then copied the stolen data to external CnC servers under their control using the FTP command line utility

   ID: 019

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: -

   NOTES: -

   LINK: 014, 023

   ---

   ID: 023

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: they used the FTP command to copy the stolen data to external CnC servers.

   TOOLS: -

   NOTE: -

   LINK: 019

 * Page #7:
   > FIN6 used an alternative extraction method to upload payment card data to a public file sharing service.

   ID: 020

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel. The data may also be sent to an alternate network location from the main command and control server.

   TOOLS: -

   NOTES: -

   LINK: 014

