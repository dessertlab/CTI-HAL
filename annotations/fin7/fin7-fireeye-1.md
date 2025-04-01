## Detailed comments

 * Page #1:
   > BOOSTWRITE and RDFSNIFFER

   ID: 000

   TOOLS: BOOSTWRITE (S0415), RDFSNIFFER

 * Page #1:
   > BOOSTWRITE – an in-memory-only dropper

   ID: 001

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: BOOSTWRITE retrieves an encryption key from a remote server

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 002

 * Page #1:
   > that decrypts embedded payloads using an encryption key retrieved from a remote server at runtime

   ID: 002

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of encryption to protect the embedded payloads is a form of obfuscation, making it harder for analysts to understand or detect the malicious content without the correct decryption key.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 001

 * Page #2:
   > The malware loads into the same process as the Command Center process by abusing the DLL load order of the legitimate Aloha utility

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware is effectively injecting itself into the process. This allows the malware to execute within the context of a trusted application, making it harder to detect and more likely to bypass security controls.

   TOOLS: RDFSNIFFER, BOOSTWRITE (S0415)

   NOTE: -

 * Page #2:
   > BOOSTWRITE is a loader cra$ed to be launched via abuse of the DLL search order of applications which load the legitimate 'Dwrite.dll' provided by the Microso$ DirectX Typography Services. The application loads the 'gdi' library, which loads the 'gdiplus' library, which ultimately loads 'Dwrite'.

   ID: 005

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: HIJACK EXECUTION FLOW (T1574)

   SUB-TECHNIQUE: DLL SEARCH ORDER HIJACKING (T1574.001)

   DESCRIPTION: OOSTWRITE is crafted to exploit the DLL search order used by applications, specifically targeting those that load the Dwrite.dll (a legitimate Microsoft DirectX Typography Services DLL). The application follows a typical load order (gdi -> gdiplus -> Dwrite), and the attacker places a malicious Dwrite.dll in a directory that the application will search first, causing it to load the malicious DLL instead of the legitimate one.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

 * Page #2:
   > Once loaded, `DWrite.dll` connects to a hard-coded IP and po#

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071)

   DESCRIPTION: BOOSTWRITE communicates over the internet using a common protocol to connect to a hardcoded IP address and retrieve the decryption key and IV. This technique involves using standard web protocols to communicate with a command-and-control (C2) server.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 008

 * Page #2:
   > it retrieves a decryption key and initialization vector (IV) to decrypt two embedded payload DLLs

   ID: 008

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: SOFTWARE PACKING (T1027.002)

   DESCRIPTION: The process of embedding and encrypting DLL payloads within the DWrite.dll file and then decrypting them using a custom key and IV retrieved from a remote server is similar to software packing. This technique is used to protect the payloads from detection until they are unpacked and executed.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 007, 009, 012

 * Page #2:
   > the malware "rst generates a random "le name to be used as a text log under the current user's %TEMP% directory; this "lename sta#s with ~rdf and is followed by a set of random numbers

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: COMPILE AFTER DELIVERY (T1027.004)

   DESCRIPTION: This technique covers instances where adversaries create or generate files at runtime, often with randomized or unpredictable names to evade detection or hinder analysis. The use of random file names can make it more difficult for defenders to identify and track malicious files.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 008, 010

 * Page #2:
   > the malware scans its own image to "nd the location of a 32-byte long multi-XOR key which is used to decode data inside its body

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: BOOSTWRITE scans its own image to find and use a multi-XOR key to decode data within its body. The decoded data includes the IP address and port needed to retrieve the encryption key and IV. This technique involves deobfuscating or decoding files or data to extract useful information, such as decryption keys.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 009, 011

 * Page #2:
   > The encryption algorithm uses the ChaCha stream cipher with a 256-bit key and 64-bit IV

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: SYMMETRIC CRYPTOGRAPHY (T1573.001)

   DESCRIPTION: BOOSTWRITE uses the ChaCha stream cipher, a symmetric encryption algorithm, to encrypt and decrypt the payloads. It retrieves a decryption key and an initialization vector (IV) from a remote server after connecting to a hardcoded IP address and port. This falls under the category of using symmetric cryptography for securing communications.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

 * Page #2:
   > Once the key and the IV are downloaded the malware decrypts the embedded payloads

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: DEOBFUSCATE/DECODE FILES OR INFORMATION (T1140)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malware decrypts embedded payloads using a key and IV, which falls under this technique. Decrypting and then loading a payload into memory without writing it to disk is a tactic to avoid detection by file-based security tools.

   TOOLS:  BOOSTWRITE (S0415)

   NOTE: -

   LINK: 008, 013

 * Page #2:
   > The payloads are expected to be PE32.DLLs which, if the tests pass, are loaded into memory without touching the "lesystem

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The downloaded and decrypted payloads are PE32.DLL files that are likely malicious. The malware performs sanity checks to ensure these files are intact and correct before proceeding to load them.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 012

 * Page #3:
   > RDFSNIFFER is a module loaded by BOOSTWRITE which allows an a!acker to monitor and tamper with legitimate connections made via NCR Corporation's 'Aloha Command Center Client' (RDFClient)

   ID: 014

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: RDFSNIFFER's interactions with RDFClient and potentially monitoring network traffic or connections align with using application layer protocols for communication.

   TOOLS: BOOSTWRITE (S0415), RDFSNIFFER

   NOTE: -

   LINK: 015

 * Page #3:
   > RDFSNIFFER loads into the same process as the legitimate RDFClient by abusing the utility's DLL load order, launching each time the 'Aloha Command Center Client' is executed on an impacted system

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: This describes how RDFSNIFFER injects itself into the process of RDFClient, which aligns with the process injection technique 

   TOOLS: BOOSTWRITE (S0415), RDFSNIFFER

   NOTE: -

   LINK: 014

 * Page #3:
   > When the RDFSNIFFER module is loaded by BOOSTWRITE it hooks several Win32 API functions intended to enable it to tamper with NCR Aloha Command Center Client sessions or hijack elements of its user-inte%ace

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Hooking Win32 API functions can be part of process injection techniques, where the malware modifies the behavior of the legitimate application to perform its own functions.

   TOOLS: BOOSTWRITE (S0415), RDFSNIFFER

   NOTE: -

   LINK: 017

 * Page #3:
   > this enables the malware to alter the user's last input time to ensure application sessions do not time out.

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: By tampering with the NCR Aloha Command Center Client's user-interface, the malware could be disguising its malicious actions as normal application behavior.

   TOOLS: BOOSTWRITE (S0415)

   NOTE: -

   LINK: 016

 * Page #4:
   > This module also contains a backdoor component that enables it to inject commands into an active RDFClient session

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The backdoor component interacts with the RDFClient session, potentially using web protocols or other application layer protocols to send and receive commands.

   TOOLS: -

   NOTE: -

   LINK: 019

 * Page #4:
   > This backdoor allows an a!acker to upload, download, execute and/or delete arbitrary "les

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The ability to upload and download files is directly related to this technique, which involves transferring tools or files into or out of a compromised environment.

   TOOLS: -

   NOTE: -

   LINK: 018

 * Page #6:
   > CARBANAK

   ID: S01

   TOOL: CABANAK (S0030)

 * Page #6:
   > BABYMETAL,

   ID: S02

   TOOL BABYMETAL

