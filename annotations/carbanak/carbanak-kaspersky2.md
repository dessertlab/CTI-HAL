## Detailed comments

 * Page #3:
   > the initial infections were achieved using spear phishing emails that appeared to be legitimate banking communications, with Microsoft Word 97 – 2003 (.doc) and Control Panel Applet (.CPL) files attached.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending phishing emails with malicious attachments to compromise the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > The email attachments exploit vulnerabilities in Microsoft Office 2003, 2007 and 2010 (CVE-2012-0158 and CVE-2013-3906) and Microsoft Word (CVE-2014- 1761). Once the vulnerability is successfully exploited, the shellcode decrypts and executes the backdoor known as Carbanak.

   ID: 039

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: the shellcode  executes the backdoor Carbanak

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #3:
   > The email attachments exploit vulnerabilities in Microsoft Office 2003, 2007 and 2010 (CVE-2012-0158 and CVE-2013-3906) and Microsoft Word (CVE-2014- 1761)

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION:  Exploitation of vulnerabilities in client software (e.g., document reader) to execute arbitrary code.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #3:
   > the shellcode decrypts and executes the backdoor known as Carbanak

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using command and script interpreters to execute malicious commands and scripts.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 002

 * Page #3:
   > Carbanak is a remote backdoor (initially based on Carberp), designed for espionage, data exfiltration and to provide remote access to infected machines

   ID: 004

   TOOLS: CARBANAK (S0030)

 * Page #3:
   > They then install additional software such as the Ammyy Remote Administration Tool, or even compromise SSH servers

   ID: 005

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Attackers use remote services to move laterally in the compromised network.

   TOOLS: -

   NOTE: -

 * Page #4:
   > video recordings of the activities of bank employees, particularly system administrators, were made

   ID: 006

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: VIDEO CAPTURE (T1125)

   SUB-TECHNIQUE: -

   DESCRIPTION: Attackers capture video of the victim's system, often for surveillance or to collect credentials and other sensitive information.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #4:
   > The videos were sent to the C2 server

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Communications with the command and control server (C2)

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #4:
   > the attackers abused the aforementioned services by impersonating legitimate local users who had the permissions to perform the actions later reproduced by the cybercriminals

   ID: 040

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: ACCESS TOKEN MANIPULATION (T1134)

   SUB-TECHNIQUE: TOKEN IMPERSONATION/THEFT (T1134.001)

   DESCRIPTION: The attackers abused the aforementioned services by impersonating legitimate local users

   TOOLS: -

   NOTE: -

 * Page #5:
   > spear phishing emails with CPL files attached

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending phishing emails with malicious attachments to compromise the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #5:
   > install the same Carberp-like malware

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of tools or files from outside to the compromised system.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Carbanak contains an espionage component that allows the attackers to take control of video capabilities on the victim systems

   ID: 010

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: VIDEO CAPTURE (T1125)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak uses espionage components to control the video capabilities of victim systems.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #5:
   > spear phishing emails with Microsoft Word 97 – 2003 (.doc) files attached or CPL files

   ID: 011

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending phishing emails with malicious attachments to compromise the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 012, 013

 * Page #5:
   > The doc files exploit both Microsoft Office (CVE- 2012-0158 and CVE-2013-3906) and Microsoft Word (CVE- 2014-1761).

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of software vulnerabilities to execute arbitrary code on the victim system.

   TOOLS: -

   NOTE: -

   LINK: 011, 014

 * Page #6:
   > Once the remote code execution vulnerability is successfully exploited, it installs Carbanak on the victim's system

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transfer of tools or files from an external system to a system within the victim's environment.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #6:
   > The spear phishing email messages appeared legitimate and in some cases were sent from compromised coworkers´ accounts

   ID: 013

   SOURCE: TEXT

   TACTIC: INITAL ACCESS (TA0001), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using valid accounts to gain unauthorized access to systems.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #7:
   > Carbanak is a backdoor used by the attackers to compromise the victim's machine once the exploit, either in the spear phishing email or exploit kit, successfully executes its payload

   ID: 015

   TOOLS: CARBANAK (S0030)

   LINK: 016, 017, 018, 019, 020, 021, 022, 023, 024, 025, 026, 027, 028, 029, 030, 031, 032

 * Page #7:
   > Carbanak copies itself into "%system32%\com" with the name "svchost.exe"

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: The attacker renames a malicious file with a legitimate name to avoid detection.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015, 017

 * Page #7:
   > with the file attributes: system, hidden and read-only.

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: HIDE ARTIFACTS (T1564)

   SUB-TECHNIQUE: HIDDEN FILES AND DIRECTORIES (T1564.001)

   DESCRIPTION: The attacker hides files and directories by making them invisible to users and security tools.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 016, 018

 * Page #7:
   > The original file created by the exploit payload is then deleted.

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: The attacker deletes files to eliminate traces of his activity and obstruct investigations.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 017

 * Page #7:
   > To ensure that Carbanak has autorun privileges the malware creates a new service

   ID: 019

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Creation or modification of a service to achieve persistence and automatic execution.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015, 020

 * Page #7:
   > The naming syntax is "<ServiceName>Sys" where ServiceName is any existing service randomly chosen, with the first character deleted.

   ID: 020

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Changing the names of files or processes to make them look legitimate.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 019

 * Page #8:
   > Carbanak determines if either the avp.exe or avpui.exe processes (components of Kaspersky Internet Security) is running.

   ID: 021

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak performs process discovery to identify specific processes associated with Kaspersky Internet Security (avp.exe or avpui.exe). 

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #8:
   > the malware gets the proxy configuration from the registry entry: [HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings]

   ID: 022

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1060)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The malware use registry keys to execute commands or to configure automatic loading at system startup. 

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #8:
   > Carbanak injects its code into svchost.exe.

   ID: 023

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak injects its code into the svchost.exe process to mask its activities within the legitimate Windows process.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #8:
   > Carbanak downloads the file kldconfig.plug from its C2 server.

   ID: 024

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak communicates with its C2 server to download the file kldconfig.plug, which includes the names of the processes to be monitored.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #8:
   > takes screenshots every 20 seconds

   ID: 026

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak captures desktop screenshots every 20 seconds to monitor user activity and collect additional sensitive information.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #8:
   > Carbanak logs keystrokes

   ID: 025

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak records keystrokes on the infected system's keyboard to collect sensitive information such as credentials and other data.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #9:
   > Carbanak sets Termservice service execution mode to Auto. Also, after executing this service

   ID: 027

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak sets Termservice in automatic execution mode (Auto).

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015, 028

 * Page #9:
   > it modifies the executable code in memory in order to establish simultaneous work processes for both remote and local users. Modules modified in this process are: termsrv.dll, csrsrv.dll, msgina.dll and winlogon.exe.

   ID: 041

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: ACCESS TOKEN MANIPULATION (T1134)

   SUB-TECHNIQUE: CREATE PROCESS WITH TOKEN (T1134.002)

   DESCRIPTION: Carbanak modifies the executable code in memory

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #9:
   > it modifies the executable code in memory in order to establish simultaneous work processes for both remote and local users

   ID: 028

   SOURCE: TEXT

   TACTIC: 

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Modifies executable code in memory to establish simultaneous work processes for remote and local users.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015, 027

 * Page #9:
   > If Carbanak detects the banking application BLIZKO (funds transfer software) in the infected computer

   ID: 029

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak detects the presence of BLIZKO

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

   ---

   ID: 042

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: If Carbanak detects the banking application BLIZKO (funds transfer software) in the infected computer, it sends a special notification to its C2 server

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #9:
   > Carbanak is also aware of the IFOBS banking application and can, on command, substitute the details of payment documents in the IFOBS system

   ID: 030

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA MANIPULATION (T1565)

   SUB-TECHNIQUE: STORED DATA MANIPULATION (T1565.001)

   DESCRIPTION: Carbanak can manipulate payment document details in the IFOBS system on command.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015

 * Page #9:
   > with RC2+Base64 encryption,

   ID: 032

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak uses RC2+Base64 encryption to encrypt data transmitted through the command and control channel.

   TOOLS: CARBANAK (S0030)

   NOTE:

   LINK: 015, 031

 * Page #9:
   > Carbanak uses the HTTP protocol

   ID: 031

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Carbanak uses the HTTP protocol to communicate with its C2 server.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 015, 032

 * Page #18:
   > There appears to be a preference for the Ammyy Admin remote administration tool for remote control

   ID: 033

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (S0030)

   TECHNIQUE: REMOTE ACCESS TOOL (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique specifically covers the use of Ammyy Admin as a remote administration tool for controlling systems within a compromised network.

   TOOLS: AMMYY

   NOTE: -

 * Page #18:
   > a Secure Shell (SSH) backdoor was used to communicate with the C2 server in 190.97.165.126 (operatemesscont.net).

   ID: 034

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE ACCESS TOOL (T1021)

   SUB-TECHNIQUE: SSH (T1021.004)

   DESCRIPTION: This technique involves the use of SSH for establishing unauthorized access to remote systems.

   TOOLS: -

   NOTE: Adversaries often leverage SSH for secure, encrypted communication with compromised hosts, allowing them to maintain persistent access and exfiltrate data.

 * Page #18:
   > Metasploit,

   ID: 035

   TOOLS: METASPLOIT

 * Page #18:
   > PsExec

   ID: 036

   TOOLS: PSEXEC (S0029)

 * Page #18:
   > Mimikatz.

   ID: 037

   TOOLS: MIMIKATZ (S0002)

 * Page #21:
   > The video file naming conventions used the name of the application in the foreground (e.g., Outlook, Cmd, etc.) and only recorded user activity

   ID: 038

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: VIDEO CAPTURE (T1125)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves capturing video of a user's actions on a system.

   TOOLS: -

   NOTE: -

