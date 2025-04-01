## Detailed comments

 * Page #2:
   > The destructive nature of this malware aims to render the machine unusable by deleting shadow copies, event logs and trying to use PsExec & WMI to further move through the environment.

   ID: 001

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or modify artifacts generated within systems to remove evidence of their presence or hinder defenses.

   TOOLS: -

   NOTE: -

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: PsExec (S0029)

   NOTES: -

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse Windows Management Instrumentation (WMI) to execute malicious commands and payloads.

   TOOLS: -

   NOTES: -

 * Page #2:
   > These Gles are embedded as resources (obfuscated).

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obfuscate files or information to hide malicious code or artifacts, making it more difficult for security tools to detect them.

   TOOLS: -

   NOTE: -

 * Page #2:
   > a binary that, when executed, drops multiple Gles on to the victim host

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Adversaries may rely on users to execute a binary that initiates the infection process, such as dropping multiple files onto the victim host.

   TOOLS: -

   NOTE: -

 * Page #2:
   > These Gles are named using randomly generated Gle names

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use randomly generated file names to disguise the true nature of malicious files, making detection more difficult.

   TOOLS: -

   NOTE: -

 * Page #3:
   > By checking the ARP table with the Windows API GetIPNetTable

   ID: 007

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE DISCOVERY (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to get a listing of services running on remote hosts and local network infrastructure devices, including those that may be vulnerable to remote software exploitation.

   TOOLS: Windows API (GetIPNetTable)

   NOTE: Adversaries may use the ARP table to gather information about systems on the local network by using the Windows API GetIPNetTable.

 * Page #3:
   > By WMI (using WQL) with the following request: "SELECT ds_cn FROM ds_computer". This request attempts to list all the systems within the current environment/directory.

   ID: 008

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to get a listing of other systems by IP address, hostname, or other logical identifier on a network that may be used for Lateral Movement from the current system.

   TOOLS: WMI (WQL Query: "SELECT ds_cn FROM ds_computer")

   NOTE: The WQL query is used to list all systems within the current environment.

 * Page #3:
   > execute it via a VBScript

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Adversaries may abuse Visual Basic (VB) for execution.

   TOOLS: -

   NOTES: -

 * Page #4:
   > The malware dynamically updates this list after using the password stealers.

   ID: 010

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: Password Stealers

   NOTE: The malware updates its list of credentials based on those stolen from infected systems.

 * Page #5:
   > parses the registry and it queries the sqlite Gle in order to retrieve stored credentials

   ID: 011

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: QUERY REGISTRY (T1012)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may interact with the Windows Registry to gather information about the system, configuration, and installed software.

   TOOLS: -

   NOTE: -

   ID: 012

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The stealer attempts to obtain credentials from LSASS

   ID: 013

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: LSASS MEMORY (T1003.001)

   DESCRIPTION: Adversaries may attempt to access credential material stored in the process memory of the Local Security Authority Subsystem Service (LSASS). After a user logs on, the system generates and stores a variety of credential materials in LSASS process memory.

   TOOLS: -

   NOTE: -

 * Page #5:
   > By leveraging cmd.exe from the host the malware Grst deletes all possible shadow copies on the system using vssadmin

   ID: 014

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: INHIBIT SYSTEM RECOVERY (T1490)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or remove built-in data and turn off services designed to aid in the recovery of a corrupted system to prevent recovery.

   TOOLS: cmd.exe, vssadmin

   NOTE: The malware uses cmd.exe to execute the vssadmin command, deleting all possible shadow copies on the system.

 * Page #5:
   > This step is executed to ensure that Gle recovery is not trivial

   ID: 015

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: INHIBIT SYSTEM RECOVERY (T1490)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or remove built-in data and turn off services designed to aid in the recovery of a corrupted system to prevent recovery.

   TOOLS: cmd.exe, wbadmin

   NOTE: The malware uses cmd.exe to execute wbadmin.exe delete catalog -quiet, preventing the use of WBAdmin for file recovery.

 * Page #5:
   > The next step the attacker takes in this destructive path is to, again leverage cmd.exe, but this time use bcdedit, a tool used for boot conGg data information, to ensure that the

   ID: 016

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: INHIBIT SYSTEM RECOVERY (T1490)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or remove built-in data and turn off services designed to aid in the recovery of a corrupted system to prevent recovery.

   TOOLS: cmd.exe, bcdedit

   NOTE: The attacker uses cmd.exe to execute bcdedit commands, disabling the Windows Recovery Console.

 * Page #6:
   > to further cover their tracks the deletion of the System & Security windows event log is performed

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: CLEAR WINDOWS EVENT LOGS (T1070.001)

   DESCRIPTION: Adversaries may clear Windows Event Logs to hide the activity of an intrusion.

   TOOLS: -

   NOTE: The attacker deletes the System & Security Windows event logs to obscure evidence and make recovery and analysis more difficult.

 * Page #6:
   > Additionally, the destroyer disables all the services on the system:

   ID: 018

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SERVICE STOPPING (T1489)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may stop or disable services on a system to render those services unavailable to legitimate users.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Additionally, the malware lists mapped Gle shares and for each share, it will wipe the writable Gles (using either uninitialized data or 0x00 depending of the Gle size).

   ID: 019

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: -

   NOTE: -

 * Page #6:
   > the destroyer shutdowns the compromised system

   ID: 020

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SYSTEM SHUTDOWN/REBOOT (T1529)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may shutdown/reboot systems to interrupt access to, or aid in the destruction of, those systems.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Additionally, the Olympic Destroyer drops the legitimate, digitally signed, PsExec Gle in order to perform lateral movement by using this legitimate tool from Microsoft.

   ID: 021

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Valid Accounts to log into a service that accepts remote connections, such as telnet, SSH, and VNC. The adversary may then perform actions as the logged-on user.

   TOOLS: PsExec (S0029)

   NOTE: -
