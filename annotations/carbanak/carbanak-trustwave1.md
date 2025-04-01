## Detailed comments

 * Page #3:
   > The common successful entry point within all operations was an email message targeted to victim's public-facing services that contained a Microsoft Word document attachment

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending targeted emails containing malicious attachments to gain initial access.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > Upon opening the attachment

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Execution of malicious code when the user opens a file or link.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #3:
   > multiple malicious files were created or downloaded allowing the attackers to gain some level of access into the victim's infrastructure.

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of tools or files from an external system to the compromised system.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #5:
   > Figure 4: File process

   ID: 004

   SOURCE: FIGURE

   DESCRIPTION: the role of each of the four dropped files

 * Page #6:
   > Data from section "last" is written into registry perhaps to keep track of last executed command

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: Modification of registry keys for various malicious purposes, such as keeping track of the last command executed.

   TOOLS: -

   NOTE: -

 * Page #7:
   > persistence was achieved by utilizing scheduled tasks

   ID: 006

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of scheduled tasks to maintain persistence in the system.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #7:
   > several of the Operating System's auto-start locations

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using automatic operating system startup locations to maintain persistence.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #7:
   > allowed attackers to gain Domain or even Enterprise Admin access

   ID: 008

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using valid credentials to access various systems.

   TOOLS: -

   NOTE: -

 * Page #8:
   > Cloud services such as Google Docs and Google Forms were involved allowing attackers to keep track of infected systems, spread malware and perform further malicious activities

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: DEAD DROP RESOLVER (T1102.001)

   DESCRIPTION: Using web services to store information that threat actors can retrieve.

   TOOLS: -

   NOTE: -

   ---

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Cloud services were involved

   TOOLS: -

   NOTE: -

 * Page #9:
   > scripting code (PowerShell, JavaScript, VBS)

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using command interpreters and scripting to execute code.

   TOOLS: -

   NOTE: The use of PowerShell, JavaScript, and VBS implies the use of scripting interpreters to execute malicious code.

 * Page #9:
   > What seems to be the core tools of these activities is a variant of Anunak, remote backdoor, along with a Visual Basic Script specially crafted with data exfiltration features

   ID: 014

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Steal data by exfiltrating it over a command and control channel

   TOOLS: ANUNAK (S0030)

   NOTE: -

 * Page #9:
   > Anunak,

   ID: 011

   TOOLS: ANUNAK (S0030)

 * Page #10:
   > One other significant finding is that some of the executables were signed using valid certificates from Comodo, a Certification Authority

   ID: 012

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: CODE SIGNING CERTIFICATES (T1588.003)

   DESCRIPTION: Attackers acquire code signing certificates to sign their malicious executables.

   TOOLS: ANUNAK (S0030)

   NOTE: The use of valid certificates by Comodo to sign malicious executables is a clear example of this technique.

