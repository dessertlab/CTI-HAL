## Detailed comments

 * Page #31:
   > COZY BEAR

   ID: 000

   TOOLS: COZYDUKE (S0046)

 * Page #31:
   > COZY BEAR's preferred intrusion method is a broadly targeted spearphish campaign that typically includes web links to a malicious dropper.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: The technique describes sending spearphishing emails that contain links to a malicious dropper.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

 * Page #31:
   > the code will deliver one of a number of sophisticated Remote Access Tools (RATs), including AdobeARM, ATI-Agent, and MiniDionis

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The technique describes the transfer of tools as RATs on the victim's machine.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   ---

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: The technique describes the use of remote access software to maintain control over infected systems., , and MiniDionis are examples of such tools.

   TOOLS: AdobeARM, ATI-Agent, MiniDionis

   NOTE: -

 * Page #32:
   > not being analyzed on a virtual machine, using a debugger, or located within a sandbox

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The dropper and payload contain techniques to ensure that the sample is not analyzed on a virtual machine, using a debugger, or within a sandbox.

   TOOLS: -

   NOTE: -

 * Page #32:
   > They have extensive checks for the various security software that is installed on the system and their specific configurations.

   ID: 005

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SOFTWARE DISCOVERY (T1518)

   SUB-TECHNIQUE: SECURITY SOFTWARE DISCOVERY (T1518.001)

   DESCRIPTION: Attackers perform extensive checks to identify the security software installed on the system and their specific configurations.

   TOOLS: -

   NOTE: -

 * Page #32:
   > When specific versions are discovered that may cause issues for the RAT, it promptly exits

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: EXECUTION GUARDRAILS (T1480)

   SUB-TECHNIQUE: -

   DESCRIPTION: When specific versions of security software are discovered that may cause problems for the RAT, the malware promptly closes to avoid detection or blocking.

   TOOLS: -

   NOTE: -

 * Page #32:
   > The implants are highly configurable via encrypted configuration files

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Implants (implants) use encrypted configuration files to hide and protect sensitive information such as command and control (C2) servers, initial tasks, persistence mechanisms, and encryption keys.

   TOOLS: -

   NOTE: -

 * Page #32:
   > An HTTP protocol with encrypted payload is used for the Command & Control communication

   ID: 011

   SOURCE: TEXT



   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -



   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.



   TOOLS: -



   NOTES: -

 * Page #34:
   > The COZY BEAR intrusion relied primarily on the SeaDaddy implant developed in Python and compiled with py2exe and another Powershell backdoor with persistence accomplished via Windows Management Instrumentation (WMI) system, which allowed the adversary to launch malicious code automatically after a specified period of system uptime or on a specific schedule

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: a single obfuscated command setup to run persistently via Windows Management Instrumentation (WMI) system

   TOOLS: -

   NOTE: -

 * Page #35:
   > It consists of a single obfuscated command setup to run persistently

   ID: 012



   SOURCE: TEXT



   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -



   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.



   TOOLS: -



   NOTES: -

 * Page #37:
   > This one-line powershell command, stored only in WMI database

   D: 013



   SOURCE: TEXT



   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)



   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution.



   TOOLS: -



   NOTES: -

   LINK: 014, 015

 * Page #37:
   > an encrypted connection to C2

   ID: 014



   SOURCE: TEXT



   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -



   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.



   TOOLS: -



   NOTES: -

   LINK: 013

 * Page #37:
   > downloads additional powershell modules from it, executing them in memory

    ID: 015



   SOURCE: TEXT



   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -



   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.



   TOOLS: -



   NOTES: -

   LINK: 013

 * Page #37:
   > Powershell version of credential theft tool MimiKatz was also used by the actors to facilitate credential acquisition for lateral movement purposes

   ID: 016



   SOURCE: TEXT



   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -



   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material.



   TOOLS: MimiKatz (S0002)



   NOTES: -

 * Page #37:
   > It was executed via rundll32 commands

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SIGNED BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: rundll32 commands were used

   TOOLS: -

   NOTE: -

 * Page #38:
   > They also engaged in a number of antiforensic analysis measures, such as periodic event log clearing (viawevtutil cl Systemand wevtutil cl Securitycommands) and resetting timestamps of files

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: delete or modify artifacts generated within systems to remove evidence of their presence or hinder defenses

   TOOLS: -

   NOTE: -
