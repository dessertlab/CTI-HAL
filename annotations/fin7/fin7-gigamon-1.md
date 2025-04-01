## Detailed comments

 * Page #2:
   > FIN7 leverages a number of targeted phishing techniques to initially exploit victims in the retail sector

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: phishing techniques were used

   TOOLS: -

   NOTE: -

 * Page #3:
   > the actor primarily utilize malicious shortcut files (LNK) or visual basic scripts (VBS or VBE) to achieve code execution from within their lure

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The actor relies on users to open malicious LNK or Visual Basic script (VBS/VBE) files embedded within documents, triggering the infection.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > visual basic scripts

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: The use of Visual Basic scripts (VBS or VBE) to execute malicious code within the victim system.

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #3:
   > FIN7 appears to have pivoted from using OLE embedded LNK files to using OLE embedded CMD files. When executed, the CMD file writes JScript to "tt.txt"

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: FIN7 uses CMD files embedded within documents, which require user interaction to execute malicious code.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #3:
   > The batch script then copies itself to "pp.txt", also under the current user's home directory, before running WScript using the JScript engine on the file

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The CMD file writes and then executes JScript code using the WScript engine to evaluate further instructions from the file.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #4:
   > The attacker now obfuscates that name and continues to break up the base64 string into multiple strings within an array

   ID: 005

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attacker continues to obfuscate the codebase by breaking up the base64-encoded string into multiple parts and renaming variables to evade detection.

   TOOLS: -

   NOTE: -

