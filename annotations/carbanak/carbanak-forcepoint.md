## Detailed comments

 * Page #1:
   > contains an encoded Visual Basic Script (VBScript)

   ID: 001

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The use of VBScript for executing commands or scripts on the victim system.

   TOOLS: -

   NOTE: -

 * Page #1:
   > The RTF document we analyzed (SHA1 1ec48e5c0b88f4f850facc718bbdec9200e4bd2d) has an embedded OLE object contains a VBScript file

   ID: 002

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The use of VBScript for executing commands or scripts on the victim system.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #1:
   > When the document is opened the targeted user is lured into double-clicking on the embedded object which is disguised as an image

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: When the user double-clicks on the embedded object disguised as an image, the malicious script or executable is run.

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #2:
   > Double clicking on the image results in a file open dialog for "unprotected.vbe". If the user executes this file then the malware will begin to execute.

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The user is tricked into double-clicking on the disguised embedded object, which leads to the execution of the malicious .vbe file.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #2:
   > The VBScript malware inside the RTF document (SHA1 cd75662751c59951717b4704ea2cdb6fb7ec19bc) is an encoded file.

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: NON-STANDARD ENCODING (T1132.002)

   DESCRIPTION: The VBScript is encoded within the RTF document, making it more difficult to detect and analyze.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The module is base64 encoded inside the main VBScript file

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The module is base64 encoded, which is a form of obfuscation to hide the malicious code from security tools and analysts.

   TOOLS: -

   NOTE: -

 * Page #2:
   > The "ggldr" script will send and receive commands to and from Google Apps Script, Google Sheets, and Google Forms

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: The "ggldr" script uses legitimate third-party web services such as Google Apps Script, Google Sheets, and Google Forms for C&C communication, hiding in plain sight within legitimate traffic.

   TOOLS: -

   NOTE: -

   ---

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The "ggldr" script is responsible for transferring commands and receiving data through the use of Google services.

   TOOLS: -

   NOTE: -

   ---

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: "The \"ggldr\" script will send and receive commands with web protocols.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Upon the first attempt to contact the hard-coded Google Apps Script URL with the user's unique infection ID, the C& that no spreadsheet currently exists for the user.

   ID: 009

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using legitimate third-party web services like Google Apps Script, Google Sheets, and Google Forms for C&C communication.

   TOOLS: -

   NOTE: -

 * Page #3:

   

   ID: 008

   SOURCE: TEXT

   DESCRIPTION: The C&C procedure

