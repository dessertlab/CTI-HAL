## Detailed comments

 * Page #2:
   > FrameworkPOS scraping malware installed on some of the thin clients,

   ID: 001

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: TERMINAL SERVICES (T1505.001)

   DESCRIPTION: FrameworkPOS scraping malware installed on thin clients

   TOOLS: -

   NOTE: -

 * Page #2:
   > initializing PowerShell/WMI stages that downloaded and reflectively loaded Cobalt-Strike beacon with PowerShell extension directly into the memory

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Initializing PowerShell stages

   TOOLS: -

   NOTE: -

   ---

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Initializing WMI stages

   TOOLS: -

   NOTE: -

   ---

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading a payload such as the Cobalt Strike beacon.

   TOOLS: -

   NOTE: -

   ---

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: REFLECTIVE CODE LOADING (T1620)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Loading code (such as Cobalt Strike beacon) directly into memory without writing it to disk

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   ---

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell extensions to load the Cobalt Strike beacon into memory

   TOOLS: -

   NOTE: -

 * Page #2:
   > the Cobalt Strike beacon payload gives attackers full control over the infected system

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using remote access tools such as the Cobalt Strike beacon to control the infected system

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #2:
   > the ability to move laterally to other systems

   ID: 008

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using remote services to move laterally between systems

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #2:
   > harvest user credentials

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: harvest user credentials

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #3:
   > evading advanced EDR scanning techniques

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: IMPAIR DEFENSES (T1562)

   SUB-TECHNIQUE: -

   DESCRIPTION: Techniques for evading detection by Endpoint Detection and Response (EDR) systems.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #3:
   > one vector is executed through HTA files

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: MSHTA (T1218.005)

   DESCRIPTION: Using HTA (HTML Application) files to execute malicious code

   TOOLS:  -

   NOTE: -

   LINK: 012

 * Page #3:
   > that execute PowerShell scripts

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: HTA files that execute PowerShell scripts

   TOOLS: -

   NOTE: -

   LINK: 011, 013

 * Page #3:
   > part of an embedded VBScript

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Use of embedded VBScript to execute malicious commands.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #4:
   > some of them are executed through WMI

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using WMI to execute commands and scripts

   TOOLS: -

   NOTE: -

 * Page #6:
   > base64 encoded script

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using base64 encoding to obfuscate script content

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #6:
   > that is either remotely injected into the existing 32 bit or into a newly created 32 bit PowerShell process (if the current PowerShell is 64bit)

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Remotely injected into the existing 32 bit or into a newly created 32 bit PowerShell process

   TOOLS: -

   NOTE: -

   LINK: 015

 * Page #6:
   > The injected shellcode is a regular Metasploit downloader shellcode

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Injected shellcode is a regular Metasploit downloader shellcode

   TOOLS:  METASPLOIT

   NOTE: -

   LINK: 018

 * Page #6:
   > that traverses the PEB, resolves the function names by the standard ROR 13 hash,

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: REFLECTIVE CODE LOADING (T1620)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using advanced techniques to reflexively load code into memory by hashing out function names

   TOOLS: -

   NOTE: -

   LINK: 017, 019

 * Page #6:
   > downloads the next stage shellcode directly into memory from the C2

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading the payload of the next stage directly into memory from the command and control servers (C2)

   TOOLS: -

   NOTE: -

   LINK: 018

 * Page #7:
   > 2 types

   ID: 020

   NOTE: FIN6 uses two types of beacons

   LINK: T01 OR T02

 * Page #7:
   > regular direct reflective loaded Cobalt Strike DLL beacon, usually XOR encoded

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: REFLECTIVE CODE LOADING (T1620)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Direct reflexive loading of a DLL, a technique often used to inject code into memory without touching the disk

   TOOLS: -

   NOTE: -

   LINK: 022

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using XOR encoding to obfuscate the beacon

   TOOLS: -

   NOTE: -

   LINK: 021

 * Page #7:
   > the first one

   ID: T01

   LINK: 021, 022

 * Page #7:
   > The second type

   ID: T02

   LINK: 023, 024

 * Page #7:
   > shellcode backdoor beacon with PowerShell and Mimikatz functionality

   ID: 023

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to execute malicious commands and scripts

   TOOLS: -

   NOTE: -

   ---

   ID: 024

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T10003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Using Mimikatz to collect credentials from the memory of the LSASS process.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #7:
   > install "WindowsHelpAssistant" task in the task scheduler

   ID: 025

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002),  PERSISTENCE (TA0003),  PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Using the Windows task scheduler to maintain persistence.

   TOOLS: -

   NOTE: -

 * Page #7:
   > uses rundll32.exe with System privileges to execute and export function "workerInstance"

   ID: 026

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: Uses rundll32.exe with System privileges to execute and export function "workerInstance" from a downloaded binary DLL "Assistant32.dll"

   TOOLS: -

   NOTE: -

 * Page #8:
   > similar command execution as part of the HKLM Run key

   ID: 027

   SOURCE: TEXT 

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1547.001)

   DESCRIPTION: Using Run registry keys to maintain persistence

   TOOLS: -

   NOTE: -

 * Page #8:
   > The malware XOR's (xor 0xAA) the credit card information before exfiltration through DNS tunneling.

   ID: 028

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of information (XOR) before exfiltration

   TOOLS: -

   NOTE: -

   LINK: 029

   ---

   ID: 029

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICAITON LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (1071.004)

   DESCRIPTION: Using DNS tunneling to exfiltrate data.

   TOOLS: -

   NOTE: -

   LINK: 028

