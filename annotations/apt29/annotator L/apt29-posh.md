## Detailed comments

 * Page #1:
   > POSHSPY leverages two of the tools the group frequently uses

   ID: 000

   TOOLS: POSHSPY (S0150)

   LINK: 001, 002

 * Page #1:
   > Windows Management Instrumentation (WMI)

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of WMI to maintain persistence on the system. POSHSPY leverages WMI as one of the main tools.

   TOOLS: -

   NOTE: -

 * Page #1:
   > PowerShell

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The use of PowerShell to execute malicious commands or scripts. POSHSPY uses PowerShell as part of its toolkit.

   TOOLS: -

   NOTE: -

 * Page #2:
   > POSHSPY's use of WMI to both store and persist the backdoor code makes it nearly invisible to anyone not familiar with the intricacies of WMI

   ID: 003

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: WINDOWS INSTRUMENTATION EVENT SUBSCRIPTION (T1546.003)

   DESCRIPTION: The use of WMI to maintain persistence on the system. POSHSPY uses WMI to store and persist the backdoor code.

   TOOLS: -

   NOTE: -

   ---

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of WMI to execute commands in order to avoid detection.

   TOOLS: POSHSPY (S0150)

   NOTE: -

 * Page #2:
   > Its use of a PowerShell payload means that only legitimate system processes are utilized and that the malicious code execution can only be identi#ed through enhanced logging or in memory

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The use of PowerShell payloads allows only legitimate system processes to be used, making detection of malicious code more difficult.

   TOOLS: -

   NOTE: -

 * Page #2:
   > tra$c obfuscation,

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of traffic and data.

   TOOLS: -

   NOTE: -

 * Page #4:
   > created a new WMI class and added a text prope%y to it in order to store a string value

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: Creating a new WMI class and adding a text property.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #4:
   > APT29 wrote the encrypted and base64- encoded PowerShell backdoor code into that prope%y

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to run the backdoor

   TOOLS: -

   NOTE: -

   LINK: 009

   ---

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: PowerShell code is encrypted and encoded in base64.

   TOOLS: -

   NOTE: -

   LINK: 007, 008

 * Page #4:
   > APT29 then created a WMI event subscription in order to execute the backdoor

   ID: 010

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), DEFENSE EVASION (TA0005)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION EVENT SUBSCRIPTION (T1546.003)

   DESCRIPTION: Creating a WMI event subscription to run the backdoor.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #4:
   > The subscription was con#gured to run a PowerShell command that read, decrypted, and executed the backdoor code directly from the new WMI prope%y

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Running PowerShell commands to read, decrypt, and execute the backdoor code.

   TOOLS: -

   NOTE: -

   LINK: 010, 012

   ---

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Decryption of the backdoor code.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #4:
   > install a persistent backdoor without leaving any a%ifacts on the system's hard drive

   ID: 021

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIDE ARTIFACTS (T1564)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may attempt to hide artifacts associated with their behaviors to evade detection.

    

   TOOLS: -

    

   NOTES: -

 * Page #6:
   > The POSHSPY backdoor is designed to download and execute additional PowerShell code and Windows binaries

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Download additional code to execute.

   TOOLS: POSHSPY (S0150)

   NOTE: -

   ---

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Run additional PowerShell code.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Downloading and executing PowerShell code

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Download additional code to execute.

   TOOLS: POSHSPY (S0150)

   NOTE: -

   ---

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Run additional PowerShell code.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Writing executables to a randomly-selected directory under Program Files, and naming the EXE to match the chosen directory name, or, if that fails, writing the executable to a systemgenerated temporary #le name, using the EXE extension

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: This technique involves masking executable files with names and paths that seem legitimate or familiar to the user, such as using file names that correspond to random directory names under Program Files.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Modifying the Standard Information timestamps (created, modi#ed, accessed) of every downloaded executable to match a randomly selected #le from the System32 directory that was created prior to 2013

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENDE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: TIMESTAMP (T1070.006)

   DESCRIPTION: This TTP describes the action of modifying or manipulating file timestamps to hide malware activities, making it more difficult to detect and analyze operations performed on the system.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Encrypting communications using AES and RSA public key cryptography

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: SYMMETIC CRYPTOGRAPHY (T1573.001), ASYMMETIC CRYPTOGRAPHY (T1573.002)

   DESCRIPTION:  to the use of asymmetric encryption algorithms, such as RSA, and symmetric encryption algorithms, such as AES, to protect communications, making it more difficult for defenders to monitor and intercept communications.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Deriving C2 URLs from a Domain Generation Algorithm (DGA)

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE: DOMAIN GENERATION ALGORITHMS (T1568.002)

   DESCRIPTION: dynamically generate a list of command and control (C2) domains on the fly, making it more difficult for defenders to block or detect C2 domains because they are randomly or pseudo-randomly generated.

   TOOLS: -

   NOTE: -

 * Page #8:
   > Using a custom User Agent string or the system's User Agent string derived from urlmon.dll

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: POSHSPY uses custom or system-derived User Agent strings and employs custom or randomly generated cookie names and values

   TOOLS: POSHSPY (S0150)

   NOTE: -

