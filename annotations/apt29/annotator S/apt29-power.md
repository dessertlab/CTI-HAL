## Detailed comments

 * Page #2:
   > These spear phishing messages were spoofed and made to appear to have been sent from real individuals at well-known think tanks in the United States and Europe.

   ID: 027

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may send phishing messages to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #2:
   > The Dukes are known for launching their attacks by sending links to ZIP files, that contain malicious executables, hosted on legitimate compromised web servers.

   ID: 029

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #2:
   > each of the e-mail messages from the August attacks contained a Microsoft O#ce Word (.doc) or Excel (.xls) attachment.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #3:
   > the attackers inserted macros into the documents designed to install a malware downloader on the system. Successful exploitation would result in the download of a PNG image file from a compromised webserver.

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

    

   NOTES: -

   ---

   ID: 030

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

    

   NOTES: -

 * Page #3:
   > These attack campaigns leveraged steganography in the PNG files by hiding components of a backdoor that would exist only in memory after being loaded into rundll32.exe.

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: STEGANOGRAPHY (T1027.003)

   DESCRIPTION: Adversaries may use steganography techniques in order to prevent the detection of hidden information. Steganographic techniques can be used to hide data in digital media such as images, audio tracks, video clips, or text files.

   TOOLS: -

    

   NOTES: -

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #3:
   > Three of the five attack waves contained links to download files from domains that the attackers appear to have control over.

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The other two attacks contained documents with malicious macros embedded within them.

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #3:
   > This message claims to have been sent from Secure Fax Corp. and has a link to a ZIP file that contains a Microsoft shortcut file (.LNK).

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #3:
   > This shortcut file contains PowerShell commands that conduct anti-VM checks,

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various techniques to detect and evade virtual machine or sandbox environments.

   TOOLS: -

   NOTES: -

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may use PowerShell commands to execute various actions on a system, including anti-VM checks.

   TOOLS: -

   NOTES: -

 * Page #5:
   > Primary PowerDuke backdoor (DLL) loader (leverages kxwn.lock:schemas) dropped to "%APPDATA\Roaming\Microsoft\" with persistence via HKCU Run Key "WebCache" (rundll32.exe %APPDATA\Roaming\Microsoft\kxwn.lock , #2).

   ID: 025

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1070.011)

   DESCRIPTION: The PowerDuke backdoor file is dropped with persistence via HKCU Run Key and executed via rundll32.exe.

   TOOLS: -

   NOTES: -

   ID: 026

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerDuke backdoor is persisted via HKCU Run Key.

   TOOLS: -

   NOTES: -

 * Page #6:
   > The second attack wave that Volexity observed leveraged a Microsoft Word document with a malicious embedded macro.

   ID: 010

   SOURCE: TEXT

   TACTIC:  EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #6:
   > The Macros contain several anti-VM checks designed to avoid executing in virtualized environments.

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various techniques to detect and evade virtual machine or sandbox environments.

   TOOLS: -

   NOTES: -

 * Page #9:
   > The fourth attack wave that Volexity observed leveraged a Microsoft Word document with a malicious embedded macro.

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #9:
   > The Macros contain several anti-VM checks designed to avoid executing in virtualized environments.

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various techniques to detect and evade virtual machine or sandbox environments.

   TOOLS: -

   NOTES: -

 * Page #11:
   > The link in the e-mail points to a ZIP file that has a Microsoft shortcut file (.LNK) inside of it.

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

    

   NOTES: -

 * Page #11:
   > This shortcut file contains PowerShell commands that conduct anti-VM checks, drop a backdoor, and launch a clean decoy document.

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various techniques to detect and evade virtual machine or sandbox environments.

   TOOLS: -

   NOTES: -

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may use PowerShell commands to execute various actions on a system, including anti-VM checks.

   TOOLS: -

   NOTES: -

 * Page #14:
   > The PowerDuke backdoor boasts a pretty extensive list of features that allow the Dukes to examine and control a system.

   ID: 028

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerDuke backdoor boasts a feature set that allows the attackers to examine the system.

   TOOLS: POWERDUKE (S0139)

   NOTES: -

 * Page #14:
   > comp get the NetBIOS name via GetComputerNameEx domain get the computer's domain via NetWkstaGetInfo

   ID: 017

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use various utilities to retrieve system network configuration information, such as NetBIOS name and domain information.

   TOOLS: -

   NOTES: comp get the NetBIOS name via GetComputerNameEx, domain get the computer's domain via NetWkstaGetInfo

 * Page #14:
   > drives get logical drives, drive type, free space, serial number, etc. fsize get the size of a file via GetFileAttributesExW or failing that, by mapping the file and getting the size

   ID: 018

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search for files and directories on local and remote systems.

   TOOLS: -

   NOTES: drives get logical drives, drive type, free space, serial number, etc., fsize get the size of a file via GetFileAttributesExW

 * Page #14:
   > memstat get memory usage status via GlobalMemoryStatusEx, total RAM, percent used, etc. osdate get the time the machine was built (via InstallDate registry key) osver get OS info via registry, such as ProductName, CurrentBuild, CurrentVersion, CSDBuildNumber, etc.

   ID: 020

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to gather information about the operating system and hardware.

   TOOLS: -

   NOTES: memstat get memory usage status via GlobalMemoryStatusEx, osdate get the time the machine was built (via InstallDate registry key), osver get OS info via registry

 * Page #14:
   > pslist list processes via CreateToolhelp32Snapshot

   ID: 019

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to get information about running processes on a system.

   TOOLS: -

   NOTES: pslist list processes via CreateToolhelp32Snapshot

 * Page #14:
   > run # start a process via CreateProcessW runs cmd.exe /c and gets the output via Named Pipe and sends the data back

   ID: 022

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: run start a process via CreateProcessW, # runs cmd.exe /c and gets the output via Named Pipe and sends the data back

 * Page #14:
   > siduser gets the current user's SID via GetTokenInformation and LookupAccountSidW

   ID: 021

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM OWNER/USER DISCOVERY (T1033)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may try to identify the current user of the system.

   TOOLS: -

   NOTES: siduser gets the current user's SID via GetTokenInformation and LookupAccountSidW

 * Page #15:
   > time the time + timezone (GetLocalTime and GetTimeZoneInformation)

   ID: 023

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM TIME DISCOVERY (T1124)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather the system time and time zone information from a local or remote system.

   TOOLS: -

   NOTES: time the time + timezone (GetLocalTime and GetTimeZoneInformation), uptime number of seconds since the last boot

