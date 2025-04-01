## Detailed comments

 * Page #2:
   > The actor often spearphishes targets with e-mails containing a link to a hacked website.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #2:
   > Sometimes it is a high pro#le, legitimate site such as "diplomacy.pl", hosting a ZIP archive. The ZIP archive contains a RAR SFX which installs the malware and shows an empty PDF decoy.

   ID: 002

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENTE (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may compromise third-party infrastructure.

   TOOLS: -

   NOTES: -

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

   LINK: #002 THEN #001 THEN #003

 * Page #2:
   > In other highly successful runs, this actor sends out phony $ash videos directly as email attachments

   ID: 004

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

   LINK: #001 OR #004

 * Page #2:
   > The executable within not only plays a $ash video, but drops and runs another CozyDuke executable. These videos are quickly passed around o!ices with delight while systems are infected in the background silently

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious file in order to gain execution. 

   TOOLS: -

   NOTES: -

   LINK: #004 THEN #005

 * Page #4:
   > It #rst launches Monkeys.exe, playing a selfcontained, very funny video of white-collar tie wearing chimpanzees working in a high rise o!ice with a human colleague.

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious file in order to gain execution. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > It then launches player.exe, a CozyDuke dropper maintaining anti-detection techniques:

   ID: 019

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

    

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: The player.exe dropper uses anti-detection techniques to avoid detection.

    

   TOOLS: COZYDUKE (S0046)

    

   NOTE: -

 * Page #4:
   > The #le collects system information

   ID: 007

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.  

   TOOLS: -

   NOTES: -

   LINK: #006 THEN #007

 * Page #4:
   > invokes a WMI instance in the rootsecuritycenter namespace to identify security products installed on the system

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads. 

   TOOLS: -

   NOTES: -

 * Page #5:
   > In addition to the WMI/wql use, it also hunts through the "SOFTWAREMicrosoftWindowsCurrentVersionUnin stall" registry key looking for security products to avoid.

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: QUERY REGISTRY (T1012)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may interact with the Windows Registry to gather information about the system, configuration, and installed software.

   TOOLS: -

   NOTES: -

 * Page #5:
   > it drops several more malware #les signed with the pasted AMD digital signature to a directory it creates

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

   TOOLS: -

   NOTES: -

   LINK: #009 THEN #010

 * Page #5:
   > These #les are stored within an 217kb encrypted cab #le in the dropper's resources under the name "A". The cab #le was encrypted and decrypted using a simple xor cipher with a rotating 16 byte key

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it.

   TOOLS: -

   NOTES: -

 * Page #6:
   > The code copies rundll32.exe from windowssystem32 to its newly created %appdata%ATI_Subsystem subdirectory as "amdocl_as32.exe" alongside the three dll's listed above. It runs atiumdag.dll with two parameter values, it's only export and an arbitrary pid

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTES: -

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIJACK EXECUTION FLOW (T1574)

   SUB-TECHNIQUE: DLL SIDE-LOADING (T1574.002)

   DESCRIPTION: Adversaries may execute their own malicious payloads by side-loading DLLs.

   TOOLS: -

   NOTES: -

 * Page #6:
   > The code collects information about the system and xml formats this data prior to encryption for proper parsing:

   ID: 015

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.  

   TOOLS: -

   NOTES: -

 * Page #6:
   > Finally, this process beacons to www.sanjosemaristas.com

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTES: -

 * Page #7:
   > It uses standard Win32 base cryptography functions to generate a CALG_RC4 session key to encrypt the collected data communications and POSTs it to the server.

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTES: -

 * Page #7:
   > Samples are usually signed with a fake certi#cate – we've seen two instances, one AMD and one Intel

   ID: 020

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

   TOOLS: -

   NOTES: -

 * Page #7:
   > Some of the malware uses an encrypted con#guration #le which is stored on disk as "racss.dat". This is encrypted by RC4, using the key {0xb5, 0x78, 0x62, 0x52, 0x98, 0x3e, 0x24, 0xd7, 0x3b, 0xc6, 0xee, 0x7c, 0xb9, 0xed, 0x91, 0x62}.

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #8:
   > The attackers send commands and new modules to be executed to the victims through the C&Cs.

   ID: 022

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #8:
   > The C&C scripts store these temporarily until the victim next connects to retrieve local #les.

   ID: 016

    

   SOURCE: TEXT

    

   TACTIC: COLLECTION (TA0009)

    

   TECHNIQUE: DATA STAGED (T1074)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: C&Cs temporarily store commands and new forms until the victim reconnects to retrieve local files.

    

   TOOLS: -

    

   NOTE: -

    

 * Page #8:
   > These are BASE64 encoded and use the same RC4 encryption key as the malware con#guration.

   ID: 023

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #9:
   > screenshot_task.dll is a 32-bit dll used to take a screenshot of the full desktop window and save it as a bitmap in %temp%.

   ID: 025

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to take screen captures of the desktop to gather information over the course of an operation.

   TOOLS: -

   NOTES: -

 * Page #9:
   > cmd_task.dll is a 32-bit dll that maintains several primitives. It is used to create new processes, perform as a command line shell, and several other tasks.

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #12:
   > Structurally, "Cache.dll" is a fairly large backdoor at 425KB. It maintains both code and data in the raw, encrypted blobs of data to be decrypted and used at runtime, and hidden functionality that isn't exposed until runtime.

   ID: 028

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

   ID: 029

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #13:
   > It #rst grabs an encrypted blob stored away in a global variable and pulls out 381 bytes of this encrypted data

   ID: 030

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #13:
   > The standard win32 api CryptDecrypt uses rc4 to decrypt this blob into a hardcoded c2, url path, and url parameters listed below with a simple 140-bit key

   ID: 031

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it.

   TOOLS: -

   NOTES: -

 * Page #14:
   > Much like the prior o!ice monkey "atiumdag.dll" component, this code collects identifying system information using standard win32 API calls

   ID: 032

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture.  

   TOOLS: -

   NOTES: -

 * Page #15:
   > It then uses the runtime resolved networking API calls to send the collected data back to a hardcoded c2 and set of urls.

   ID: 033

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTES: -

   ID: 034

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel. 

   TOOLS: -

   NOTES: -

