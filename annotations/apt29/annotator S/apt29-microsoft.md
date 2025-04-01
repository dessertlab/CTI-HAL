## Detailed comments

 * Page #3:
   > The spear-phishing emails used in this attack resemble file-sharing notifications from OneDrive. The emails contain a link to a legitimate, but compromised third-party website

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

   ID: 002

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: WEB SERVER (T1584.006)

   DESCRIPTION: Adversaries may compromise access to third-party web services.

   TOOLS: -

   NOTES: -

 * Page #4:
   > When users click the link

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious link in order to gain execution. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > they are served a ZIP archive containing a malicious LNK file.

   ID: 004

    

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

    

   TECHNIQUE: USER EXECUTION (T1204)

    

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

    

   DESCRIPTION: The ZIP archive contains a malicious LNK file.

    

   TOOLS: -

    

   NOTE: -

 * Page #4:
   > It executes an obfuscated PowerShell command that extracts a base64-encoded payload from within the LNK file itself

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > The first-stage DLL, cyzfc.dat, is created by the PowerShell script in the path %AppData%\Local\cyzfc.dat. It is a 64-bit DLL that exports one function: PointFunctionCall.

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DLL INJECTION (T1055.001)

   DESCRIPTION: Adversaries may inject dynamic-link libraries (DLLs).

   TOOLS: -

   NOTES: -

 * Page #4:
   > The PowerShell script then executes cyzfc.dat by calling rundll32.exe.

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: Adversaries may abuse rundll32.exe to proxy execution of malicious code.

   TOOLS: -

   NOTES: -

 * Page #4:
   > After connecting to the first-stage command-and-control server at pandorasong[.]com (95.216.59.92), cyzfc.dat begins to install the final payload

   ID: 008

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

    

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION:  `cyzfc.dat` extracts and installs the final payload.

    

   TOOLS: -

   NOTE: -

 * Page #5:
   > key 0xC5.

   ID: 016

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

    

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: De-XOR of the second-stage payload with a rotating XOR (ROR1), starting at byte 0xC5.

    

   TOOLS: -

    

   NOTE: -

 * Page #6:
   > That payload is XORed with the same XORing algorithm used for reading.

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit. 

   TOOLS: -

   NOTES: -

 * Page #6:
   > When decrypted, it forms a PE file with a Meterpreter header, interpreting instructions in the PE header and moving control to a reflective loader:

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it. 

   TOOLS: -

   NOTES: -

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may execute malicious payloads via loading shared modules. 

   TOOLS: -

   NOTES: -

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: REFLECTIVE CODE LOADING (T1620)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may reflectively load code into a process in order to conceal the execution of malicious payloads.

   TOOLS: -

   NOTES: -

   LINK: #009 THEN #010 THEN #011, #012

 * Page #6:
   > The third payload eventually gets loaded and connects to the command-andcontrol (C&C) server address that is baked-in inside configuration information in the PE file.

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.

   TOOLS: -

   NOTES: -

   LINK: #011, #012 THEN #013

 * Page #6:
   > This configuration information is de-XORed at the third payload runtime:

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it. 

   TOOLS: -

   NOTES: -

 * Page #6:
   > CobaltStrike is a feature-rich penetration testing tool that provides remote attackers with a wide range of capabilities, including escalating privileges, capturing user input, executing arbitrary commands through PowerShell or WMI, performing reconnaissance, communicating with C&C servers over various protocols, and downloading and installing additional malware.

   ID: 17

   TOOLS: CobaltStrike (S0154)

