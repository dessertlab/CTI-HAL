## Detailed comments

 * Page #2:
   > CosmicDuke.

   ID: 000

   TOOLS: COSMICDUKE (S0050)

 * Page #2:
   > CosmicDuke infections start by tricking victims into opening either a PDF file that contains an exploit or a Windows executable whose filename is manipulated to make it look like a document or image file.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTE: -

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTE: -

 * Page #2:
   > keylogger

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Adversaries may use keylogging to capture keystrokes to collect credentials.

   TOOLS: -

   NOTE: -

 * Page #2:
   > password stealers

   ID: 007

    

   SOURCE: TEXT

    

   TACTIC: CREDENTIAL ACCESS (TA0006)

    

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: password

   stealers for a variety of popular chat, email and web browsing programs

    

   TOOLS: -

    

   NOTE: -

 * Page #2:
   > clipboard stealer

   ID: 005

    

   SOURCE: TEXT

    

   TACTIC: COLLECTION (TA0009)

    

   TECHNIQUE: CLIPBOARD DATA (T1115)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Theft of data in the system clipboard.

    

   TOOLS: -

    

   NOTE: -

 * Page #2:
   > screenshotter,

   ID: 006

    

   SOURCE: TEXT

    

   TACTIC: COLLECTION (TA0009)

    

   TECHNIQUE: SCREEN CAPTURE (T1113)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Capture of desktop screens or specific windows

    

   TOOLS: -

    

   NOTE: -

 * Page #2:
   > It also collects information about the files on the system

   ID: 008

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources, such as file systems and configuration files or local databases, to find files of interest and sensitive data prior to Exfiltration.

   TOOLS: -

   NOTE: -

 * Page #2:
   > has the capability to export cryptographic certificates and the associated private keys.

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: PRIVATE KEYS (T1552.004)

   DESCRIPTION: Adversaries may search compromised systems to find and obtain insecurely stored credentials. 

   TOOLS: -

   NOTE: -

 * Page #2:
   > it is sent out to remote servers via FTP

   ID: 010

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Cosmu allows the attacker to download and execute other malware on the system

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #3:
   > Keylogger

   ID: 016

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Adversaries may use keylogging to capture keystrokes to collect credentials.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Taking screenshots

   ID: 017

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use screen capture to collect information by capturing the screen content.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing data from clipboard

   ID: 018

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: CLIPBOARD DATA (T1115)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may collect data stored in the clipboard.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing files

   ID: 019

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources, such as file systems and configuration files or local databases, to find files of interest and sensitive data prior to Exfiltration.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing PKI certificates and associated private keys

   ID: 020

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: PRIVATE KEYS (T1552.004)

   DESCRIPTION: Adversaries may search compromised systems to find and obtain insecurely stored credentials. 

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing usernames and passwords from browsers, instant messengers and email clients y StealingWLAN passwords y StealingWindows password hashes

   ID: 021

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search for common password storage locations to obtain user credentials.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The information collected by the malware is automatically uploaded to remote servers via FTP

   ID: 022

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel.

   TOOLS: -

   NOTE:

 * Page #3:
   > It is possible that the PDF documents containing exploits were emailed to the targeted users as file attachments.

   ID: 013

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #3:
   > CosmicDuke samples use simple social engineering to trick the user into willingly launching the attack file

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTE: -

 * Page #3:
   > the malware's executable file is first disguised as an image or document to make it seem innocuous

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTE: -

 * Page #7:
   > It creates a scheduled task and installs a Windows service.

   ID: 023

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Adversaries may abuse the Windows Task Scheduler to perform task scheduling for initial or recurring execution of malicious code. 

   TOOLS: -

   NOTE: -

   ID: 024

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.003)

   DESCRIPTION: Adversaries may create or modify Windows services to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

 * Page #9:
   > The malware uses the FTP servers and WebDav servers both for exfiltrating the collected data and for updating the malware.

   ID: 025

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Cosmu uses RC4 to decrypt incoming data and encrypt outgoing data.

   ID: 026

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: STANDARD ENCODING (T1132.001)

   DESCRIPTION: Adversaries may encode data with a standard data encoding system to make the content of command and control traffic more difficult to detect.

   TOOLS: -

   NOTE: -

