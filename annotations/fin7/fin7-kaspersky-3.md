## Detailed comments

 * Page #2:
   > Astra. The panel, written in PHP, functions as a script-management system

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using PHP for management and control of attack scripts fits under the use of scripting languages for execution and control in the attack lifecycle.

   TOOLS: ASTRA

   NOTE: -

   LINK: 002

 * Page #2:
   > pushing attack scripts down to compromised computers

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The panel pushing attack scripts down to compromised systems indicates transferring malicious tools or files to target systems.

   TOOLS: ASTRA

   NOTE: -

   LINK: 001

 * Page #2:
   > The attackers gain an initial foothold on targeted machines via phishing emails containing malicious attachments

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Attackers send targeted emails containing malicious attachments to entice victims into opening them and executing the payload.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #2:
   > The emails are often industryspecific and crafted to entice a victim to open the message and execute the attached document

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Victims are tricked into opening and executing the attached document, enabling the attackers to gain an initial foothold.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > malware that drops files and executes SQL scripts on the host system

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: SQLRat uses SQL scripts to execute commands on the host system, which is an uncommon method but falls under the use of SQL as a command interpreter.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #2:
   > Once they are deleted by the attackers' code, there is nothing left to be forensically recovered.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: After SQL scripts are executed, the attackers' code deletes the files, leaving minimal forensic artifacts, making recovery difficult.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #3:
   > DNSbot, which is used to exchange commands and push data to and from compromised machines

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: DNSbot uses DNS to send and receive commands and data between the compromised machine and the attacker's command-and-control (C2) server.

   TOOLS: DNSBOT

   NOTE: -

   LINK: 008

 * Page #3:
   > can also switch to encrypted channels such as HTTPS or SSL

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: DNSbot has the ability to switch to encrypted communication channels such as HTTPS or SSL when necessary.

   TOOLS: DNSBOT

   NOTE: -

   LINK: 007

 * Page #3:
   > The campaigns maintain persistence on machines by creating two daily scheduled task entries

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Creating scheduled task entries to maintain persistence on compromised machines.

   TOOLS: -

   NOTE: -

   LINK: 017

   ---

   ID: 017

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: creating daily scheduled task

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #3:
   > Once a user has double-clicked the embedded image, the form executes a VB setup script

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The lure document tricks the user into executing a malicious file.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #3:
   > The script writes files to the path %appdata%\Roaming\Microsoft\Templates\, then creates two task entries

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Creating scheduled task entries to maintain persistence.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #4:
   > The scripts are responsible for deobfuscating and executing the main JavaScript file mspromo.dot.

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Execution of malicious JavaScript code after deobfuscation.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #4:
   > The file uses a character insertion obfuscation technique, making it appear to contain Chinese characters

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of obfuscation techniques to hide the true nature of malicious code.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #4:
   > execute scripts

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: This covers the execution of scripts, particularly those that drop and execute files on a system.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The SQLRat script is designed to make a direct SQL connection to a Microsoft database controlled by the attackers

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: SQLRat uses a direct SQL connection to retrieve and execute files from a remote database, indicating the use of a web-based protocol to communicate with a malicious database.

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #4:
   > The script retrieves an item from the bindata table and writes the file to disk

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: SQLRat retrieves and writes files to disk, which can then be executed.

   TOOLS: -

   NOTE: -

   LINK: 015

