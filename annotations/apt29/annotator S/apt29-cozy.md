## Detailed comments

 * Page #1:
   > The a!empts involved a phishing email appearing to be from the U.S. Depa"ment of State with links to zip #les containing malicious Windows sho"cuts that delivered Cobalt Strike Beacon.

   ID: 016

    

   SOURCE: TEXT

    

   TACTIC: INITIAL ACCESS (TA0001)

    

   TECHNIQUE: PHISHING (T1566)

    

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

    

   DESCRIPTION: Phishing emails that contain links to malicious zipper files.

    

   TOOLS: -

    

   NOTE: -

 * Page #2:
   > The a!acker appears to have compromised the email server of a hospital and the corporate website of a consulting company in order to use their infrastructure to send phishing emails.

   ID: 015

    

   SOURCE: TEXT

    

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may buy and/or steal capabilities that can be used during targeting.

    

   TOOLS: -

    

   NOTES: -

 * Page #2:
   > The a!acker used unique links in each phishing email

   ID: 017

    

   SOURCE: TEXT

    

   TACTIC: INITIAL ACCESS (TA0001)

    

   TECHNIQUE: PHISHING (T1566)

    

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

    

   DESCRIPTION: Phishing emails that contain links to malicious zipper files.

    

   TOOLS: -

    

   NOTE: -

 * Page #3:
   > The threat actor cra&ed the phishing emails to masquerade as a U.S. Depa"ment of State Public A%airs o$cial sharing an o$cial document.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #3:
   > The links led to a ZIP archive that contained a weaponized Windows sho"cut #le hosted on a likely compromised legitimate domain,

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: MALICIOUS FILE (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTES: -

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTES: -

   LINK: #001 THEN #002

 * Page #3:
   > The sho"cut #le was cra&ed to execute a PowerShell command that read, decoded, and executed additional code from within the sho"cut #le.

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #3:
   > Cobalt Strike

   ID: 000

   TOOLS: Cobalt Strike (S0154)

 * Page #3:
   > The BEACON payload was con#gured with a modi#ed variation of the publicly available "Pandora" Malleable C2 Pro#le and used a command and control (C2) domain

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTES: -

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Commands to the remote system, and often the results of those commands, will be embedded within the protocol traffic between the client and server.

   TOOLS: -

   NOTES: -

 * Page #5:
   > Each phishing email contained a unique malicious URL, likely for tracking victim clicks.

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link.

   TOOLS: -

   NOTES: -

 * Page #6:
   > ds7002.lnk was a malicious sho"cut (LNK) #le that contained an embedded BEACON DLL and decoy PDF, and was cra&ed to launch a PowerShell command.

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTES: -

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution. 

   TOOLS: -

   NOTES: -

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DLL INJECTION (T1055.001)

   DESCRIPTION: Adversaries may inject dynamic-link libraries (DLLs).

   TOOLS: -

   NOTES: -

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #6:
   > the PowerShell command extracted and executed the Cobalt Strike BEACON backdoor and decoy PDF.

   ID: 012

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.

   TOOLS: -

   NOTES: -

 * Page #8:
   > This command included some speci#c obfuscation, which may indicate a!empts to bypass speci#c detection logic. For example, the use of 'FromBase'+0x40+'String', in place of FromBase64String, the PowerShell command used to decode base64.

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit. 

   TOOLS: -

   NOTES: -

 * Page #9:
   > The PowerShell loader code is obfuscated

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit. 

   TOOLS: -

   NOTES: -

 * Page #10:
   > The dropped BEACON loader DLL was executed by RunDll32.exe using the expo" function "PointFunctionCall":

   ID: 014

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

    

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

    

   TOOLS: -

    

   NOTES: -

