## Detailed comments

 * Page #1:
   > Seaduke

   ID: 000

   TOOLS: SEADUKE (S0053)

 * Page #1:
   > the UPX packer

   ID: 001

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: SOFTWARE PACKING (T1027.002)

   DESCRIPTION: Malware is packaged using UPX, a common packer to compress and obfuscate the contents of the malware.

   TOOLS: UPX

   NOTE: -

 * Page #1:
   > a sample compiled using PyInstaller. This program allows an individual to write a program using the Python scripting language and convert it into an executable for the Microsoft Windows, Linux, Mac OSX, Solaris, or AIX platform

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: PYTHON (T1027.006)

   DESCRIPTION: Even if the UPX packer is removed, using PyInstaller to convert a Python program into an executable can result in some degree of obfuscation, further hiding the source code and intentions of the malware.

   TOOLS: PYINSTALLER

   NOTE: -

 * Page #2:
   > the underlying Python code has been obfuscated

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The underlying Python code has been obfuscated

   TOOLS: -

   NOTE: -

 * Page #3:
   > an 'exec(ZxkBDKLakV)' statement, which will presumably execute some Python code

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: PYTHON (T1059.006)

   DESCRIPTION: The use of `exec()` to execute Python code dynamically . This allows malware to execute arbitrary commands or runtime code.

   TOOLS: -

   NOTE: -

 * Page #3:
   > we discover that this string is generated via appending a number of strings to the 'ZxkBDKLakV' variable. Finally, we find that after this string is created, it is base64-decoded and subsequently decompressed using the ZLIB library

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of obfuscated code, string manipulation, and the use of methods such as string append, base64 decoding, and ZLIB decompression are all obfuscation techniques to hide the true intentions and functionality of the code.

   TOOLS: -

   NOTE: -

 * Page #5:
   > The remaining Python code still appears to be obfuscated

   ID: 007

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The Python code still appears to be obfuscated

   TOOLS: -

   NOTE: -

 * Page #5:
   > all variable names and class names have been obfuscated using long unique strings

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of obfuscated variable and class names with long, unique strings is an obfuscation technique.

   TOOLS: -

   NOTE: -

 * Page #6:
   > large blob of base64-encoded data, which is additionally decompressed using ZLIB

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of base64-encoded data and further compressed with ZLIB is an obfuscation technique.

   TOOLS: -

   NOTE: -

 * Page #6:
   > it will determine on which operating system it is running

   ID: 010

   SOURCE: TEXT

   TACTIC: DISCOVERY

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware determines which operating system it is running on, which is a form of system information discovery.

   TOOLS: -

   NOTE: -

 * Page #7:
   > Persistence via PowerShell

   ID: 011

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: POWERSHELL PROFILE (T1546.013)

   DESCRIPTION: Persistence via PowerShell

   TOOLS: -

   NOTE: -

 * Page #7:
   > Persistence via the Run registry key

   ID: 012

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/STARTUP FOLDER (T1547.001)

   DESCRIPTION: Persistence via the Run registry key

   TOOLS: -

   NOTE: -

 * Page #7:
   > Persistence via a .lnk file stored in the Startup directory

   ID: 013

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUTOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: SHORTCUT MODIFICATION (T1547.009)

   DESCRIPTION: Persistence via .lnk stored in the startup directory

   TOOLS: -

   NOTE: -

 * Page #8:
   > All network communications are performed over HTTP for this particular sample; however, it appears to support HTTPS as well

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The use of HTTP/HTTPS for communication.

   TOOLS: -

   NOTE: -

 * Page #8:
   > this Cookie value contains encrypted data

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Encryption and base64 encoding of the data in the Cookie value are obfuscation techniques.

   TOOLS: -

   NOTE: -

 * Page #9:
   > the encrypted data is encrypted using the RC4 algorithm

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILES (T1027.013)

   DESCRIPTION: RC4 algorithm is used

   TOOLS: -

   NOTE: -

 * Page #10:
   > This data is then base64-decoded with additional characters ('-_') prior to being decrypted via RC4 using the previously discussed key.

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: ENCRYPTED/ENCODED FILES (T1027.013)

   DESCRIPTION: RC4 algorithm is used

   TOOLS: -

   NOTE: -

