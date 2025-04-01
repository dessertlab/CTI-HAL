## Detailed comments

 * Page #2:
   > the agent opened the attachment contained in the email

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attacker uses social engineering to convince the agent to open a malicious email attachment. The email contains a malicious Word document.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > The email attachment was a malicious Word Document

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The agent executes the malicious attachment, triggered by the attacker. The malicious Word document contains the encoded .VBS script.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > that contained an encoded .VBS script capable of

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The attack involves a .VBS script that performs various malicious activities.

   TOOLS: -

   NOTE: -

   LINK: 002, 004, 005, 006

 * Page #2:
   > stealing system information

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: The script is capable of stealing system information.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > desktop screenshots

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: The script takes desktop screenshots.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > to download additional malware

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The encoded .VBS script downloads additional malware after being executed on the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > The malicious VB Script will use macros to search for instances of Microsoft Word running on the system

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: This involves the use of Visual Basic scripts to execute commands on the system, which is what the malicious VB Script is doing.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The victim system will then reach out to http://95.215.47.105 to retrieve additional malware called AdobeUpdateManagementTool.vbs

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves transferring tools or files from an external system into the victim environment. The victim system retrieves the additional malware from http://95.215.47.105.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #3:
   > Adds file to WindowsUpdate folder: vbs

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves transferring tools or files to the victim system. The malware adds the VBS file to the `WindowsUpdate` folder.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Adds persistence mechanism to the CURRENT_USER registry hive in the CurrentVersion\Run and CurrentVersion\RunOnce keys to autostart AdobeUpdateManagementTool.

   ID: 010

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1547.001)

   DESCRIPTION: This technique involves adding registry keys to automatically execute programs upon user logon. The malware adds entries to the `CurrentVersion\Run` and `CurrentVersion\RunOnce` keys.

   TOOLS: -

   NOTE: -

 * Page #3:
   > A scheduled task is created named SysChecks which calls the vbs

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: This technique involves using scheduled tasks for persistence. The malware creates a scheduled task named `SysChecks` to execute the VBS script.

   TOOLS: -

   NOTE: -

 * Page #4:
   > A service is created named 'ADOBEUPDTOOL' which calls the AdobeUpdateManagementTool.vbs

   ID: 012

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves creating or modifying Windows services for persistence or to execute malicious code.

   TOOLS: -

   NOTE: A service named 'ADOBEUPDTOOL' is created to call the `AdobeUpdateManagementTool.vbs`.

 * Page #4:
   > The malware drops a Shockwave Flash icon and disguises itself as such

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: his technique involves disguising malicious files or processes to appear as legitimate ones.

   TOOLS: -

   NOTE: The malware disguises itself as a Shockwave Flash icon.

 * Page #4:
   > The malware contacts the following and may attempt to download doc:

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTE: The malware attempts to download a file (possibly a document) from an external server.

 * Page #4:
   > This malware was capable of stealing significant system and network information

   ID: 015

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to get detailed information about the system they are targeting.

   TOOLS: -

   NOTE: The malware is capable of stealing significant system information.

 * Page #4:
   > It was also used to download several other reconnaissance tools to map out the network.

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA00011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: NMAP, FREEDRP, NCAT, NPING

   NOTE: The malware downloads several reconnaissance tools such as Nmap, FreeRDP, NCat, NPing, and others.

 * Page #5:
   > Downloaded tools have included Nmap, FreeRDP, NCat, NPing, and others

   ID: 068

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware downloads several reconnaissance tools like Nmap, FreeRDP, NCat, NPing to map out the network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > it also downloaded additional malware that enables the next stage of the attack

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA00011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTE: The system reaches out to retrieve additional malware.

   LINK: 018

 * Page #5:
   > could execute powershell scripts on command

   ID: 018

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution.

   TOOLS: -

   NOTE: The malware can execute PowerShell scripts on command.

 * Page #5:
   > Beaconing messages are sent out to 179.43.133.34 via standard HTTP GET requests every 5 minutes

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries may use web protocols like HTTP to communicate with their command and control (C2) servers.

   TOOLS: -

   NOTE: Beaconing messages are sent out via standard HTTP GET requests, indicating the use of HTTP for communication.

 * Page #5:
   > The content of the GET request is encoded with Base64 and secondarily encrypted with RC4

   ID: 020

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use various methods to obfuscate data to evade detection.

   TOOLS: -

   NOTE: The content of the GET request is Base64 encoded and encrypted with RC4, indicating an attempt to obfuscate the traffic.

 * Page #7:
   > This malware executes a new iteration of svchost.exe and injects its malicious code into this running process

   ID: 021

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may inject code into the address space of another process to evade detection and achieve persistence.

   TOOLS: CARBANAK (S0030)

   NOTE: The malware injects its code into a running `svchost.exe` process to hide its presence.

   LINK: 022

 * Page #7:
   > It then drops a pseudo-randomly named configuration file into the %ProgramData%\Mozilla folder. This file's name is base64 encoded and based on the infected system's MAC code, so identifying it by name will be challenging.

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use masquerading to disguise their files or processes as something legitimate to avoid detection.

   TOOLS: CARBANAK (S0030)

   NOTE: The malware drops a configuration file with a pseudo-random name and a `.bin` extension, making it harder to identify or distinguish from legitimate files. The name is based on the MAC address and is base64 encoded to further obfuscate its purpose.

   LINK: 021, 023

 * Page #8:
   > It then searches Kaspersky antivirus processes and terminates them if running on the victim system.

   ID: 023

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DISABLING SECURITY TOOLS (T1089)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may disable or interfere with security tools to prevent them from detecting or responding to the attack.

   TOOLS: CARBANAK (S0030)

   NOTE: Specifically, terminating antivirus processes falls under this technique as it directly impacts the functionality of security tools on the system.

   LINK: 022, 024

   ---

   ID: 069

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: IMPAIR DEFENSE (T1562)

   SUB-TECHNIQUE: DISABLE OR MODIFY TOOLS (T1562.001)

   DESCRIPTION: The malware searches Kaspersky antivirus processes and terminates them if running on the victim system.

   TOOLS: -

   NOTE: -

 * Page #8:
   > it registers itself as a service with the following details: Service name: RpcSsSys (this name is random, may vary on different system)

   ID: 024

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM SERVICE (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.003)

   DESCRIPTION: Adversaries may create or modify Windows services to ensure their malware runs automatically when the system starts or when a service is started.

   TOOLS: CARBANAK (S0030)

   NOTE: The text describes registering the malware as a Windows service with a specific service name, path, and display name, which aligns with creating or modifying a system service for persistence.

   LINK: 023

 * Page #8:
   > steal local passwords

   ID: 025

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may dump credentials to obtain user passwords or hashes.

   TOOLS: CARBANAK (S0030)

   NOTE: The malware's ability to steal local passwords indicates it may use credential dumping techniques.

 * Page #9:
   > install completely different remote desktop programs, such as VNC or AMMYY

   ID: 026

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use remote access tools to control systems and maintain persistence.

   TOOLS: CARBANAK (S0030)

   NOTE: The installation of remote desktop programs (such as VNC or AMMYY) is a classic example of using remote access tools for control and persistence.

 * Page #9:
   > It communicates via an encrypted tunnel on port 443

   ID: 027

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICAITON LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries use application layer protocols for command and control (C2) communications.

   TOOLS: -

   NOTE: The malware communicates via an encrypted tunnel over port 443 and sends data via HTTP POST messages.

 * Page #9:
   > screen captures

   ID: 028

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture screenshots to gather information from the victim's desktop.

   TOOLS: -

   NOTE: The malware is capable of stealing screen captures.

 * Page #9:
   > email addresses from the PST file

   ID: 030

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather data from local systems for exfiltration.

   TOOLS: -

   NOTE: The malware collects various types of data, including email addresses from PST files.

 * Page #9:
   > keylogger information

   ID: 029

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Adversaries may capture keystrokes to gather information from the victim.

   TOOLS: -

   NOTE: -

 * Page #10:
   > The file is OLE compound file format that contains an embedded .VBE (encoded VBS) script

   ID: 031

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: This technique involves the use of scripting languages such as VBS (Visual Basic Script) to execute malicious actions. The .VBE (encoded VBS) script is a form of scripting used to perform various actions.

   TOOLS: -

   NOTE: The embedded .VBE script in the OLE compound file performs actions such as stealing system information and screenshots, and downloading additional malware.

   LINK: 032, 033, 034, 035

 * Page #10:
   > stealing system information

   ID: 032

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather data from local systems for exfiltration.

   TOOLS: -

   NOTE: -

   LINK: 031

 * Page #10:
   > desktop screenshots

   ID: 033

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture screenshots to gather information from the victim's desktop.

   TOOLS: -

   NOTE: The malware is capable of stealing screen captures.

   LINK: 031

 * Page #10:
   > download / execute additional malware

   ID: 034

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA00011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTE: The system reaches out to retrieve additional malware.

   LINK: 031

 * Page #11:
   > When the malicious document file is opened, the embedded VBScript (VBE) file is dropped in the Windows %temp% folder.

   ID: 035

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves configuring the system to execute the malicious payload during system boot or user logon. Although not directly related to dropping the VBScript, the placement in %temp% could be part of a persistence mechanism.

   TOOLS: -

   NOTE: -

   LINK: 031

 * Page #11:
   > The dropped VBE file is a loader script that drops, installs and executes

   ID: 036

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA00011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTE: -

   LINK: 037

 * Page #11:
   > a second layer VBScript payload in the victim's system.

   ID: 037

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: This technique involves the use of scripting languages such as VBS (Visual Basic Script) to execute malicious actions.

   TOOLS: -

   NOTE: -

   LINK: 036, 038

 * Page #11:
   > It creates a folder named "WindowsUpdate_" in the Window's %temp% directory, If the folder already exists, it will create the folder in the parent directory where the script resides.

   ID: 038

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION:  This technique involves disguising files or processes to make them appear legitimate. The creation of the "WindowsUpdate_" folder and the naming conventions used may be attempts to blend in with legitimate system operations.

   TOOLS: -

   NOTE: The folder named "WindowsUpdate_" is an example of masquerading, as it attempts to appear as a legitimate Windows folder.

   LINK: 037

 * Page #12:
   > A registry key is created that points to the Loader's directory sh.RegWriTe"HKEY_CURRENT_USER\System\CurrentControlSet\Control

   ID: 039

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOTT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves creating or modifying registry entries to ensure that the malware executes automatically upon system boot or user logon.

   TOOLS: -

   NOTE: y creating a registry key that points to the directory containing the loader, the malware can ensure that its components are executed automatically when the system starts or when a user logs in.

 * Page #12:
   > The second VBScript payload is embedded in the loader script as a Base64 string

   ID: 040

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves encoding or obfuscating files or information to hide their true purpose. The use of Base64 encoding is a form of obfuscation that helps to evade detection by making the payload less recognizable.

   TOOLS: -

   NOTE: The second VBScript payload is encoded in Base64 to obscure its content within the loader script.

 * Page #12:
   > The loader script decodes the base64 string

   ID: 041

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves decoding or deobfuscating information to make it usable. The loader script decodes the Base64 string to retrieve the VBScript payload.

   TOOLS: -

   NOTE: The decoding process is a key step in making the malicious VBScript operational.

 * Page #12:
   > This is then saved to a file named "AdobeUpdateManagementTool.vbs" into the "\WindowsUpdate_" folder

   ID: 042

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves transferring tools or files into a compromised system. The VBScript file is saved and created in the target system's directory.

   TOOLS: -

   NOTE: The decoded VBScript is saved to a file in the \WindowsUpdate_ folder, transferring the malicious payload onto the system.

 * Page #12:
   > A persistence registry key is also created by the loader script: HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run

   ID: 043

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/STARTUP (T1547.001)

   DESCRIPTION: Adversaries may achieve persistence by adding a program to a startup folder or referencing it with a Registry run key. These mechanisms ensure that the program runs each time the user logs in or the system starts.

   TOOLS: -

   NOTE: The loader script creates a registry key under `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run` to ensure that the script runs at startup, providing persistence on the infected system.

 * Page #12:
   > The loader script adds a scheduled task with a task named "SysChecks". The purpose of this scheduled task is to run the payload script (AdobeUpdateManagementTool.vbs) in every 5 minutes

   ID: 044

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION:  Adversaries may abuse task scheduling functionality to facilitate initial or recurring execution of malicious code. This can be used to execute code at a specific time or on a recurring schedule.

   TOOLS: -

   NOTE: The loader script creates a scheduled task named "SysChecks" to run the payload script (AdobeUpdateManagementTool.vbs) every 5 minutes. This ensures that the malicious script executes periodically, maintaining the persistence of the malware.

 * Page #13:
   > A SWF icon file is also dropped in the folder in order to disguise the dropped file as a Shockwave Flash file

   ID: 045

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MASQUERADE FILE TYPE (T1036.008)

   DESCRIPTION: Adversaries may change the file extension of a file to match a different file type. They can use this tactic to disguise files as benign or known types, making them less likely to be detected or scrutinized by security tools or users.

   TOOLS: -

   NOTE: The malware drops a SWF (Shockwave Flash) icon file to disguise the dropped file as a Shockwave Flash file. This masquerading helps evade detection by making the malicious file appear as a legitimate and familiar file type.

 * Page #13:
   > A shortcut file is also added in the Windows startup folder as "AdobeUpdateManagementTool.lnk"

   ID: 046

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: SHORTCUT MODIFICATION (T1547.009)

   DESCRIPTION: Adversaries may create or modify shortcut files (.lnk) that are automatically started at boot or logon to execute malware or other malicious code. This technique involves placing shortcuts in specific locations, such as the startup folder, to achieve persistence.

   TOOLS: -

   NOTE:  The malware adds a shortcut file named "AdobeUpdateManagementTool.lnk" in the Windows startup folder. This ensures that the malware runs every time the system starts, providing a persistent foothold on the infected system.

 * Page #13:
   > script uses obfuscation, a combination of base64 and integer-ed characters (chr) to hide malicious code

   ID: 047

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of base64 encoding and integer-ed characters (chr) to obfuscate the script. This more accurately reflects the described obfuscation of the VBScript payload.

   TOOLS: -

   NOTE: -

 * Page #14:
   > Steal system information System Name System Manufacturer System Model Time Zone Total Physical Memory Processor System Type Processor BIOS Version Networking information Computer name Domain User name

   ID: 048

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collecting information about the system, such as system name, system manufacturer, system model, total physical memory, processor details, BIOS version, and system type.

   TOOLS: -

   NOTE: -

 * Page #15:
   > A powershell script (filename: screenshot__.ps1) is created

   ID: 049

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The creation and execution of a PowerShell script.

   TOOLS: -

   NOTE: -

   LINK: 050

 * Page #15:
   > to screenshot victim's desktop

   ID: 050

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may capture screenshots of the victim's desktop.

   TOOLS: -

   NOTE: -

   LINK: 049

 * Page #15:
   > It may also be able to receive additional malware executables and install them on the victim's computer.

   ID: 051

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware can receive additional executables from the attacker and install them on the victim's system. This technique involves transferring tools or files to a compromised system.

   TOOLS: -

   NOTE: -

 * Page #16:
   > The data is sent as a data encrypted with RC4 and Base64 It is sent via an HTTP POST tunnel to the attacker's server

   ID: 052

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The data is encrypted with RC4 and Base64, which constitutes obfuscation. Obfuscation techniques are used to make it harder for security tools to analyze or detect the exfiltrated data.

   TOOLS: -

   NOTE: -

 * Page #16:
   > It can receive commands from the attacker to download and execute EXE files, VBScript, or Powershell script files.

   ID: 051

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware can download and execute EXE files, VBScript, or PowerShell scripts, which aligns with the use of a backdoor to transfer tools or additional payloads into the victim's system.

   TOOLS: -

   NOTE: -

 * Page #17:
   > screenshot__.ps1 - a powershell script that takes screenshots of the active desktop

   ID: 054

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Powershell script 

   TOOLS: -

   NOTE: -

 * Page #18:
   > vb__.vbs - a VBscript sent by the attacker

   ID: 055

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: a VBscript

   TOOLS: -

   NOTE: -

 * Page #18:
   > ps1__.ps1 - a Powershell script sent by the attacker

   ID: 056

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: A PowerShell script.

   TOOLS: -

   NOTE: -

 * Page #23:
   > it writes the cmdunig value to this registry key: HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion

   ID: 057

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1547.001)

   DESCRIPTION: If the registry key is used to ensure the malware runs on startup or after a logon, this technique applies.

   TOOLS: -

   NOTE: -

 * Page #23:
   > Following is the System information sent to the control server when the command "INFO" is received from the attacker. OS Name Version Service Pack OS Manufacturer Windows Directory Locale Available Physical Memory Total Virtual Memory Available Virtual Memory System Name System Manufacturer System Model Time Zone Total Physical Memory Processor System Type Processor BIOS Version Computer name Domain User name

   ID: 058

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collecting information about the system, such as system name, system manufacturer, system model, total physical memory, processor details, BIOS version, and system type.

   TOOLS: -

   NOTE: -

 * Page #23:
   > This system information is also stored in this registry key: HKEY_CURRENT_USER\System\CurrentControlSet\Control\Network\CLM

   ID: 059

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware interacts with the Windows registry, specifically modifying registry keys

   TOOLS: -

   NOTE: -

 * Page #26:
   > The config filename is a base64 string comprising of a unique string and the MAC address of the infected system

   ID: 060

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The configuration filename is a base64 string, indicating the use of obfuscation.

   TOOLS: -

   NOTE: -

 * Page #26:
   > injects its code to that process

   ID: 061

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005),  PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: he malware injects its code into a new `svchost.exe` process. Process injection is a common technique used to execute malicious code within the context of a legitimate process to evade detection and 

   TOOLS: -

   NOTE: -

 * Page #26:
   > it registers itself as a service with the following details: Service name: RpcSsSys (this name is random, may vary on different systems)

   ID: 062

   SOURCE: text

   TACTIC: PERSITENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware creates a new Windows service to ensure its persistence. It sets up the service with a path that disguises its true nature, often using a name that mimics legitimate services.

   TOOLS: -

   NOTE: -

 * Page #26:
   > The malware checks for the "isDebugged" flag in the PEB (Process Environment Block). It also checks for significant delay of code execution by utilizing the GetTickCount() function.

   ID: 070

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005),  DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: SYSTEM CHECKS (T1497.001)

   DESCRIPTION: The malware checks the \"isDebugged\" flag in the PEB (Process Environment Block) and also checks for significant delay of code execution by utilizing the GetTickCount() function to detect if the process is being debugged

   TOOLS: -

   NOTE: -

 * Page #27:
   > Strings are heavily obfuscated to avoid static string analysis

   ID: 063

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Strings are obfuscated to avoid static string analysis

   TOOLS: -

   NOTE: -

 * Page #29:
   > The malware enables the Remote Desktop by starting the Termservice service

   ID: 064

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves using remote services such as Remote Desktop Protocol (RDP) or other remote access tools. Enabling and configuring Remote Desktop is a direct use of this technique to maintain access to the system.

   TOOLS: -

   NOTE: -

   LINK: 065

 * Page #29:
   > It also sets the service to auto-mode so that the service will start on Windows startup.

   ID: 065

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION:  Modifying the Termservice service to start automatically on Windows startup is a form of persistence where the malware ensures that it will be able to reconnect to the system after a reboot.

   TOOLS: -

   NOTE: -

 * Page #30:
   > The malware utilizes the open source project called Mimikatz and reused codes from this project to steal clear text local passwords from Lsass memory dump.

   ID: 066

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves extracting credentials from operating system memory, files, or other sources. Mimikatz is a well-known tool for credential dumping, and its use to extract passwords from LSASS memory falls directly under this technique.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #31:
   > $"  ammyy.pl- this enables the malware to run AMMYY remote desktop control software %"  vnc.pl- this enables the malware to run a remote desktop VNC application

   ID: 067

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: This technique involves the use of Remote Desktop Protocol (RDP) for remote access to systems. While the text specifically mentions Ammyy and VNC, RDP is a common protocol for similar purposes.

   TOOLS: AMMYY, VNC

   NOTE: -

