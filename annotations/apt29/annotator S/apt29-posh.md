## Detailed comments

 * Page #2:
   > POSHSPY's use of WMI to both store and persist the backdoor code makes it nearly invisible to anyone not familiar with the intricacies of WMI.

   ID: 022

    

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

    

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads.

    

   TOOLS: POSHSPY (S0150)

    

   NOTE: -

 * Page #2:
   > Its use of a PowerShell payload means that only legitimate system processes are utilized and that the malicious code execution can only be identi#ed through enhanced logging or in memory.

   ID: 023

    

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

    

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

    

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

    

   DESCRIPTION: The use of PowerShell payloads allows only legitimate system processes to be used, making detection of malicious code more difficult.

    

   TOOLS: -

    

   NOTE: -

 * Page #3:
   > WMI permanent event subscriptions can be used to trigger actions when speci#ed conditions are met.

   ID: 020

    

   SOURCE: TEXT

    

   TACTIC: PERSISTENCE (TA0003), DEFENSE EVASION (TA0005)

    

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

    

   SUB-TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION EVENT SUBSCRIPTION (T1546.003)

    

   DESCRIPTION: Creating a WMI event subscription to run the backdoor.

    

   TOOLS: -

    

   NOTE: -

 * Page #4:
   > We have observed APT29 use WMI to persist a backdoor and also store the PowerShell backdoor code.

   ID: 001

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: WMI EVENT SUBSCRIPTION (T1546.003)

   DESCRIPTION: Adversaries may establish persistence and elevate privileges by executing malicious content triggered by a Windows Management Instrumentation (WMI) event subscription.

   TOOLS: -

   NOTES: -

 * Page #4:
   > APT29 wrote the encrypted and base64- encoded PowerShell backdoor code into that prope%y.

   D: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: Base64 encoding.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > APT29 then created a WMI event subscription in order to execute the backdoor.

   ID: 004

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: WMI EVENT SUBSCRIPTION (T1546.003)

   DESCRIPTION: Adversaries may establish persistence and elevate privileges by executing malicious content triggered by a Windows Management Instrumentation (WMI) event subscription.

   TOOLS: -

   NOTES: -

 * Page #4:
   > The subscription was con#gured to run a PowerShell command that read, decrypted, and executed the backdoor code directly from the new WMI prope%y.

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it.

   TOOLS: -

   NOTES: -

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > This allowed them to install a persistent backdoor without leaving any a%ifacts on the system's hard drive, outside of the WMI repository. This "#leless" backdoor methodology made the identi#cation of the backdoor much more di$cult using standard host analysis techniques.

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIDE ARTIFACTS (T1564)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to hide artifacts associated with their behaviors to evade detection. 

   TOOLS: -

   NOTES: -

 * Page #5:
   > The WindowsParentalControlsMigration consumer was con#gured to silently execute a base64- encoded PowerShell command. Upon execution, this command extracted, decrypted, and executed the PowerShell backdoor payload stored in the HiveUploadTask text prope%y of the RacTask class.

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #6:
   > The POSHSPY backdoor is designed to download and execute additional PowerShell code and Windows binaries.

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #6:
   > Downloading and executing PowerShell code as an EncodedCommand

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

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #7:
   > Writing executables to a randomly-selected directory under Program Files, and naming the EXE to match the chosen directory name, or, if that fails, writing the executable to a systemgenerated temporary #le name, using the EXE extension

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: Adversaries may match or approximate the name or location of legitimate files or resources when naming/placing them. 

   TOOLS: -

   NOTES: -

 * Page #7:
   > Modifying the Standard Information timestamps (created, modi#ed, accessed) of every downloaded executable to match a randomly selected #le from the System32 directory that was created prior to 2013

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: TIMESTOMP (T1070.006)

   DESCRIPTION: Adversaries may modify file time attributes to hide new or changes to existing files. Timestomping is a technique that modifies the timestamps of a file (the modify, access, create, and change times), often to mimic files that are in the same folder..

   TOOLS: -

   NOTES: -

 * Page #7:
   > Encrypting communications using AES and RSA public key cryptography

   ID: 015

    SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

    

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

    

   SUB-TECHNIQUE: SYMMETIC CRYPTOGRAPHY (T1573.001), ASYMMETIC CRYPTOGRAPHY (T1573.002)

    

   DESCRIPTION:  to the use of asymmetric encryption algorithms, such as RSA, and symmetric encryption algorithms, such as AES, to protect communications, making it more difficult for defenders to monitor and intercept communications.

    

   TOOLS: -

    

   NOTE: -

 * Page #7:
   > Deriving C2 URLs from a Domain Generation Algorithm (DGA)

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE: DOMAIN GENERATION ALGORITHMS (T1568.002)

   DESCRIPTION: Adversaries may make use of Domain Generation Algorithms (DGAs) to dynamically identify a destination domain for command and control traffic rather than relying on a list of static IP addresses or domains.

   TOOLS: -

   NOTES: -

 * Page #8:
   > Using a custom User Agent string or the system's User Agent string derived from urlmon.dll

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA OBFUSCATION (T1001)

   SUB-TECHNIQUE: PROTOCOL IMPERSONATION (T1001.003)

   DESCRIPTION: Adversaries may impersonate legitimate protocols or web service traffic to disguise command and control activity and thwart analysis efforts.

   TOOLS: -

   NOTES: -

   ---

   ID: 021

    

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

    

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

    

   SUB-TECHNIQUE: WEB PROTOCOLS (T1546.001)

    

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols to avoid detection/network filtering by blending in with existing traffic.

    

   TOOLS: POSHSPY (S0150)

    

   NOTE: -

 * Page #8:
   > Uploading data in 2048-byte chunks

   ID: 018

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: DATA TRANSFER SIZE LIMITS (T1030)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may exfiltrate data in fixed size chunks instead of whole files or limit packet sizes below certain thresholds. This approach may be used to avoid triggering network data transfer threshold alerts.

   TOOLS: -

   NOTES: -

 * Page #9:
   > Appending a #le signature header to all encrypted data, prior to upload or download, by randomly selecting from the #le types: ICO GIF JPG PNG MP3 BMP

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: Adversaries may match or approximate the name or location of legitimate files or resources when naming/placing them. 

   TOOLS: -

   NOTES: -

