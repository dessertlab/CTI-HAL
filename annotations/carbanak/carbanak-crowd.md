## Detailed comments

 * Page #1:
   > Anunak

   ID: 001

   TOOLS: ANUNAK (S0030)

   LINK: 002, 003, 004, 005, 006, 007

 * Page #1:
   > Primary remote access toolkit (RAT) for monitoring victim systems of interest

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of remote access software to control victims' machines.

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > It contains all the functionality you would expect from a RAT, allowing the adversary to execute commands, manage the file system, manage processes, and collect data

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using remote access software to execute commands and manage victim systems.

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > it can record videos of victim sessions

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capture of compromised system screenshots

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > install Ammyy Admin or VNC modules

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EXTERNAL REMOTE SERVICES (T1133)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of external remote services to maintain compromised system access.

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > log keystrokes

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Capture of keyboard inputs.

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > enable remote desktop

   ID: 006

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Using RDP to access and control the victim's system.

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #1:
   > Agent ORM

   ID: 008

   TOOLS: AGENT ORM

   LINK: 009, 010, 011

 * Page #1:
   > The malware collects basic system information

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of basic system information.

   TOOLS: AGENT ORM

   NOTE: -

   ---

   ID: 030

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware collects basic system information and is able to take screenshots of victim systems

   TOOLS: AGENT ORM

   NOTE: -

 * Page #1:
   > take screenshots of victim systems

   ID: 010

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capture of compromised system screenshots

   TOOLS: AGENT ORM

   NOTE: -

 * Page #1:
   > It is used to download next-stage payloads when systems of interest are identified

   ID: 011

   SOURCE:  TEXT

   TACTIC: COMMAND AND CONTROLE (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of additional tools or payloads to the compromised system.

   TOOLS: AGENT ORM

   NOTE: -

 * Page #1:
   > VB Flash

   ID: 012

   TOOLS: VB FLASH

   LINK: 013, 014

 * Page #1:
   > Several versions of VB Flash were developed including ones that utilized Google Forms, Google Macros, and Google Spreadsheets together to make a command-and-control (C2) channel

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of legitimate web services for command and control.

   TOOLS: VB FLASH

   NOTE: -

 * Page #1:
   > This variant would POST victim data to a specified Google form, then make a request to a Google macro script, receiving an address for a Google Spreadsheet from which to request commands

   ID: 014

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER WEB SERVICE (T1567)

   SUB-TECHNIQUE: -

   DESCRIPTION: Data exfiltration through legitimate web services.

   TOOLS: VB FLASH

   NOTE: -

 * Page #1:
   > JS Flash

   ID: 015

   TOOLS: JS FLASH

   LINK: 016, 017, 018, 019

 * Page #1:
   > JS Flash capabilities closely resemble those of VB Flash and leverage interesting techniques in deployment via batch scripts embedded as OLE objects in malicious documents

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Using the Windows command shell to execute commands and scripts.

   TOOLS: JS FLASH

   NOTE: -

 * Page #1:
   > minor changes to obfuscation

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of files or information to avoid detection.

   TOOLS: JS FLASH

   NOTE: -

 * Page #1:
   > ability to downloadTinyMet(a cutdown of theMetasploit Meterpreterpayload)

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRASNFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of additional tools or payloads to the compromised system.

   TOOLS: JS FLASH, METERPETER

   NOTE: -

 * Page #1:
   > PowerShell was also used heavily for the execution of commands and arbitrary script execution

   ID: 019

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute arbitrary commands and scripts.

   TOOLS: JS FLASH

   NOTE: -

 * Page #1:
   > Bateleur

   ID: 020

   TOOLS: BATELEUR

   LINKS: 021, 022, 023, 024, 025

 * Page #1:
   > download arbitrary scripts and executables, deploy TinyMet

   ID: 021

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOLS TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of additional tools or payloads to the compromised system.

   TOOLS: BATELEUR

   NOTE: -

 * Page #1:
   > execute commands via PowerShell

   ID: 022

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute commands.

   TOOLS: BATELEUR

   NOTE: -

 * Page #1:
   > deploy a credential stealer

   ID: 023

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: Extraction of credentials from password repositories

   TOOLS: BATELEUR

   NOTE: -

 * Page #1:
   > collect victim system information

   ID: 024

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of system information.

   TOOLS: BATELEUR

   NOTE: -

 * Page #1:
   > spear phishing emails to deploy malicious documents

   ID: 025

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0002)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of spear phishing attachments to gain initial access.

   TOOLS: -

   NOTE: -

   LINK: 026, 027

 * Page #1:
   > used exploits

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using exploits to execute code on the victim's machine.

   TOOLS: -

   NOTE: -

   LINK: 025

 * Page #1:
   > they have used macros and OLE embedded objects

   ID: 027

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS DOCUMENT (T1204.002)

   DESCRIPTION: Use of malicious documents that require user intervention for execution.

   TOOLS: -

   NOTE: -

   LINK: 025

 * Page #1:
   > that use exploits for a variety of vulnerabilities in Microsoft Office: CVE-2015-2545 CVE-2014-4114 CVE-2015-1770 CVE-2015-1641

   ID: 029

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using exploits to execute code on the victim's machine.

   TOOLS: -

   NOTE: Spear phishing attachments exploit various vulnerabilities in Microsoft Office (CVE-2015-2545, CVE-2014-4114, CVE-2015-1770, CVE-2015-1641) to execute malicious code.

   LINK: 028

 * Page #1:
   > spear phishing emails

   ID: 028

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0002)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of spear phishing attachments to gain initial access.

   TOOLS: -

   NOTE: -

   LINK: 029

