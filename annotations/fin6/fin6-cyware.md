## Detailed comments

 * Page #1:
   > FIN6 relied on Windows' Remote Desktop Protocol (RDP) to move laterally across a ected networks

   ID: 001

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Using Windows' Remote Desktop Protocol (RDP) to move laterally across affected networks

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #1:
   > two di erent techniques

   ID: 002

   NOTE: FIN6 employed two different techniques after using RDP

   LINK: 001 THEN T01 OR T02

 * Page #1:
   > This movement enabled FIN6 to then inject LockerGoga and Ryuk ransomware

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Injecting LockerGoga and Ryuk ransomware

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #1:
   > executing an encoded command through PowerShell

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Executing an encoded command through PowerShell

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #1:
   >  rst technique

   ID: T001

   LINK: 004, 005, 006

 * Page #1:
   > which in turn was con gured to drop a malicious payload onto the systems

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Cobalt Strike payload dropping a malicious payload onto the systems

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 005

 * Page #1:
   > The command downloaded a Cobalt Strike payload

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading a Cobalt Strike payload

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 004, 006

 * Page #1:
   > use of a Windows Service created by Metasploit

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCLATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.003)

   DESCRIPTION: Use of a Windows Service created by Metasploit

   TOOLS: METASPLOIT

   NOTE: -

   LINK: 008

 * Page #1:
   > second technique

   ID: T02

   LINK: 007, 008, 009

 * Page #1:
   > that was used to communicate with a C2 server for dropping additional payloads into compromised systems.

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Communicating with a C2 server for dropping additional payloads

   TOOLS: -

   NOTE: -

   LINK: 007, 009

 * Page #1:
   > This would allow FIN6 to escalate privileges in the system.

   ID: 009

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCLATION (TA0004)

   TECHNIQUE: EXPLOITATION FOR PRIVILEGE ESCALATION (T1068)

   SUB-TECHNIQUE: -

   DESCRIPTION: Escalating privileges in the system

   TOOLS: -

   NOTE: -

   LINK: 008

