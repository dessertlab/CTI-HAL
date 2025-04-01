## Detailed comments

 * Page #2:
   > spearphishing campaigns leveraging web links to a malicious dropper

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: APT29 created targeted spearphishing campaigns using links to a malicious dropper.

   TOOLS: -

   NOTE: -

   LINK: 002, 003

 * Page #2:
   > once executed, the code delivers Remote Access Tools (RATs) and evades detection using a range of techniques

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS LINK (T1204.001)

   DESCRIPTION: Once executed, the malicious link code delivers remote access tools (RATs).

   TOOLS: -

   NOTE: -

   LINK: 001, 003

   ---

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The dropper downloads and installs remote access tools (RATs) on the victim's machine.

   TOOLS: -

   NOTE: -

   LINK: 001, 002

 * Page #2:
   > These actors set up operational infrastructure to obfuscate their source infrastructure, host domains and malware

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Obfuscation of files or information to evade detection.

   TOOLS: -

   NOTE: -

 * Page #2:
   > APT29 spearphishing campaign directed emails containing a malicious link

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Sending targeted emails containing malicious links to compromise target systems.

   TOOLS: -

   NOTE: -

