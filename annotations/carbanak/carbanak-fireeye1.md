## Detailed comments

 * Page #1:
   > CARBANAK is a full-featured backdoor with data-stealing capabilities and a plugin architecture

   ID: 001

   TOOLS: CARBANAK (S0030)

   LINK: 002, 003, 004, 005, 006, 007, 008, 009

 * Page #1:
   > key logging

   ID: 002

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Capturing keystrokes to gather sensitive information 

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > desktop video capture

   ID: 003

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capturing screenshots of the victim's desktop to monitor user activity.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > #le system management

   ID: 005

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: FILE AND DIRECTORY DISCOVERY (T1083)

   SUB-TECHNIQUE: -

   DESCRIPTION: Managing and navigating the file system to locate files of interest.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #1:
   > VNC

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using tools like VNC to remotely control the victim's machine.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > OS destruction

   ID: 008

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Destroying data on the victim's system to disrupt operations or cover tracks.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > #le transfer

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Transferring files to or from a compromised system.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > TCP tunneling

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: PROTOCOL TUNNELING (T1572)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using techniques like TCP tunneling to encapsulate traffic and avoid detection.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #1:
   > POS and Outlook data the$

   ID: 009

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Stealing data from point-of-sale (POS) systems and Outlook.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 001

 * Page #2:
   > Key logger

   ID: 010

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: KEYLOGGING (T1056.001)

   DESCRIPTION: Logs key strokes for con#gured processes and sends them to the command and control (C2) server

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #2:
   > The command and parameter names are hashed before being compared by the binary, making it di'cult to recover the original names of commands and parameters

   ID: 011

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: The commands and parameter names are hashed before being compared by the binary, making it difficult to recover the original names of commands and parameters.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #3:
   > Desktop video recording

   ID: 012

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capturing screenshots of the victim's desktop to monitor user activity.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #3:
   > Downloads executable

   ID: 013

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The act of downloading an executable aligns with this technique, which covers the transfer of tools or files into a victim's environment.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 014

 * Page #3:
   > injects into new process

   ID: 014

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0006)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: The technique of injecting code into a new process is directly described by "injects into new process".

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 013

 * Page #3:
   > Ammyy Admin tool

   ID: 015

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Ammyy Admin is a legitimate remote access tool often abused by attackers to gain remote control of victim systems.

   TOOLS: CARBANAK (S0030), AMMYY

   NOTE: -

 * Page #3:
   > Renders computer unbootable by wiping the MBR

   ID: 016

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DISK WIPE (T1561)

   SUB-TECHNIQUE: DISK STRUCTURE WIPE (T1561.002)

   DESCRIPTION: This involves the destruction of data structures, such as the MBR, to prevent the operating system from booting. This technique aims to render the system unusable.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #4:
   > Creates

   ID: 017

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE ACCOUNT (T1136)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create user accounts to establish persistence, elevate privileges, or facilitate other malicious activities.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #4:
   > deletes Windows user account

   ID: 018

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ACCOUNT ACCESS REMOVAL (T1531)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may remove accounts to limit access to the system or to deny access to specific users, which can include deleting user accounts.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #4:
   > Deletes #le or service

   ID: 019

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: INDICATOR REMOVAL ON HOST (T1070)

   SUB-TECHNIQUE: FILE DELETION (T1070.004)

   DESCRIPTION: Adversaries may delete files to remove artifacts and other traces of their presence from the host to avoid detection.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #4:
   > Downloads executable

   ID: 020

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: The act of downloading an executable aligns with this technique, which covers the transfer of tools or files into a victim's environment.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 021

 * Page #4:
   > injects directly into new process

   ID: 021

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PRIVILEGE ESCALATION (TA0006)

   TECHNIQUE: PROCESS INJECTION (T1055)

   SUB-TECHNIQUE: -

   DESCRIPTION: The technique of injecting code into a new process is directly described by "injects into new process".

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 020

 * Page #4:
   > the desktop Takes a screenshot of

   ID: 022

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE:

   DESCRIPTION: Adversaries may use utilities to capture screenshots of the victim's desktop to gather information about the environment and operations on the victim's system.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 023

 * Page #4:
   > sends it to the C2 server

   ID: 023

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICTION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Sending data to the C2 server could utilize common web protocols to communicate, making the traffic blend in with legitimate web traffic.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 022

 * Page #4:
   > Runs VNC plugin

   ID: 024

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: REMOTE ACCESS SOFTWARE (T1219)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using tools like VNC to remotely control the victim's machine.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #5:
   > processes to the C2 Returns list of running server

   ID: 025

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: PROCESS DISCOVERY (T1057)

   SUB-TECHNIQUE: -

   DESCRIPTION: monitoring and collecting information about the processes running on a system.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #5:
   > Download and execute shellcode from speci#ed address

   ID: 026

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Downloading and executing shellcode from a specific address

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #6:
   > CARBANAK communicates to its C2 servers

   ID: 034

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: The CARBANAK backdoor communicates with its command and control servers to exfiltrate stolen data

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #6:
   > Messages are encrypted using Microso$'s implementation of RC2 in CBC mode with PKCS#5 padding

   ID: 027

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA ENCRYPTED (T1486)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of RC2 in CBC mode with PKCS#5 padding to encrypt messages.

   TOOLS: -

   NOTE: -

   LINK: 028

 * Page #6:
   > The encrypted message is then Base64 encoded

   ID: 028

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: DATA ENCODING (T1132)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of Base64 encoding to represent encrypted data

   TOOLS: -

   NOTE: -

   LINK: 027, 029

 * Page #6:
   > replacing all the '/' and '+' characters

   ID: 029

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of Base64 encoding to replace specific characters ('/' and '+') with others ('.' and '-')

   TOOLS: -

   NOTE: with '.' and '-'

   LINK: 028

 * Page #7:
   > The encoded payload is then made to look like a URI by having a random number of '/' characters inse%ed at random locations within the encoded payload

   ID: 030

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Described when the encoded payload is made to resemble a URI by inserting a random number of '/' characters in random locations. This is used to disguise the payload as a normal URI.

   TOOLS: -

   NOTE: with '.' and '-'

   LINK: 031

 * Page #7:
   > The malware then appends a script extension (php, bml, or cgi) with a random number of random parameters or a #le extension from the following list with no parameters: gif, jpg, png, htm, html, php

   ID: 031

   SOURCE: TEX

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Described when the malware adds a script extension (php, bml or cgi) with a random number of random parameters or a file extension (gif, jpg, png, htm, html, php) with no parameters. 

   TOOLS: -

   NOTE: This helps the malware camouflage itself as a legitimate file or another type of file that can be run or opened.

   LINK: 030

 * Page #8:
   > A 256-bit AES session key is generated and used to encrypt both message headers and bodies separately

   ID: 035

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: ASYMMETRIC CRYPTOGRAPHIC (T1573.002)

   DESCRIPTION: The CARBANAK backdoor's custom binary protocol uses RSA for the initial key exchange and AES for subsequent message encryption, providing an encrypted communication channel

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 036

 * Page #8:
   > All subsequent messages are encrypted with AES in CBC mode

   ID: 036

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: ASYMMETRIC CRYPTOGRAPHIC (T1573.002)

   DESCRIPTION: "The CARBANAK backdoor's custom binary protocol uses AES in CBC mode to encrypt message headers and bodies, providing an encrypted communication channel.

   TOOLS: CARBANAK (S0030)

   NOTE: -

   LINK: 035

 * Page #9:
   > the backdoor was embedded as a packed payload in another executable or in a weaponized document #le of some kind

   ID: 037

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.001)

   DESCRIPTION: CARBANAK has been delivered via weaponized document files and packed payloads in other executables, which can involve user execution of malicious files

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #9:
   > CARBANAK's strings are encrypted in order to make analysis more di'cult

   ID: 032

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique involves making analysis more difficult by encoding or encrypting data and/or commands. It can be used to protect strings, file names, command-and-control (C2) server addresses, and other variables used by the malware.

   TOOLS: CARBANAK (S0030)

   NOTE: -

 * Page #13:
   > the use of Power Admin PAExec for lateral movement

   ID: 033

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: use of PAExec

   TOOLS: -

   NOTE: -

