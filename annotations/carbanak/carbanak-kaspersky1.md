## Detailed comments

 * Page #2:
   > Further forensic analysis took us to the point of initial infection: a spear phishing e-mail with a CPL attachment; although in other cases Word documents exploiting known vulnerabilities were used

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: a spear-phishing email with a CPL attachment

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #2:
   > a spear phishing e-mail with a CPL attachment; although in other cases Word documents

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing e-mails with malicious attachments to induce the victim to execute the malware.

   TOOLS: -

   NOTE: -

   LINK: 002, 006

 * Page #2:
   > exploiting known vulnerabilities were used

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of vulnerabilities in client software to execute arbitrary code.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > After executing the shellcode, a backdoor based on Carberp, is installed on the system

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of tools or payloads from an external network to a compromised network.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 002

 * Page #3:
   > infected computers were used to record videos that were then sent to the Command and Control servers

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: VIDEO CAPTURE (T1125)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of video from compromised devices.

   TOOLS: -

   NOTE: -

   LINK: 007, 008

   ---

   ID: 007

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of video from compromised devices

   TOOLS:  -

   NOTE: -

   LINK: 004, 008

 * Page #3:
   > Even though the quality of the videos was relatively poor, they were still good enough for the attackers, armed also with the keylogged data for that particular machine to understand what the victim was doing

   ID: 008

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: attackers with the keylogged data for that particular machine can understand what the victim was doing

   TOOLS:  - 

   NOTE: -

   LINK: 004, 007

 * Page #7:
   > Attackers used spear phishing emails with malicious attachments

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing e-mails with malicious attachments to induce the victim to execute the malware.

   TOOLS: -

   NOTE: -

