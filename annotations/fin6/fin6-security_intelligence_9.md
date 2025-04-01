## Highlights

 * Page #7:
   > The process begins with the consistent execution of a malicious DLL using the legitimate regsvr32.exe Windows Utility


## Detailed comments

 * Page #2:
   > targeting specific employees with spear phishing emails advertising fake job advertisements

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISING LINK (T1566.002)

   DESCRIPTION: Use of spear phishing emails to attract specific employees with fake job ads.

   TOOLS: -

   NOTE: -

 * Page #2:
   > deploying the More_eggs JScript backdoor malware (aka Terra Loader, SpicyOmelette)

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT/JSCRIPT (T1059.007)

   DESCRIPTION: Using JavaScript/JScript to execute the More_eggs malware.

   TOOLS: MORE_EGGS (S0284)

   NOTE: -

   LINK: 003

 * Page #2:
   > This tool, a TTP observed in ITG08 attacks since 2018, is sold on the dark web by an underground malware-as-aservice (MaaS) provider

   ID: 003

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: MALWARE (T1588.006)

   DESCRIPTION: Purchase of malware from a malware-as-a-service provider

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > the use of Windows Management Instrumentation (WMI) to automate the remote execution of PowerShell scripts

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of Windows Management Instrumentation (WMI) to automate the remote execution of PowerShell scripts

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #2:
   > PowerShell commands with base64 encoding,

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute commands.

   TOOLS: -

   NOTE: -

   LINK: 004, 006

   ---

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of PowerShell commands using base64 encoding.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #2:
   > Metasploit and PowerShell to move laterally and deploy malware.

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), LATERAL MOVEMENT (TA0008)

   TECHNIQUE: SOFTWARE DEPLOYMENT TOOLS (T1072)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of tools such as Metasploit for malware distribution.

   TOOLS: METASPLOIT

   NOTE: -

 * Page #3:
   > the threat actor began by targeting handpicked employees using LinkedIn messaging and email

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001) 

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing emails containing links to malicious payloads.

   TOOLS: -

   NOTE: -

   ---

   ID: 009

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001) 

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Sending spear phishing links via LinkedIn or email.

   TOOLS: -

   NOTE: -

 * Page #4:
   > downloaded a ZIP file containing a malicious Windows Script File (WSF) that initiated the infection routine of the More_eggs backdoor

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Using Windows scripts to execute malicious commands.

   TOOLS: MORE_EGGS (S0284)

   NOTE: Using a Windows Script File (WSF)

   ---

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Deception of the user to execute a malicious file.

   TOOLS: -

   NOTE: -

 * Page #4:
   > the ZIP file and WSF files were deleted upon a successful malware infection

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: Deletion of malicious files to hide traces.

   TOOLS: -

   NOTE: -

 * Page #4:
   > a nonmalicious decoy document dropped to the disk drive

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: TAINTED FILE (T1070.006)

   DESCRIPTION: Creation of non-malicious decoy documents to confuse researchers and obfuscate malicious activities.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The spear phishing attacks

   ID: 014

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001) 

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing emails containing links to malicious payloads.

   TOOLS: -

   NOTE: -

   LINK: 016

   ---

   ID: 015

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001) 

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Sending spear phishing links via LinkedIn or email.

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #5:
   > the installation of the More_eggs JScript backdoor

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Using JavaScript to execute malicious commands.

   TOOLS: MORE_EGGS (S0284)

   NOTE: -

   LINK: 014, 015, 017, 021, 022

 * Page #5:
   > established a reverse shell connection to the attacker's command-and-control (C&C) infrastructure

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Use of web protocols for malicious communications.

   TOOLS: -

   NOTE: -

   ---

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION:  Transfer of malicious tools from an external system to the compromised network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > download and execution of files and scripts and running commands using cmd.exe

   ID: 019

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Executing commands through the Windows shell.

   TOOLS: -

   NOTE: -

   ---

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION:  Downloading files and scripts.

   TOOLS: -

   NOTE: -

 * Page #5:
   > the More_eggs backdoor later downloaded additional files, including a signed binary shellcode loader and a signed Dynamic Link Library (DLL)

   ID: 021

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Loading of shared modules, such as signed DLLs.

   TOOLS: MORE_EGGS (S0284)

   NOTE: -

   LINK: 016, 023

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION:  Transfer of additional malicious files.

   TOOLS: -

   NOTE: -

   LINK: 016, 023

 * Page #5:
   > to create a reverse shell and connect to a remote host

   ID: 023

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Execution of commands and scripts using PowerShell.

   TOOLS: -

    

   NOTE: -

   LINK: 021, 022, 024

   ---

   ID: 024

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Communication with the command and control server.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The shellcode loader was observed on one infected device as updater.exe with the Metasploit-style service name APTYnDS1ABEuUHEA, indicating that it was installed as a service

   ID: 033

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: the shellcode loader was observed as updater.exe

   TOOLS: -

   NOTE: -

 * Page #5:
   > they employed WMI and PowerShell techniques to perform network reconnaissance and move laterally within the environment

   ID: 025

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using WMI to perform network reconnaissance and lateral movement within the environment.

   TOOLS: -

   NOTE: -

   ---

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to perform network reconnaissance and lateral movement within the environment.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The attackers used this technique to remotely install a Metasploit reverse TCP stager on select systems, subsequently spawning a Meterpreter session and Mimikatz

   ID: 027

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS TOOLS (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using remote access tools such as Meterpreter to establish a session with the compromised system

   TOOLS: -

   NOTE: -

   LINK: 028, 029

 * Page #5:
   > Meterpreter is a payload component in the Metasploit Framework that uses in-memory DLL injection

   ID: 028

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005), 

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DLL INJECTION (T1055.012)

   DESCRIPTION: Meterpreter, a payload component in the Metasploit framework, uses in-memory DLL injection.

   TOOLS: -

   NOTE: -

   LINK: 027

 * Page #5:
   > Mimikatz is a post-exploitation tool that allows attackers to extract credentials from volatile memory

   ID: 029

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Mimikatz is a post-exploitation tool used to extract credentials from volatile memory

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

   LINK: 027

 * Page #6:
   > second stage Meterpreter DLL into memory, allowing the attacker to spawn a Meterpreter session via a handler and initiate the loading of extensions, such as Mimikatz

   ID: 030

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005),

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DLL INJECTION (T1055.012)

   DESCRIPTION: The attacker loaded a second stage of Meterpreter DLL into memory, allowing Meterpreter sessions to be executed and extensions such as Mimikatz to be loaded

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #6:
   > the attacker leveraged in-memory attacks by injecting malicious code, in this case Mimikatz, into legitimate system processes

   ID: 031

   SOURCE: TEXT

   TACTIC: EPRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005),

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The attacker used Metasploit to inject malicious code (Mimikatz) into legitimate system processes.

   TOOLS: -

   NOTE: -

 * Page #6:
   > ITG08 remotely connected to these devices using PowerShell and WMI and downloaded and executed a DLL file,

   ID: 032

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE EXECUTION (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attacker used PowerShell and WMI to connect and download and execute a DLL file

   TOOLS: -

   NOTE: -

 * Page #7:
   > The process begins with the consistent execution of a malicious DLL using the legitimate regsvr32.exe Windows Utility

   ID: 034

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: REGSVR32 (T1218.010)

   DESCRIPTION: regsvr32.exe is used

   TOOLS: -

   NOTE: -

 * Page #10:
   > The JScript loader file is highly obfuscated and decodes the More_eggs backdoor in a variety of ways, including RC4 decryption

   ID: 036

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: the loader decodes the backdoor

   TOOLS: -

   NOTE: -

 * Page #11:
   > The RC4 key is then used to encrypt data, which is additionally basE91 encoded and sent back to the C&C. BasE91 is a method for encoding binary as ASCII characters

   ID: 035

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: encoding methods were used

   TOOLS: -

   NOTE: -

