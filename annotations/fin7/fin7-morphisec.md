## Detailed comments

 * Page #2:
   > the initial infection vector is a malicious Word document attached to a phishing email that is well-tailored to the targeted business

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: use of a spear phishing email with an attached malicious Word document to initiate an attack. The document is crafted to target specific business interests or individuals

   TOOLS: -

   NOTE: -

   LINK: 002, 003

 * Page #3:
   > The Word document executes a fileless attack that uses DNS queries to deliver the next shellcode stage (Meterpreter)

   ID: 002

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.001)

   DESCRIPTION: use of DNS queries as a communication method to deliver and execute payloads in a fileless manner. 

   TOOLS: -

   NOTE: -

   LINK: 001

 * Page #4:
   > The attached .rtf file uses OLE

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

    

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: This TTP refers to the exploitation of vulnerabilities in client applications to execute malicious code. In this case, the .rtf file uses Object Linking and Embedding (OLE) to execute code.

   TOOLS: -

   NOTE: -

   LINK: 001, 004

 * Page #4:
   > executes obfuscated JavaScript code

   ID: 004

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: using JavaScript to execute malicious code. The obfuscated JavaScript in the document is executed to deliver the payload.

   TOOLS: -

   NOTE: -

   LINK: 003, 005

 * Page #5:
   > The first stage JavaScript copies additional JavaScript code snippets in txt format from the RTF document into a random directory "C:\Users\<User Name>\<Random guid>\". The same code snippets are combined into a second stage JavaScript in "C:\Users\<User Name>\".

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: avaScript is used to handle and execute code snippets.

   TOOLS: -

   NOTE: -

   LINK: 004, 006

 * Page #5:
   > the first stage JavaScript creates a scheduled task that executes the second stage code within a minute

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: The scheduled task is used here to delay the execution of the second stage code, helping to evade detection.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #6:
   > an additional scheduled task "AdobeFlashSync" is created for persistency

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION:  The task named "AdobeFlashSync" is used to repeatedly execute actions, including recreating JavaScript code and executing a PowerShell script, thereby maintaining persistence on the victim's system.

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #6:
   > recreating the JavaScript code

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: JavaScript is used as part of the attack chain, specifically to generate and execute additional scripts. This aligns with the technique of using JavaScript to perform malicious actions.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #6:
   > which later will create and execute a PowerShell script (described below).

   ID: 009

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: This involves using PowerShell scripts as part of the infection chain. The PowerShell script is created and executed as a subsequent stage of the attack.

   TOOLS: -

   NOTE: -

   LINK: 008, 010

 * Page #6:
   > Afterwards, it deletes its own JavaScript code traces

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: removing files or traces of the attack from the host to cover the tracks and avoid detection

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #7:
   > The PowerShell script executes a compressed first stage PowerShell child process, which then performs a second stage PowerShell process

   ID: 011

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: the PowerShell script is used to launch a series of PowerShell processes, demonstrating how PowerShell can be leveraged for multiple stages of execution.

   TOOLS: -

   NOTE: -

   LINK: 009, 012

 * Page #7:
   > The latter PowerShell injects a shellcode into its own process using well-known CreateThread and VirtualAlloc techniques

   ID: 012

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DYNAMIC-LINK LIBRARY INJECTION (T1055.001)

   DESCRIPTION: the PowerShell script is using techniques like CreateThread and VirtualAlloc for shellcode injection

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #8:
   > FIN7 implemented a shellcode that gets the next stage shellcode using the DNS messaging technique directly from memory

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: The shellcode retrieves the next stage of the attack by leveraging DNS queries to fetch additional malicious code, demonstrating the use of DNS for covert data exfiltration or payload delivery.

   TOOLS: -

   NOTE: -

 * Page #10:
   > the shellcode deletes the 'MZ' prefix from within a very important part of the shellcode. This prefix indicates it may be a dll, and its deletion helps the attack to evade memory scanning solutions.

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OVFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: the shellcode is encrypted

   TOOLS: -

   NOTE: -

