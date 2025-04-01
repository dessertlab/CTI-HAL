## Detailed comments

 * Page #3:
   > the group still deploys lightweight JavaScript backdoor with communication over HTTPS mimicking Content Delivery Network (CDN) domains

   ID: 001

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The backdoor uses HTTPS for communication, which is an application layer protocol. Mimicking CDN domains indicates that the traffic is designed to blend in with legitimate web traffic.

   TOOLS: -

   NOTE: -

 * Page #3:
   > they still leverage JavaScript backdoor via renamedwscript.exe with the actual JavaScript code called "errors.txt," for example

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The backdoor is implemented using JavaScript, executed via the Windows Script Host (wscript.exe), which is a common scripting interpreter.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The FIN7 Microsoft document loaders do not rely on any exploits but simply require a social engineering trick (https://www.sentinelone.com/blog/phishing-revealingvulnerable-targets/) to "Enable Content" to activate macros.

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: a Microsoft document is used.

   TOOLS: -

   NOTE: -

 * Page #3:
   > the macro logic copies the original JavaScript execution enginewscript.exe in %LOCALAPPDATA%

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: wscript.exe is used to execute JavaScript scripts. The adversaries rely on this interpreter to execute their malicious JavaScript.

   TOOLS: -

   NOTE: -

 * Page #3:
   > checking the system drive size viaGetDrive.TotalSize of more than 2456 bytes to possibly thwart anti-sandbox check

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: SYSTEM CHECKS (T1497.001)

   DESCRIPTION: The malware performs checks on the system environment to detect if it is running in a sandbox (e.g., by checking the size of the drive).

   TOOLS: -

   NOTE: -

 * Page #4:
   > The actual obfuscated Javascript backdoor is stored in UserForm object, which is also written to a disc as "errors.txt" in%TEMP%

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: an obfuscated JavaScript backdoor is used

   TOOLS: -

   NOTE: -

 * Page #4:
   > The final execution of the backdoor is performed via this following command: %LOCALAPPDATA%mses.exe //b /e:jscript %temp%errors.txt

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION:  The command executes a JavaScript backdoor using mses.exe, which is associated with executing JScript.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The malware checks for the presence of virtual machine

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: SYSTEM CHECKS (T1497.001)

   DESCRIPTION: checking whether the malware is running in a virtualized environment

   TOOLS: -

   NOTE: -

 * Page #6:
   > queries active directory

   ID: 007

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: DOMAIN TRUST DISCOVERY (T1482)

   SUB-TECHNIQUE: -

   DESCRIPTION: This refers to querying Active Directory to discover domain trust relationships, which helps attackers gather information about the environment.

   TOOLS: -

   NOTE: -

 * Page #6:
   > operating system, screen resolution

   ID: 008

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE:

   DESCRIPTION: Retrieving information about the operating system and the screen resolution 

   TOOLS: -

   NOTE: -

 * Page #6:
   > retrieves a process list.

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Retrieving a list of running processes helps attackers understand the environment, identify security software, or locate valuable processes to exploit.

   TOOLS: -

   NOTE: -

