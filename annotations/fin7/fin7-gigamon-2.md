## Detailed comments

 * Page #2:
   > FIN7 would gain access to the POS environment primarily using PSExec

   ID: 001

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: FIN7 used PSExec, a legitimate remote administration tool from Sysinternals, to execute processes on the POS systems remotely, which is part of their lateral movement strategy to spread malware across a network.

   TOOLS: PSEXEC (S0029)

   NOTE: -

   LINK: 002

 * Page #2:
   > combined with a custom PowerShell script to deploy their payload.

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: A custom PowerShell script is used to execute and manage payload delivery, showcasing the use of PowerShell as an execution platform. PowerShell scripts are commonly abused by attackers to execute arbitrary code and evade detection due to their presence in most Windows environments.

   TOOLS: -

   NOTE: -

   LINK: 001, 003

 * Page #2:
   > The weaponized PowerShell script was built to load an embedded DLL using reflective injection

   ID: 003

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: REFLECTIVE CODE LOADING (T1620)

   SUB-TECHNIQUE: -

   DESCRIPTION: eflective DLL injection is a technique where a DLL is injected into a process without touching disk, which helps evade traditional security controls.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #3:
   > the script executed code from PowerSploit designed to resolve Windows API functions necessary for performing the injection

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of Windows API functions to perform the injection, manage memory, and create threads is a critical aspect of reflective DLL injection. By directly accessing low-level system calls, FIN7 ensures the payload remains hidden in memory.

   TOOLS: -

   NOTE: -

   LINK: 005

 * Page #3:
   > the script would allocate memory in its current process and use the System.Runtime.Interopservices.Marshal class to copy code into the newly allocated memory

   ID: 005

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DYNAMIC-LINK LIBRARY (T1055.001)

   DESCRIPTION: Creating a thread to execute the bootstrap code for loading a DLL is an example of process injection. This technique is used to inject malicious code into another process's address space, which helps evade detection by running malicious code within a legitimate process.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #3:
   > Once injected, the payload proceeded to write a binary encoded blob into the registry key HKLM\Software\Microsoft\DRM

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves modifying the Windows Registry to store malicious data or configurations. FIN7 uses this method to write a binary blob into the registry, which is later accessed and executed as part of their payload, making it harder to detect or remove since the data isn't stored on disk.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #3:
   > install persistence using a custom Shim targeting services.exe and adding it to the shim database by executing sdbinst.exe

   ID: 007

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: EVENT TRIGGERED EXECUTION (T1546)

   SUB-TECHNIQUE: APPLICAITON SHIMMING (T1546.011)

   DESCRIPTION: Application Shimming is a technique that involves modifying how applications are executed on the system by creating a custom compatibility shim. In this case, FIN7 creates a shim for services.exe to ensure the malicious payload is executed whenever the service starts, achieving persistence. This is done by adding the shim to the shim database using the sdbinst.exe tool.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #5:
   > the POS scraping capability will attempt to inject Library/Webinar-H Platform.html) Utm_source=Giga Service Providers itself into svchost.exe, wuauclt.exe or explorer.exe (in that order) Links&Utm_conte (Https://Www.gig

   ID: 008

   SOURCE: TEXT

   TACTIC:

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: DYNAMIC-LINK LIBRARY (T1055.001)

   DESCRIPTION: Injecting malicious code into the memory of legitimate processes such as svchost.exe, wuauclt.exe, and explorer.exe. 

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #5:
   > Upon successful injection, the scraper enumerates running Provider.htm Product Do (Https://Ww processes, comparing them to a list provided via a text file on (Https://Com Cloud/Gigavu disk

   ID: 009

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: This describes enumerating running processes on the infected system, which is a process discovery technique. The malware checks for specific processes to determine which ones it can target for scraping sensitive data.

   TOOLS: -

   NOTE: -

   LINK: 008, 010

 * Page #5:
   > Once the scraping capability has identified a process of interest, OpenStack the payload will read memory from the process and extract track (Https://Www.giga one and track two data formats

   ID: 010

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Memory scraping is a method used to extract sensitive data, such as payment card information, directly from the memory of running processes. The malware specifically targets track one and track two data, which are commonly found in credit card transactions and contain information like account numbers, expiration dates, and service codes.

   TOOLS: -

   NOTE: -

   LINK: 009, 011

 * Page #5:
   > Once extracted, the malware Cloud/Gigavue encrypts the data and writes it to disk for later collection by the VMware threat actors.

   ID: 011

   SOURCE: TEXT 

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: After scraping the sensitive data, the malware encrypts the stolen information before writing it to disk. This ensures that even if the files are discovered by security teams, the data remains unreadable without the decryption key. Obfuscation or encryption is a common tactic to hide stolen data from detection.

   TOOLS: -

   NOTE: -

   LINK: 010

