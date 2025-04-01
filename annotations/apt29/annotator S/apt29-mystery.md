## Detailed comments

 * Page #2:
   > To compromise the victims, the attackers used extremely e"ective social engineering techniques which involved sending malicious PDF documents to their targets.

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: It is not specified that the PDF is attached in emails.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: MALICIOUS FILE (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution.

   TOOLS: -

   NOTES: -

   LINK: #001 THEN #002

 * Page #2:
   > These malicious PDF !les were rigged with exploits UkraineCommissionalsoagreedonaseriesofconcreteandimmedi attacking Adobe Reader versions 9, 10 and 11, bypassing its sandbox.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may exploit software vulnerabilities in client applications to execute code. 

   TOOLS: -

   NOTES: APT29 exploits an Adobe Reader 0-day vulnerability.

 * Page #2:
   > This downloader is unique per system and contains a customized backdoor written in Assembler

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries. 

   TOOLS: -

   NOTES: -

 * Page #2:
   > When loaded at system boot

   ID: 005

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may configure system settings to automatically execute a program during system boot or logon to maintain persistence or gain higher-level privileges on compromised systems. 

   TOOLS: -

   NOTES: -

 * Page #2:
   > the downloader uses a set of mathematical calculations to determine the computer-s unique !ngerprint,

   ID: 006

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may do this to gather information.

   TOOLS: -

   NOTES: APT29's goal is to get a fingerprint.

 * Page #3:
   > encrypt its communications later

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may employ an encryption algorithm to conceal command and control traffic rather than relying on any inherent protections provided by a communication protocol.

   TOOLS: -

   NOTES: -

   LINK: #006 THEN #007

 * Page #3:
   > the malware will use Twitter (unbeknownst to the user) and start looking for speci!c tweets from pre-made accounts

   ID: 008

   SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

    

   TECHNIQUE: WEB SERVICE (T1102)

    

   SUB-TECHNIQUE: -

    

   DESCRIPTION: The malware uses Twitter and searches for specific tweets from pre-made accounts.

    

   TOOLS: -

    

   NOTE: -

 * Page #3:
   > the tweets maintain speci!c tags labeling encrypted URLs for the backdoors

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #3:
   > These URLs provide access to the C2s, which then provide potential commands and encrypted transfers of additional backdoors onto the system via GIF !les.

   ID: 010

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #3:
   > if Twitter isn-t working or the accounts are down, the malware can use Google Search to !nd the encrypted strings to the next C2

   ID: 016

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: FALLBACK CHANNELS (T1008)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use fallback or alternate communication channels if the primary channel is compromised or inaccessible in order to maintain reliable command and control and to avoid data transfer thresholds.

   TOOLS: -

   NOTES: -

 * Page #3:
   > the malware can use Google Search to !nd the encrypted strings to the next C2

   ID: 011

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: WEB SERVICES (T1583.006)

   DESCRIPTION: Adversaries may register for web services. Using common services, such as those offered by Google or Twitter, makes it easier for adversaries to hide in expected noise.

   TOOLS: -

   NOTES: -

 * Page #3:
   > it receives encrypted backdoors that are obfuscated within GIF !les and disguised as pictures that appear on a victim-s machine

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T027)

   SUB-TECHNIQUE: STEGANOGRAPHY (T1027.003)

   DESCRIPTION: Adversaries may use steganography techniques in order to prevent the detection of hidden information. Steganographic techniques can be used to hide data in digital media such as images, audio tracks, video clips, or text files.

   TOOLS: -

   NOTES: -

 * Page #4:
   > Once they are downloaded to the machine,

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

   TOOLS: -

   NOTES: -

 * Page #4:
   > through functions such as copy !le, move !le, remove !le, make directory, kill process and of course, download and execute new malware and lateral movement tools.

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries. 

   TOOLS: -

   NOTES: -

 * Page #4:
   > The !nal stage backdoor connects to two servers, one in Panama and one in Turkey to receive the instructions from the attackers

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Commands to the remote system, and often the results of those commands, will be embedded within the protocol traffic between the client and server.

   TOOLS: -

   NOTES: -

