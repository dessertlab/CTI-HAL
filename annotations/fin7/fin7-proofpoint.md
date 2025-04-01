## Detailed comments

 * Page #1:
   > JScript backdoor called Bateleur

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The Bateleur backdoor, written in JScript, is executed as part of the attack chain, allowing remote code execution.

   TOOLS: -

   NOTE: -

 * Page #1:
   > The new macros and Bateleur backdoor use sophisticated anti-analysis and sandbox evasion techniques

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7's Bateleur backdoor and the updated macros use sophisticated methods to detect and evade sandboxes or analysis environments.

   TOOLS: -

   NOTE: -

 * Page #1:
   > the Vrst FIN7 change we observed was in the obfuscation technique found in their usual document attachments

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 changed their obfuscation techniques in the document attachments to hide malicious content.

   TOOLS: -

   NOTE: -

 * Page #1:
   > drop a previously undocumented JScript backdoor, which we have named "Bateleur"

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: FIN7 transitioned from their previous GGLDR script to a new JScript backdoor called Bateleur.execution.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The email is sent from an Outlook.com account, and the attachment document lure also matches that information by claiming "This document is encrypted by Outlook Protect Service".

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The email contains a malicious attachment designed to deceive the recipient into opening the file. The use of a service-specific lure, such as claiming encryption by Outlook Protect Service or Google Documents Protect Service, is a form of social engineering to persuade the victim to interact with the file.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #3:
   > The email contains a macro-laden Word document.

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The macro-laden Word document requires the user to open the file and enable the macro for execution, leading to the extraction of the JScript payload.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #3:
   > The caption contains a "|*|"-delimited obfuscated JScript payload

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The malicious payload is a JScript that is extracted and executed. JScript is a common scripting language used for automation and code execution.

   TOOLS: -

   NOTE: -

   LINK: 006, 008

 * Page #3:
   > The macro Vrst extracts the JScript from the caption then saves the content to debug.txt in the current user's temporary folder (%TMP%)

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: The macro writes the extracted JScript payload to the debug.txt file in the temporary folder, likely with the intent to delete this file after execution to evade detection and forensic analysis.

   TOOLS: -

   NOTE: -

   LINK: 007, 009

 * Page #3:
   > the macro creates a scheduled task

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The macro creates a scheduled task to ensure the execution of the JScript payload.

   TOOLS: -

   NOTE: -

   LINK: 008, 010

 * Page #3:
   > execute debug.txt as a JScript.

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The malicious payload is a JScript that is extracted and executed. JScript is a common scripting language used for automation and code execution.

   TOOLS: -

   NOTE: -

   LINK: 009, 011

 * Page #4:
   > Finally, the macro sleeps for 10 seconds then deletes the malicious scheduled task

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: his involves removing files that may indicate malicious activity, such as deleting scheduled tasks or other artifacts after they have been executed to avoid detection.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #4:
   > The malicious JScript has robust capabilities that include anti-sandbox functionality, anti-analysis (obfuscation)

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The adversary uses obfuscation to hide malicious code or make it harder to analyze.

   TOOLS: -

   NOTE: -

 * Page #4:
   > execution of  custom commands and PowerShell scripts

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The malware uses PowerShell scripts for executing commands.

   TOOLS: -

   NOTE: -

 * Page #4:
   > retrieval of infected system information

   ID: 013

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware gathers information about the infected system.

   TOOLS: -

   NOTE: -

 * Page #4:
   > listing of running processes

   ID: 014

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware lists running processes on the system.

   TOOLS: -

   NOTE: -

 * Page #4:
   > uninstalling and updating itself

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware can update itself by downloading new versions from the command and control server.

   TOOLS: -

   NOTE: -

 * Page #4:
   > loading of EXEs and DLLs

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware loads executables (EXEs) and dynamic-link libraries (DLLs) into memory.

   TOOLS: -

   NOTE: -

 * Page #4:
   > taking screenshots

   ID: 017

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware takes screenshots of the infected system.

   TOOLS: -

   NOTE: -

 * Page #4:
   > possibly the ability to exVltrate passwords, although the latter requires an additional module from the command and control server (C&C)

   ID: 019

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware exfiltrates credentials (passwords) from the victim's machine, though it requires an additional module from the C&C server.

   TOOLS: -

   NOTE: -

 * Page #4:
   > it creates a scheduled task "GoogleUpdateTaskMachineSystem" for persistence using the following command pattern: schtasks /Create /f /tn "GoogleUpdateTaskMachineSystem" /tr "wscript.exe //b /e:jscript C:\Users\[user account]\AppData\Local\Temp\{[hex]-[hex]-[hex]-[hex]-[hex]}\debug.txt" /sc minute /mo 5

   ID: 020

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: This technique involves the use of scheduled tasks to execute programs or scripts at a specific time or interval for persistence.

   TOOLS: -

   NOTE: -

   LINK: 046

   ---

   ID: 046

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: a legitimate name is used for the scheduled task

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #5:
   > Bateleur has anti-sandbox features but they do not appear to be used at this time.  This includes detection of Virtualbox, VMware, or Parallels via SMBIOSBIOSVersion and any of the following strings in DeviceID

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves malware checking the environment for signs of being run in a virtualized or sandboxed environment to avoid detection or analysis. Common checks include identifying virtual machines or sandbox-specific indicators.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Return various information about the infected machine, such as computer and domain name, OS, screen size,

   ID: 022

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves gathering information about the system to better understand the environment or to gather information useful for further attacks. This can include details like the computer name, operating system, and more.

   TOOLS: -

   NOTE: -

   LINK: 023

 * Page #5:
   > net view

   ID: 023

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE SCANNING (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves scanning network services to gather information about the network and potentially identify other systems and 

   TOOLS: -

   NOTE: -

 * Page #5:
   > Return running process list (name + id)

   ID: 014

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Listing the processes that are currently running on a system. 

   TOOLS: -

   NOTE: -

 * Page #5:
   > Delete installation Vle and path and remove scheduled task

   ID: 025

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: Removing installation file and path and remove scheduled tasks. 

   TOOLS: -

   NOTE: -

 * Page #6:
   > Perform a "load_exe" request to the C&C to retrieve an EXE

   ID: 026

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves transferring tools or other files to a compromised system. In this case, the load_exe request to the command and control (C&C) server to retrieve an executable file.

   TOOLS: -

   NOTE: -

   LINK: 027

 * Page #6:
   > write a cmd.exe command to a Vle named debug.cmd and then execute debug.cmd with cmd.exe

   ID: 027

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: This technique involves writing and executing commands or scripts. In this case, writing a cmd.exe command to a file and then executing it.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Perform a "load_exe" request to C&C to retrieve an EXE, save it as debug.log

   ID: 028

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: the load_exe request to the command and control (C&C) server to retrieve an executable file.

   TOOLS: -

   NOTE: -

   LINK: 029

 * Page #6:
   > execute the EXE via WMI

   ID: 029

   SOURCE: TEXT 

   TACTIC: EXECUTION (TA00002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves using Windows Management Instrumentation (WMI) to execute commands or scripts. Here, WMI is used to execute the retrieved EXE.

   TOOLS: -

   NOTE: -

   LINK: 028

 * Page #6:
   > Perform a "load_dll" request to the C&C to retrieve a DLL, save it as debug.backup

   ID: 030

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: the load_dll request to the command and control (C&C) server retrieves a DLL.

   TOOLS: -

   NOTE: -

   LINK: 031

 * Page #6:
   > write a regsvr32 command to a Vle named debug.cmd and then execute debug.cmd with cmd.exe

   ID: 031

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SIGNED SCRIPT PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: REGSVR32 (T1218.010)

   DESCRIPTION: a regsvr32 command is written to a file and then executed.

   TOOLS: -

   NOTE: -

   LINK: 030

 * Page #6:
   > Perform a "load_cmd" request to the C&C to retrieve a command to execute

   ID: 032

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: A command file is retrieved from the command and control (C&C) server.

   TOOLS: -

   NOTE: -

   LINK: 033

 * Page #6:
   > create temp Vle named log_[date].cmd containing command to execute, execute the command and sleep for 55 seconds

   ID: 033

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: a command is executed via a batch file

   TOOLS: -

   NOTE: -

   LINK: 032, 034

 * Page #6:
   > Send Vle output to the C&C via a POST request

   ID: 034

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Using web protocols (HTTP/HTTPS) for command and control communication. Sending the output of the executed command to the C&C server.

   TOOLS: -

   NOTE: -

   LINK: 033, 035

 * Page #6:
   > remove the temporary command Vle

   ID: 035

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: removing the temporary command file

   TOOLS: -

   NOTE: -

   LINK: 034

 * Page #6:
   > Perform a "load_powershell" request to the C&C to retrieve a command to execute

   ID: 036

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: A command file is retrieved from the command and control (C&C) server.

   TOOLS: -

   NOTE: -

   LINK: 037

 * Page #6:
   > create a temp Vle named log_[date].log containing a PowerShell command to execute, execute the command, and sleep for 55 seconds

   ID: 037

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION:  Executing commands via PowerShell.

   TOOLS: -

   NOTE: -

   LINK: 036, 038

 * Page #6:
   > Send Vle output to the C&C via a POST request

   ID: 038

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Sending the output of the executed command to the C&C server.

   TOOLS: -

   NOTE: -

   LINK: 037, 039

 * Page #6:
   > remove the temporary command Vle

   ID: 039

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: removing the temporary command file

   TOOLS: -

   NOTE: -

   LINK: 038

 * Page #6:
   > executes a PowerShell command via WMI

   ID: 040

   SOURCE: TEXT 

   TACTIC: EXECUTION (TA00002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using WMI to execute commands

   TOOLS: -

   NOTE: -

 * Page #6:
   > Take a screenshot and save it as screenshot.png in the install_path

   ID: 041

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capturing screenshots of the victim's machine.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Perform a "load_pass" request to the C&C to retrieve a PowerShell command

   ID: 042

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: A command file is retrieved from the command and control (C&C) server.

   TOOLS: -

   NOTE: -

   LINK: 043

 * Page #6:
   > PowerShell command containing a payload

   ID: 043

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: A PowerShell command containing a payload

   TOOLS: -

   NOTE: -

   LINK: 044

 * Page #6:
   > capable of retrieving user account credentials

   ID: 044

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Retrieving credentials

   TOOLS: -

   NOTE: -

 * Page #6:
   > The Bateleur C&C protocol occurs over HTTPS and is fairly straightforward with no additional encoding or obfuscation. Bateleur uses HTTP POST requests with a URI of "/?page=wait" while the backdoor is waiting for instructions.

   ID: 045

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Bateleur communicates with its C&C server using web protocols (HTTPS and HTTP POST), which is common for exfiltrating data and receiving commands.

   TOOLS: -

   NOTE: -

