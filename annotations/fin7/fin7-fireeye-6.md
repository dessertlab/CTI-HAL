## Detailed comments

 * Page #2:
   > FIN7 phishing lures implements hidden sho%cut "les (LNK "les) to initiate the infection

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of LNK files and VBScript, along with mshta.exe, are methods used to exploit the client system for execution of the malware.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > VBScript functionality launched by mshta.exe to infect the victim

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The use of VBScript and mshta.exe demonstrates the application of scripting to achieve malicious goals.

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #2:
   > FIN7 is targeting organizations with spear phishing emails containing either a malicious DOCX or RTF "le – two versions of the same LNK "le and VBScript technique

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: targeting individuals or organizations with phishing emails that contain malicious attachments, such as DOCX or RTF files. The goal is to deceive the recipient into opening the attachment and executing the embedded malware.

   TOOLS: -

   NOTE: -

 * Page #3:
   > By requiring this unique interaction – doubleclicking on the image and clicking the "Open" bu!on in the security warning popup – the phishing lure a!empts to evade dynamic detection as many sandboxes are not con"gured to simulate that speci"c user action.

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The combined script from Word textbox drops the following components: \Users\ [user_name]\Intel\58d2a83f7778d5.36783181.v bs \Users\ [user_name]\Intel\58d2a83f777942.26535794. ps1 \Users\ [user_name]\Intel\58d2a83f777908.23270411.v bs

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

   NOTE: -

 * Page #5:
   > the script creates a named schedule task for persistence to launch "58d2a83f7778d5.36783181.vbs" every 25 minutes.

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: how a scheduled task is set up to execute a VBScript file at a specified interval for maintaining persistence on the system.​

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #6:
   > This VBScript checks if the "58d2a83f777942.26535794.ps1" PowerShell script is running using WMI queries and, if not, launches it.

   ID: 005

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: The VBScript is using WMI queries to check if a particular PowerShell script is running, which is an example of process discovery. This technique involves identifying running processes on a system. If the process is not found, the script then starts it, ensuring the required script is active.​

   TOOLS: -

   NOTE: -

   LINK: 004, 006

 * Page #6:
   > "58d2a83f777942.26535794.ps1" is a multilayer obfuscated PowerShell script, which launches shellcode for a Cobalt Strike stager

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: This TTP involves the use of PowerShell scripts for execution. The script mentioned is heavily obfuscated and is used to execute shellcode.

   TOOLS: -

   NOTE: -

   LINK: 005

   ---

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The shellcode retrieves an additional payload by connecting to the following C2 server using DNS: aaa.stage.14919005.www1.proslr3[.]com

   ID: 007

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: the use of DNS for command and control (C2) communications. The shellcode retrieves further payloads by connecting to a C2 server using DNS queries.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #6:
   > Once a successful reply is received from the command and control (C2) server, the PowerShell script executes the embedded Cobalt Strike shellcode

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: This TTP involves the use of PowerShell scripts for execution. The script mentioned is heavily obfuscated and is used to execute shellcode.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #8:
   > info: Sends victim machine information (OS, Processor, BIOS and running processes) using WMI queries

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0009)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: gathering information about the victim's system, such as operating system details, processor information, BIOS version, and running processes. This is done using WMI queries, which helps the attacker understand the environment and plan further actions.

   TOOLS: -

   NOTE: -

   ---

   ID: 021

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0009)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Sends victim machine information (OS, Processor, BIOS, and running processes) using WMI queries.

   TOOLS: -

   NOTE: -

 * Page #8:
   > processList: Send list of process running

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: identifying and listing the processes currently running on the victim's system

   TOOLS: -

   NOTE: -

 * Page #8:
   > screenshot: Takes screen shot of victim machine

   ID: 011

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: capturing screenshots of the victim's desktop

   TOOLS: -

   NOTE: -

 * Page #8:
   > runvbs: Executes a VB script

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The use of VBScript

   TOOLS: -

   NOTE: -

 * Page #8:
   > runps1: Executes PowerShell script

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: the use of PowerShell scripts for execution

   TOOLS: -

   NOTE: -

 * Page #8:
   > delete: Delete the speci"ed "le

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: the delete function is used to remove specified files

   TOOLS: -

   NOTE: -

 * Page #9:
   > encoded using the following technique, represented in pseudo code: Function send_data(data) random_string = custom_function_to_generate_random_string

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTE: -

 * Page #9:
   > the document creates two scheduled tasks and creates one auto-sta% registry entry pointing to the LNK "le

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: creating tasks or jobs that run at specified intervals or times to maintain persistence on the victim system

   TOOLS: -

   NOTE: -

   ---

   ID: 018

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1547.001)

   DESCRIPTION: Adversaries may achieve persistence by adding a program to a startup folder or referencing it with a Registry run key.

   TOOLS: -

   NOTE: -

