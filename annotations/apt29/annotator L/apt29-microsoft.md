## Detailed comments

 * Page #1:
   > CozyBear

   ID: 000

   TOOLS: COZYBEAR (S0046)

 * Page #2:
   > The spear-phishing emails mimicked sharing notifications from OneDrive

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: The spear-phishing emails included links that looked like OneDrive share notifications.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > If recipients clicked a link on the spear-phishing emails

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: The exploitation chain is initiated when recipients click on the link in the spear-phishing email

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > they began an exploitation chain that resulted in the implantation of a DLL backdoor

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The exploitation chain involves the installation of a backdoor DLL on the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #2:
   > that gave the attackers remote access to the recipients' machines.

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: The backdoor DLL provides attackers with remote access to victim systems.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #3:
   > Attack chain

   ID: 005

   SOURCE: IMAGE

   NOTE: ATTACK CHAIN

 * Page #3:
   > The spear-phishing emails used in this attack resemble file-sharing notifications from OneDrive.

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: The spear-phishing emails included links that looked like OneDrive share notifications.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #3:
   > The emails contain a link to a legitimate, but compromised third-party website

   ID: 007

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: DOMAINS (T1584.001)

   DESCRIPTION: Attackers use a legitimate but compromised third-party website to host malicious content.

   TOOLS: -

   NOTE: -

   LINK: 006, 008

 * Page #3:
   > they are served a ZIP archive containing a malicious LNK file

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The ZIP archive contains a malicious LNK file.

   TOOLS: -

   NOTE: -

   LINK: 008, 010

 * Page #3:
   > users click the link

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: Users must open the malicious LNK file.

   TOOLS: -

   NOTE: -

   LINK: 007, 009

 * Page #4:
   > It executes an obfuscated PowerShell command

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: An obfuscated PowerShell command is executed.

   TOOLS: -

   NOTE: -

   LINK: 011, 012

   ---

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerShell command is obfuscated.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #4:
   > that extracts a base64-encoded payload from within the LNK file itself,

   ID: 012

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

    

   TOOLS: -

    

   NOTES: -

   LINK: 010

 * Page #4:
   > cyzfc.dat, is created by the PowerShell script in the path %AppData%\Local\cyzfc.dat.

   ID: 013

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The PowerShell script creates the first stage DLL, `cyzfc.dat`, in the path `%AppData%\Local\cyzfc.dat`.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The PowerShell script then executes cyzfc.dat by calling rundll32.exe.

   ID: 014

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The PowerShell script executes `cyzfc.dat` by calling `rundll32.exe`.

   TOOLS: -

   NOTE: -

   LINK: 015, 019

   ---

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: The PowerShell script then executes cyzfc.dat by calling rundll32.exe

   TOOLS: -

   NOTE: -

 * Page #4:
   > cyzfc.dat begins to install the final payload by taking the following actions

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION:  `cyzfc.dat` extracts and installs the final payload.

   TOOLS: -

   NOTE: -

 * Page #4:
   > De-XOR the second-stage payload with a rolling XOR (ROR1), starting from key 0xC5.

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: De-XOR of the second-stage payload with a rotating XOR (ROR1), starting at byte 0xC5.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The second stage is an instance of Cobalt Strike

   ID: 017

   TOOLS: COBALTSTRIKE (S0154)

 * Page #5:
   > That payload is XORed with the same XORing algorithm used for reading

   ID: 020

    

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

    

   TOOLS: -

    

   NOTES: -

 * Page #5:
   > Meterpreter

   ID: 018

   TOOLS: METERPETER

 * Page #5:
   > The third payload eventually gets loaded and connects to the command-andcontrol (C&C) server address that is baked-in inside configuration information in the PE file

   ID: 021

    

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.

    

   TOOLS: -

    

   NOTES: -

