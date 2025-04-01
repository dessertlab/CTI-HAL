## Detailed comments

 * Page #6:
   > These campaigns utilized specially-crafted malicious Microsoft Word documents and PDF files, which were sent as e-mail attachments to various personnel in an attempt to infiltrate the targeted organizations.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #7:
   > CosmicDuke would often embed PinchDuke so that, upon execution, CosmicDuke would write to disk and execute PinchDuke

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTES: -

 * Page #7:
   > performing separate information gathering, data exfiltration and communication with a command and control (C&C) server

   ID: 003

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources, such as file systems and configuration files or local databases, to find files of interest and sensitive data prior to Exfiltration.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTES: -

   ID: 004

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTES: -

 * Page #8:
   > While the Dukes employed both hacked websites and purposely rented servers for their C&C infrastructure, the group rarely registered their own domain names, preferring instead to connect to their self- operated servers via IP addresses.

   ID: 005

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may buy, lease, rent, or obtain infrastructure that can be used during targeting.

   TOOLS: -

   NOTES: -

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: -

   NOTES: APT29 hacked websites.

 * Page #8:
   > a large grouping of domain names was registered by the Dukes in two batches

   ID: 007

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: DOMAINS (T1583.001)

   DESCRIPTION: Adversaries may acquire domains that can be used during targeting.

   TOOLS: -

   NOTES: -

 * Page #8:
   > MiniDuke is centered on a simplistic backdoor component whose purpose is to enable the remote execution of commands on the compromised system.

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: MINIDUKE (S0051)

   NOTES: -

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may use legitimate desktop support and remote access software to establish an interactive command and control channel to target systems within networks.

   TOOLS: MINIDUKE (S0051)

   NOTES: -

 * Page #9:
   > CozyDuke is a highly versatile, modular, malware "platform" whose functionality lies not in a single core component but in an array of modules that it may be instructed to download from its C&C server. These modules are used to selectively provide CozyDuke with just the functionality deemed necessary for the mission at hand.

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

 * Page #9:
   > even the earliest known GeminiDuke samples encrypted any strings that might have given away the malware's true nature.

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

 * Page #11:
   > the MiniDuke campaigns from February 2013 employed spear-phishing emails with malicious PDF file attachments. These PDFs would attempt to silently infect the recipient with MiniDuke, while distracting them by displaying a decoy document.

   ID: 012

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: MALICIOUS FILE (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTES: -

 * Page #12:
   > password stealing, information gathering

   ID: 014

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: ONIONDUKE (S0052)

   NOTES: -

 * Page #12:
   > denial of service (DoS) attacks

   ID: 015

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENDPOINT DENIAL OF SERVICE (T1499)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may perform Endpoint Denial of Service (DoS) attacks to degrade or block the availability of services to users.

   TOOLS: ONIONDUKE (S0052)

   NOTES: -

 * Page #15:
   > This campaign, like later CozyDuke campaigns, began with spear-phishing emails that tried to impersonate commonly seen spam emails. These spear-phishing emails would contain links that eventually lead the victim to becoming infected with CozyDuke.

   ID: 016

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

 * Page #16:
   > a malicious Tor exit node

   ID: 017

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may compromise third-party infrastructure that can be used during targeting.

   TOOLS: -

   NOTES: -

 * Page #16:
   > Executing the modified applications obtained this way would result in the victim being infected with unidentified malware.

   ID: 018

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

   NOTES: Modified executables are executed by victims, resulting in the infection.

   LINK: #017 THEN #018

 * Page #18:
   > one of these modules gathers system information

   ID: 019

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.

   TOOLS: ONIONDUKE (S0052)

   NOTES: -

 * Page #18:
   > another attempts to steal the victim's usernames and passwords

   ID: 020

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: ONIONDUKE (S0052)

   NOTES: -

 * Page #18:
   > one is designed for use in DoS attacks

   ID: 021

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENDPOINT DENIAL OF SERVICE (T1499)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may perform Endpoint Denial of Service (DoS) attacks to degrade or block the availability of services to users.

   TOOLS: ONIONDUKE (S0052)

   NOTES: -

 * Page #18:
   > thousands of recipients being sent spear-phishing emails that contained links to compromised websites hosting CozyDuke

   ID: 022

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

   ID: 023

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may compromise third-party infrastructure that can be used during targeting.

   TOOLS: -

   NOTES: -

 * Page #19:
   > They would then use the toolset to gather initial information on the victims

   ID: 024

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

 * Page #19:
   > The simpler one will connect to a hardcoded C&C server over HTTP or HTTPS to download commands to execute.

   ID: 024

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: HAMMERDUKE (S0037)

   NOTES: -

 * Page #19:
   > The more advanced variant, on the other hand, will use an algorithm to generate a periodically-changing Twitter account name and will then attempt to find tweets from that account containing links to the actual download location of the commands to execute.

   ID: 025

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: HAMMERDUKE (S0037), MINIDUKE (S0051), ONIONDUKE (S0052), COZYDUKE (S0046)

   NOTES: -

 * Page #20:
   > Both backdoors (internally referred to by their authors as "BastionSolution" and "OneDriveSolution") essentially allow the operator to remotely execute commands on the compromised machine.

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: CLOUDDUKE (S0054)

   NOTES: -

 * Page #20:
   > the BastionSolution variant simply retrieves commands from a hard-coded C&C server controlled by the Dukes

   ID: 027

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: CLOUDDUKE (S0054)

   NOTES: -

 * Page #20:
   > the OneDriveSolution utilizes Microsoft's OneDrive cloud storage service for communicating with its masters

   ID: 028

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: CLOUDDUKE (S0054)

   NOTES: -

 * Page #21:
   > spear- phishing emails containing malicious attachments

   ID: 029

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #22:
   > The PinchDuke information stealer gathers system configuration information, steals user credentials, and collects user files from the compromised host transferring these via HTTP(S) to a C&C server.

   ID: 030

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources, such as file systems and configuration files or local databases, to find files of interest and sensitive data prior to Exfiltration.

   TOOLS: PINCHDUKE (S0048)

   NOTES: -

   ID: 031

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: PINCHDUKE (S0048)

   NOTES: -

   ID: 032

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: PINCHDUKE (S0048)

   NOTES: -

 * Page #23:
   > Unlike CosmicDuke and PinchDuke, GeminiDuke primarily collects information on the victim computer's configuration. The collected details include: •Local user accounts •Network settings Internet proxy settings • Installed drivers • •Running processes •Programs previously executed by users •Programs and services configured to automatically run at startup •Values of environment variables •Files and folders present in any users home folder •Files and folders present in any users My Documents •Programs installed to the Program Files folder •Recently accessed files, folders and programs

   ID: 033

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may collect detailed information about the victim's system, such as local user accounts, network settings, installed drivers, environment variables, and recently accessed files.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

   ID: 034

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: LOCAL ACCOUNTS (T1087.001)

   DESCRIPTION: Adversaries may enumerate accounts to learn about user and administrator accounts.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

   ID: 035

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may look for details about the network configuration and settings.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

   ID: 036

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather information about the running processes on the system.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

   ID: 037

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search for files, folders, and directories on local and remote systems.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

   ID: 038

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources, such as file systems and configuration files or local databases, to find files of interest and sensitive data prior to Exfiltration.

   TOOLS: GEMINIDUKE (S0049)

   NOTES: -

 * Page #25:
   > CosmicDuke's information stealing functionality includes: •Keylogging •Taking screenshots •Stealing clipboard contents •Stealing user files with file extensions that match a predefined list •Exporting the users cryptographic certificates including private keys •Collecting user credentials, including passwords, for a variety of popular chat and email programs as well as from web browsers

   ID: 039

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Adversaries may use keylogging to capture user input, including passwords and other sensitive information.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

   ID: 040

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture screenshots of the victim's desktop to gather information.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

   ID: 041

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: CLIPBOARD DATA (T1115)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture data stored in the clipboard, potentially revealing sensitive information.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

   ID: 042

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search for and collect files from a local system, including those with specific file extensions.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

   ID: 043

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

 * Page #25:
   > CosmicDuke may use HTTP, HTTPS, FTP or WebDav to exfiltrate the collected data to a hardcoded C&C server.

   ID: 044

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel. Stolen data is encoded into the normal communications channel using the same protocol as command and control communications.

   TOOLS: COSMICDUKE (S0050)

   NOTES: -

 * Page #27:
   > obtain the address of a current C&C server via Twitter

   ID: 045

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: MINIDUKE (S0051)

   NOTES: -

 * Page #28:
   > This component can be instructed by the C&C server to download and execute arbitrary modules

   ID: 046

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: COZYDUKE (S0046)



   NOTES: -

   ID: 047

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands and scripts.

   TOOLS: COZYDUKE (S0046)



   NOTES: -

 * Page #28:
   > Known CozyDuke modules include: •Command execution module for executing arbitrary Windows Command Prompt commands •Password stealer module •NT LAN Manager (NTLM) hash stealer module •System information gathering module •Screenshot module

   ID: 048

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands and scripts.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

   ID: 049

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

   ID: 050

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather information about the system's configurations and settings.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

   ID: 051

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture screenshots to gather information about the victim's system.

   TOOLS: COZYDUKE (S0046)

   NOTES: -

 * Page #29:
   > The Tor node would intercept any unencrypted executable files being downloaded and modify those executables by adding a malicious wrapper contained an embedded OnionDuke

   ID: 052

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may compromise third-party infrastructure that can be used during targeting.

   TOOLS: -

   NOTES: -

   ID: 053

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

   NOTES: Modified executables are executed by victims, resulting in the infection.

 * Page #30:
   > SeaDuke is a simple backdoor that focuses on executing commands retrieved from its C&C server, such as uploading and downloading files, executing system commands and evaluating additional Python code.

   ID: 054

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: SEADUKE (S0053)



   NOTES: -

   ID: 055

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands and scripts.

   TOOLS: SEADUKE (S0053)



   NOTES: -

 * Page #31:
   > Some HammerDuke variants only contain a hardcoded C&C server address from which they will retrieve commands,

   ID: 057

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: HAMMERDUKE (S0037)

   NOTES: -

 * Page #31:
   > its occasional use of Twitter as a C&C communication channel

   ID: 056

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: HAMMERDUKE (S0037)

   NOTES: -

 * Page #32:
   > The CloudDuke downloader will download and execute additional malware from a preconfigured location. Interestingly, that location may be either a web address or a Microsoft OneDrive account.

   ID: 057

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: CLOUDDUKE (S0054)



   NOTES: -

   ID: 058

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands and scripts.

   TOOLS: CLOUDDUKE (S0054)



   NOTES: -

   ID: 059

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an existing, legitimate external Web service as a means for relaying data to/from a compromised system.

   TOOLS: CLOUDDUKE (S0054)

   NOTES: -

 * Page #32:
   > one variant will use a preconfigured C&C server over HTTP or HTTPS

   ID: 060

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: HAMMERDUKE (S0037)

   NOTES: -