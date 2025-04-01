## Detailed comments

 * Page #2:
   > spear-phishing  emails  with  malicious  URLs

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Use of spear-phishing emails with malicious URLs

   TOOLS: -

   NOTE: -

 * Page #2:
   > tainted documents

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of contaminated documents to download a Cobalt Strike beacon component.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > Cobalt Strike

   ID: 003

   NOTE: download of a Cobalt Strike beacon from the email attachment

   TOOLS: COBALT STRIKE (S0154)

   LINK: 002

 * Page #2:
   > identify critical documents

   ID: 004

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Discovery activities to identify and locate sensitive information and files within the compromised infrastructure.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #2:
   > prepare them for exfiltration

   ID: 005

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Attackers prepare data to be exfiltrated from the compromised network to a location controlled by them.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #3:
   > malicious URLs

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Use of spear-phishing emails with malicious URLs

   TOOLS: -

   NOTE: -

 * Page #3:
   > booby-trapped documents

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of contaminated documents.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Cobalt  Strike

   ID: 008

   TOOLS: COBALT STRIKE (S0154)

 * Page #4:
   > The spear-phishing emails sent to the financial institutions either end up with victims downloading a tampered document

   ID: 009

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of contaminated documents to download a Cobalt Strike beacon component.

   TOOLS: -

   NOTE: -

   LINK: 010 OR 011, 012

 * Page #4:
   > download the Cobalt Strike beacon

   ID: 010

   NOTE: a tampered document meant to download the Cobalt Strike beacon

   TOOLS: COBALT STRIKE (S0154)

   LINK: 009

 * Page #4:
   > to exploit several unpatched Remote Code Execution Vulnerabilities and deploy a backdoor

   ID: 011

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of vulnerabilities to execute remote code.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #4:
   > Once the user attempts to open the attached documents,

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Execution of malicious files by the user.

   TOOLS: -

   NOTE: -

   LINK: 009, 013

 * Page #4:
   > scripts (Fig. 1) embedded within the files are dropped on the disk and automatically executed in the background.

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Scripts are embedded in the attached files and run automatically when the files are opened.

   TOOLS: -

   NOTE: -

   LINK: 012, 014

 * Page #4:
   > the attacks use reconnaissance tools designed to assess the state of the victim's workstation and determine what tools should be downloaded next

   ID: 014

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Gather information about the system to evaluate the configuration and installed applications.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #5:
   > spear-phishing attachment

   ID: 015

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Use of contaminated documents to download a Cobalt Strike beacon component.

   TOOLS: -

   NOTE: -

   LINK: 016

 * Page #5:
   > 16:48 – one of the employees opened the document within the spear-phishing email 16:49 – a second employee opened the same tainted document

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Execution of compromised documents by users.

   TOOLS: -

   NOTE: -

   LINK: 015, 017

 * Page #5:
   > Finally, a backdoor from the Command and Control Server was used to establish persistence in the infrastructure

   ID: 017

   NOTE: a backdoor from the Command and Control Server was used to estabilish. persistence in the infrastructure

   LINK: 018, 019, 020, 021

 * Page #5:
   > run shell commands to move laterally in the infrastructure,

   ID: 019

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION:  The attacker executes commands to interact with the system and move laterally.

   TOOLS: -

   NOTE: -

 * Page #5:
   > download additional scripts

   ID: 018

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading additional scripts.

   TOOLS: -

   NOTE: -

 * Page #5:
   > delete files from the system

   ID: 020

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Deleting files from the system.

   TOOLS: -

   NOTE: -

 * Page #5:
   > cleaning registry keys to leave fewer forensics traces

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: Attackers clean the logs to reduce the signs of their activities.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Credentials for one Domain Administrator were compromised and used throughout the duration of the attack

   ID: 022

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Compromising the credentials of a domain administrator.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The"swift-fraud[.]com/documents/94563784.doc"URL  was  opened  from  the  body  of  an  email  received  in  a spearphishing campaign targeting financial institutions.

   ID: 023

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Use of spear-phishing emails with malicious URLs

   TOOLS: -

   NOTE: -

   LINK: 024

 * Page #8:
   > The attack flow leaves behind a temporary file

   ID: 025

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The document downloaded from the malicious URL introduces files into the victim's system.

   TOOLS: -

   NOTE: -

   ID: 024

 * Page #8:
   > after the opening of the original document file, downloaded from the malicious URL mentioned above

   ID: 024

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Opening the original document downloaded from the malicious URL triggers the creation of the temporary file.

   TOOLS: -

   NOTE: -

   LINK: 023, 025

 * Page #8:
   > KbhpQIcahFCuZwq.sct - (bb784d55895db10b67b1b4f1f5b0be16) This object was not found on disk, it was deleted after running by "MGsCOxPSNK.txt".

   ID: 026

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION:  The file "MGsCOxPSNK.txt" was deleted after execution to avoid detection and forensic analysis.

   TOOLS: -

   NOTE: -

 * Page #8:
   > cqHfjCkTtMwG.doc (c2a9443aac258a60d8cace43e839cf9f) This file can be found at the path: C:\Users\[redacted]\AppData\Local\Temp\cqHfjCkTtMwG.doc. It is a decoy file, because it acts as a normal document file

   ID: 027

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of decoy files that look like normal documents.

   The file is used to disguise the malicious activity by making it look like a normal document.

   TOOLS: -

   NOTE: -

   LINK: 028

 * Page #8:
   > executed on the system

   ID: 029

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: Execution of the malicious payload through user interaction.

   The user opens the decoy file, which initiates the drop and execution of the malicious payload 

   TOOLS: -

   NOTE: -

 * Page #8:
   > the malicious payload is being dropped

   ID: 028

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer and placement of the malicious payload on the system.

   The decoy file facilitates the drop of the malicious payload onto the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 029

 * Page #8:
   > tCrrDqBQoCcEkbnK.txt (581c2a76b382deedb48d1df077e5bdf1) This object can be found at the path: C:\Users\[redacted]\AppData\Local\Temp\tCrrDqBQoCcEkbnK.txt. It is a configuration file for cmstp.exe. It downloads a DLL dropper from "cloud[.]yourdocument[.]biz/robots.txt"

   ID: 030

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of malicious tools or files into the target system.

   Downloading the DLL dropper from an external URL indicates the use of this technique to introduce malware into the system.

   TOOLS: -

   NOTE: -

   LINK: 031

 * Page #9:
   > the role of decrypting and dropping yet another JavaScript Dropper on the system

   ID: 031

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation or encryption of files to avoid detection.

   The DLL Dropper has the role of decrypting another dropper, suggesting that files are obfuscated or encrypted.

   TOOLS: -

   NOTE: -

   LINK: 030

 * Page #9:
   > the  DLL  will self-delete.

   ID: 032

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION:  Deleting the DLL from the system to avoid detection.

   TOOLS: -

   NOTE: -

 * Page #9:
   > the binary tried to download a JavaScript backdoor from the Command and Control server (C&C)"nl[.][redacted][.]kz/robots.txt"and saved the file to"%APPDATA%\9D01CA.txt"

   ID: 034

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: File transfer from a command and control (C2) server.	

   TOOLS: -

   NOTE: -

 * Page #9:
   > the file was obfuscated and encrypted with RC4

   ID: 033

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of files to avoid detection.

   TOOLS: -

   NOTE: -

 * Page #9:
   > The file "9D01CA.txt"sent an initial fingerprint of the system compromised which contained the name of the antivirus solution installed on the system, the local IP address, username, computername and OS version

   ID: 035

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The file "9D01CA.txt" collects and sends basic information about the compromised system, including computer name and operating system version.

   TOOLS: -

   NOTE: -

