## Detailed comments

 * Page #3:
   > Trickbot,

   ID: 001

   SOURCE: TEXT

   TOOLS: TRICKBOT (S0266)

 * Page #3:
   > UNC1878 obtains credentials using Mimikatz, LaZagne and Kerbrute

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PERSISTENCE (TA0003), INITIAL ACCESS (TA0001), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using stolen credentials obtained by tools like Mimikatz, LaZagne, and Kerbrute.

   TOOLS: MIMIKATZ (S0002), LAZAGNE (S0349)

   LINK: 003, 004

   ---

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIALS ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #3:
   > extended their access by connecting to network shares and directly to systems over RDP

   ID: 003

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Using RDP for lateral movement within the network.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #4:
   > and SSH

   ID: 004

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SSH (T1021.004)

   DESCRIPTION: Using SSH for lateral movement within the network

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #4:
   > renewed phishing attempts to re-establish a foothold

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using phishing  to re-establish a foothold

   TOOLS: -

   NOTE: -

 * Page #5:
   > into a directory they create named "share$

   ID: 007

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA STAGED (T1074)

   SUB-TECHNIQUE: LOCAL DATA STAGING (T1074.001)

   DESCRIPTION: Unzipping files into a created directory named share$ for local staging.

   TOOLS: RYUK (S0446)

   NOTE: -

   LINK: 006

 * Page #5:
   > They'll then unzip

   ID: 006

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: The process of unzipping files, which may also imply the initial use of zipping for archiving collected or staged data.

   TOOLS: RYUK (S0446)

   NOTE: -

   LINK: 007

 * Page #5:
   > There are three ".bat" scripts used for iterating computer names to execute Ryuk.

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of .bat scripts for executing commands, in this case, for iterating computer names and executing Ryuk.

   TOOLS: RYUK (S0446)

   NOTE: -
