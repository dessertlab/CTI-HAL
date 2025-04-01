## Detailed comments

 * Page #1:
   > This document is used in phishing campaigns to execute a series of scripting languages

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Attackers use email attachments containing malicious files

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #1:
   > to execute a series of scripting languages containing multiple obfuscation mechanisms and advanced techniques to bypass traditional security mechanisms.

   ID: 002

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of script languages to execute malicious code.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #1:
   > containing multiple obfuscation mechanisms

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 uses techniques such as file obfuscation to avoid detection by traditional security tools.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #1:
   > The document contains messages enticing the user to click on an embedded object that executes scripts

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Attackers rely on user actions to open malicious files or click on embedded objects, triggering the malware execution.

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #1:
   > This malware is then used to steal passwords from popular browsers and mail clients

   ID: 005

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: CREDENTIALS FROM WEB BROWSERS (T1555.003)

   DESCRIPTION: Attackers steal saved login credentials from web browsers, gaining access to accounts.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #1:
   > which are sent to remote nodes

   ID: 006

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.011)

   DESCRIPTION: FIN7's malware uses legitimate web protocols such as HTTP/HTTPS to communicate with its command-and-control servers. 

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #2:
   > a new infection vector technique using an RTF document containing an embedded JavaScript OLE object

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Attackers deliver phishing emails containing malicious attachments, in this case, an RTF document embedded with a JavaScript OLE object.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #2:
   > When clicked it launches an infection chain

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The attack relies on the user clicking the embedded OLE object to trigger the infection chain.

   TOOLS: -

   NOTE: -

   LINK: 007, 009

 * Page #2:
   > an infection chain made up of JavaScript, and a Knal shellcode payload

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Execution of JavaScript from the embedded OLE object to begin the infection process.

   TOOLS: -

   NOTE: -

   LINK: 008, 010

 * Page #2:
   > that makes use of DNS to load additional shellcode from a remote command and control server

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: Using DNS as a channel to communicate with the command and control (C2) server and load additional shellcode.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #2:
   > this new document variant that makes use of an LNK embedded OLE object

   ID: 011

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attack starts with a spear-phishing email containing a malicious document with an LNK embedded OLE object.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #2:
   > which extracts a JavaScript bot from a document object,

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The JavaScript bot is extracted and executed as part of the infection chain.

   TOOLS: -

   NOTE: -

   LINK: 011, 013

 * Page #2:
   > injects a stealer DLL in memory

   ID: 013

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DYNAMIC-LINK LIBRARY INJECTION (T1055.001)

   DESCRIPTION: The stealer DLL is injected directly into memory using PowerShell, allowing the malware to run in the context of legitimate processes.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #2:
   > using PowerShell.

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell is used to inject the stealer DLL into memory, a key part of the execution chain.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #2:
   > The dropper variant that we encountered makes use of an LNK Kle to execute wscript.exe

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The dropper leverages a crafted LNK file to initiate the execution of malicious code on the victim's machine, embedded within the Word document.

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #2:
   > the beginning of the JavaScript chain

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The JavaScript chain is used for the next stage of execution

   TOOLS: -

   NOTE: -

   LINK: 015, 017

 * Page #2:
   > from a word document object

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The victim likely opens a malicious Word document object, initiating the infection process.

   TOOLS: -

   NOTE: -

   LINK: 016

