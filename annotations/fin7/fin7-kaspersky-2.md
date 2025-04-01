## Detailed comments

 * Page #2:
   > The emails were e"icient socialengineering attempts that appealed to a vast number of human emotions (fear, stress, anger, etc.) to elicit a response from their victims

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: This reflects the use of spear-phishing campaigns.

   TOOLS: -

   NOTE: -

 * Page #2:
   > We have seen two types of documents sent to victims in these spear phishing campaigns.

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: This reflects the use of spear-phishing campaigns to deliver malicious documents.

   TOOLS: -

   NOTE: -

   LINK: 003 OR 005

 * Page #2:
   > exploits the INCLUDEPICTURE feature of Microsoft Word

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The use of the INCLUDEPICTURE feature to gather information from a document represents a method of executing malicious content when the user interacts with the document.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #2:
   > to get context information about the victim's computer, and the availability and version number of Microsoft Word.

   ID: 004

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Gathering information about the victim's computer, such as the availability and version number of Microsoft Word, is an example of system information discovery.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > The second one, which in many cases is an O"ice document protected with a trivial password, such as "12345", "1234", etc., uses macros to execute a GRIFFON implant on the target's computer

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of macros to execute malicious code (the GRIFFON implant).

   TOOLS: -

   NOTE: -

   LINK: 002, 006

 * Page #2:
   > In various cases, the associated macro also scheduled tasks to make GRIFFON persistent.

   ID: 006

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Scheduling tasks via macros to ensure persistence of the GRIFFON implant is a common technique used to maintain access to a compromised system.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #4:
   > The GRIFFON implant is a lightweight JScript validatorstyle implant without any persistence mechanism

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVA SCRIPT (T1059.007)

   DESCRIPTION: The GRIFFON implant is written in JScript, meaning it uses JavaScript to execute commands and scripts.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The !rst module downloaded by the GRIFFON malware to the victim's computer is an information-gathering JScript

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVA SCRIPT (T1059.007)

   DESCRIPTION: the module is written in JScript, a scripting language used for command execution.

   TOOLS: -

   NOTE: -

 * Page #4:
   > This module mainly relies on WMI and Windows objects to deliver results

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of WMI (Windows Management Instrumentation) indicates that the malware queries system information through this interface for reconnaissance purposes.

   TOOLS: -

   NOTE: -

 * Page #4:
   > more than 20 artifacts are retrieved from the system by this implant during the reconnaissance stage,

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Gathering details about the system, such as operating system version and environment, is a form of system discovery.

   TOOLS: -

   NOTE: -

 * Page #4:
   > from the date and time of operating system installation and membership in a Windows domain

   ID: 011

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: Retrieving domain membership information is part of network configuration discovery.

   TOOLS: -

   NOTE: -

 * Page #4:
   > a list of and the resolutions of the workstation's monitors

   ID: 012

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collecting information about hardware configurations

   TOOLS: -

   NOTE: -

 * Page #4:
   > The second module is used by the operators to execute an obfuscated PowerShell script

   ID: 013

   SOURCE:TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell script is used to run the obfuscated script.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #4:
   > contains a Meterpreter downloader widely known as "Tinymet". This downloader, seen in past FIN7 campaigns, downloads a one-byte XOR-encrypted (eg. with the key equal to 0x50 or 0x51) piece of meterpreter shellcode to execute

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: An obfuscated PowerShell script and XOR-encrypted Meterpreter shellcode are downloaded into the victim's environment.

   TOOLS: METERPRETER

   NOTE: -

   LINK: 013, 015

 * Page #4:
   > XOR-encrypted (eg. with the key equal to 0x50 or 0x51)

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of XOR encryption and obfuscation of the shellcode directly relates to this technique.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #4:
   > allows the operators to take a screenshot of the remote system

   ID: 016

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: capturing screenshots of the victim's system

   TOOLS: -

   NOTE: -

   LINK: 017

 * Page #4:
   > it also drops a PowerShell script on the workstation to execute. The script executes an open-source .NET class used for taking a screenshot.

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: a PowerShell script on the workstation to execute, which uses an open-source .NET class to take a screenshot. 

   TOOLS: -

   NOTE: -

   LINK: 016, 018

 * Page #5:
   > If the victim appears valuable to the attackers, a GRIFFON implant installer is pushed to the victim's workstation

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Pushing a GRIFFON implant installer to the victim's workstation, which involves transferring files into the target system.

   TOOLS: -

   NOTE: -

   LINK: 019

 * Page #5:
   > This module stores another instance of the GRIFFON implant inside the registry to achieve persistence

   ID: 019

   SOURCE: TEXT

   TACTIC: PERISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/START FOLDER (T1547.001)

   DESCRIPTION: storing an instance of the GRIFFON implant in the registry

   TOOLS: -

   NOTE: -

   LINK: 018

 * Page #8:
   > AveMaria is a classic infostealer bot that collects all possible credentials

   ID: 020

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: The bot collects credentials from various software, which can include valid accounts for different services.

   TOOLS: AVEMARIA

   NOTE: -

   LINK: 021

 * Page #8:
   > can act as a keylogger.

   ID: 021

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009), CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: AveMaria acts as a keylogger, which involves capturing keystrokes made by the user to collect sensitive information.

   TOOLS: AVEMARIA

   NOTE: -

 * Page #8:
   > the cyber criminals use spearphishing emails with various types of attachments

   ID: 022

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The use of spear-phishing emails to deliver malware falls under phishing techniques.

   TOOLS: -

   NOTE: -

   LINK: 023

 * Page #8:
   > MS O"ice documents or spreadsheet !les exploiting some known vulnerability like CVE-2017-11882,

   ID: 023

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploiting known vulnerabilities in documents, such as CVE-2017-11882, to execute malware.

   TOOLS: -

   NOTE: -

   LINK: 022

