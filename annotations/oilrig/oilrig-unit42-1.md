## Detailed comments

 * Page #3:
   > spear-phishing as their initial attack vector

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: OilRig uses spear-phishing emails

   TOOLS: -

   NOTE: -

 * Page #3:
   > OilRig preferred macro-enabled Microsoft Office (Word and Excel) documents to install their custom payloads

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: OilRig uses spear-phishing emails with macro-enabled Microsoft Office (Word and Excel) documents to deliver their custom payloads.

   TOOLS: -

   NOTE: -

   LINK: 003, 004

 * Page #3:
   > ilRig's custom payloads frequently used DNS tunneling as a command and control (C2) channel.

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: Custom payloads frequently use DNS tunneling for C2 communication.

   TOOLS: -

   NOTE: -

 * Page #3:
   > PowerShell

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Custom payloads include PowerShell scripts.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > VBScripts.

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Custom payloads include VBScripts.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > Once gaining access to an end point, actors would use credential dumping tools, such as Mimikatz to gather credentials to legitimate accounts to then move laterally to other systems on the network

   ID: 006

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using tools like Mimikatz to dump credentials

   TOOLS: MIMIKATZ (S0002)

   NOTE: -

 * Page #3:
   > OilRig would install a webshell as another ingress point to maintain access to the network

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: WEB SHELL (T1505.003)

   DESCRIPTION: Installing web shells on compromised web servers to maintain access.

   TOOLS: -

   NOTE: -

