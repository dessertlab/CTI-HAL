## Detailed comments

 * Page #4:
   > SandWorm threat group members primarily used spearphishing emails to gain access to computers or account credentials.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may send spearphishing emails in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #5:
   > SandWorm heavily leveraged PowerShell commands and scripts to discover system information, execute code, and download malware.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Adversaries may abuse PowerShell commands and scripts for execution.

   TOOLS: -

   NOTES: -

 * Page #5:
   > Many of the spearphishing emails sent by SandWorm contained malware-laced documents that required user execution to deploy.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may rely upon specific actions by a user in order to gain execution.

   TOOLS: -

   NOTES: -

 * Page #6:
   > To maintain their foothold, SandWorm obtained and repeatedly used existing accounts' credentials to preserve persistence in victim systems.

   ID: 004

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts as a means of gaining Persistence.

   TOOLS: -

   NOTES: -

 * Page #6:
   > SandWorm leveraged malware to escalate system privileges and determine whether particular antivirus processors were running, then attempted to identify other computers on the same network to potentially compromise.

   ID: 005

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0004)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts as a means of gaining Privilege Escalation.

   TOOLS: -

   NOTES: -

 * Page #6:
   > SandWorm used an algorithm to obscure particular features of the Olympic Destroyer malware to obstruct post-attack investigations and avoid detection. The group also attempted to obfuscate their activity by deleting data from compromised machines and servers and

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or modify artifacts generated within systems to remove evidence of their presence or hinder defenses.

   TOOLS: -

   NOTE: -

 * Page #7:
   > On multiple occasions, SandWorm attempted to masquerade their activity through researching and emulating malware used by the Lazarus Group.

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use randomly generated file names to disguise the true nature of malicious files, making detection more difficult.

   TOOLS: -

   NOTE: -

 * Page #7:
   > SandWorm dumped credentials to obtain account login and credential details from compromised machines.

   ID: 008

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: -

   NOTE: -

 * Page #7:
   > SandWorm leveraged customized malware to overwrite itself to incorporate any additional usernames and passwords that it could obtain from the previous computer before spreading to the next computer.

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search compromised systems to find and obtain insecurely stored credentials.

   TOOLS: -

   NOTE: -

 * Page #7:
   > SandWorm repeatedly accessed and browsed Vles, ran malicious scripts, and searched compromised machines for credential Vles

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may enumerate files and directories or may search in specific locations of a host or network share for certain information within a file system.

   TOOLS: -

   NOTE: -

 * Page #8:
   > SandWorm exploited remote services to gain unauthorized access to internal systems. Once they gained access to the remote system, they deployed malware that was leveraged to obtain system privileges, extract and execute an open-source credential harvesting tool, and move laterally throughout the network.

   ID: 011

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit remote services to gain unauthorized access to internal systems once inside of a network.

   TOOLS: -

   NOTE: -

 * Page #8:
   > After gaining access to victims' computers, SandWorm threat actors performed various functions designed to identify, collect, package, and view targeted data, including usernames, IP addresses, and server data relating to RDP sessions on the target computers. This activity included stealing

   ID: 012

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may enumerate files and directories or may search in specific locations of a host or network share for certain information within a file system.

   TOOLS: -

   NOTE: -

 * Page #9:
   > SandWorm established command and control to create a single point of access between compromised networks and a server they controlled. The tunnel allowed them to hide their activity, issue commands, install additional tools, and transfer data.

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA OBFUSCATION (T1001)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obfuscate command and control traffic to make it more difficult to detect.

   TOOLS: -

   NOTE: -

 * Page #9:
   > SandWorm leveraged legitimate credentials to exVltrate data from a victim network and retrieve internal documents from machines inside victim environments.

   ID: 014

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts as a means of gaining Exfiltration.

   TOOLS: -

   NOTES: -

 * Page #10:
   > SandWorm defaced approximately 1,500 websites and disrupted service to some of those websites following the Georgian web hosting provider's compromise.

   ID: 015

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DEFACEMENT (T1491)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may modify visual content available internally or externally to an enterprise network, thus affecting the integrity of the original content.

   TOOLS: -

   NOTE: -

 * Page #10:
   > The group deployed destructive malware to delete Vles from the hard drive, force shutdowns, and impede rebooting and recovery by misconVguring BitLocker, rendering computers inoperable.

   ID: 016

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: INHIBIT SYSTEM RECOVERY (T1490)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may delete or remove built-in data and turn off services designed to aid in the recovery of a corrupted system to prevent recovery.

   TOOLS: -

   NOTE: -
