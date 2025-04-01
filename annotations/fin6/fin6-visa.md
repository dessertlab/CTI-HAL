## Detailed comments

 * Page #1:
   > TRINITY POS (aka FrameworkPOS)

   ID: 000

   TOOLS: FRAMEWORKPOS

 * Page #1:
   > FIN6 targets companies, using phishing emails in an attempt to infect the targeted victim's network

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using phishing emails to infect the targeted victim's network

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 actors targeted multiple high value eCommerce merchants with malicious documents that contained links to a malicious server

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Malicious documents containing links to a malicious server

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #1:
   > that allowed the execution of PowerShell scripts, granting the attackers direct access to the merchants' networks.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell scripts to gain direct access to merchant networks.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #1:
   > The FIN6 actors were able to utilize this access to move through the merchant's networks to access the eCommerce environment, and specifically the payment servers.

   ID: 004

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: Discovery of remote systems to identify eCommerce payment environments and servers

   TOOLS: -

   NOTE: -

 * Page #2:
   > use of malicious documents to infect victims

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Malicious documents to infect victims

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #2:
   > that is used to launch malicious scripts on the infected machine.

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Launch malicious scripts on the infected machine

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #2:
   > malware known asMore_Eggs (aka Terra Loader)

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Infect victims with malware known as More_Eggs (aka Terra Loader)

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #2:
   > FIN6 establishes a foothold within a victim's environment by leveraging various payloads, such as components of the Metasploit Framework (e.g., Meterpreter,JSPSPYand CmdSQL)

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Leveraging various payloads such as Metasploit Framework components (e.g., Meterpreter, JSPSPY, and CmdSQL)

   TOOLS: METASPLOIT, METERPRETER, JSPPY, CMDSQL

   NOTE: -

 * Page #2:
   > or

   ID: 009

   LINK: 008 OR 010 THEN 011

 * Page #3:
   > specialized version of theAMMYYremote administration tool (RAT) known as FlawedAmmyy

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Specialized version of the AMMYY remote administration tool (RAT) known as FlawedAmmyy

   TOOLS: FLAWEDAMMYY

   NOTE: -

 * Page #3:
   > attackers then establish persistent access to the victim's network using Meterpreter related code, allowing the attackers to maintain a remote connection to the infected system.

   ID: 011

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: -

   DESCRIPTION: Establishing persistent access using Meterpreter related code

   TOOLS: METERPETER

   NOTE: -

 * Page #3:
   > FIN6 uses legitimate publicly available tools to map the internal network and conduct reconnaissance

   ID: 012

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using legitimate publicly available tools to map the internal network and conduct reconnaissance

   TOOLS: -

   NOTE: -

 * Page #3:
   > the actors gather information on systems running SQL Database Server instances and dump schemas for multiple databases and SQL user accounts

   ID: 013

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM INFORMATION REPOSITORIES (T1213)

   SUB-TECHNIQUE: DATABASE (T1213.002)

   DESCRIPTION: Gathering information on systems running SQL Database Server instances and dumping schemas for multiple databases and SQL user accounts.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The actors also target network credentials using a malware family known asStealer One(see below in the sectionTechnical Analysis and Indicators ofCompromise).

   ID: 014

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Targeting network credentials using a malware family known as Stealer One

   TOOLS: -

   NOTE: -

 * Page #3:
   > FIN6 employs legitimate administrative tools,

   ID: 015

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: SERVICE EXECUTION (T1569.002)

   DESCRIPTION: Employing legitimate administrative tools

   TOOLS: -

   NOTE: -

   LINK: 016, 017, 018

 * Page #3:
   > Microsoft's built-in SQL querying tool

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of native tools such as osql.exe to perform SQL queries.

   TOOLS:  OSQL

   NOTE: -

 * Page #3:
   > AdFind (a free command-line tool for querying Active Directory)

   ID: 017

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: DOMAIN ACCOUNT (T1087.002)

   DESCRIPTION: AdFind used to query Active Directory

   TOOLS: ADFIND (S0552)

   NOTE: -

 * Page #3:
   > ProcDump (a Microsoft SysInternals command-line utility used to perform analysis of running processes).

   ID: 018

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: ProcDump for analysis of running processes.

   TOOLS: PROCDUMP

   NOTE: -

 * Page #3:
   > WindowsCredentials Editor

   ID: 019

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of system credentials using Windows Credentials Editor

   TOOLS: WINDOWS CREDENTIALS EDITOR

   NOTE: -

 * Page #3:
   > Metasploit-related tools

   ID: 020

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: EXPLOITATION FOR PRIVILEGE ESCALATION (T1068)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Metasploit-related tools to exploit vulnerabilities and gain elevated privileges.

   TOOLS: METASPLOIT

   NOTE: -

   ---

   ID: 021

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Metasploit tools for remote access and privilege escalation.

   TOOLS: METASPLOIT

   NOTE -

 * Page #3:
   > FIN6 relies on credentials stolen from various systems (e.g. usernames and password hashes) for lateral movement

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using valid accounts for lateral movement

   TOOLS: -

   NOTE: -

   ---

   ID: 023

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of system credentials, such as usernames and password hashes.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Investigations show that FIN6 relies on PowerShell scripts and Meterpreter based shells to maintain access to and move laterally through the network (see below in the sectionTechnical Analysis and Indicators ofCompromise).

   ID: 024

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell scripts to maintain access and move laterally through the network

   TOOLS: -

   NOTE: -

   ---

   ID: 025

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESSS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using Meterpreter-based shells to maintain access and move laterally through the network

   TOOLS: METERPRETER

   NOTE: -

 * Page #6:
   > The malware checks network connectivity by sending an HTTP HEAD (GET in some new versions) request to the following legitimate URL: •hxxp://www[.]w3[.]org/1999/XSL/Format

   ID: 026

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: the malware use HTTP HEAD to check network connectivity

   TOOLS: -

   NOTE: -
