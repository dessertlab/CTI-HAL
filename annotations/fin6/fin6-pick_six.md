## Detailed comments

 * Page #1:
   > Cobalt Strike, Metasploit, and publicly available tools such as Adfind and 7-Zip to conduct internal reconnaissance, compress data, and aid their overall mission

   ID: 002

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM NETWORK DISCOVERY (T1016)

   SUB-TECHNIQUE: -

   DESCRIPTION: these tools were used to conduct internal reconaissance

   TOOLS: COBALT STRIKE (S0154), METASPLOIT, ADFIND (S0552)

   NOTE: -

   ---

   ID: 003

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: -

   DESCRIPTION: 7-Zip was used to compress data

   TOOLS: 7-Zip

   NOTE: -

 * Page #1:
   > in the initial phase of an intrusion using stolen credentials

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: stolen credentials were used in the initial phase of the intrusion

   TOOLS: -

   NOTE: -

 * Page #1:
   > Pivoting from these initial leads, analysts identified suspicious SMB connections and Windows Registry artifacts that indicated the attacker had installed malicious Windows services to execute PowerShell commands on remote systems.

   ID: 004

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SMB/WINDOWS ADMIN SHARES (T1021.002)

   DESCRIPTION: SMB connections were used.

   Togheter with ID.005 indicated that the attacker had installed malicious Windows services.

   TOOLS: -

   NOTE: -

   LINK: ID.005

   ---

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: it was used, togheter with ID.004, to install malicious Windows services.

   TOOLS: -

   NOTE: -

   LINK: ID.004

   ---

   ID: 006

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.002)

   DESCRIPTION: it was used, togheter with ID.004, to install malicious Windows services. These services execute PowerShell commands on remote systems.

   TOOLS: -

   NOTE: -

   LINK: (ID.004 AND ID.005), ID.007

   ---

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002),

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell commands were used on remote systems.

   TOOLS: -

   NOTE: -

   LINK: ID.006

 * Page #1:
   > FIN6 compromised an internet facing system.

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (T0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATION (T1190)

   SUB-TECHNIQUE: -

   DESCRIPTION: to initially gain access to the environment, FIN6 compromised and internet facing system.

   TOOLS: -

   NOTE: INITIAL COMPROMISE

 * Page #1:
   > FIN6 leveraged stolen credentials to move laterally

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), LATERAL MOVEMENT (TA0008)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN6 used stolen credentials to access system and move laterally within the environment

   TOOLS: -

   NOTE: - 

   LINK: 010

 * Page #1:
   > using the Windows' Remote Desktop Protocol (RDP)

   ID: 010

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: FIN6 exploited the RDP protocol to move laterally within the environment using stolen credentials

   TOOLS:  -

   NOTE: -

   LINK: 009

 * Page #1:
   > FIN6 used two different techniques to establish a foothold

   ID : 011

   NOTE: FIN6 used two different techniques to estabilish a foothold

   LINK: T01 OR T02

 * Page #1:
   > First technique

   ID: T01

   LINK: 012, 013, 014, 015, 016

 * Page #1:
   > The command consisted of a byte array containing a base64 encoded payload

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN6 used base64-encoded payloads to obfuscate the malicious content and make it less obvious to security tools.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #1:
   > FIN6 used PowerShell to execute an encoded command.

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Use of PowerShell to execute an encoded command

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #1:
   > The encoded payload was a Cobalt Strike httpsstager that was injected into the PowerShell process that ran the command.

   ID: 014

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE:

   DESCRIPTION: Cobal Strike httpsstager injected into the PowerShell process

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

 * Page #1:
   > The Cobalt Strike httpsstager was configured to download a second payload from hxxps://176.126.85[.]207:443/7sJh.

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Cobalt Strike httpsstager configured to download a second payload

   TOOLS: -

   NOTE: -

 * Page #1:
   > it was a shellcode payload configured to download a third payload from hxxps://176.126.85[.]207/ca

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Cobalt Strike httpsstager configured to download a third payload

   TOOLS: -

   NOTE: -

 * Page #1:
   > Second technique

   ID: T02

   LINK: 017, 018, 019, 020

 * Page #1:
   > FIN6 also leveraged the creation of Windows services (named with a random 16- character string such as IXiCDtPbtGWnrAGQ) to execute encoded PowerShell commands

   ID: 017

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.003)

   DESCRIPTION: Creation of Windows services with random 16-character names

   TOOLS: -

   NOTE: -

 * Page #1:
   > The encoded command contained a Metasploit reverse HTTP shellcode payload stored in a byte-array like the first technique

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Metasploit revere HTTP shellcode payload

   TOOLS: METASPLOIT

   NOTE: -

   LINK: 019

 * Page #1:
   > The Metasploit reverse HTTP payload was configured to communicate with the command and control (C2) IP address 176.126.85[.]207 with a randomly named resource such as "/ilX9zObq6LleAF8BBdsdHwRjapd8_1Tl4Y- 9Rc6hMbPXHPgVTWTtb0xfb7BpIyC1Lia31F5gCN_btvkad7aR2JF5ySRLZmTtY" over TCP port 443.

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Communicate with the C2 IP address over TCP port 443

   TOOLS: -

   NOTE: -

   LINK: 018, 020

 * Page #1:
   > This C2 URL contained shellcode that would make an HTTPS request for an additional download.

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: HTTPS request for an additional download

   TOOLS: -

   NOTE: -

   LINK: 019

 * Page #1:
   > To achieve privilege escalation within the environment, FIN6 utilized a named pipe impersonation technique included within the Metasploit framework that allows for SYSTEM-level privilege escalation

   ID: 021

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION

   TECHNIQUE: EXPLOITATION FOR PRIVILEGE ESCALATION (T1068)

   SUB-TECHNIQUE: - 

   DESCRIPTION: FIN6 useD a named pipe impersonation technique included in the Metasploit framework to obtain SYSTEM level privileges.

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 conducted internal reconnaissance with a Windows batch file leveraging Adfind to query Active Directory

   ID: 022

   SOURCE: 

   TACTIC:

   TECHNIQUE: SYSTEM NETWORK CONFIGURATION DISCOVERY (T1016)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Internal reconnaissance using Adfind to query Active Directory

   TOOLS: ADFIND (S0552)

   NOTE: -

   LINK: 023

 * Page #1:
   > 7-zip to compress the results for exfiltration

   ID: 023

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: ARCHIVE COLLECTED DATA (T1560)

   SUB-TECHNIQUE: ARCHIVE VIA UTILITY (T1560.001)

   DESCRIPTION: 7-zip to compress the results for exfiltration

   TOOLS: 7-zip

   NOTE: -

   LINK: 022

 * Page #1:
   > FIN6 was able to identify user accounts that could access additional hosts in the domain

   ID: 024

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: ACCOUNT DISCOVERY (T1087)

   SUB-TECHNIQUE: DOMAIN ACCOUNT (T1087.002)

   DESCRIPTION: Identify user accounts that could access additional hosts in the domain.

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 used another set of compromised credentials with membership to additional groups in the domain to RDP to other hosts

   ID: 025

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of compromised credentials to access additional systems.

   TOOLS: -

   NOTE: -

   ---

   ID: 026

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICE (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Using RDP protocol to move laterally between systems using compromised credentials.

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 used encoded PowerShell commands to install Cobalt Strike on compromised systems.

   ID: 027

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Encoded PowerShell commands to install Cobalt Strike.

   TOOLS: -

   NOTE: -

 * Page #1:
   > The attacker made use of Cobalt Strike's "psexec" lateral movement command to create a Windows service named with a random 16-character string on the target system and execute encoded PowerShell.

   ID: 028

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: SERVICE EXECUTION (T1569.002)

   DESCRIPTION: Cobalt Strike's "psexec" lateral movement command

   TOOLS: -

   NOTE: -

 * Page #1:
   > In some cases, the encoded PowerShell commands were used to download and execute content hosted on the paste site hxxps://pastebin[.]com.

   ID: 029

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Encoded PowerShell commands to download and execute content from Pastebin

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 also moved laterally to servers in the environment using RDP

   ID: 030

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Moved laterally using RDP

   TOOLS: -

   NOTE: -

   LINK: 031

 * Page #1:
   > configured them as malware "distribution" servers

   ID: 031

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Configured servers as malware distribution servers

   TOOLS: -

   NOTE: -

   LINK: 030

 * Page #1:
   > The distribution servers were used to stage the LockerGoga ransomware, additional utilities, and deployment scripts to automate installation of the ransomware.

   ID: 032

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE:

   DESCRIPTION: Staging LockerGaga for the installation

   TOOLS: -

   NOTE: -

   LINK: 031

   --- 

   ID: 033

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Preparation of distribution and utility scripts for later transfer and use.

   TOOLS: -

   NOTE: -

 * Page #1:
   > Mandiant identified a utility script named kill.bat that was run on systems in the environment. This script contained a series of anti-forensics and other commands intended to disable antivirus and destabilize the operating system.

   ID: 034

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: Utility script with anti-forensic commands to remove indicators on compromised systems.

   TOOLS: -

   NOTE: -

   ---

   ID: 035

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: IMPAIR DEFENSE (T1562)

   SUB-TECHNIQUE: DISABLE OR MODIFY TOOLS (T1562.001)

   DESCRIPTION: Disabling antivirus and destabilizing the operating system using kill.bat commands.

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 automated the deployment of kill.bat and the LockerGoga ransomware using batch script files.

   ID: 036

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: WINDOWS COMMAND SHELL (T1059.003)

   DESCRIPTION: Using batch scripts to automate ransomware deployment and kill.bat.

   TOOLS: -

   NOTE: -

 * Page #1:
   > These BAT files contained psexec commands to connect to remote systems and deploy kill.bat along with LockerGoga

   ID: 037

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: SERVICE EXECUTION (T1569.002)

   DESCRIPTION: Use of psexec to run services and scripts on remote systems.

   TOOLS: -

   NOTE: -

   ---

   ID: 038

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SMB/WINDOWS ADMIN SHARES (T1021.002)

   DESCRIPTION: Use of psexec for lateral movement via Windows administrative shares.

   TOOLS: -

   NOTE: -

 * Page #1:
   > FIN6 renamed the psexec service name to "mstdc" in order to masquerade as the legitimate Windows executable "msdtc."

   ID: 039

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: Renamed psexec service name to "mstdc" to masquerade as legitimate Windows executable "msdtc"

   TOOLS: -

   NOTE: -

 * Page #1:
   > Domain administrators have complete control over Windows systems in an Active Directory environment

   ID: 040

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: DOMAIN ACCOUNS (T1078.002)

   DESCRIPTION: Used compromised domain administrator credential

   TOOLS: -

   NOTE: -
