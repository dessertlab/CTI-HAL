## Detailed comments

 * Page 1:
   > FIN7 typically initiated its cyberattacks by delivering a "phishing" email to a company employee.  Each email included an attached file, often an innocuous-appearing Microsoft Word document, with embedded malware

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: phishing emails that contain a malicious Microsoft Word document designed to look harmless but includes embedded malware.

   TOOLS: -

   NOTE: -

 * Page 1:
   > The text within the email simulated a legitimate businessrelated message in order to lead the recipient employee to open the attachment and unwittingly activate the malware that would infect the computer.

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: It leads the employee to open the attachment and activate the malware.

   TOOLS: -

   NOTE: -

 * Page 1:
   > Once infected, the compromised victim computer connected to one of FIN7's command and control servers located throughout the world

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The infected computer connects to a command and control server, allowing FIN7 to remotely control the victim's machine.

   TOOLS: -

   NOTE: -

 * Page 1:
   > Through a specially designed control panel, FIN7 could download a wide array of additional malware to the victim computer,

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 downloads additional malware to the victim computer through its control panel.

   TOOLS: -

   NOTE: -

 * Page 1:
   > FIN7 incorporated and adapted the notorious Carbanak

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of Carbanak malware for persistent access and control.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page 1:
   > enabling them to secretly steal credentials and other network information

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Stealing credentials through surveillance for unauthorized access to sensitive information.

   TOOLS: -

   NOTE: -

   LINK: 005, 006

 * Page 1:
   > video recordings of desktop activity

   ID: 006

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: VIDEO CAPTURE (T1125)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware also recorded videos of desktop activity, enabling more detailed surveillance and data theft.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page 1:
   > FIN7 then used its unauthorized access to the victim's computer system to locate and extract various information and property of value, such as financial information and caches of customer payment card data

   ID: 008

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 used its access to extract financial information and customer payment card data from the victim's system.

   TOOLS: -

   NOTE: -

 * Page 1:
   > FIN7's malware allowed its members to conduct surveillance on company employees, including taking screen shots

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7's malware took screenshots of desktop activity to steal credentials and other sensitive information.

   TOOLS: -

   NOTE: -

   LINK: 007

