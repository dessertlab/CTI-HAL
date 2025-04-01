## Detailed comments

 * Page #1:
   > The malware arrives via an email disguised as a tax incentive notification from a major financial services company. This email includes a macro enabled (XLSM) Microsoft Excel spreadsheet attachment (detected as Trojan.W97M.MERETAM.A) that purportedly contains the details of the tax incentive.

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0002)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Trickbot arrives via an email disguised as a tax incentive notification.

   TOOLS: TRICKBOT

   NOTE: -

   LINK: 003

   ---

   ID: 016

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Macro-enabled spreadsheet suggests Visual Basic macro used for initial payload delivery.

   TOOLS: -

   NOTE: -

 * Page #1:
   > Figure 1. Infection chain for the malware

   ID: 001

   SOURCE: FIGURE

   DESCRIPTION: infection chain for the malware

 * Page #2:
   > download and deploy Trickbot on the user's machine

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The macro downloads Trickbot from a remote server.

   TOOLS: TRICKBOT

   NOTE: -

   LINK: 003

 * Page #2:
   > once activated

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The email attachment is a macro-enabled Excel spreadsheet that the user is tricked into opening.

   TOOLS: TRICKBOT

   NOTE: -

   LINK: 002, 004

 * Page #2:
   > Virtual Network Computing (VNC)

   ID: 005

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: VNC (T1021.005)

   DESCRIPTION: The malware includes functionality to exploit VNC.

   TOOLS: TRICKBOT

   NOTE: -

 * Page #2:
   > PuTTY

   ID: 006

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SSH (T1021.004)

   DESCRIPTION: The malware includes functionality to exploit SSH, particularly via PuTTY.

   TOOLS: TRICKBOT

   NOTE: -

 * Page #2:
   > Remote Desktop Protocol (RDP)

   ID: 007

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: The malware includes functionality to exploit RDP.

   TOOLS: TRICKBOT

   NOTE: -

 * Page #3:
   > encrypts the strings it uses via simple variants of XOR or SUB routines

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use obfuscation techniques to hide code or strings within the malware.

   TOOLS: -

   NOTE: -

 * Page #4:
   > It also makes use of API hashes for indirect API calling, which was prominently attributed to the Carberp trojan source code leak from 2013

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using API hashing to obscure API calls

   TOOLS: -

   NOTE: -

 * Page #4:
   > the pwgrab module searches for files using the "*.vnc.lnk" a!x

   ID: 010

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: CREDENTIALS IN FILES (T1552.001)

   DESCRIPTION: Adversaries may search for and steal credentials stored in files.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The module will send the required data via POST, which is configured through a downloaded configuration file using the filename "dpost."

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Using HTTP POST for data exfiltration to evade detection.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #5:
   > This file contains a list of command-and-control (C&C) servers that will receive the exfiltrated data from the victim.

   ID: 012

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Sending exfiltrated data to C2 servers via HTTP POST.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #5:
   > it queries the registry key Software\SimonTatham\Putty\Sessions to identify the saved connection settings

   ID: 013

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Querying the registry to identify PuTTY sessions and settings.

   TOOLS: -

   NOTE: -

   LINK: 014

   ---

   ID: 017

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Trickbot specifically queries registry for saved credentials.

   TOOLS: -

   NOTE: -

   LINK: -

 * Page #5:
   > To retrieve the PuTTY credentials, it queries the registry key Software\SimonTatham\Putty\Sessions to identify the saved connection settings, which allows the module to retrieve information such as the Hostname and Username, and Private Key Files used for authentication.

   ID: 018

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Credential harvesting across multiple local applications and services, including VNC and PuTTY, demonstrated by searching specific directories and registry keys.

   TOOLS: -

   NOTE: -

   LINK: -

 * Page #5:
   > which allows the module to retrieve information such as the Hostname and Username, and Private Key Files used for authentication

   ID: 014

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1522)

   SUB-TECHNIQUE: PRIVATE KEYS (T1522.004)

   DESCRIPTION: Retrieving PuTTY private keys used for SSH authentication.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #6:
   > Its third function related to RDP uses the CredEnumerateA API to identify and steal saved credentials.

   ID: 015

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: CREDENTIAL API (T1552.006)

   DESCRIPTION: Using CredEnumerateA API to steal saved RDP credentials.

   TOOLS: -

   NOTE: -
