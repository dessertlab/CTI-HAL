## Detailed comments

 * Page #2:
   > APT29 has been observed crafting targeted spearphishing campaigns leveraging web links to a malicious dropper

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious link in order to gain execution. 

   TOOLS: -

   NOTES: -

 * Page #2:
   > once executed, the code delivers Remote Access Tools (RATs) and evades detection using a range of techniques.

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may use legitimate desktop support and remote access software to establish an interactive command and control channel to target systems within networks. 

   TOOLS: -

   NOTES: -

   ---

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious link in order to gain execution.

   TOOLS: -

   NOTES: -

 * Page #2:
   > both groups exfiltrate and analyze information to gain intelligence value

   ID: 004

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: AUTOMATED EXFILTRATION (T1020)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exfiltrate data. 

   TOOLS: -

   NOTES: -

 * Page #2:
   > These actors set up operational infrastructure to obfuscate their source infrastructure, host domains and malware for targeting organizations, establish command and control nodes, and harvest credentials and other valuable information from their targets.

   ID: 005

   SOURCE: TEXT

    

   TACTIC: DEFENSE EVASION (TA0005)

    

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Obfuscation of files or information to evade detection.

    

   TOOLS: -

    

   NOTE: -

   ID: 006

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material.

   TOOLS: -

   NOTES: -

 * Page #2:
   > an APT29 spearphishing campaign directed emails containing a malicious link to over 1,000 recipients

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #3:
   > At least one targeted individual activated links to malware hosted on operational infrastructure of opened attachments containing malware

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: An adversary may rely upon a user clicking a malicious link in order to gain execution. 

   TOOLS: -

   NOTES: -

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTES: -

   LINK: #007 THEN #008, #009

 * Page #3:
   > APT29 delivered malware to the political party's systems

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #3:
   > enumerated active directory accounts

   ID: 011

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: APT29 conducted reconnaissance against Active Directory.

   TOOLS: -

   NOTES: -

 * Page #3:
   > through encrypted connections back through operational infrastructure.

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTES: -

 * Page #3:
   > exfiltrated email from several accounts

   ID: 012

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel.

   TOOLS: -

   NOTES: -

