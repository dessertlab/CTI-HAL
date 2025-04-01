## Detailed comments

 * Page #2:
   > MiniDuke

   ID: 000

   TOOLS: MINIDUKE (S0051)

 * Page #2:
   > CosmicDuke infections start by tricking victims into opening either a PDF file that contains an exploit

   ID: T01

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of vulnerabilities in client software to execute code. In the case of CosmicDuke, opening a PDF containing an exploit exploits a vulnerability to execute malicious code.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

 * Page #2:
   > a Windows executable whose filename is manipulated to make it look like a document or image file.

   ID: T02

   LINK: 002, 003

   ---

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: This technique involves inducing the user to run a malicious file, such as a Windows executable whose name has been manipulated to look like a document or image file.

   TOOLS: COSMICDUKE (S0050)

   NOTE: --

   LINK: 003

   ---

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves manipulating the file name to make it look like a different type of file, such as a document or image, in order to trick the victim into executing the malicious file.

   TOOLS: COSMICDUKE (S0050)

   NOTE: --

   LINK: 003

 * Page #2:
   > or

   ID: 001

   LINK: T01 OR T02 THEN T03 THEN T04

 * Page #2:
   > Once the victim opens the file, the malware gains persistence on the system and starts collecting information.

   ID: T03

   LINK: 004, 005, 006, 007, 008, 009

 * Page #2:
   > keylogger,

   ID: 004

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: recording of keystrokes made by the user to capture sensitive information such as credentials.

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > password stealers

   ID: 007

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: password

   stealers for a variety of popular chat, email and web browsing programs

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > clipboard stealer,

   ID: 005

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: CLIPBOARD DATA (T1115)

   SUB-TECHNIQUE: -

   DESCRIPTION: Theft of data in the system clipboard.

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > screenshotter,

   ID: 006

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capture of desktop screens or specific windows

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > It also collects information about the files on the system

   ID: 008

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of data from files in the system.

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > the capability to export cryptographic certificates and the associated private keys

   ID: 009

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: PRIVATE KEYS (T1552.004)

   DESCRIPTION: The exfiltration of private keys and cryptographic certificates.

   TOOLS: -

   NOTE: -

   LINK: T03

 * Page #2:
   > Once the information has been collected

   ID: T04

   LINK: 010, 011

 * Page #2:
   > it is sent out to remote servers via FTP

   ID: 010

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of FTP specifically to exfiltrate data

   TOOLS: -

   NOTE: -

   LINK: T04

 * Page #2:
   > Cosmu allows the attacker to download and execute other malware on the system

   ID: 011

    SOURCE: TEXT

    

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may transfer tools or other files from an external system into a compromised environment.

    

   TOOLS: -

    

   NOTES: -

   LINK: T04

 * Page #3:
   > Keylogger

   ID: 017

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: recording of keystrokes made by the user to capture sensitive information such as credentials.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Taking screenshots

   ID: 017

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capture of desktop screens or specific windows

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing data from clipboard

   ID: 018

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: CLIPBOARD DATA (T1115)

   SUB-TECHNIQUE: -

   DESCRIPTION: Theft of data in the system clipboard.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing files

   ID: 019

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of data from files in the system.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing PKI certificates and associated private keys

   ID: 020

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: UNSECURED CREDENTIALS (T1552)

   SUB-TECHNIQUE: PRIVATE KEYS (T1552.004)

   DESCRIPTION: The exfiltration of private keys and cryptographic certificates.

   TOOLS: -

   NOTE: -

 * Page #3:
   > Stealing usernames and passwords from browsers, instant messengers and email clients

   ID: 007

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: password

   stealers for a variety of popular chat, email and web browsing programs

   TOOLS: -

   NOTE: -

 * Page #3:
   > The information collected by the malware is automatically uploaded to remote servers via FTP

   ID: 010

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of FTP specifically to exfiltrate data

   TOOLS: -

   NOTE: -

 * Page #3:
   > It is possible that the PDF documents containing exploits were emailed to the targeted users as file attachments

   ID: 012

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Sending malicious attachments via email to induce victims to open them. PDF documents containing exploits are sent to targeted users as email attachments.

   TOOLS: -

   NOTE: -

 * Page #3:
   > CosmicDuke malware samples that use exploits to gain entry onto a target system (referred to as exploit files in the rest of this document) start with a malicious Flash object embedded into a PDF file.

   ID: 013

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: EXPLOIT PUBLIC-FACING APPLICATION (T1190)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exploitation of known vulnerabilities in publicly exposed applications, as in the case of exploits used in PDF files containing malicious Flash objects

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 014

 * Page #3:
   > When the file is launched, the object exploits the known CVE-2011-0611 vulnerability in specific versions of Adobe Flash, Reader and Acrobat products.

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPOLITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: exploitation of vulnerabilities in client software to execute malicious code. the malicious Flash object embedded in the PDF file exploits a known vulnerability in Adobe Flash, Reader, and Acrobat to execute the malware.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 013

 * Page #3:
   > social engineering to trick the user into willingly launching the attack file

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: CosmicDuke uses social engineering to induce the user to launch the attack file.

   TOOLS: COMSICDUKE (S0050)

   NOTE: -

   LINK: 016

 * Page #3:
   > the malware's executable file is first disguised as an image or document to make it seem innocuous

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Disguising the malicious file as an image or document to look legitimate.

   TOOLS: -

   NOTE: -

   LINK: 015

 * Page #7:
   > It creates a scheduled task and installs a Windows service

   ID: 021

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: SCHEDULED TASK (T1053.005)

   DESCRIPTION: Creation of planned activities to maintain persistence on the system.

   TOOLS: COSMU/MINIDUKE (S0051)

   NOTE: -

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: WINDOWS SERVICE (T1543.003)

   DESCRIPTION: installation of Windows services to maintain persistence on the system.

   TOOLS: COSMU/MINIDUKE (S0051)

   NOTE: -

 * Page #9:
   > The malware uses the FTP servers and WebDav servers both for exfiltrating the collected data and for updating the malware

   ID: 029

   SOURCE: TEXT

    

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

    

   DESCRIPTION: Adversaries may steal data by exfiltrating it over a different protocol than that of the existing command and control channel.

    

   TOOLS: -

    

   NOTE: -

 * Page #9:
   > Cosmu uses RC4 to decrypt incoming data and encrypt outgoing data

   ID: 023

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: STANDARD ENCODING (T1132.001)

   DESCRIPTION: use of standard encodings to transform data for transfer or storage, as in the case of using RC4 to encrypt and decrypt data.

   TOOLS: COSMU/MINIDUKE (S0051)

   NOTE: -

