## Detailed comments

 * Page #3:
   > MiniDuke, CosmicDuke, OnionDuke, CozyDuke, CloudDuke, SeaDuke, HammerDuke, PinchDuke, and GeminiDuke

   ID: 000

   TOOLS: MINIDUKE (S0051), COSMICDUKE (S0050), ONION DUKE (S0052), COZYDUKE (S0046), CLOUDDUKE (S0054), SEADUKE (S0053), HAMMERDUKE (S0037), PINCHDUKE (S0048), GEMINIDUKE (S0049)

 * Page #6:
   > specially-crafted malicious Microsoft Word documents and PDF files, which were sent as e-mail attachments to various personnel in an attempt to infiltrate the targeted organizations

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: ATTACHMENT (T1566.001)

   DESCRIPTION: Using specially crafted Microsoft Word documents and PDFs as malicious e-mail attachments to infiltrate target organizations.

   TOOLS: -

   NOTE: -

 * Page #7:
   > CosmicDuke would write to disk and execute PinchDuke

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SYSTEM SERVICES (T1569)

   SUB-TECHNIQUE: SERVICE EXECUTION (T1569.002)

   DESCRIPTION: Creation and writing of a malicious executable to disk and its subsequent execution.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTE: -

 * Page #7:
   > data exfiltration and communication with a command and control (C&C) server

   ID: 004

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Exfiltration of data through a command-and-control (C&C) channel.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTE: -

 * Page #7:
   > separate information gathering

   ID: 003

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of information on the compromised system.

   TOOLS: COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTE: -

 * Page #8:
   > MiniDuke is centered on a simplistic backdoor component whose purpose is to enable the remote execution of commands on the compromised system

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Executing remote commands on the compromised machine.

   NOTE: -

   TOOLS: MINIDUKE (S0051)

 * Page #11:
   > the MiniDuke campaigns from February 2013 employed spear-phishing emails with malicious PDF file attachments

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: ATTACHMENT (T1566.001)

   DESCRIPTION: Use of spearphishing attachments to deliver malware.

   TOOLS: MINIDUKE (S0051)

   NOTE: -

 * Page #12:
   > password stealing, information gathering

   ID: 006

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIAL DUMPING (T1003)

   SUB-TECHNIQUE: - 

   DESCRIPTION: Collection of credentials through various techniques.

   TOOLS: ONIONDUKE (S0052)

   NOTE: -

 * Page #12:
   > denial of service (DoS) attacks

   ID: 007

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: ENDPOINT DENIAL OF SERVICE (T1499)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of DoS attacks to compromise or limit the availability of systems.

   TOOLS: ONIONDUKE (S0052)

   NOTE: -

 * Page #15:
   > CozyDuke campaigns, began with spear-phishing emails that tried to impersonate commonly seen spam emails. These spear-phishing emails would contain links that eventually lead the victim to becoming infected with CozyDuke

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Use of links in spearphishing emails to induce victims to visit compromised websites or download malware.

   TOOLS: COZY (S0046)

   NOTE: -

 * Page #15:
   > the email instead contained a link to a zip-archive file named "Office Monkeys LOL Video.zip", which was hosted on the DropBox cloud storage service

   ID: 009

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Using a spearphishing email containing a link to a zipper file hosted on a cloud storage service (DropBox).

   TOOLS: CLOUDDUKE (S0054)

   NOTE: -

 * Page #16:
   > They noted that this node appeared to be maliciously modifying any executables

   ID: 010

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: COMPROMISE INFRASTRUCTURE (T1584)

   SUB-TECHNIQUE: -

   DESCRIPTION: the compromised Tor node modifies executables downloaded over an HTTP connection to introduce malware or other malicious coding.

   TOOLS: -

   NOTE: -

   LINK: 011, 012

 * Page #16:
   > Executing the modified applications obtained this way would result in the victim being infected with unidentified malware.

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Modified executables are executed by victims, resulting in the infection.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #16:
   > that were downloaded through it over a HTTP connection.

   ID: 011

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Using HTTP connections to download executables.

   TOOLS: -

   NOTE: -

   LINK: 010

 * Page #18:
   > one of these modules gathers system information and another attempts to steal the victim's usernames and passwords

   ID: 013

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM OWNER/USER DISCOVERY (T1033)

   SUB-TECHNIQUE: -

   DESCRIPTION: One of the capabilities of OnionDuke is to collect system information and attempt to steal usernames and passwords of victims.

   TOOLS: ONIONDUKE (S0052)

   NOTE: -

 * Page #18:
   > the other two known OnionDuke modules are quite the opposite; one is designed for use in DoS attacks

   ID: 013

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: NETWORK DENIAL OF SERVICE (T1498)

   SUB-TECHNIQUE: -

   DESCRIPTION: One of OnionDuke's modules is designed to perform Denial of Service (DoS) attacks.

   TOOLS: ONIONDUKE (S0052)

   NOTE: -

 * Page #18:
   > thousands of recipients being sent spear-phishing emails that contained links to compromised websites hosting CozyDuke

   ID: 014

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: 'sending spear-phishing e-mails containing malicious links leading victims to a compromised Web site hosting cozyduke.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

 * Page #19:
   > SeaDuke

   ID: 015

   TOOLS: SEADUKE (S0053)

   NOTE: it was written in Python and designed to work on both Windows and Linux systems

 * Page #19:
   > HammerDuke

   ID: 016

   TOOLS: HAMMERDUKE (S0037)

   NOTE: it is a windows-only malware (written in .NET) and comes in two variants

   LINK: 017, 018

 * Page #19:
   > The simpler one will connect to a hardcoded C&C server over HTTP or HTTPS to download commands to execute

   ID: 017

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: WEB SERVICE (T1102)

   SUB-TECHNIQUE: -

   DESCRIPTION: communication with a command and control (C&C) server via HTTP or HTTPS to download commands for execution.

   TOOLS: HAMMERDUKE (S0037)

   NOTE: simpler variant

   LINK: 016

 * Page #19:
   > The more advanced variant, on the other hand, will use an algorithm to generate a periodically-changing Twitter account name and will then attempt to find tweets from that account containing links to the actual download location of the commands to execute.

   ID: 018

   TOOLS: HAMMERDUKE (S0037)

   NOTE: use o twitter to find tweet containing links to the actual download location of the commands to execute

   LINK: 016

 * Page #20:
   > Both backdoors (internally referred to by their authors as "BastionSolution" and "OneDriveSolution") essentially allow the operator to remotely execute commands on the compromised machine

   ID: 019

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using remote services to execute commands on compromised machines.

   TOOLS: CLOUDDUKE (S0054)

   NOTE: -

 * Page #22:
   > The PinchDuke toolset consists of multiple loaders and a core information stealer trojan

   ID: 020

   TOOLS: PINCHDUKE (S0048)

   LINK: 021, 022, 023, 024

 * Page #22:
   > The PinchDuke information stealer gathers system configuration information, steals user credentials, and collects user files from the compromised host transferring these via HTTP(S) to a C&C server

   ID: 021

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Data collection activity by an attacker from a local system. 

   TOOLS: PINCHDUKE (S0048)

   NOTE: -

   LINK: 020,022,023

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER COMMAND AND CONTROL CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Using C&C (Command and Control) channels to exfiltrate stolen data from the compromised system.

   TOOLS: PINCHDUKE (S0048)

   NOTE: -

   LINK: 020,021

   ---

   ID: 023

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Use of web protocols (HTTP/HTTPS) for communication with the C&C server and transfer of exfiltrated data.

   TOOLS: PINCHDUKE (S0048)

   NOTE: -

   LINK: 020,021

 * Page #23:
   > PinchDuke will also search for files that have been created within a predefined timeframe and whose file extension is present in a predefined list

   ID: 024

   SOURCE: TEXT

   TACTIC: COLLECITON (TA0009)

   TECHNIQUE: DATA FROM LOCAL (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of data from the local system, as files created within a given period and with specific extensions.

   TOOLS: PINCHDUKE (S0048)

   NOTE: -

 * Page #23:
   > The GeminiDuke toolset consists of a core information stealer, a loader and multiple persistencerelated components

   ID: 025

   TOOLS: GEMINIDUKE (S0049)

   LINK: 026

 * Page #23:
   > GeminiDuke primarily collects information on the victim computer's configuration

   ID: 026

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DISCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: collection of system information about the configuration of the victim computer.

   TOOLS: GEMINIDUKE (S0049)

   NOTE: -

   LINK: 025

 * Page #25:
   > The CosmicDuke toolset is designed around a main information stealer component

   ID: 027

   TOOLS: COSMICDUKE (S0050)

   LINK: 028, 029, 030, 031, 032, 033, 034

 * Page #25:
   > Keylogging

   ID: 028

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: INPUT CAPTURE (T1056)

   SUB-TECHNIQUE: -

   DESCRIPTION: Keylogging, which is the capture of user input data

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #25:
   > Taking screenshots

   ID: 029

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: Capturing screenshots of the desktop or specific windows.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #25:
   > Stealing clipboard contents

   ID: 030

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: CLIPBOARD DATA (T1115)

   SUB-TECHNIQUE: -

   DESCRIPTION: Theft of the contents of the system clipboard.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #25:
   > Stealing user files with file extensions that match a predefined list

   ID: 031

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Collection of data from the local system, including user files with specific extensions.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #25:
   > Collecting user credentials, including passwords, for a variety of popular chat and email programs as well as from web browsers

   ID: 032

   SOURCE: TEXT

   TACTIC: CREDENTIAL ACCESS (TA0006)

   TECHNIQUE: CREDENTIALS FROM PASSWORD STORES (T1555)

   SUB-TECHNIQUE: CREDENTIALS FROM WEB BROWSERS (T1555.003)

   DESCRIPTION: Theft of credentials stored in web browsers.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #25:
   > CosmicDuke may use HTTP, HTTPS, FTP or WebDav to exfiltrate the collected data to a hardcoded C&C server

   ID: 033

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER ALTERNATIVE PROTOCOL (T1048)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of protocols other than the standard communication protocol to exfiltrate stolen data, such as HTTP, HTTPS, FTP, or WebDav

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

   ---

   ID: 034

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER COMMAND AND CONTROL CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of a command and control channel to exfiltrate collected data to a C&C server.

   TOOLS: COSMICDUKE (S0050)

   NOTE: -

   LINK: 027

 * Page #27:
   > The MiniDuke toolset consists of multiple downloader and backdoor components

   ID: 035

   TOOLS: MINIDUKE (S0051)

   LINK: 036

 * Page #27:
   > it has also commonly been used in conjunction with CosmicDuke and PinchDuke

   ID: 036

   TOOLS: MINIDUKE (S0051), COSMICDUKE (S0050), PINCHDUKE (S0048)

   NOTE: MiniDuke has been used in conjuction with the other two

   LINK: 035

 * Page #28:
   > CozyDuke

   ID: 037

   TOOLS: COZYDUKE (S0046)

   LINK: 038, 039, 040, 041

 * Page #28:
   > Command execution module for executing arbitrary Windows Command Prompt commands

   ID: 038

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Execution of arbitrary commands through the Windows Command Prompt or other script interpreters.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 037

 * Page #28:
   > System information gathering module

   ID: 038

   SOURCE: TEXT

   TACTIC: DISCOVERY (TA0007)

   TECHNIQUE: SYSTEM INFORMATION DOSCOVERY (T1082)

   SUB-TECHNIQUE: -

   DESCRIPTION: system information gathering, which could be exploited by the system information gathering module to gather details about the compromised system.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 037

 * Page #28:
   > Screenshot module

   ID: 040

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: SCREEN CAPTURE (T1113)

   SUB-TECHNIQUE: -

   DESCRIPTION: capture of screenshots of the desktop or specific windows, used by the screenshot module to collect visual information from the system.

   TOOLS: COZYDUKE (S0046)

   NOTE: -

   LINK: 037

 * Page #28:
   > these executables were self-extracting archive files containing common hacking tools, such as PSExec and Mimikatz, combined with script files that execute these tools.

   ID: 041

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: use of scripts to perform specific actions, such as executing hacking tools via script files included in self-extracting archives

   TOOLS: COZYDUKE (S0046), PSEXEC (S0029), MIMIKATZ (S0002)

   NOTE: -

   LINK: 037

 * Page #29:
   > The OnionDuke toolset includes at least a dropper, a loader, an information stealer trojan and multiple modular variants with associated modules

   ID: 041

   TOOLS: ONIONDUKE (S0052)

   LINK: 042, 043

 * Page #29:
   > The Tor node would intercept any unencrypted executable files being downloaded and modify those executables by adding a malicious wrapper contained an embedded OnionDuke

   ID: 042

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of techniques to mask the activity or malicious nature of the software. In the specific case of OnionDuke, the malicious wrapper added to executable files could be considered a form of masking to avoid detection

   TOOLS: ONIONDUKE (S0052)

   NOTE: -

   LINK: 041, 043

 * Page #29:
   > Once the victim finished downloading the file and executed it, the wrapper would infect the victim's computer with OnionDuke before executing the original legitimate executable.

   ID: 043

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: -

   DESCRIPTION: persuasion of the user to run a malicious file, which in the case of OnionDuke occurs when the user runs the modified file containing the malicious wrapper.

   TOOLS:  ONIONDUKE (S0052)

   NOTE: -

   LINK: 041, 042

 * Page #30:
   > SeaDuke is a simple backdoor that focuses on executing commands retrieved from its C&C server, such as uploading and downloading files, executing system commands and evaluating additional Python code

   ID: 044

   TOOLS: SEADUKE (S0053)

   NOTE: it is written in python and designed to be cross-platform, so that it works on both windows and linux

 * Page #31:
   > HammerDuke is a simple backdoor that is apparently designed for similar use cases as SeaDuke

   ID: 045

   TOOLS: HAMMERDUKE (S0037)

   NOTE: it is written in .NET

 * Page #32:
   > CloudDuke is a malware toolset known to consist of, at least, a downloader, a loader and two backdoor variants

   ID: 046

   TOOLS: CLOUDDUKE (S0054)

