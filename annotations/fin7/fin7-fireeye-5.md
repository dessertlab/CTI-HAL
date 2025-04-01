## Detailed comments

 * Page #2:
   > The shim injected a malicious in-memory patch into the Services Control Manager ("services.exe") process, and then spawned a CARBANAK backdoor process.

   ID: 006

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), PERSISTENCE (TA0003)

   TECHNIQUE: EVENT TRIGGER EXECUTION (T1546)

   SUB-TECHNIQUE: APPLICATION SHIMMING (T1546.011)

   DESCRIPTION: FIN7 leveraged an application shim database to achieve persistent access on systems in multiple environments.

   TOOLS: -

   NOTE: -

 * Page #4:
   > FIN7 used a custom Base64 encoded PowerShell script, which ran the "sdbinst.exe" utility to register a custom shim database #le containing a patch onto a system.

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell is used to run a utility (sdbinst.exe) to register a shim database file, which is part of the persistence mechanism.

   TOOLS: -

   NOTE: -

 * Page #7:
   > obtained an additional shellcode payload stored in a registry key.

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: the shellcode is stored in a registry key for later retrieval and execution.

   TOOLS: -

   NOTE: -

 * Page #7:
   > The second stage shellcode launched the CARBANAK DLL (stored in a registry key), which spawned an instance of Service Host ("svchost.exe") and injected itself into that process

   ID: 003

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), DEFENSE EVASION (TA0005)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: The CARBANAK DLL is injected into the svchost.exe process, demonstrating the use of process injection techniques.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The new "ScRegisterTCPEndpoint" function (shellcode) contained a reference to the path of "\REGISTRY\MACHINE\SOFTWARE\Microso$\ DRM", which is a registry location where additional malicious shellcode and the CARBANAK DLL payload was stored on the system

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MODIFY REGISTRY (T1112)

   SUB-TECHNIQUE: -

   DESCRIPTION: the ScRegisterTCPEndpoint function references a registry path where malicious shellcode and the CARBANAK DLL are stored.

   TOOLS: -

   NOTE: -

 * Page #8:
   > The shellcode stored within the registry path "HKLM\SOFTWARE\Microso$\DRM" used the API function "RtlDecompressBu%er" to decompress the payload

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: NATIVE API (T1106)

   SUB-TECHNIQUE: -

   DESCRIPTION: The use of RtlDecompressBuffer to handle decompression of the payload indicates leveraging native APIs to perform specific tasks.

   TOOLS: -

   NOTE: -

 * Page #8:
   > Once loaded in memory, it created a new process named "svchost.exe" that contained the CARBANAK DLL.

   ID: 007

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004), PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

