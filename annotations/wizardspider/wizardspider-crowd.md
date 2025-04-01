## Detailed comments

 * Page #5:
   > TrickBot

   ID: 001

   SOURCE: TEXT

   TOOLS: TRICKBOT (S0266)

   LINK: 002 OR 003

 * Page #5:
   > typically distributed either via spam email

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: -

   DESCRIPTION: he initial compromise involves TrickBot, which is typically distributed via spam email, suggesting the use of phishing techniques to gain an initial foothold.

   TOOLS: TRICKBOT (S0266)

   NOTE: -

   LINK: 001

 * Page #5:
   > through the use of the Emotet

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Distribution via Emotet

   TOOLS: TRICKBOT (S0266), EMOTET

   NOTE: Emotet's role in downloading and executing TrickBot within the victim environment showcases the technique of transferring tools from external systems to the victim's network.

   LINK: 001

 * Page #5:
   > TrickBot's modules (such aspwgrab)could aid in recovering the credentials needed to compromise environments

   ID: 004

   SOURCE: TEXT

   TACTIC: CREDENTIALS ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: -

   DESCRIPTION: TrickBot's pwgrab module: This module is designed to recover credentials, aiding in further compromising environments by obtaining necessary credentials.

   TOOLS: TRICKBOT (S0266)

   NOTE: -

   LINK: 005

   ---

   ID: 035

   SOURCE: TEXT

   TACTIC: CREDENTIALS ACCESS (TA0006)

   TECHNIQUE: OS CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to dump credentials to obtain account login and credential material, normally in the form of a hash or a clear text password.

   TOOLS: TRICKBOT (S0266)

   NOTE: -

 * Page #5:
   > PowerShell Empire traffic to perform reconnaissance and lateral movement

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Tunneling PowerShell Empire traffic: This technique involves using PowerShell scripts for reconnaissance and lateral movement within the compromised environment.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #5:
   > An obfuscated PowerShell script is executed

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Use of obfuscated PowerShell scripts to avoid detection.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #5:
   > connects to a remote IP address

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: -

   DESCRIPTION: Establishing command and control communication with a remote IP.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #5:
   > A reverse shell is downloaded and executed on the compromised host.

   ID: 008

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading and executing a reverse shell on the compromised host.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Reconnaissance of the network is conducted using standard Windows command line tools along with external uploaded tools

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: REMOTE SYSTEM DISCOVERY (T1018)

   SUB-TECHNIQUE: -

   DESCRIPTION: Utilizing standard and external tools to gather information about the network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Lateral movement throughout the network is enabled using Remote Desktop Protocol (RDP)

   ID: 010

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: REMOTE DESKTOP PROTOCOL (T1021.001)

   DESCRIPTION: Using RDP for moving laterally within the network.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Service User Accounts are created

   ID: 011

   SOURCE: TEXT

   TACTIC: INITAL ACCESS (TA0001), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using or creating new user accounts for persistence and privilege escalation.

   TOOLS: -

   NOTE: -

 * Page #5:
   > PowerShell Empire is downloaded

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Downloading and installing PowerShell Empire for post-exploitation activities.

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #5:
   > installed as a service

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SERVICE EXECUTION (T1035)

   SUB-TECHNIQUE: -

   DESCRIPTION: Installing PowerShell Empire as a service to maintain persistence and control.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #5:
   > PSEXEC is used to push out the Ryuk binary to individual hosts

   ID: 014

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: SMB/WINDOWS ADMIN SHARES (T1021.002)

   DESCRIPTION: Employing PsExec to push out the Ryuk binary to multiple hosts.

   TOOLS: -

   NOTE: -

 * Page #5:
   > Batch scripts are executed to terminate processes/services and remove backups, followed by the Ryuk binary

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXECUTION THROUGH API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using batch scripts to terminate processes/services and remove backups before executing the Ryuk binary.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Ryuk was tailored to target enterprise environments and some of the modifications include removing anti-analysis checks

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: SOFTWARE PACKING (T1027.002)

   DESCRIPTION: Modifying the malware to remove checks that could detect analysis environments.

   TOOLS: -

   NOTE: -

 * Page #6:
   > checking to see if the host is running VirtualBox by calling the instruction CPUID

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), DISCOVERY (TA0007)

   TECHNIQUE: VIRTUALIZATION/SANDBOX EVASION (T1497)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using CPUID instruction to detect if the malware is running in a virtualized environment like VirtualBox.

   TOOLS: -

   NOTE: -

 * Page #6:
   > Encrypts files using RSA-2048 and AES-256

   ID: 018

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Encrypts files using RSA-2048 and AES-256

   TOOLS: -

   NOTE: This indicates that the malware encrypts victim files to make them inaccessible, demanding a ransom for decryption.

 * Page #6:
   > Stores keys in the executable using the proprietary Microsoft SIMPLEBLOB format

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL  (T1070)

   SUB-TECHNIQUE: -

   DESCRIPTION: Stores keys in the executable using the proprietary Microsoft SIMPLEBLOB format

   TOOLS: -

   NOTE: This method involves storing encryption keys in a specific format to obfuscate their presence and avoid detection.

 * Page #6:
   > Uses a file marker ofHERMESto mark or check if a file has been encrypted

   ID: 020

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Uses a file marker of HERMES to mark or check if a file has been encrypted

   TOOLS: -

   NOTE: This is a method to identify encrypted files and avoid re-encrypting them.

 * Page #7:
   > Upon execution, the dropper constructs an installation folder path. The folder path is created by calling GetWindowsDirectoryWand then inserting a null byte at the fourth character of the path. This is used to create a string that contains the drive letter path

   ID: 022

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: GetWindowsDirectoryW to construct installation folder path

   TOOLS: -

   NOTE: The dropper uses a native Windows API call to get the Windows directory path and then manipulates it to create a drive letter path. This is used for constructing the installation folder path, which aids in evasion and persistence.

   LINK: 023

 * Page #7:
   > Ryuk executable payload deleting the dropper when executed

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: Deleting the dropper when executed

   TOOLS: -

   NOTE: The executable payload removes the initial dropper to minimize traces of the initial infection vector and reduce the chances of detection and analysis.

   LINK: 022

 * Page #7:
   > If the host operating system is Windows XP or earlier, the stringDocuments and Settings\Default User\is appended to the drive letter path. If the host is Windows Vista or newer, the stringusers\Public\is appended to the drive letter path. For Windows XP, an example folder path would beC:\Documents and Settings\Default User\,and for Window Vista or higher, the path would be C:\Users\Public

   ID: 023

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Environment awareness based on OS version

   TOOLS: -

   NOTE: The malware checks the OS version to determine the appropriate folder path for installation. For Windows XP or earlier, it appends Documents and Settings\Default User\ to the drive letter path. For Windows Vista or newer, it appends Users\Public\ to the drive letter path. This OS-specific behavior indicates awareness of the environment to ensure compatibility and persistence.

   LINK: 022, 024

 * Page #7:
   > A random executable file name is then constructed. It is created by calling_srand with a seed value returned from callingGetTickCount,then_randis continuously called until five alphabetic characters are concatenated together. The extension .exeis then appended

   ID: 024

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: MATCH LEGITIMATE NAME OR LOCATION (T1036.003)

   DESCRIPTION: A random executable file name is constructed by calling _srand with a seed value from GetTickCount and _rand to generate five alphabetic characters

   TOOLS: -

   NOTE: This technique generates a random file name, making it less likely to be detected as a known malicious file.

   LINK: 023, 025

 * Page #7:
   > The dropper checks whether the host is 32-bit or 64-bit by callingIsWow64Processand writes one of two embedded payload executables corresponding to the host's architecture

   ID: 025

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using IsWow64Process to determine system architecture

   TOOLS: -

   NOTE: This technique checks the system architecture to ensure the correct payload is used.

   LINK: 024, 026

 * Page #7:
   > The newly written executable is then run by callingShellExecuteW

   ID: 026

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: Constructing and running the executable using ShellExecuteW

   TOOLS: -

   NOTE: This involves calling native APIs to execute the payload, enabling direct interaction with the system for execution.

   LINK: 025

 * Page #7:
   > a ping-like request to an IP address once the encryption process was completed

   ID: 027

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006), DISCOVERY (TA0007)

   TECHNIQUE: NETWORK SNIFFING (T1040)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ping-like request to an IP address once the encryption process was completed

   TOOLS: -

   NOTE: -

 * Page #8:
   > many ransomware families contain extensive lists of file extensions or folder names that should not be encrypted (whitelisted), but Ryuk only whitelists three extensions: It will not encrypt files with the extensionsexe, dll,orhrmlog.

   ID: 028

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ryuk specifically avoids encrypting files with the extensions .exe, .dll, and .hrmlog. This technique is employed to prevent the encryption of executable files, dynamic link libraries, and debug log files, which might be critical for system operation or development/debugging purposes.

   TOOLS: -

   NOTE: -

 * Page #8:
   > Ryuk uses a combination of symmetric (AES) and asymmetric (RSA) encryption to encrypt files

   ID: 029

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED FOR IMPACT (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: AES-256 Encryption: Applied to the victim's files to securely encrypt them. RSA-2048 Encryption: Used to encrypt the AES key, ensuring that only the attacker can decrypt the AES key and subsequently decrypt the files.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Ryuk created a registry entry under the Run key using Windowscmd.exeshell.

   ID: 030

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: BOOT OR LOGON AUOSTART EXECUTION (T1547)

   SUB-TECHNIQUE: REGISTRY RUN KEYS/STARTUP FOLDER (T1547.001)

   DESCRIPTION: This technique is used by Ryuk to ensure persistence by modifying the Windows Registry Run key to execute its payload on startup.

   TOOLS: -

   NOTE: -

 * Page #9:
   > Ryuk attempts to adjust its token privileges to have theSeDebugPrivilege

   ID: 031

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: ACCESS TOKEN MANIPULATION (T1134)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ryuk attempts to adjust token privileges to gain necessary permissions for process manipulation.

   TOOLS: -

   NOTE: -

   LINK: 032

 * Page #9:
   > Ryuk also callsCreateToolhelp32Snapshotto enumerate all running processes.

   ID: 032

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ryuk uses process enumeration to identify suitable targets for code injection.

   TOOLS: -

   NOTE: -

   LINK: 031, 033

 * Page #9:
   > Ryuk will inject itself into this single process

   ID: 033

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ryuk uses process injection methods to execute code within the context of a target process.

   TOOLS: -

   NOTE: -

   LINK: 032

 * Page #11:
   > The final set of commands deletes files based on their extension or folder locations

   ID: 034

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: This tactic is used to destroy files

   TOOLS: -

   NOTE: -
