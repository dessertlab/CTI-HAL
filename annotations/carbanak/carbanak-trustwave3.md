## Detailed comments

 * Page #1:
   > a malicious  Word  or  RTF  document  was  sent  to specific  employees

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: In each campaign, a malicious Word or RTF document was sent to specific employees. This is a form of spearphishing where the attacker targets specific individuals with malicious attachments to gain initial access.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > This from social isaugmentedwitha engineeringscam personalphonecall theattacker,

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING VIA SERVICE (T1566.002)

   DESCRIPTION: This technique involves using social engineering over a phone call to persuade the victim to open a malicious email attachment. The attacker's follow-up call to confirm the document was opened adds another layer of social engineering to ensure the malicious payload is executed.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > encouraging  the  intended  victim  to  open  the email  attachment  and  click  inside  it

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0003)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: This technique involves tricking the user into executing a file that contains malicious code.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > screen-shot grabbing  malware

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Taking screenshots of the victim's desktop to capture sensitive information displayed on the screen.

   TOOLS: -

   NOTE: -

 * Page #3:
   > is two VBS

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: There are two VBS scripts 

   TOOLS: -

   NOTE: -

 * Page #3:
   > Persistence  is established  by  creating  a  scheduled  task  that runs the main malware file every 25 minutes

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Using scheduled tasks to execute programs or scripts at specific times or intervals.

   TOOLS: -

   NOTE: -

   ---

   ID: 025

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Persistence is established by creating a scheduled task

   TOOLS: -

   NOTE: -

 * Page #7:
   > four  more VBS  scripts

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: There are four more VBS scripts 

   TOOLS: -

   NOTE: -

 * Page #8:
   > the  INI  file,  using  it  to  issue  commands  to  the compromised machine as well as to reflect the status of previous commands

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using command-line interfaces to execute commands.

   TOOLS: -

   NOTE: -

 * Page #8:
   > the  victim's  system information

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The adversary gathers information about the system.

   TOOLS: -

   NOTE: -

 * Page #8:
   > list  of  currently  running processes back to the attacker

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY DESCRIPTION (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: The adversary attempts to get a listing of running processes on a system.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Screenshot (save screenshot as screenshot.png)

   ID: 011

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Taking screenshots of the victim's desktop to capture sensitive information displayed on the screen.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Runvbs

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Run VBS

   TOOLS: -

   NOTE: -

 * Page #11:
   > the  malware  uses "http  POST"  to  send  data  that  has  been retrieved/stolen  from  the  infected  system  to the CnC server

   ID: 013

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: The adversary uses an existing command and control channel to exfiltrate data.

   TOOLS: -

   NOTE: The malware uses "HTTP POST" to send data that has been retrieved/stolen from the infected system to the C2 server.

   LINK: 014, 024

   ---

   ID: 024

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: the malware uses \"http POST\" to send data 

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #11:
   > Information  is  sent  using  randomized  variable names  and  simple  encryption  on  the  textbaseddatausingbase64encodingand substitution encryption with these alphabets

   ID: 014

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1022)

   SUB-TECHNIQUE: -

   DESCRIPTION: The adversary encrypts files and data to make them inaccessible to users and applications and potentially to exfiltrate information from the victim's network.

   TOOLS: -

   NOTE: The malware uses base64 encoding and substitution encryption to obfuscate data before exfiltration.

 * Page #17:
   > uses  SMB  commands (including  TreeConnect  and  Open/Write  AndX) to  locate  a  vulnerable  host

   ID: 015

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SERVICE SCANNING (T1046)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries use network service scanning to locate systems and services that are accessible over the network.

   TOOLS: -

   NOTE: The malware checks the ability to write data to a specific folder on a remote system to identify a vulnerable host.

 * Page #17:
   > to folderand The  attacking  system  reads  the  log  file  and uses  its  contents  to  then  transfer  a  32-bit  or thevictim's 64-bitexecutable file it. run C:\Windows\Temp

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or files to the victim's system to perform further actions or operations. This technique involves moving executables or other files to the target system.

   TOOLS: -

   NOTE: The malware transfers a 32-bit or 64-bit executable file to the victim's C:\Windows\Temp folder.

 * Page #17:
   > ThemeterpreterDLL ismade operational  via  reflective  DLL  injection,  which copies  the  meterpreter  DLL  into  the  memory space  of  a  chosen  victim  process  (such  as explorer.exe) and runs it as a thread.

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: 

   DESCRIPTION: dversaries inject code into the address space of another process to execute their payload. Reflective DLL injection is a method of process injection where a DLL is loaded into the address space of a process without the use of traditional Windows APIs.

   TOOLS: METERPRETER

   NOTE: -

   ---

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transferring tools or files to the victim's system. This encompasses the initial transfer of the Meterpreter DLL.

   TOOLS: -

   NOTE: The executable acts as a stager to transfer the Meterpreter DLL to the victim system.

 * Page #18:
   > The  {~random}  file  names  are  not  really random,  but  instead  a  base64  combination  of the  victim's  system  volume  serial  number  and MAC  address,  which  are  obtained  by  queries to  the  system's  WMI  Service

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: WINDOWS MANAGEMENT INSTRUMENTATION (T1047)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries use Windows Management Instrumentation (WMI) to obtain information.

   TOOLS: -

   NOTE: -

 * Page #19:
   > A PowerShell script created by the infected email attachment

   ID: 019

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: This technique involves using PowerShell to execute commands and scripts. The described behavior of using a PowerShell script to handle a base64-encoded payload is a common use case of PowerShell for malicious activities.

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #19:
   > contains a base64-encoded block of text that is decoded,

   ID: 020

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes various methods of obfuscating files or data to avoid detection. Base64 encoding is a common method of obfuscation used to hide the contents of a payload.

   TOOLS: -

   NOTE: -

   LINK: 019, 021

 * Page #19:
   > written into memory as a thread, and executed.

   ID: 021

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves injecting code into the memory space of another process. The action of writing the decoded payload into memory and executing it as a thread aligns with process injection techniques.

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #23:
   > PowerShell script file created from base64 encoded string

   ID: 022

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell script file created from a base64 encoded string hidden in a Word document 

   TOOLS: -

   NOTE: -

 * Page #25:
   > other files arealsoencodedandobfuscated.

   ID: 023

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes various methods of obfuscating files or data to avoid detection. Base64 encoding is a common method of obfuscation used to hide the contents of a payload.

   TOOLS: -

   NOTE: -

   LINK: 019, 021

