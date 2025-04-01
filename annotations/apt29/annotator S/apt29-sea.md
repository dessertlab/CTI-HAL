## Detailed comments

 * Page #1:
   > it becomes quickly apparent that we're dealing with a sample compiled using PyInstaller. This program allows an individual to write a program using the Python scripting language and convert it into an executable for the Microsoft Windows, Linux, Mac OSX, Solaris, or AIX platform.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: PYTHON (T1059.006)

   DESCRIPTION: Adversaries may abuse Python commands and scripts for execution. 

   TOOLS: -

   NOTES: -

 * Page #1:
   > the UPX packer

   ID: 001

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: Packing's goal is obfuscation. This is the first layer of obfuscation.

 * Page #2:
   > we quickly realize that the underlying Python code has been obfuscated.

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #3:
   > Tracing through the obfuscated code, we identify an 'exec(ZxkBDKLakV)' statement, which will presumably execute some Python code.

   ID: 003

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: PYTHON (T1059.006)

   DESCRIPTION: Adversaries may abuse Python commands and scripts for execution. 

   TOOLS: -

   NOTES: It has been identified exec statement.

 * Page #3:
   > we discover that this string is generated via appending a number of strings to the 'ZxkBDKLakV' variable. Finally, we find that after this string is created, it is base64-decoded and subsequently decompressed using the ZLIB library.

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #5:
   > almost all variable names and class names have been obfuscated using long unique strings.

   ID: 013

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #6:
   > One of the first things we notice is a large blob of base64-encoded data, which is additionally decompressed using ZLIB.

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover or analyze by encrypting, encoding, or otherwise obfuscating its contents on the system or in transit.

   TOOLS: -

   NOTES: -

 * Page #6:
   > When the malware is initially run, it will determine on which operating system it is running.

   ID: 005

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: An adversary may attempt to get detailed information about the operating system and hardware, including version, patches, hotfixes, service packs, and architecture. 

   TOOLS: -

   NOTES: -

 * Page #7:
   > Persistence via PowerShell

   ID: 006

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: POWERSHELL PROFILE (T1546.013)

   DESCRIPTION: Adversaries may gain persistence and elevate privileges by executing malicious content triggered by PowerShell profiles.

   TOOLS: -

   NOTES: -

 * Page #7:
   > 2. Persistence via the Run registry key 3. Persistence via a .lnk file stored in the Startup directory

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS / STARTUP FOLDER (T1547.001)

   DESCRIPTION: Adversaries may achieve persistence by adding a program to a startup folder or referencing it with a Registry run key.

   TOOLS: -

   NOTES: -

 * Page #8:
   > After the malware installs itself, it begins making network requests. All network communications are performed over HTTP for this particular sample; however, it appears to support HTTPS as well.

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may communicate using OSI application layer protocols.

   TOOLS: -

   NOTES: -

 * Page #8:
   > In actuality, this Cookie value contains encrypted data. The base64-encoded data is parsed from the Cookie value (padding is added as necessary).

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILES (T1027.013)

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTES: Base64 encoding.

 * Page #9:
   > Finally, the encrypted data is encrypted using the RC4 algorithm. The key is generated by concatenating the previously used random string with the new one, and taking the SHA1 hash of this data.

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILES (T1027.013)

   DESCRIPTION: Adversaries may encrypt or encode files to obfuscate strings, bytes, and other specific patterns to impede detection.

   TOOLS: -

   NOTES: RC4 encoding.

 * Page #10:
   > This data is then base64-decoded with additional characters ('-_') prior to being decrypted via RC4 using the previously discussed key.

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Obfuscated Files or Information to hide artifacts of an intrusion from analysis. They may require separate mechanisms to decode or deobfuscate that information depending on how they intend to use it.

   TOOLS: -

   NOTES: -

