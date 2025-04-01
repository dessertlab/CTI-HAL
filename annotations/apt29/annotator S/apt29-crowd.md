## Detailed comments

 * Page #31:
   > COZY BEAR's preferred intrusion method is a broadly targeted spearphish campaign that typically includes web links to a malicious dropper

   ID: 004

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious link in order to gain execution. 

   TOOLS: -

   NOTES: -

 * Page #31:
   > the code will deliver one of a number of sophisticated Remote Access Tools (RATs), including AdobeARM, ATI-Agent, and MiniDionis

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may use legitimate desktop support and remote access software to establish an interactive command and control channel to target systems within networks. 

   TOOLS: AdobeARM, ATI-Agent, MiniDionis

   NOTES: -

 * Page #32:
   > ensure the sample is not being analyzed on a virtual machine, using a debugger, or located within a sandbox

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEBUGGER EVASION (T1622)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various means to detect and avoid debuggers.

   TOOLS: -

   NOTES: -

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various means to detect and avoid virtualization and analysis environments. This may include changing behaviors based on the results of checks for the presence of artifacts indicative of a virtual machine environment (VME) or sandbox.

   TOOLS: -

   NOTES: -

 * Page #32:
   > They have extensive checks for the various security software that is installed on the system and their specific configurations.

   ID: 001

    

   SOURCE: TEXT

    

   TACTIC: DISCOVERY (TA0007)

    

   TECHNIQUE: SOFTWARE DISCOVERY (T1518)

    

   SUB-TECHNIQUE: SECURITY SOFTWARE DISCOVERY (T1518.001)

    

   DESCRIPTION: Attackers perform extensive checks to identify the security software installed on the system and their specific configurations.

    

   TOOLS: -

    

   NOTE: -

 * Page #32:
   > An HTTP protocol with encrypted payload is used for the Command & Control communication.

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.

   TOOLS: -

   NOTES: -

 * Page #34:
   > The COZY BEAR intrusion relied primarily on the SeaDaddy implant developed in Python and compiled with py2exe and another Powershell backdoor with persistence accomplished via Windows Management Instrumentation (WMI) system, which allowed the adversary to launch malicious code automatically after a specified period of system uptime or on a specific schedule.

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads.

   TOOLS: -

   NOTES: -

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
   > This one-line powershell command

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #37:
   > establishes an encrypted connection to C2

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTES: -

 * Page #37:
   > downloads additional powershell modules from it

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #37:
   > Powershell version of credential theft tool MimiKatz was also used by the actors to facilitate credential acquisition for lateral movement purposes.

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

   ID: 017

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

    

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

    

   TOOLS: -

    

   NOTE: -

 * Page #38:
   > They also engaged in a number of antiforensic analysis measures, such as periodic event log clearing

   ID: 017

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

    

   TECHNIQUE: INDICATOR REMOVAL (T1070)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may delete or modify artifacts generated within systems to remove evidence of their presence or hinder defenses.

    

   TOOLS: -

    

   NOTE: -

