## Detailed comments

 * Page #1:
   > PowerDuke

   ID: 000

   TOOLS: POWERDUKE (S0139)

 * Page #1:
   > These e-mails came from a mix of attacker created Google Gmail accounts and what appears to be compromised e-mail accounts at Harvard's Faculty of Arts and Sciences (FAS)

   ID: 001

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE ACCOUNTS (T1586)

   SUB-TECHNIQUE: EMAIL ACCOUNTS (T1586.002)

   DESCRIPTION: Attackers will compromise legitimate e-mail accounts to send phishing e-mails from seemingly trustworthy sources, thus increasing the likelihood that victims will fall for the deception.

   TOOLS: -

   NOTE: -

 * Page #2:
   > These spear phishing messages were spoofed and made to appear to have been sent from real individuals at well-known think tanks in the United States and Europe

   ID: 002

   SOURCE: TEXT

   TACTIC: INITAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1586)

   SUB-TECHNIQUE: -

   DESCRIPTION: phishing e-mails from seemingly trustworthy sources were sent.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The Dukes are known for launching their attacks by sending links to ZIP files, that contain malicious executables, hosted on legitimate compromised web servers

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING LINK (T1566.002)

   DESCRIPTION: Targeted phishing attacks that use links in emails to trick victims into clicking and downloading malicious files. This fits the description of attacks in which the Dukes send links to ZIP files containing malicious executables hosted on compromised legitimate Web servers.

   TOOLS: -

   NOTE: -

 * Page #2:
   > each of the e-mail messages from the August attacks contained a Microsoft O#ce Word (.doc) or Excel (.xls) attachment

   ID: 004

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Targeted phishing attacks that use attachments of Microsoft Office documents (.doc or .xls) to distribute malware. This fits perfectly with the description of attacks in which emails contain Word or Excel attachments.

   TOOLS: -

   NOTE: -

 * Page #3:
   > the attackers inserted macros into the documents designed to install a malware downloader on the system

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Users execute malicious files, such as documents with macros that download additional malicious payloads. The attacker inserts macros into documents that, when opened, execute a malware downloader.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Successful exploitation would result in the download of a PNG image file from a compromised webserver

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading malicious tools from a remote location. The attacker downloads a PNG file that contains the hidden components of the backdoor.

   TOOLS: -

   NOTE: -

 * Page #3:
   > These attack campaigns leveraged steganography in the PNG files by hiding components of a backdoor that would exist only in memory

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OF INFORMATION (T1027)

   SUB-TECHNIQUE: STEGANOGRAPHY (T1027.003)

   DESCRIPTION: Use of steganography to hide data within legitimate files. In this case, backdoor components are hidden within PNG images.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #3:
   > after being loaded into rundll32.exe

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Process injection techniques to execute malicious code inside a legitimate process. The backdoor is loaded into memory and executed via rundll32.exe, avoiding leaving traces on the disk.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #3:
   > Three of the five attack waves contained links to download files

   ID: 009

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING LINK (T1566.002)

   DESCRIPTION: Use of targeted phishing links in emails to induce victims to download malicious files. Attack waves contain links to download files.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The other two attacks contained documents with malicious macros embedded within them

   ID: 010

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending phishing emails with malicious attachments, such as documents with malicious macros.

   TOOLS: -

   NOTE: -

 * Page #3:
   > This message claims to have been sent from Secure Fax Corp. and has a link to a ZIP file that contains a Microsoft shortcut file (.LNK).

   ID: 011

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING LINK (T1566.002)

   DESCRIPTION: Use a link to a ZIP file in spear phishing emails.

   TOOLS: -

   NOTE: -

   LINK: 012

   ---

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: Induce the user to run the malicious .LNK file, often making it look legitimate or interesting.

   TOOLS: -

   NOTE: -

   LINK: 011, 013

 * Page #3:
   > This shortcut file contains PowerShell commands that conduct anti-VM checks

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes efforts to detect and avoid execution in virtualized or sandbox environments.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #5:
   > Primary PowerDuke backdoor (DLL) loader (leverages kxwn.lock:schemas) dropped to "%APPDATA\Roaming\Microsoft\" with persistence via HKCU Run Key "WebCache" (rundll32.exe %APPDATA\Roaming\Microsoft\kxwn.lock , #2).

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: The PowerDuke backdoor file is dropped with persistence via HKCU Run Key and executed via rundll32.exe.

   TOOLS: -

   NOTE: -

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerDuke backdoor is persisted via HKCU Run Key.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The second attack wave that Volexity observed leveraged a Microsoft Word document with a malicious embedded macro

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Microsoft Word document with a malicious embedded macro.

   TOOLS: -

   NOTE: -

   LINK: 015

 * Page #6:
   > The Macros contain several anti-VM checks designed to avoid executing in virtualized environments

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes efforts to detect and avoid execution in virtualized or sandbox environments.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #9:
   > The fourth attack wave that Volexity observed leveraged a Microsoft Word document with a malicious embedded macro

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Microsoft Word document with a malicious embedded macro.

   TOOLS: -

   NOTE: -

   LINK: 017

 * Page #9:
   > The Macros contain several anti-VM checks designed to avoid executing in virtualized environments.

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes efforts to detect and avoid execution in virtualized or sandbox environments.

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #11:
   > The link in the e-mail points to a ZIP file that has a Microsoft shortcut file (.LNK) inside of it.

   ID: 018

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEAR PHISHING LINK (T1566.002)

   DESCRIPTION: link to a ZIP file, which in turn contains a file

   TOOLS: -

   NOTE: -

   LINK: 019

 * Page #11:
   > This shortcut file contains PowerShell commands that conduct anti-VM checks,

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes efforts to detect and avoid execution in virtualized or sandbox environments.

   TOOLS: -

   NOTE: -

   LINK: 018

 * Page #14:
   > The PowerDuke backdoor boasts a pretty extensive list of features that allow the Dukes to examine and control a system

   ID: 023

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerDuke backdoor boasts a feature set that allows the attackers to examine the system

   TOOLS: POWERDUKE (S0139)

   NOTE: -

 * Page #14:
   > Volexity suspects the feature set that has been built into PowerDuke is an extension of their anti-VM capabilities in the initial dropper files

   ID: 020

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes efforts to detect and avoid execution in virtualized or sandbox environments.

   TOOLS: POWERDUKE (S0139)

   NOTE: -

 * Page #14:
   > comp get the NetBIOS name via GetComputerNameEx domain get the computer's domain via NetWkstaGetInfo

   ID: 024

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may use various utilities to retrieve system network configuration information, such as NetBIOS name and domain information.

    

   TOOLS: -

    

   NOTES: comp get the NetBIOS name via GetComputerNameEx, domain get the computer's domain via NetWkstaGetInfo

 * Page #14:
   > drives get logical drives, drive type, free space, serial number, etc. fsize get the size of a file via GetFileAttributesExW or failing that, by mapping the file and getting the size

   ID: 025

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may search for files and directories on local and remote systems.

    

   TOOLS: -

    

   NOTES: drives get logical drives, drive type, free space, serial number, etc., fsize get the size of a file via GetFileAttributesExW

 * Page #14:
   > memstat get memory usage status via GlobalMemoryStatusEx, total RAM, percent used, etc. osdate get the time the machine was built (via InstallDate registry key) osver get OS info via registry, such as ProductName, CurrentBuild, CurrentVersion, CSDBuildNumber, etc.

   ID: 026

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may attempt to gather information about the operating system and hardware.

    

   TOOLS: -

    

   NOTES: memstat get memory usage status via GlobalMemoryStatusEx, osdate get the time the machine was built (via InstallDate registry key), osver get OS info via registry

 * Page #14:
   > pslist list processes via CreateToolhelp32Snapshot

   ID: 027

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may attempt to get information about running processes on a system.

    

   TOOLS: -

    

   NOTES: pslist list processes via CreateToolhelp32Snapshot

 * Page #14:
   > run # start a process via CreateProcessW runs cmd.exe /c and gets the output via Named Pipe and sends the data back

   ID: 028

    

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

    

   TOOLS: -

    

   NOTES: run start a process via CreateProcessW, # runs cmd.exe /c and gets the output via Named Pipe and sends the data back

 * Page #14:
   > siduser gets the current user's SID via GetTokenInformation and LookupAccountSidW

   ID: 029

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM OWNER/USER DISCOVERY (T1033)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may try to identify the current user of the system.

    

   TOOLS: -

    

   NOTES: siduser gets the current user's SID via GetTokenInformation and LookupAccountSidW

 * Page #15:
   > time the time + timezone (GetLocalTime and GetTimeZoneInformation)

   ID: 030

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM TIME DISCOVERY (T1124)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may gather the system time and time zone information from a local or remote system.

    

   TOOLS: -

    

   NOTES: time the time + timezone (GetLocalTime and GetTimeZoneInformation), uptime number of seconds since the last boot

