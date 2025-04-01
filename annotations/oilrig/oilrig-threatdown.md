## Detailed comments

 * Page #1:
   > a suspicious email that targeted a government oFcial from Jordan's foreign ministry. The email contained a malicious Excel document that drops a new backdoor named Saitama

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The malicious email targeting a government official from Jordan's foreign ministry, which contained a malicious Excel document, is a clear example of spear-phishing with an attachment.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The malicious email was sent to the victim via a Microsoft Outlook account with the subject "ConCrmation Receive Document" with an Excel Cle called "ConCrmation Receive Document.xls". The sender pretends to be a person from the Government of Jordan by using its coat of arms as a signature.

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION:  The malicious email with the subject "Confirmation Receive Document" and the attachment "Confirmation Receive Document.xls"

   TOOLS: -

   NOTE: -

 * Page #2:
   > The Excel attachment contains a macro that performs malicious activities

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The Excel attachment contains a macro that performs malicious activities. 

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #2:
   > The document has an image that tries to convince the victim to enable a macro.

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The image in the document is a social engineering tactic designed to persuade the victim to enable the macro, which is crucial for the attack to proceed.

   TOOLS: -

   NOTE: -

   LINK: 003, 005

 * Page #3:
   > After enabling the macro, the image is replaced with the Jordan government's the coat of the arms

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIDE ARTIFACTS (T1564)

   SUB-TECHNIQUE: MASQUERADE FILE (T1564.004)

   DESCRIPTION: After the macro is enabled, the image is replaced with the coat of arms of the Jordanian government. This act of swapping images can be seen as a form of masquerading, where the attacker attempts to make the document appear more legitimate to avoid raising suspicion from the victim.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #4:
   > Hides the current sheet and shows the new sheet that contains the coat of arms image

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIDE ARTIFACTS (T1564)

   SUB-TECHNIQUE: HIDDEN WINDOW (T1564.003)

   DESCRIPTION:  The Excel macro hides the current sheet (which likely contains the initial content that lures the victim into enabling macros) and shows a new sheet with the Jordanian government's coat of arms

   TOOLS: -

   NOTE: -

 * Page #4:
   > Calls the "eNotif' function which is used to send a notiCcation of each steps of macro execution to its server using the DNS protocol

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: Adversaries use DNS for communication between the malware and its C2 server.

   TOOLS: -

   NOTE: -

 * Page #4:
   > it uses the following WMI query to get the IP address of the request

   ID: 019

   SOURCE: TEXT 

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Uses WMI query to get IP address information.

   TOOLS: -

   NOTE: -

 * Page #4:
   > Creates a TaskService object and Gets the task folder that contains the list of the current tasks

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The creation of a `TaskService` object and retrieving the task folder that contains the list of current tasks indicates that the malware is interacting with the Windows Task Scheduler.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Checks if there is a mouse connected to PC

   ID: 009

   SOURCE: TEXT 

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: SYSTEM CHECKS (T1497.001)

   DESCRIPTION: The malware checks if a mouse is connected, which suggests it's attempting to determine if it is running on a real machine rather than in a virtualized or sandbox environment. This helps the malware avoid execution in an analysis environment, thus impairing defenses.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #5:
   > Reads the content of the UserForm1.label1, UserForm2.label1 and UserForm3.label1 that are in base64 format, decodes them and Cnally writes them into the created Cles in the previous step

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: he malware reads base64-encoded content from the user forms, decodes it, and writes the decoded content into the created files. 

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #5:
   > Checks the existence of theUpdate.exeCle

   ID: 011

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/STARTUP FOLDER (T1547.001)

   DESCRIPTION: This technique involves using the Windows Registry or startup folder to ensure that malicious executables are run at system startup or user logon.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #5:
   > it writes it using a technique that loads a DotNet assembly directly using mscorlib and Assembly.Load by manually accessing the VTable of the IUnknown

   ID: 012

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves the transfer of files or tools into a compromised environment, often from a remote server.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #6:
   > DeCnes a xml schema for a scheduled task and registers it using the RegisterTask function. The name of the scheduled task is MicrosoftUpdate and is used to make update.exepersistent

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: This technique involves creating or modifying scheduled tasks or jobs to establish persistence or perform automated tasks. In your case, the malware uses a scheduled task to ensure that update.exe remains persistent on the system.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Saitama backdoor abuses the DNS protocol for its command and control communications

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.003)

   DESCRIPTION: This technique involves using DNS (Domain Name System) for C2 communications.

   TOOLS: -

   NOTE: -

 * Page #7:
   > the actor cleverly uses techniques such as compression

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of compression to obscure the data being transmitted is an example of data obfuscation. 

   TOOLS: -

   NOTE: -

 * Page #9:
   > This state fetches the C&C server, expecting to receive a command from the attackers. These servers are generated by using the PRNG algorithm that involves transformations like the Mersenne Twister

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE:  DOMAIN GENERATION ALGORITHM (T1568.002)

   DESCRIPTION: The malware uses a Pseudo-Random Number Generator (PRNG), such as the Mersenne Twister, to generate subdomains dynamically. 

   TOOLS: -

   NOTE: -

 * Page #14:
   > As domain names are used to exCltrate unknown amounts of data, attackers had to split this data in different buffers. Every buffer is then sent through a different DNS request.

   ID: 020

   SOURCE: TEXT 

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: -

   NOTE: -

 * Page #15:
   > scheduled task that would launch the executable every X minutes

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The malicious document registers a scheduled task to execute an executable every X minutes, ensuring the malware runs persistently and systematically.

   TOOLS: -

   NOTE: -

 * Page #15:
   > anti sandboxing technique (checking if there is a mouse connected to the PC or not)

   ID: 018

   SOURCE: TEXT 

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: SYSTEM CHECKS (T1497.001)

   DESCRIPTION: The malware checks if a mouse is connected, which suggests it's attempting to determine if it is running on a real machine rather than in a virtualized or sandbox environment. This helps the malware avoid execution in an analysis environment, thus impairing defenses.

   TOOLS: -

   NOTE: -

