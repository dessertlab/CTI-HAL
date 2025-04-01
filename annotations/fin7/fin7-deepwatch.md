## Detailed comments

 * Page #3:
   > This starts as a spear phishing email sent to the initial target

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION:  FIN7 starts their attack with spear phishing emails to deliver malware. The emails are crafted to provoke a reaction from the target, often using emotional triggers such as 

   TOOLS: -

   NOTE: -

 * Page #3:
   > The exchange then leads to an initial document delivery that is usually benign

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: sending attachments as part of a spear phishing campaign. The initial document may appear benign but includes tracking mechanisms.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #3:
   > possesses a tracking pixel that allows the actor to verify whether or not the target is opening attachments, and if so can provide initial visibility into the system of the target

   ID: 003

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: SYSTEM NETWORK CONNECTIONS DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: the document or tracking mechanism provides information about network connections or system details

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > The second document the attacker sends is usually the one with the actual payload. This document has either a VBA macro or an embedded OLE which persuades the target to run these in order to drop the first stage loaders

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPOLITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploiting vulnerabilities in client applications to execute malicious payloads. 

   TOOLS: -

   NOTE: -

   ---

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTE: -

   ---

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Adversaries may abuse Visual Basic (VB) for execution.

   TOOLS: -

   NOTE: -

 * Page #4:
   > Spear phishing a target with a document loaded with a malware payload which as of May 2018 has been the Gri"on payload, or a combination of SQLRat and DNSBot historically.

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: sending phishing emails with malicious attachments to target individuals.

   TOOLS: -

   NOTE: -

 * Page #4:
   > To establish persistence, the group then injects a scheduled task to reestablish the C2 connection to Cobalt Strike which historically is run twice a day

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Creating scheduled tasks to ensure persistence and reestablish connections is covered under this TTP.

   TOOLS: -

   NOTE: -

 * Page #4:
   > From there the adversary loads process injection tools or memory scrapers (commonly mimikatz) and pivots using tools like powersploit, RDP services, and PowerAdmin Exec.

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCLATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may inject code into processes in order to evade process-based defenses as well as possibly elevate privileges.

   TOOLS: -

   NOTE: -

   ---

   ID: 010

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Adversaries may attempt to access credential material stored in the process memory of LSASS.

   TOOLS: Mimikatz (S0002)

   NOTE: -

   ---

   ID: 011

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT(TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Adversaries may use Valid Accounts to log into a computer using the Remote Desktop Protocol (RDP). The adversary may then perform actions as the logged-on user.

   TOOLS: -

   NOTE: -

