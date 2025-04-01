## Detailed comments

 * Page #2:
   > spear-phishing operation conducted by APT34

   ID: 001

   SOURCE:  TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The `survey.xls` file was likely distributed as an attachment in a spearphishing email, enticing the user to open it by masquerading as a legitimate survey.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > a file named survey.xls that was designed to look like an employee satisfaction survey tailored to either Westat employees or Westat customers

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The `survey.xls` file is designed to look like a legitimate employee satisfaction survey, which is a form of social engineering to get the victim to open the file and potentially enable macros.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #3:
   > At first the spreadsheet appeared to be blank. Only once the victim enables macros, the survey is displayed to the user and the malicious VBA code begins to execute

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059) 

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The malicious VBA code within the `survey.xls` file begins to execute once macros are enabled by the user, which is an example of scripting for malicious purposes.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #3:
   > The embedded VBA code unpacks a zip file into a temporary folder

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059) 

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The embedded VBA code that unpacks and installs the executable is an example of using VBA for malicious purposes.

   TOOLS: -

   NOTE: -

   LINK: 003, 005

 * Page #3:
   > extracts a "Client update.exe" executable file and installs it to "C:Users<User>valsClient update.exe"

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The unpacking of "Client update.exe" and its installation to the user's directory represents the transfer of a malicious tool onto the victim's machine.

   TOOLS: -

   NOTE: -

   LINK: 004, 006

 * Page #3:
   > the crtt function creates a scheduled task "CheckUpdate" that runs the unpacked executable five minutes after being infected by it, as well as on future log-ons.

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCLATION (TA0004) 

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The creation of the scheduled task "CheckUpdate" to run the executable is an example of using a scheduled task for persistence.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #5:
   > TONEDEAF is a backdoor that communicates with its Command and Control server via HTTP in order to receive and

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: TONEDEAF 2.0 uses HTTP for communication with its C2 server. This TTP describes how the backdoor establishes a connection and maintains communication with the adversary's infrastructure.

   TOOLS: TONEDEAF

   NOTE: -

 * Page #6:
   > shell execution capabilities

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION:  TONEDEAF 2.0's capability to execute arbitrary shell commands falls under this TTP, as it allows the attacker to issue any command on the compromised system.

   TOOLS: TONEDEAF

   NOTE: -

 * Page #6:
   > string decoding

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: TONEDEAF 2.0's use of string decoding is an example of this technique. By decoding strings dynamically, the malware avoids easy detection and analysis.

   TOOLS: TONEDEAF

   NOTE: -

 * Page #6:
   > the backdoor checks whether it was executed with "..." as an argument

   ID: 010

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: SERVICE EXECUTION (T1569.002)

   DESCRIPTION:  The scheduled task using the "..." argument to execute the backdoor aligns with this tactic.

   TOOLS: -

   NOTE: -

 * Page #6:
   > In the case it's executed without the correct argument, such as by launching it via a double click, it will display a blank GUI Window to the user

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.005)

   DESCRIPTION: The malware is trying to deceive the user into believing that the application is a legitimate, albeit broken, program, rather than malicious software.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #7:
   > TONEDEAF 2.0 also attempts to be more stealthy than its predecessor by hiding many of the interesting API imports it uses. The names of these APIs, and the DLLs that contain them, are stored as encoded strings and are decoded and resolved on demand during runtime

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: TONEDEAF 2.0 obfuscates the names of APIs and the DLLs that contain them by encoding these strings. The encoded strings are only decoded during runtime, making static analysis more difficult and increasing the stealthiness of the malware.

   TOOLS: TONEDEAF

   NOTE: -

   ---

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: Dynamically decodes API and DLL names during runtime to resolve them on demand.

   TOOLS: -

   NOTE: -

 * Page #7:
   > The backdoor uses HTTP for C2 communication

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION:  TONEDEAF 2.0 uses HTTP to communicate with its Command and Control (C2) server.

   TOOLS: TONEDEAF

   NOTE: -

   LINK: 014

 * Page #7:
   > custom encoding

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: The mention of a custom encoding mechanism indicates that TONEDEAF 2.0 is likely using a method to encode its C2 communications.

   TOOLS: TONEDEAF

   NOTE: -

   LINK: 013

   ---

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Uses custom encoding for C2 communication and message exchanges.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Messages sent by the backdoor always contain the HTTP query parameter "?ser=<6 digits>" as an identifier. The first three digits are the <server_id> and the last three are the <client_id>.

   ID: 022

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: TRAFFIC SIGNALING (T1205)

   SUB-TECHNIQUE: -

   DESCRIPTION: Uses specific HTTP query parameters as communication identifier.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Before performing the first request, the malware will generate the <client_id> derived from the environment variables %HOMEPATH% and %COMPUTERNAME% using a custom formula.

   ID: 018

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFOMRATION DISCOVERY (T1426)

   SUB-TECHNIQUE: -

   DESCRIPTION: Generates client ID using environment variables %HOMEPATH% and %COMPUTERNAME%.

   TOOLS: -

   NOTE: -

 * Page #8:
   > it will reply with an encoded message that contains the <server_id>

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The C2 server's response is encoded and contains the command within an HTML <div> element with a special class name. 

   TOOLS: -

   NOTE: -

 * Page #8:
   > The malware extracts the command by looking for an HTTP div element

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of a web page and an HTTP <div> element to transmit commands from the C2 to the malware aligns with using web services for C2. 

   TOOLS: -

   NOTE: -

 * Page #12:
   > Only Chrome password dumping is now supported, although interestingly the use of the file "fsociety.dat" as a password data store under the "AppData\Roaming" directory stayed the same.

   ID: 020

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: VALUEVAULT 2.0 specifically targets Chrome password dumping from local system.

   TOOLS: -

   NOTE: -

   ---

   ID: 021

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1115)

   SUB-TECHNIQUE: CREDENTIALS FROM WEB BROWSERS (T1115.003)

   DESCRIPTION: Uses 'fsociety.dat' in AppData\\Roaming to store stolen Chrome passwords.

   TOOLS: -

   NOTE: -

