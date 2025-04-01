## Detailed comments

 * Page #3:
   > FIN7 sent spear phishing emails to personnel involved with United States Securities and Exchange Commission (SEC) #lings at multiple organizations

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: FIN7's use of spear-phishing emails with malicious attachments to target individuals with access to valuable SEC filings

   TOOLS: -

   NOTE: -

 * Page #4:
   > FIN7's spear phishing emails that leveraged hidden sho%cut #les (LNK #les)

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: FIN7 used spear-phishing emails containing LNK files to trick victims into initiating the infection process.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #4:
   > leveraged hidden sho%cut #les (LNK #les) to initiate the infection

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The use of LNK files as a method of delivering malware that requires the victim to execute the file.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #4:
   > VBScript functionality launched by mshta.exe to infect the victim

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPOLITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The mshta.exe process and VBScript execution are used to exploit the system for code execution without relying on Office macros.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #4:
   > FIN7's use of the CARBANAK backdoor as a postexploitation tool to cement their foothold in a network and maintain access to victim environments

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: The CARBANAK backdoor allows FIN7 to maintain remote access to victim systems, giving them control over compromised environments for extended periods.

   TOOLS: CARBANAK (S0030)

   NOTE: -

