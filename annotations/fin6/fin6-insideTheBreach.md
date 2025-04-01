## Detailed comments

 * Page #3:
   > Magecart injects scripts designed to steal sensitive data that consumers enter into online payment forms on e-commerce websites directly or through compromised third-party suppliers used by these sites

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Adversaries may abuse various implementations of JavaScript for execution.

   TOOLS: -

   NOTES: In the document it is specified that the script is in JS. This is a modified version of the Modernizr JS library.

   ID: 002

   SOURCE: TEXT

   TACTIC: COLLECTION (T0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use methods of capturing user input to obtain credentials or collect information. 

   TOOLS: -

   NOTES: -

 * Page #8:
   > once a user hits the button to submit their payment on the compromised British Airways site, the information from the payment form is extracted along with their name and sent to the attacker's server.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: -

   NOTES: -

 * Page #8:
   > We saw proof of this on the domain name baways.com as well as the drop server path. The domain was hosted on 89.47.162.248 which is located in Romania and is, in fact, part of a VPS provider named Time4VPS based in Lithuania.

   IOC: Domain Name and IP address

 * Page #8:
   > they decided to go with a paid certificate from Comodo instead of a free LetsEncrypt certificate, likely to make it appear like a legitimate server

   ID: 004

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: DIGITAL CERTIFICATES (T1588.004)

   DESCRIPTION: Adversaries may buy and/or steal SSL/TLS certificates that can be used during targeting. SSL/TLS certificates are designed to instill trust.

   TOOLS: -

   NOTES: -

