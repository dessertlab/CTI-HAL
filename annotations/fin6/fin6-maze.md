## Detailed comments

 * Page #2:
   > MAZE ransomware

   ID: 001

   TOOLS: MAZE

 * Page #5:
   > MAZE ransomware was initially distributed directly via exploit kits

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Initial deployment of Maze ransomware via exploit kits.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Mandiant observed multiple email campaigns delivering Maze ransomware

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Email campaigns used to distribute Maze ransomware

   TOOLS: -

   NOTE: -

   LINK: 004, 005

 * Page #5:
   > These emails used tax, invoice, and package delivery themes with document a!achments

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISING ATTACHMENT (T1566.001)

   DESCRIPTION: Email campaigns containing document attachments used to distribute Maze ransomware.

   TOOLS: -

   NOTE: -

   LINK: 003, 004,

 * Page #5:
   > or

   ID: 004

   NOTE: emails can contain two different types of attachments

   LINK: 005 OR 006

 * Page #5:
   > inline links to documents which download and execute Maze ransomware

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Email campaigns that contain inline links to documents that download and execute Maze ransomware

   TOOLS: -

   NOTE: -

   LINK: 003, 004

 * Page #6:
   > These emails originated from a compromised or spoofed account

   ID: 007

   SOURCE: TEXT

   TACTIC: INTIAL ACCESS (TA0001), PRIVILEGE ESCALATION(TA0004), DEFENSE EVASION (TA0005), 

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of compromised accounts to send phishing emails.

   TOOLS: -

   NOTE: -

   LINK: 008

   Compromised or Spoofed Accounts:

   	•	T1078 - Valid Accounts:

 * Page #6:
   > contained an inline link to download a Maze executable payload

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Email campaigns that contain inline links to documents that download and execute Maze ransomware

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #6:
   > These emails used the subjects "Missed package delivery" and "Your AT&T wireless bill is ready to view"

   ID: 009

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: emails with misleading themes (e.g., "Missed package delivery" and "Your AT&T wireless bill is ready to view") to induce victims to open the messages.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #6:
   > were sent using a number of malicious domains with the registrant address abusereceive@hitler.rocks

   ID: 010

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: DOMAINS (T1584.001)

   DESCRIPTION: Use of malicious domains to send phishing emails.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #8:
   > A user downloaded a malicious resumethemed Microso# Word document that contained macros

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading and opening a Word document containing malicious macros.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #8:
   > launched an IcedID payload, which was ultimately used to execute an instance of BEACON

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Macros that execute commands to launch the IcedID payload.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #8:
   > An actor logged into an internet-facing system via RDP

   ID: 013

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Access via RDP.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #8:
   > The account used to grant initial access was a generic suppo$ account

   ID: 014

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: DEFAULT ACCOUNTS (T1078.001)

   DESCRIPTION: Using a generic account (support account) for initial access.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #8:
   > An actor exploited a miscon%guration on an Internet-facing system.

   ID: 015

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATION (T1190)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of a misconfiguration on an Internet-exposed system.

   TOOLS: -

   NOTE: -

 * Page #8:
   > An actor logged into a Citrix web po$al account with a weak password.

   ID: 016

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: To access the Citrix web portal.

   TOOLS: -

   NOTE: -

 * Page #8:
   > launch a Meterpreter payload on an internal system

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Meterpreter to access and control the system.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The use of legitimate credentials and broad distribution of BEACON across victim environments

   ID: 018

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of legitimate credentials to gain access and maintain control.

   TOOLS: -

   NOTE: -

 * Page #9:
   > an actor create their own domain account to enable la!er-stage operations

   ID: 019

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE ACCOUNT (T1136)

   SUB-TECHNIQUE: -

   DESCRIPTION: Creating an account for subsequent operations

   TOOLS: -

   NOTE: -

 * Page #9:
   > installing BEACON payloads on many servers and workstations

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transferring BEACON payloads to servers and workstations.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Web shells were deployed to an internetfacing system.

   ID: 021

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: WEB SHELL (T1505.003)

   DESCRIPTION: Deployment of web shells on an Internet-exposed system.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Intrusion operators regularly obtained and maintained access to multiple domain and local system accounts with varying permissions that were used throughout their operations

   ID: 022

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of various local and domain system accounts.

   TOOLS: -

   NOTE: -

 * Page #9:
   > An actor created a new domain account and added it to the domain administrators group

   ID: 023

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0011)

   TECHNIQUE: CREATE ACCOUNT (T1136)

   SUB-TECHNIQUE: DOMAIN ACCOUNT (T1136.002)

   DESCRIPTION: Creating a new domain account.

   TOOLS: -

   NOTE: -

 * Page #9:
   > MAZE intrusion operators employed Mimikatz to collect credentials to enable privilege escalation

   ID: 024

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Mimikatz to collect credentials.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #9:
   > use of Bloodhound, and more manual searches for %les containing credentials

   ID: 025

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: DOMAIN TRUST DISCOVERY (T1482)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Bloodhound to explore Active Directory configuration and identify attack paths to gain domain privileges

   TOOLS: BLOODHOUND

   NOTE: -

 * Page #10:
   > Mimikatz.

   ID: 026

   TOOLS: MIMIKATZ (S0002)

 * Page #10:
   > The actor a!empted to %nd %les with the word "password" within the environment

   ID: 027

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1522)

   SUB-TECHNIQUE: CREDENTIALS IN FILES (T1552.001)

   DESCRIPTION: Searching for files containing credentials (e.g., files with the word "password")

   TOOLS: -

   NOTE: -

 * Page #10:
   > The actor a!empted to identify hosts running the KeePass password safe so#ware

   ID: 028

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: identify whether keepass is installed on the target devices

   TOOLS: -

   NOTE: -

 * Page #10:
   > Actors primarily used Procdump and Mimikatz to collect credentials used to enable later stages of their intrusion.

   ID: 029

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Procdump and Mimikatz are tools used to extract credentials from system memory or system files

   TOOLS: PROCDUMP, MIMIKATZ (S0002)

   NOTE: -

 * Page #10:
   > Bloodhound and PingCastle were also used, presumably to enable a!ackers' e&o$s to understand the impacted organization's Active Directory con%guration

   ID: 030

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: DOMAIN TRUST DISCOVERY (T1482)

   SUB-TECHNIQUE: -

   DESCRIPTION: PingCastle is used to analyze and evaluate the security of Active Directory configuration

   TOOLS:  PINGCASTLE

   NOTE: -

   LINK: 031

 * Page #10:
   > In this case the responsible actors also a!empted to ex%ltrate collected credentials to multiple di&erent cloud %le storage services

   ID: 031

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER WEB SERVICE (T1567)

   SUB-TECHNIQUE: EXFILTRATION TO CLOUD STORAGE (T1567.002)

   DESCRIPTION: Attempts to exfiltrate sensitive data on cloud storage services

   TOOLS: -

   NOTE: -

   LINK: 030

 * Page #11:
   > The responsible actor executed a large number of reconnaissance scripts via Cobalt Strike to collect network, host, %lesystem, and domain related information

   ID: 032

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Cobalt Strike to gather network configuration information

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   ---

   ID: 033

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Cobalt Strike to discover account information

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   ---

   ID: 034

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Cobalt Strike to discover information about files and directories on compromised systems

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #11:
   > Multiple built-in Windows commands were used to enable network, account, and host reconnaissance of the impacted environment,

   ID: 035

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using built-in Windows commands to discover network configuration information

   TOOLS: -

   NOTE: -

   ---

   ID: 036

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using built-in Windows commands to discover account information

   TOOLS: -

   NOTE: -

 * Page #11:
   > the actors also supplied and used Advanced IP Scanner and Ad%nd to suppo$ this stage of their operations

   ID: 037

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Advanced IP Scanner to scan IP and network devices.

   TOOLS: ADVANCED IP SCANNER, ADFIND (S0552)

   NOTE: -

 * Page #11:
   > a batch script named '2.bat' which contained a series of nslookup commands

   ID: 038

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using nslookup to identify information about remote systems

   TOOLS: -

   NOTE: -

 * Page #12:
   > via an encoded PowerShell script

   ID: 040

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to run scripts, in this case to exfiltrate data.

   TOOLS: -

   NOTE: -

   ---

   ID: 041

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscated Files or Information: Using a coded PowerShell script to obfuscate the intent and content of the script

   TOOLS: -

   NOTE: -

 * Page #12:
   > FTP server

   ID: 039

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Using an application layer protocol (FTP) to exfiltrate data

   TOOLS: -

   NOTE: -

   LINK: 040

 * Page #12:
   > Bloodhound

   ID: 042

   TOOLS: BLOODHOUND

 * Page #12:
   > PowerSploit/PowerView

   ID: 043

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE SCANNING (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: PowerSploit/PowerView (Invoke-ShareFinder) can be used to scan the network and locate available services and resources.

   TOOLS: POWERSPLOIT/POWEVIEW

   NOTE: -

 * Page #12:
   > a reconnaissance script designed to enumerate directories across internal hosts

   ID: 044

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using reconnaissance scripts to enumerate directories on internal hosts.

   TOOLS: -

   NOTE: -

 * Page #12:
   > An actor employed the ad%nd tool and a batch script to collect information about their network, hosts, domain, and users.

   ID: 045

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of network configuration information

   TOOLS: ADFIND (S0552)

   NOTE: -

   ---

   ID: 046

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of user account information.

   TOOLS: ADFIND (S0552)

   NOTE: -

   ---

   ID: 047

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: DOMAIN TRUST DISCOVERY (T1482)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of information on trust relationships between domains.

   TOOLS: ADFIND (S0552)

   NOTE: -

   ---

   ID: 048

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Using batch scripts to automate commands and gather information.

   TOOLS: -

   NOTE: -

 * Page #12:
   > The output from this batch script (2ad%nd.bat) was saved into an archive named 'ad.7z' using an instance of the 7zip archiving utility named 7.exe.

   ID: 049

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA STAGED (T1074)

   SUB-TECHNIQUE: LOCAL DATA STAGING (T1074.001)

   DESCRIPTION: Storage and compression of locally collected data.

   TOOLS:  7-ZIP

   NOTE: -

 * Page #12:
   > An actor collected directory listings from %le servers across an impacted environment

   ID: 050

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: The actor collected directory listings from file servers in the affected environment.

   TOOLS: -

   NOTE: -

 * Page #13:
   > Cobalt Strike

   ID: 051

   TOOLS: COBALT STRIKE (S0154)

 * Page #13:
   > Cobalt Strike

   ID: 052

   TOOLS: COBALT STRIKE (S0154)

 * Page #13:
   > they also tunneled RDP using the ngrok utility

   ID: 053

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: PROXY (T1090)

   SUB-TECHNIQUE: MULTI-HOP PROXY (T1090.003)

   DESCRIPTION: Using ngrok for tunneling RDP sessions through multi-hop proxies

   TOOLS: NGROK

   NOTE: -

 * Page #13:
   > employed tscon to hijack legitimate rdp sessions to enable both lateral movement and privilege escalation

   ID: 054

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1563)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1563.001)

   DESCRIPTION: Use of tscon for hijacking legitimate RDP sessions, falling under the manipulation of remote services for lateral movement

   TOOLS: -

   NOTE: -

 * Page #13:
   > Stolen credentials were then used to move laterally

   ID: 055

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using compromised accounts (services and users) to move laterally through the network

   TOOLS: -

   NOTE: -

   LINK: 056

 * Page #13:
   > across the network via RDP

   ID: 056

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Use of stolen credentials to move laterally through RDP

   TOOLS: - 

   NOTE: -

   LINK: 055

 * Page #13:
   > Metasploit

   ID: 057

   TOOLS: METASPLOIT

 * Page #13:
   > Cobalt Strike

   ID: 058

   TOOLS: COBAL STRIKE (S0154)

 * Page #13:
   > using a local administrator account

   ID: 059

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: LOCAL ACCOUNTS (T1078.003)

   DESCRIPTION: Using local accounts with administrator privileges to move laterally and to install payloads

   TOOLS: METASPLOIT, COBALT STRIKE (S0154)

   NOTE: -

 * Page #13:
   > EternalBlue

   ID: 060

   TOOLS: ETERNAL BLUE

 * Page #14:
   > MAZE

   ID: 061

   TOOLS: MAZE

 * Page #14:
   > a base64-encoded PowerShell script

   ID: 062

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute data exfiltration commands.

   TOOLS: -

   NOTE: -

 * Page #14:
   > a prede%ned FTP server using a hard-coded username and password

   ID: 063

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Use of hard-coded credentials for FTP authentication during data exfiltration.

   TOOLS: -

   NOTE: -

 * Page #14:
   > A di&erent base64-encoded PowerShell command

   ID: 064

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute data exfiltration commands.

   TOOLS: -

   NOTE: -

 * Page #14:
   > Actors deploying MAZE ransomware have also used the utility WinSCP to ex%ltrate data to an a!acker-controlled FTP server

   ID: 065

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER COMMAND AND CONTROL CHANNEL (T1041)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Using file transfer applications such as WinSCP to exfiltrate data on an FTP server controlled by the attacker

   TOOLS: MAZE, WINSCP

   NOTE: -

 * Page #14:
   > An actor has been observed employing a %le replication utility and copying the stolen data to a cloud %le hosting/sharing service.

   ID: 066

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Using file synchronization or replication applications to copy data to cloud file hosting or sharing services

   TOOLS: -

   NOTE: -

 * Page #14:
   > threat actors employed the 7zip utility to archive data from across various corporate %le shares

   ID: 067

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: ARCHIVE VIA UTILITY (T1560.001)

   DESCRIPTION: Using utilities such as 7zip to compress data from various corporate file shares before exfiltration.

   TOOLS: -

   NOTE: -

 * Page #14:
   > These archives were then ex%ltrated to an a!acker-controlled server via FTP using the WinSCP utility

   ID: 068

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER COMMAND AND CONTROL CHANNEL (T1041)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Using file transfer applications such as WinSCP to exfiltrate data on an FTP server controlled by the attacker.

   TOOLS: WINSCP

   NOTE: -

 * Page #15:
   > Five days a#er data was ex%ltrated from a victim environment the actor copied a MAZE ransomware binary to 15 hosts within the victim environment and successfully executed it on a po$ion of these systems.

   ID: 069

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Distribution and execution of MAZE ransomware on numerous servers and workstations within the victim's environment.

   TOOLS: -

   NOTE: -

 * Page #15:
   > A!ackers employed batch scripts and a series to txt %les containing host names to distribute and execute MAZE ransomware on many servers and workstations across the victim environment

   ID: 070

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using batch scripts to deploy and execute MAZE ransomware on many servers and workstations in the victim's environment.

   TOOLS: MAZE

   NOTE: -

 * Page #15:
   > using a domain administrator account created earlier in the intru

   ID: 071

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: LOCAL ACCOUNTS (T1078.003)

   DESCRIPTION: Using a previously created domain administrator account to access systems and deploy MAZE ransomware.

   TOOLS: MAZE

   NOTE: -

 * Page #16:
   > Each of these batch scripts contained a series of commands that employed the copy command, WMIC, and PsExec to copy and execute a kill script (windows.bat) and an instance of MAZE ransomware (sss.exe) on hosts across the impacted environment

   ID: 071

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SMB/WINDOWS ADMIN SHARES (T1021.002)

   DESCRIPTION: Using PsExec for remote execution of scripts and ransomware on affected systems.

   TOOLS: PSEXEC, WMIC

   NOTE: -

 * Page #16:
   > Notably, forensic analysis of the impacted environment revealed MAZE deployment scripts targeting ten times as many hosts as were ultimately encrypted

   ID: 072

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Running MAZE ransomware (sss.exe) on different systems to encrypt data

   TOOLS: MAZE

   NOTE: -

