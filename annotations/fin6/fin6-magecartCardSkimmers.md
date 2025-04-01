## Detailed comments

 * Page #3:
   > The attackers injected their code into a library provided on Volusion's e-commerce platform for their client shops.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATION (T1190)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to exploit a weakness in an Internet-facing host or system to initially access a network.

   TOOLS: -

   NOTES: -

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #3:
   > They created a new object "e.widget.unbridge" right before the original object "e.widget.bridge" and the malicious code is inside the new object. It's worth noting that the attackers even wrote their malicious code in a similar coding style to make it look more like a part of the original source code.

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTES: -

 * Page #3:
   > The injected object will create a new script element to load another remote script stored on Google Storage.

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Tools or files may be copied from an external adversary-controlled system to the victim network through the command and control channel.

   TOOLS: -

   NOTES: -

 * Page #4:
   > The skimmer copies the information on the entire payment form: the victim's name, address, phone number, email address, and credit card details (the number, cardholder name, expiration month, expiration year, and CVV number).

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (T0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use methods of capturing user input to obtain credentials or collect information. 

   TOOLS: -

   NOTES: -

 * Page #5:
   > Once the skimmer has the credit card details, it serializes the copied data into a string and encodes it with Base64. Then, it performs a character permutation on the encoded string to make sure it can't be directly decoded with Base64 decoding.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHINQUE: ENCRYPTED/ENCODED FILE (T1027.013)

   DESCRIPTION: Encrypting and/or encoding file content aims to conceal malicious artifacts within a file used in an intrusion.

   TOOLS: -

   NOTES: It is not possible to decode the string in the standard way, beacause of permutation.

 * Page #5:
   > The data will then be stored in sessionStorage with the key "__utmz_opt_in_out"

   IOC: Host Artifacts

 * Page #5:
   > it will use HTTP POST to send the stolen payment information to a remote server at "hxxps[:]//volusion-cdn[.]com/analytics/beacon" for exfiltration.

   ID: 007

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: -

   NOTES: -

