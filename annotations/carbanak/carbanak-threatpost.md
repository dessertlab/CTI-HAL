## Detailed comments

 * Page #1:
   > The crime group would send out bank employees spear phishing emails, impersonating legitimate companies, which harbored a malicious attachment

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing emails with malicious attachments.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #1:
   > the criminals would use their malware to remotely control the victims' machines

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of remote access software to control victims' machines.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #1:
   > If the attachments were executed

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: If the attachments are executed, the malware is activated.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > The group first launched a campaign in 2013 using malware known as Anunak to target financial transfers and ATM networks of financial institutions, but by the following year that malware had been improved into a more sophisticated version known as Carbanak.

   ID: 004

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: DEVELOP CAPABILITIES (T1587)

   SUB-TECHNIQUE: MALWARE (T1587.001)

   DESCRIPTION: the attackers use Anunak

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #2:
   > From then onwards, the crime syndicate focused their efforts into developing an even more sophisticated wave of attacks by using tailormade malware based on the Cobalt Strike penetration testing software,"

   ID: 009

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: DEVELOP CAPABITILITES (T1587)

   SUB-TECHNIQUE: MALWARE (T1587.001)

   DESCRIPTION: use of a malware based on the Cobalt Strike penetration testing sofware 

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #3:
   > The spear-phishing emails contain attachments

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending spear phishing emails with malicious attachments.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #3:
   > that eventually download and execute a dropper

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: If the attachments are executed, the malware is activated.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #3:
   > The backdoor is used to send system information and execute malicious code

   ID: 007

   NOTE: The backdoor is used to send system information and execute malicious code

   TOOLS: CARBANAK (S0030)

   LINK: 008, 009

 * Page #3:
   > screen recording

   ID: 009

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capture of compromised system screenshots.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #3:
   > steals credentials

   ID: 008

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: Access to stored credentials

   TOOLS: -

   NOTE: -

   LINK: 007

