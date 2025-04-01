## Detailed comments

 * Page #1:
   > This spearphishing attack targeted a Jordanian diplomat, with the sender pretending to be a colleague from the IT department of the same governmental organization

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attacker pretends to be a colleague from the IT department of the same governmental organization to deliver the phishing email.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > the attached Excel file contained a confirmation form for the targeted diplomat to fill out

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The user is tricked into executing the malicious content by filling out and interacting with the confirmation form in the Excel file.

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #2:
   > The attached Excel file contains a malicious VBA ]Visual Basic Application) macro

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The malicious VBA macro within the Excel file is executed when the document is opened and macros are enabled.

   TOOLS: -

   NOTE: -

   LINK: 004, 005

 * Page #2:
   > Cobalt Strike

   ID: 004

   TOOLS: COBALT STRIKE (S0154)

 * Page #2:
   > Metasploit.

   ID: 005

   TOOLS: METASPLOIT

 * Page #2:
   > this one uses WMI ]Windows Management Instrumentation) to ping the C2 server instead of a more commonly used tool, such as PowerShell or CMD

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: The macro uses WMI to ping the C2 server, which is an uncommon choice compared to PowerShell or CMD.

   TOOLS: -

   NOTE: -

 * Page #3:
   > A malicious PE file was created as %LocalAppData%\MicrosoftUpdate\update.exe. A configuration file was created as %LocalAppData%\MicrosoftUpdate\update.exe.config.

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: The creation of %LocalAppData%\MicrosoftUpdate\update.exe and %LocalAppData%\MicrosoftUpdate\update.exe.config may contribute to persistence.

   TOOLS: -

   NOTE: -

 * Page #4:
   > base64 encoded data

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The malware authors also used the Excel macro to create a persistence method for their update.exe file. They accomplished this by setting a scheduled task

   ID: 008

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The scheduled task created by the macro to run the update.exe file ensures persistence.

   TOOLS: -

   NOTE: -

 * Page #4:
   > a second technique was also seen in this macro to possibly avoid automated analysis. This macro does this by checking for the existence of a mouse.

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Checking for mouse presence to avoid automated analysis.

   TOOLS: -

   NOTE: -

 * Page #5:
   > other program states require it to contact the C2 server.

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: HTTP (T1071.001)

   DESCRIPTION: The malware uses a DGA to generate domain names for contacting its C2 server.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #5:
   > it uses a domain generation algorithm ]DGAk to calculate a subdomain

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE: DOMANI GENERATION ALGORITHM (T1568.002)

   DESCRIPTION: DGA is a technique where malware generates a list of domain names based on a specific algorithm. The malware uses these generated domains to contact its C2 server, which can be effective in evading domain blacklists and takedown efforts.

   TOOLS: -

   NOTE: -

   LINK: 009

   ---

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: FALLBACK CHANNEL (T1008)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using multiple C2 domains with domain generation algorithm.

   TOOLS: -

   NOTE: -

 * Page #7:
   > This malware has the ability to take a DNS response and create an arbitrary file on the infected machine if that was the task the malware authors wanted to perform. File and CompressedFile are task types used to create a file

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware can create arbitrary files on the infected machine as dictated by tasks received through DNS responses.

   TOOLS: -

   NOTE: -

 * Page #7:
   > executed through PowerShell

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION:  The malware can execute commands via PowerShell.

   TOOLS: -

   NOTE: -

 * Page #7:
   > through the Windows CMD interpreter

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: 

   The malware can also execute commands through the Windows CMD interpreter.

   TOOLS: -

   NOTE: -

 * Page #9:
   > it relies on the Excel macro to create persistence by way of a scheduled task.

   ID: 017

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: Creating scheduled task for persistent execution.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Since Excel is a signed binary, maintaining persistence in this way may be missed by some behavioral detection engines.

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: Leveraging Excel as a signed binary for executing malicious macro.

   TOOLS: -

   NOTE: -

