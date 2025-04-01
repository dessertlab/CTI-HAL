## Detailed comments

 * Page #1:
   > The initial infection vector appears to be the exploitation of a Ukrainian tax software called MEDoc.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: SUPPLY CHAIN COMPROMISE (T1195)

   SUB-TECHNIQUE: SUPPLY CHAIN COMPROMISE: SOFTWARE SUPPLY CHAIN (T1195.002)

   DESCRIPTION: Adversaries may manipulate application software prior to receipt by a final consumer for the purpose of data or system compromise.

   TOOLS: -

   NOTE: The initial infection vector exploited the MEDoc software, a supply chain compromise affecting numerous industries.

 * Page #1:
   > The sample also spreads on the internal network via exploitation of the EternalBlue SMB vulnerability, PsExec, WMI, and Admin$ shares.

   ID: 002

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit vulnerabilities in remote services to move laterally within a network. 

   TOOLS: -

   NOTE: -

 * Page #2:
   > This recent sample follows the encryption and ransom note functionality seen in Petya samples.

   ID: 003

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENCRYPTION FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt data on target systems to disrupt availability and demand ransom payments.

   TOOLS: -

   NOTE: -

 * Page #2:
   > There are various reasons why malware tends to use this style of execution, with the most common being to prevent execution within a sandbox.

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ various means to detect and avoid virtualization and analysis environments.

   TOOLS: -

   NOTE: -

 * Page #2:
   > Based upon these privileges the malware will encrypt the victim system

   ID: 005

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENCRYPTION FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt data on target systems to disrupt availability and demand ransom payments.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The malware authors use a proprietary XOR encryption routine to mask what process names they are looking for.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILE (T1027.013)

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTE: -

 * Page #4:
   > The file is encrypted in memory using AES encryption and then written to disk when the FlushViewOfFile is called.

   ID: 007

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENCRYPTION FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt data on target systems to disrupt availability and demand ransom payments.

   TOOLS: -

   NOTE: -

 * Page #4:
   > After the encryption routine completes, the sample will attempt to remove forensic artifacts of its activities by utilizing cmd.exe to run the command listed in the table below.

   D: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware attempts to remove forensic artifacts by utilizing cmd.exe to execute commands to clear logs or other indicators of its activity.

   TOOLS: cmd.exe (S0106)

   NOTE: -

 * Page #4:
   > Before the sample exits it will force a reboot of the infected system using one of three methods.

   ID: 009

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SYSTEM SHUTDOWN/REBOOT (T1529)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may shutdown/reboot systems to interrupt access to, or aid in the destruction of, those systems.

   TOOLS: -

   NOTE: -

 * Page #5:
   > the ransomware utilizes the highly effective EternalBlue exploit for Windows SMB vulnerabilities to copy itself to other systems and execute, which is detailed later in this post.

   ID: 010

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: The ransomware propagates across local environments by exploiting the EternalBlue vulnerability in Windows SMB. This allows the malware to copy itself to other vulnerable systems and execute, enabling rapid spread within the network.

   TOOLS: - 

   NOTE: -

 * Page #5:
   > In addition to the SMB exploit propagation method, the malware also attempts to establish default administrative network shares (Admin$) with a call to WNetAddConnection2() using a null username and password.

   ID: 011

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: LATERAL TOOL TRANSFER (T1570)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files between systems in a compromised environment.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The malware also has the ability to extract an embedded and compressed resource (resource 3) containing the SysInternals PsExec.exe utility. The psexec.exe file is written to disk as dllhost.dat.  This utility is then used to execute this file on the remote system.

   ID: 012

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit remote services to gain unauthorized access to internal systems once inside of a network.

   TOOLS: - 

   NOTE: -

 * Page #5:
   > Failing that, the malware will then leverage the existing Windows WMI utility to execute the file on the remote system

   ID: 013

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit remote services to gain unauthorized access to internal systems once inside of a network.

   TOOLS: - 

   NOTE: -

 * Page #6:
   > After the alterations have completed the sample will remove forensic artifacts

   D: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware attempts to remove forensic artifacts by utilizing cmd.exe to execute commands to clear logs or other indicators of its activity.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The sample will then make modifications to the MBR.

   ID: 014

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENCRYPTION FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt data on target systems to disrupt availability and demand ransom payments.

   TOOLS: -

   NOTE: -

 * Page #6:
   > and then shut down

   ID: 015

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SYSTEM SHUTDOWN/REBOOT (T1529)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may shutdown/reboot systems to interrupt access to, or aid in the destruction of, those systems.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The function (highlighted in green in the image above) will gather system information and then enumerate the other systems on the domain.

   ID: 016

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE DISCOVERY (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to get a listing of services running on remote hosts and local network infrastructure devices, including those that may be vulnerable to remote software exploitation.

   TOOLS: -

   NOTE: -

 * Page #7:
   > this sample is also capable of spreading through SMB kernel exploitation (MS17-010, commonly referred to as EternalBlue).

   ID: 017

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: EXPLOITATION OF REMOTE SERVICES (T1210)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit remote services to gain unauthorized access to internal systems once inside of a network.

   TOOLS: - 

   NOTE: -

 * Page #8:
   > The table below shows the strings that were decoded in the previous image.  These strings were encoded using a simple XOR key of 0x72.

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILE (T1027.013)

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The function highlighted in the image below shows where the shellcode is first decoded with a simple XOR value of 0xCC.

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILE (T1027.013)

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTE: -

 * Page #9:
   > This function will initially attempt to determine if the operating system is either x86 or 64-bit

   ID: 020

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: IAn adversary may attempt to get detailed information about the operating system and hardware.

   TOOLS: -

   NOTE: -

 * Page #9:
   > then it will either load a password dumper from either Resource "1" or "2" (which ultimately are x86 and 64-bit executable files respectively).

   ID: 021

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password. 

   TOOLS: -

   NOTE: -

 * Page #9:
   > It should be noted that all of the four resources are stored as compressed buffers that can be inflated with zlib.

   ID: 022

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Once the OS type has been determined

   ID: 023

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: IAn adversary may attempt to get detailed information about the operating system and hardware.

   TOOLS: -

   NOTE: -

 * Page #9:
   > the sample will write the executable to the system %TEMP% path with a OS-generated temporary file name

   ID: 024

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTE: -

 * Page #9:
   > execute the file as a new process

   ID: 025

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTE: -

