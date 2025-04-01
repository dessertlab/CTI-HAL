## Detailed comments

 * Page #1:
   > CozyDuke

   ID: 000

   TOOLS: COZYDUKE (S0046)

 * Page #2:
   > The actor often spearphishes targets with e-mails containing a link to a hacked website

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Sending spearphishing emails with links to a compromised website.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > Sometimes it is a high pro#le, legitimate site such as "diplomacy.pl", hosting a ZIP archive.

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: DRIVE-BY COMPROMISE (T1189)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using a legitimate website (in this case "diplomacy.pl") to host a ZIP archive containing a malicious executable.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > The ZIP archive contains a RAR SFX which installs the malware

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using a self-extracting RAR file (RAR SFX) that, when executed by the user, installs the malware.

   TOOLS: -

   NOTE: -

   LINK: 002

   ---

   ID: 026

    

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

    

   TOOLS: -

    

   NOTES: -

    

 * Page #2:
   > this actor sends out phony $ash videos directly as email attachments

   ID: 004

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENTS (T1566.001)

   DESCRIPTION: Sending spearphishing emails with phony flash videos as attachments.

   TOOLS: -

   NOTE: -

   LINK: 005, 006

 * Page #2:
   > The executable within not only plays a $ash video, but drops and runs another CozyDuke executable

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: The user runs a malicious executable file, presumably the fake money video (cash video).

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 004

   ---

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware masquerades as a legitimate media file (in this case a money video) to trick the user.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 004

 * Page #4:
   > It #rst launches Monkeys.exe, playing a selfcontained, very funny video of white-collar tie wearing chimpanzees working in a high rise o!ice with a human colleague

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: The user voluntarily runs the executable file Monkeys.exe to play the chimpanzee video.

   TOOLS: -

   NOTE: -

   ---

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware masquerades as a harmless funny chimpanzee video to fool the user.

   TOOLS: -

   NOTE: -

 * Page #4:
   > a CozyDuke dropper maintaining anti-detection techniques

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The player.exe dropper uses anti-detection techniques to avoid detection.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

 * Page #4:
   > The #le collects system information,

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malicious file collects system information to understand the environment in which it is executed.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #4:
   > then invokes a WMI instance in the rootsecuritycenter namespace to identify security products installed on the system

   ID: 011

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads.

    

   TOOLS: -

    

   NOTES: -

   LINK: 010, 012

 * Page #5:
   > In addition to the WMI/wql use, it also hunts through the "SOFTWAREMicrosoftWindowsCurrentVersionUnin stall" registry key looking for security products to avoid

   ID: 012

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: QUERY REGISTRY (T1012)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The malware performs a registry search, specifically in the registry key "SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall," to locate installed security products.

   TOOLS: -

   NOTE: -

   LINK: 011, 013

 * Page #5:
   > it drops several more malware #les signed with the pasted AMD digital signature to a directory it creates

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware uses files signed with a digital signature (in this case, AMD's digital signature) to execute other malicious files.

   TOOLS: -

   NOTE: -

   LINK: 012, 014

 * Page #5:
   > These #les are stored within an 217kb encrypted cab #le in the dropper's resources under the name "A". The cab #le was encrypted and decrypted using a simple xor cipher with a rotating 16 byte key

   ID: 014

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware uses an XOR encryption algorithm with a 16-byte rotating key to encrypt and decrypt a CAB file containing malware.

   TOOLS: -

   NOTE: -

   LINK: 013, 015

 * Page #5:
   > The cab #le is decompressed and its contents are created on disk

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware uses an encrypted CAB file that is decompressed and whose contents are created on the disk.

   TOOLS: -

   NOTE:  This technique allows the malware to hide its true purpose and contents by using an encrypted and then decompressed CAB file to evade detection.

   LINK: 014

 * Page #6:
   > The code collects information about the system and xml formats this data prior to encryption for proper parsing

   ID: 016

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.  

    

   TOOLS: -

    

   NOTES: -

 * Page #7:
   > It uses standard Win32 base cryptography functions to generate a CALG_RC4 session key to encrypt the collected data communications and POSTs it to the server

   ID: 025

   SOURCE: TEXT 

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: collected data communications were encrypted

   TOOLS: -

   NOTE: -

 * Page #7:
   > Samples are usually signed with a fake certi#cate – we've seen two instances, one AMD and one Intel

   ID: 027

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

    

   TOOLS: -

    

   NOTES: -

 * Page #7:
   > Some of the malware uses an encrypted con#guration #le which is stored on disk as "racss.dat". This is encrypted by RC4

   ID: 017

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The malware uses the RC4 encryption algorithm to encrypt the "racss.dat" configuration file on the disk.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The attackers send commands and new modules to be executed to the victims through the C&Cs

   ID: 018

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

    

   TOOLS: -

    

   NOTES: -

   LINK: 019

 * Page #8:
   > The C&C scripts store these temporarily until the victim next connects to retrieve local #les.

   ID: 019

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA STAGED (T1074)

   SUB-TECHNIQUE: -

   DESCRIPTION: C&Cs temporarily store commands and new forms until the victim reconnects to retrieve local files.

   TOOLS: -

   NOTE: -

   LINK: 018

 * Page #8:
   > RC4 encryption key

   ID: 021

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Data encoded in BASE64 is encrypted with the RC4 algorithm using the same encryption key as the malware configuration file. 

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #8:
   > BASE64 encoded

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: The data are encoded in BASE64 to hide their true content.

   TOOLS: -

   NOTE: -

   LINK: 021

 * Page #9:
   > And a set of "reporting" #les, maintaining stolen system "info", error output, and "AgentInfo" output, from victim systems

   ID: 021

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA STAGED (T1074)

   SUB-TECHNIQUE: -

   DESCRIPTION: "Reporting" files maintain stolen system information, error output, and "AgentInfo" output from victim systems.

   TOOLS: -

   NOTE: -

 * Page #9:
   > screenshot_task.dll is a 32-bit dll used to take a screenshot of the full desktop window and save it as a bitmap in %temp%.

   ID: 022

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: `screenshot_task.dll` is a 32-bit DLL used to capture a screenshot of the full desktop window and save it as a bitmap in the %temp% directory.

   TOOLS: -

   NOTE: -

 * Page #9:
   > It is used to create new processes, perform as a command line shell, and several other tasks.

   ID: 023

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: attackers can execute shell commands through `cmd_task.dll`, allowing direct control and interaction with the victim's system.

   TOOLS: -

   NOTE: -

 * Page #14:
   > Much like the prior o!ice monkey "atiumdag.dll" component, this code collects identifying system information using standard win32 API calls

   ID: 024

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: This code collects identifying system information using standard Win32 API calls.

   TOOLS: -

   NOTE: -

 * Page #15:
   > It then uses the runtime resolved networking API calls to send the collected data back to a hardcoded c2 and set of urls

   D: 027

    

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

    

   TOOLS: -

    

   NOTES: -

    

    --- 

   ID: 028

    

   SOURCE: TEXT

    

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

    

   TOOLS: -

    

   NOTES: -

