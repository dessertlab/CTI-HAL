## Detailed comments

 * Page #3:
   > The initial document was probably sent within the Baltic region (or tested there). It was submitted to VirusTotal from Latvia. The name of the document translated from Russian is "new questioner". It is password-protected with the password: "goodmorning".

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending a document 

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #4:
   > It uses social engineering to convince the recipient to enable macros through the use of the images, logo and tagline of a newly launched, legitimate VPN tool InvinciBull by cybersecurity company Finjan.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Convincing the user to enable macros for execution through social engineering tactics

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #4:
   > the next stage obfuscated JavaScript is extracted from the form caption

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Use of obfuscated JavaScript as a next-stage payload extracted from the form caption

   TOOLS: -

   NOTE: -

   LINK: 002, 004

 * Page #4:
   > obfuscated JavaScript

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The obfuscation of both the macro and the JavaScript is part of this technique, where adversaries disguise their code to evade detection.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #5:
   > executing JavaScript from VBScript

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: the execution of VBScript, which in this case is used to launch JavaScript.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The deobfuscated JavaScript is actually a backdoor component that directly communicates to the C2 server (in this case hxxps://bing-cdn[.]com)

   ID: 006

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The C2 communication over HTTPS where adversaries communicate over common web protocols to avoid detection.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #6:
   > It executes the response

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: The backdoor uses JavaScript to execute commands received from the C2 server, leveraging the eval function to run these commands dynamically.

   TOOLS: -

   NOTE: -

   LINK: 006

