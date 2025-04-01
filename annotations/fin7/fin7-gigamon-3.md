## Detailed comments

 * Page #3:
   > FIN7 used Cobalt Strike's DNS C2 as their method of maintaining access inside target environments

   ID: 001

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: DNS tunneling is used to establish and maintain a covert channel for C2 communication, evading traditional detection mechanisms that might monitor for suspicious IP traffic.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #3:
   > C2 method leveraged a different encrypted communication

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMUNICATION AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: - 

   DESCRIPTION: an encrypted comunication channel is used

   TOOLS: -

   NOTE: -

 * Page #4:
   > the threat actors would spawn a secondary C2 component during their off-hour periods in an apparent attempt to maintain access should the DNS C2 be detected

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: FALLBACK CHANNEL (T1008)

   SUB-TECHNIQUE: - 

   DESCRIPTION: a secondary C2 is used

   TOOLS: -

   NOTE: -

 * Page #5:
   > DNS C2 leverages malicious DNS TXT and A RRs (resource records) queries which traverse standard recursive DNS channels and terminate at an attacker's authoritative DNS server

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: DNS C2 uses legitimate-looking DNS traffic to communicate with the attacker's server. Queries containing data or commands are sent as DNS TXT (Text) or A (Address) resource records, making the traffic blend into normal DNS activity. This is effective in environments with restrictive firewalls, web filters, or proxies, such as POS networks in the retail or hospitality sectors, where DNS traffic is often allowed and less scrutinized.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #6:
   > the actors used PowerShell scripts to deploy DNS TXT record stagers into memory

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell scripts are used to deploy DNS TXT record stagers into memory.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #6:
   > During execution, PowerShell would make iterative DNS TXT queries, which would return encrypted data to be concatenated and then executed in memory

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: DNS TXT queries are used for communication with the C2 server, returning encrypted data to be executed.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 003

   ---

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: encrypted data are returned

    

   TOOLS: -

   NOTE: -

 * Page #7:
   > After staging, the attacker would shift to the use of DNS A resource records. When idle, the malware would make requests to the attacker-controlled domain with a pattern matching [SessionID].MaliciousDomain.com

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: use of DNS A resource records for maintaining command and control communication

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #10:
   > FIN7 would frequently use the psexec_psh (https://blog.cobaltstrike.com/2015/07/29/cobaltstrike-2-5-advanced-pivoting/) command within Cobalt Strike, which uses the RPC Service Controller protocol to create a service on a remote host with the binary path

   ID: 006

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: use of Cobalt Strike's psexec_psh command to create and execute services on remote hosts using the RPC Service Controller protoco

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 007

 * Page #10:
   > set to execute a malicious PowerShell command

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: executing malicious PowerShell commands

   TOOLS: -

   NOTE: -

   LINK: 007

