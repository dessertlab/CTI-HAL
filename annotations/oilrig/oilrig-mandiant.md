## Detailed comments

 * Page #2:
   > using a PowerShell-based backdoor that we call POWRUNER and a downloader

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The malware utilizes PowerShell to execute malicious commands and scripts, delivering the backdoor functionality.

   TOOLS: -

   NOTE: -

   LINK: 002, 003

 * Page #2:
   > with domain generation algorithm functionality that we call BONDUPDATER, based on strings within the malware.

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE: DYNAMIC GENERATION ALGORITHMS (T1568.002)

   DESCRIPTION: The malware uses a domain generation algorithm to dynamically create command and control (C2) domain names, making it more difficult to block and track.

   TOOLS: -

   NOTE: -

   LINK: 001

   ---

   ID: 030

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: FALLBACK CHANNEL (T1008)

   SUB-TECHNIQUE: -

   DESCRIPTION: Implementing domain generation algorithm (DGA) for C2 communication.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The backdoor was delivered via a malicious .%f &le that exploited CVE-2017-0199.

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATION (T1190)

   SUB-TECHNIQUE: 

   DESCRIPTION: The initial compromise was achieved through the exploitation of a known vulnerability, CVE-2017-0199, which allows remote code execution through a specially crafted file.

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #3:
   > APT34 sent a malicious .%f &le (MD5: a0e6933f4e0497269620f44a083b2ed4) as an a!achment in a malicious spear phishing email sent to the victim organization

   ID: 004

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: APT34 sent a malicious file as an attachment in a spear-phishing email to the victim organization. This attachment is specifically crafted to exploit a vulnerability once opened by the target, leading to the execution of the malware payload.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #3:
   > The malicious &le exploits CVE-2017-11882, which corrupts the memory on the stack and then proceeds to push the malicious data to the stack.

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPOLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malicious file exploits CVE-2017-11882, a vulnerability in Microsoft Office that corrupts memory on the stack, allowing the attacker to push and execute their malicious payload on the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 004, 006

 * Page #3:
   > The malware then overwrites the function address with the address of an existing instruction from EQNEDT32.EXE. The overwri!en instruction (displayed in Figure 1) is used to call the "WinExec" function from kernel32.dll, as depicted in the instruction at 00430c12, which calls the "WinExec" function.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: EXPLOITATION FOR DEFENSE EVASION (T1211)

   SUB-TECHNIQUE: -

   DESCRIPTION: By overwriting the function address with an existing instruction from EQNEDT32.EXE, the malware avoids detection by leveraging legitimate system functions to execute its payload, thus evading security defenses.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #3:
   > the 'WinExec' function is successfully called to create a child process, "mshta.exe", in the context of current logged on user

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: CREATE PROCESS (T1543.003)

   DESCRIPTION: The malware uses the WinExec function to create a new process, mshta.exe.

   TOOLS: -

   NOTE: -

   LINK: 006, 008

   ---

   ID: 031

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SYSTEM BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may bypass process and/or signature-based defenses by proxying execution of malicious content with signed, or otherwise trusted, binaries.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The process "mshta.exe" downloads a malicious script from hxxp://mumbai-m[.]site/b.txt and executes it,

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware creates a child process (mshta.exe) that downloads a malicious script from an external URL. 

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #3:
   > The malware overwrites the function address with an existing

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: EXPLOITATION FOR DEFENSE EVASION (T1211)

   SUB-TECHNIQUE: -

   DESCRIPTION: By overwriting the function address with an existing instruction from EQNEDT32.EXE, the malware avoids detection by leveraging legitimate system functions to execute its payload, thus evading security defenses.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #4:
   > The malware creates a child process, "mshta.exe,"

   ID: 010

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: CREATE PROCESS (T1543.003)

   DESCRIPTION: The malware uses the WinExec function to create a new process, mshta.exe.

   TOOLS: -

   NOTE: -

   LINK: 009, 011

 * Page #4:
   > which downloads a &le from: hxxp://mumbai-m[.]site/b.txt.

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware creates a child process (mshta.exe) that downloads a malicious script from an external URL. 

   TOOLS: -

   NOTE: -

   LINK: 010, 012

 * Page #4:
   > b.txt contains a PowerShell command

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: The file b.txt contains a PowerShell command that downloads and executes the dropper, which is a clear use of PowerShell for executing commands and scripts.

   TOOLS: -

   NOTE: -

   LINK: 011, 013, 014

 * Page #4:
   > to download a dropper from: hxxp://dns-update[.]club/v.txt.

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The PowerShell command downloads a file (v.txt) from a URL (hxxp://dns-update[.]club/v.txt)

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #4:
   > The PowerShell command also renames the downloaded &le from v.txt to v.vbs and executes the script.

   ID: 014

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: This renaming operation helps the malware to ensure the file is recognized as a script and executed properly.

   TOOLS: -

   NOTE: -

   LINK: 012, 015, 016

 * Page #4:
   > The v.vbs script drops four components (hUpdateCheckers.base, dUpdateCheckers.base, cUpdateCheckers.bat, and GoogleUpdateschecker.vbs) to the directory: C:\ProgramData\Windows\Microso"\java\

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transferring tools or files from a remote system to an internal system.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #4:
   > v.vbs uses Ce%Util.exe, a legitimate Microso" command-line program installed as pa% of Ce%i&cate Services, to decode the base64-encoded &les hUpdateCheckers.base and dUpdateCheckers.base, and drop hUpdateCheckers.ps1 and dUpdateCheckers.ps1 to the staging directory.

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of Ce%Util.exe to decode base64-encoded files (hUpdateCheckers.base and dUpdateCheckers.base) fits this technique. It's an example of how attackers use legitimate tools to handle encoded data, revealing the actual payload.

   TOOLS: -

   NOTE: -

   LINK: 014, 017

   ---

   ID: 033

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTE: -

 * Page #4:
   > cUpdateCheckers.bat is launched and creates a scheduled task for GoogleUpdateschecker.vbs persistence.

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The creation of the scheduled task for GoogleUpdateschecker.vbs is used to maintain persistence by ensuring the script runs regularly.

   TOOLS: -

   NOTE: -

   LINK: 016, 018

   ---

   ID: 029

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using legitimate-looking filenames.

   TOOLS: -

   NOTE: -

 * Page #4:
   > cUpdateCheckers.bat and *.base are deleted from the staging directory.

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: After executing, cUpdateCheckers.bat and the *.base files are deleted from the staging directory to remove traces of the malware's presence and reduce detection risk.

   TOOLS: -

   NOTE: -

   LINK: 017

 * Page #4:
   > the Task Scheduler will launch GoogleUpdateschecker.vbs every minute

   ID: 019

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The GoogleUpdateschecker.vbs script is set up to be launched every minute by the Task Scheduler, ensuring that the scripts dUpdateCheckers.ps1 and hUpdateCheckers.ps1 are executed regularly.

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #4:
   > which in turn executes the dUpdateCheckers.ps1 and hUpdateCheckers.ps1 scripts

   ID: 020

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: It executes two PowerShell scripts

   TOOLS: -

   NOTE: -

   LINK: 019, 021

 * Page #4:
   > they include a downloader with domain generation algorithm (DGA) functionality

   ID: 021

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DYNAMIC RESOLUTION (T1568)

   SUB-TECHNIQUE: DYNAMIC GENERATION ALGORITHMS (T1568.002)

   DESCRIPTION: The downloader in the dUpdateCheckers.ps1 script uses DGA functionality to generate domains, which helps in maintaining communication with the C2 server.

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #4:
   > POWRUNER, is a PowerShell script that sends and receives commands to and from the C2 server

   ID: 022

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: POWRUNER is a PowerShell script that sends and receives commands from the C2 server, utilizing PowerShell for its operations.

   TOOLS: -

   NOTE: -

   LINK: 023

 * Page #5:
   > POWRUNER is executed every minute by the Task Scheduler

   ID: 023

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: POWRUNER is executed every minute by the Task Scheduler, ensuring it runs continuously and maintains regular communication with the C2 server.

   TOOLS: -

   NOTE: -

   LINK: 022

 * Page #5:
   > POWRUNER begins by sending a random GET request to the C2 server and waits for a response

   ID: 024

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: POWRUNER uses HTTP GET requests to communicate with the C2 server, sending and receiving data to perform its operations.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The C2 server can also send a PowerShell command to capture and store a screenshot of a victim's system.

   ID: 025

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: POWRUNER can receive a command from the C2 server to capture and store a screenshot of the victim's system

   TOOLS: -

   NOTE: -

   LINK: 026

 * Page #5:
   > POWRUNER will send the captured screenshot image &le to the C2 server if the "&leupload" command is issued.

   ID: 026

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER COMMAND AND CONTROL CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: POWRUNER uses its communication channel with the C2 server to exfiltrate the captured screenshot. This method involves sending data (in this case, the screenshot) back to the C2 server as part of its exfiltration process.

   TOOLS: -

   NOTE: -

   LINK: 025

 * Page #7:
   > The C2 server sends back Base64 encoded response.

   ID: 028

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: Encoding communication and payloads using Base64.

   TOOLS: -

   NOTE: -

 * Page #8:
   > POWRUNER may also receive batch commands from the C2 server to collect host information from the system. This may include information about the currently logged in user, the hostname, network con&guration data, active connections, process information, local and domain administrator accounts, an enumeration of user directories, and other data.

   ID: 027

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: POWRUNER collects information about the currently logged in user, hostname, network configuration, and other system details through batch commands.

   TOOLS: -

   NOTE: -

   ---

   ID: 032

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM OWNER/USER DISCOVERY (T1033)

   SUB-TECHNIQUE: -

   DESCRIPTION: Enumerating logged-in users and administrator accounts.

   TOOLS: -

   NOTE: -

