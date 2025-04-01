## Detailed comments

 * Page #3:
   > TerraLoader that deploys a signed Metasploit shellcode loader

   ID: 002

   SOURCE: TEXT

   TACTIC: 

   TECHNIQUE: SUBVERT TRUST CONTROLS (T1553)

   SUB-TECHNIQUE: CODE SIGNING (T1553.002)

   DESCRIPTION: The shellcode loader is signed, indicating the use of a signed binary to bypass security controls

   TOOLS: TERRALOADER, METASPLOIT

   NOTE: -

 * Page #3:
   > TerraLoader that installs the More_eggs backdoor

   ID: 001

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: TerraLoader facilitates the transfer and installation of the More_eggs backdoor

   TOOLS: TERRALOADER, MORE_EGGS (S0284)

   NOTE: -

 * Page #4:
   > All three C&C domains were created at the same time using the same email registration address

   ID: 003

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: DOMAINS (T1583.001)

   DESCRIPTION: The acquisition of domains to be used for command and control (C&C) purposes

   TOOLS: -

   NOTE: The fact that all three C&C domains were created at the same time using the same email registration address indicates the use of a consistent method for setting up the C&C infrastructure.

 * Page #4:
   > use the same RKey, which is used in part to encrypt communications with the C&C host

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: ASYMMETRIC CRYPTOGRAPHY (T1573.002)

   DESCRIPTION: Use of an RKey to encrypt to secure C&C communications.

   TOOLS: -

   NOTE: -

 * Page #4:
   > Anchor downloading a signed TerraLoader

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Anchor downloading a signed TerraLoader involves transferring malicious software into the target environment.

   TOOLS: ANCHOR

   NOTE: -

   LINK: 006

 * Page #4:
   > That first step was followed by installing an Apache Bench executable hollowed out with a Metasploit loader shellcode

   ID: 006

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: PROCESS HOLLOWING (T1055.012)

   DESCRIPTION: Installing an Apache Bench executable hollowed out with Metasploit loader shellcode.

   TOOLS: METASPLOIT

   NOTE: -

   LINK: 005, 007

 * Page #5:
   > received an RC4 encrypted payload

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: SYMMETRIC CRYPTOGRAPHY (T1573.001)

   DESCRIPTION:  The RC4 encrypted payload received by the shellcode

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #5:
   > ITG08 employ a signed Metasploit shellcode loader masquerading as the Apache Bench application and containing a Comodo code-signing certificate issued to "MAHTEM LTD."

   ID: 008

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: PROCESS HOLLOWING (T1055.012)

   DESCRIPTION: The signed Metasploit shellcode loader is injected into the Apache Bench process.

   TOOLS: METASPLOIT

   NOTE: -

   LINK: 009

 * Page #5:
   > The shellcode was loaded into memory and designed to receive an RC4- encrypted buffer

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: SYMMETRIC CRYPTOGRAPHY (T1573.001)

   DESCRIPTION: The encrypted RC4 buffer indicates that the shellcode is designed to receive encrypted data.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #5:
   > X-Force IRIS identified a signed TerraLoader in a public repository that also decrypts a shellcode loader masquerading as Apache Bench.

   ID: 010

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: PROCESS HOLLOWING (T0155.012)

   DESCRIPTION: The signed TerraLoader decrypts a shellcode loader masquerading as Apache Bench.

   TOOLS: TERRALOADER

   NOTE: -

   LINK: 011

   ---

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: The shellcode loader masquerading as Apache Bench.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #5:
   > used PowerShell to download and execute a TerraLoader that installed More_eggs

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell to download and run TerraLoader.

   TOOLS: POWERSHELL, TERRALOADER, MORE_EGGS (S0284)

   NOTE: -

 * Page #5:
   > it used PowerShell and Windows Management Instrumentation (WMI) to download and execute TerraLoader, then install More_eggs on remote hosts

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Using PowerShell with WMI to download and run TerraLoader.

   TOOLS: POWERSHELL, TERRALOADER, MORE_EGGS (S0284)

   NOTE: -

   LINK: 014

   ---

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading and running TerraLoader through PowerShell and WMI.

   TOOLS: WINDOWS MANAGEMENT INSTRUMENTATION, TERRALOADER, MORE_EGGS (S0284)

   NOTE: -

   LINK: 013

 * Page #6:
   > Metasploit, Cobalt Strike and AdFind

   ID: 015

   SOURCE: TEXT

   TOOLS: METASPLOIT, COBALT STRIKE (S0154), ADFIND

   NOTE:

