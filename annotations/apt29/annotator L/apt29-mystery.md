## Detailed comments

 * Page #1:
   > MiniDuke

   ID: 000

   TOOLS: MINIDUKE (S0051)

 * Page #2:
   > the attackers used extremely e"ective social engineering techniques which involved sending malicious PDF documents to their targets

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: use of malicious attachments

   TOOLS: -

   NOTE: -

 * Page #2:
   > This downloader is unique per system and contains a customized backdoor written in Assembler

   ID: 002

   SOURCE: TEXT

    

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

    

   TOOLS: -

    

   NOTES: -

 * Page #3:
   > encrypt its communications later

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: communications are encrytped

   TOOLS: -

   NOTE: -

 * Page #3:
   > the malware will use Twitter (unbeknownst to the user) and start looking for speci!c tweets from pre-made accounts

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware uses Twitter and searches for specific tweets from pre-made accounts.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #3:
   > the tweets maintain speci!c tags labeling encrypted URLs for the backdoors

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The use of encrypted URLs within tweets indicates obfuscation, as the content is concealed to avoid easy identification or analysis

   TOOLS: -

   NOTE: -

   ID: 003, 005

 * Page #3:
   > These URLs provide access to the C2s,

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: By leveraging web protocols like HTTP/HTTPS, the malware communicates with the C2 servers

   TOOLS: -

   NOTE: -

   LINK: 004, 006

 * Page #3:
   > transfers of additional backdoors onto the system via GIF !les

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: transferring tools or payloads into a compromised environmen

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #3:
   > encrypted transfers of additional backdoors onto the system via GIF !les

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION:  The use of GIF files to hide additional backdoors involves obfuscation, making it harder to detect the malicious content as it is embedded in seemingly benign file formats.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #3:
   > if Twitter isn-t working or the accounts are down, the malware can use Google Search to !nd the encrypted strings to the next C2

   ID: 012

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: FALLBACK CHANNELS (T1008)

   SUB-TECHNIQUE: -

   DESCRIPTION: If Twitter was not working or the accounts were down, the malware use Google Search to find encrypted strings.

   TOOLS: -

   NOTE: -

 * Page #3:
   > the malware can use Google Search to !nd the encrypted strings to the next C2

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: It uses encrypted strings found through Google Search to locate its next C2 server

   TOOLS: -

   NOTE: -

 * Page #3:
   > encrypted backdoors that are obfuscated within GIF !les and disguised as pictures that appear on a victim-s machine

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The backdoors are obfuscated within GIF files and are encrypted to hide their true nature

   TOOLS: -

   NOTE: -

 * Page #4:
   > they can fetch a larger backdoor which carries out the cyberespionage activities,

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Download and execute new malware from the C2 server

   TOOLS: -

   NOTES: -

   LINK: 011

 * Page #4:
   > copy !le, move !le, remove !le, make directory, kill process and of course, download and execute new malware and lateral movement tools

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Copy file, move file, make directory, and kill process

   TOOLS: -

   NOTES: -

   LINK: 010

