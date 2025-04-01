## Detailed comments

 * Page #1:
   > APT34 has been observed targeting individuals through the use of booby-trapped job opportunity documents, delivered directly to the selected targets via LinkedIn messages

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHIN VIA SERVICE (T1566.002)

   DESCRIPTION: APT34's use of LinkedIn messages to deliver booby-trapped job opportunity documents is an example of spearphishing via a service

   TOOLS: -

   NOTE: -

 * Page #1:
   > malicious Microsoft Word document namedJob-Details.doc

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The Word document "Job-Details.doc" is the malicious file that the adversary is hoping the victim will execute, leading to the compromise of their system.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Verification that there is a mouse connected to the PC (Anti-Sandboxing technique)

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: IMPAIR DEFENSES (T1562)

   SUB-TECHNIQUE: DISABLE OR MODIFY TOOLS (T1562.001)

   DESCRIPTION: The verification of a connected mouse is an anti-sandboxing technique. Sandboxes, which are often used in malware analysis, might not simulate a connected mouse, allowing the malware to detect and avoid running in such an environment.

   TOOLS: -

   NOTE: -

   ---

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: TVerification that a mouse is connected to the PC (anti-sandboxing technique).

   TOOLS: -

   NOTE: -

 * Page #2:
   > Initial fingerprinting of the target device and sending of the information to the C2 server.

   ID: 004

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION:  Initial fingerprinting and sending of the target device's information to the C2 server is an example of using web protocols for command-and-control communication.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Dropping embedded executable to disk with a "doc" extension (later to be renamed to ".exe").

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Dropping an executable with a ".doc" extension and later renaming it to ".exe" is a technique used to disguise the file's true nature and avoid detection by users or automated systems.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Registering a Windows schedule task that would launch the executable every X minutes.

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The APT34 campaign uses a scheduled task to repeatedly launch the dropped executable file ("Client update.exe") as part of their persistence mechanism. The task is set to run every X minutes, ensuring that the malware remains active on the system over time.

   TOOLS: -

   NOTE: -

 * Page #3:
   > APT34 is notorious for its heavy use of DNS tunneling through many of their different tools, and this time this feature also made its way into the initial macros stage. Once the macros are executed, DNS requests are used to beacon back to the attacker, and inform them of the current stage of the execution, as well as to deliver some victim identifiable information. Fig

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: APT34 utilizes DNS tunneling to communicate with their command and control (C2) servers during the execution of the malicious macros. The macros use DNS requests to send beacons back to the attacker, providing updates on the malware's execution stage and delivering victim-identifiable information. This technique is characteristic of APT34's operations and is employed early in the attack chain to establish communication with the C2.

   TOOLS: -

   NOTE: -

 * Page #3:
   > encoded data

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: The gathered PC information is encoded before being used, likely to obfuscate the data and make it harder to detect by security mechanisms. This technique is used to obscure the data being collected and transmitted, thereby reducing the chances of detection by defensive tools.

   TOOLS: -

   NOTE: -

   LINK: 009, 010

 * Page #3:
   > derived from the PC information

   ID: 009

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: The encoded data being derived from the PC information indicates that the malware is gathering system-specific data, which is then encoded and possibly used for further operations such as communication with the C2 server. This technique is used by the malware to collect important system information to tailor its actions according to the target environment.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #3:
   > encoded DNS data

   ID: 010

   SOURCE: FIGURE

   DESCRIPTION: The figure show how the encoded data is deriverd 

   LINK: 008

 * Page #4:
   > The functionality of the backdoor includes download, upload and shell command execution

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The backdoor's ability to download files from a remote server aligns with this technique, as it involves transferring tools or files into the compromised environment.

   TOOLS: -

   NOTE: -

 * Page #4:
   > Persistence is achieved in the1ststage, when the schedule task is registered. The scheduled task namedSystemFailureReporter will execute the2ndstage payload every 5 minutes

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The creation of a scheduled task named SystemFailureReporter to execute the payload every 5 minutes is a direct use of this technique. The task ensures that the malicious payload continues to run and maintain persistence even after reboots or other interruptions.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The backdoor starts by collecting basic information about the victim's machine and calculating a 4-byte long victim identifier, based on the user-name, computer-name and the domain name of the target environment.

   ID: 013

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Calculating a victim identifier based on user-name, computer-name, and domain name involves collecting data from the local system to create a unique identifier for tracking and communication purposes.

   TOOLS: -

   NOTE: -

 * Page #4:
   > the malware will verify that theupdate.xml file

   ID: 014

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM SERVICE DISCOVERY (T1007)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware's verification of the existence of update.xml can be considered a form of system service discovery, where it checks for the presence of specific files or components required for further operations.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The response to this request is hidden in the source code of following Flickr lookalike page:

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of a "Flickr lookalike page" is an example of masquerading, where the attacker creates a page that resembles a legitimate service to hide malicious content or responses.

   TOOLS: -

   NOTE: -

 * Page #6:
   > As the basis for the encrypted communication, the attackers utilize the Mersenne Twister pseudorandom number generator.

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The Mersenne Twister PRNG might be used to generate keys or pseudorandom values that are part of an encryption scheme. This obfuscates the data being communicated between the malware and the command and control (C2) server, making it harder for defenders to interpret or detect.

   TOOLS: -

   NOTE: -

   ---

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attackers use the Mersenne Twister pseudorandom number generator as the basis for encrypted communication.

   TOOLS: -

   NOTE: -

