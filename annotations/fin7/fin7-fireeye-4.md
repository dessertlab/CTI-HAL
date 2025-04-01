## Detailed comments

 * Page #2:
   > desktop video capture

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to take screen captures of the desktop to gather information over the course of an operation.

   TOOLS: -

   NOTE: -

 * Page #2:
   > VNC,

   ID: 006

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: VNC (T1021.005)

   DESCRIPTION: Some of its capabilities include VNC.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Logs key strokes for Key con#gured processes and logger sends them to the command and control (C2) server

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009), CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Adversaries may log user keystrokes to intercept credentials as the user types them.

   TOOLS: -

   NOTE: -

 * Page #11:
   > CARBANAK communicates to its C2 servers via pseudo-HTTP or a custom binary protocol.

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: NON-APPLICATION LAYER PROTOCOL (T1095)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use an OSI non-application layer protocol for communication between host and C2 server or among infected hosts within a network. 

   TOOLS: -

   NOTE: -

 * Page #12:
   > Messages are encrypted using Microso$'s implementation of RC2 in CBC mode with PKCS#5 padding. The encrypted message is then Base64 encoded

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Most of CARBANAK's strings are encrypted in order to make analysis more difficult.

   TOOLS: -

   NOTE: -

 * Page #16:
   > A 256-bit AES session key is generated and used to encrypt both message headers and bodies separately. Initially, the key is sent to the C2 server with the entire message and headers encrypted with the RSA key exchange algorithm. All subsequent messages are encrypted with AES in CBC mode.

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTE: -

 * Page #19:
   > This command downloads an executable from the C2 and directly runs it in memory.

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may inject code into processes in order to evade process-based defenses as well as possibly elevate privileges.

   TOOLS: -

   NOTE: -

 * Page #22:
   > FIN7 uses CARBANAK as a post-exploitation tool in later phases of an intrusion to cement their foothold in a network and maintain access, frequently using the video command to monitor users and learn about the victim network, as well as the tunnel command to proxy connections into isolated po%ions of the victim environment

   ID: 001

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 uses CARBANAK, specifically its video and tunnel commands, to maintain access and monitor the network.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #22:
   > FIN7 has consistently utilized legally purchased code signing ce%i#cates to sign their CARBANAK payloads.

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries. 

   TOOLS: -

   NOTE: -

 * Page #23:
   > FIN7 Spear Phishing Campaign Targets Personnel Involved in SEC Filings

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0002)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 uses spear phishing emails 

   TOOLS: -

   NOTE: -

