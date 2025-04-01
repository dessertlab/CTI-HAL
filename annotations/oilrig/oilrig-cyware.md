## Detailed comments

 * Page #5:
   > Microsoft Excel macros

   ID: 001

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: MALICIOUS FILE (T1203.002)

   DESCRIPTION: Attackers embed malicious macros within Microsoft Excel files. When a victim enables macro

   TOOLS: -

   NOTE: -

 * Page #5:
   > PowerShell-based exploits

   ID: 002

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: Attackers use PowerShell to execute malicious scripts

   TOOLS: -

   NOTE: -

 * Page #5:
   > They use phishing emails to deliver weaponized Microsoft Excel documents

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION:  The adversaries use phishing emails to deliver weaponized Microsoft Excel documents

   TOOLS: -

   NOTE: -

   LINK: 004, 005

 * Page #5:
   > VisualBasic

   ID: 004

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: VISUAL BASIC (T1059.005)

   DESCRIPTION: Once the Excel document is opened and the macros are enabled, Visual Basic for Applications (VBA) scripts can be executed.

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #5:
   > PowerShell

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.001)

   DESCRIPTION: PowerShell scripts are often used due to their powerful capabilities and deep integration with Windows

   TOOLS: -

   NOTE: -

   LINK: 003

 * Page #5:
   > phishing emails that included weaponized Microsoft Excel attachments

   ID: 006

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION:  The adversaries use phishing emails to deliver weaponized Microsoft Excel documents

   TOOLS: -

   NOTE: -

 * Page #6:
   > Oxford websites to deliver malware to the victims

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION:  The adversaries create and host fake websites that mimic legitimate services, such as a Juniper Networks VPN portal or University of Oxford websites. 

   TOOLS: -

   NOTE: -

   LINK: 008

 * Page #6:
   > The group registered four domain names belonging to Oxford University

   ID: 008

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: DOMAINS (T1583.001)

   DESCRIPTION: The group registers domain names similar to those of legitimate organizations (like Oxford University) to lend authenticity to their fake sites.

   TOOLS: -

   NOTE: -

   LINK: 007

 * Page #6:
   > They exploited CVE-2017-0199 remote code execution vulnerability in the Windows Object Linking and Embedding (OLE) application programming interface

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attackers exploit the CVE-2017-0199 vulnerability, which allows remote code execution due to improper handling of objects in memory by the Windows Object Linking and Embedding (OLE) API.

   TOOLS: -

   NOTE: -

 * Page #6:
   > The links between TwoFace and five other web shells were found, including RunningBee, PuTTY Link (plink)

   ID: 010

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: SERVER SOFTWARE COMPONENT (T1505)

   SUB-TECHNIQUE: WEB SHELL (T1505.003)

   DESCRIPTION: The use of web shells such as TwoFace, RunningBee, and RGDoor suggests the attackers implanted malicious scripts on compromised web servers to gain persistent access. 

   TOOLS:  TWO-FACE, RUNNINGBEE, PUTTY, RGDOOR

   NOTE: -

 * Page #7:
   > "Agent Injector" (Trojan with the specific purpose of installing the ISMAgent backdoor)

   ID: 011

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The "Agent Injector" Trojan was used to install the ISMAgent backdoor. This indicates that once the email attachment was executed by the victim, the Trojan initiated the installation of additional malicious payloads.

   TOOLS: -

   NOTE: -

   LINK: 012

 * Page #7:
   > The attack used a spearphishing spam email that had a subject of 'Importan Issue'

   ID: 012

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attackers used spearphishing emails with the subject "Important Issue" to deliver the "Agent Injector" Trojan.

   TOOLS: -

   NOTE: -

   LINK: 011

 * Page #7:
   > The group was also found to be using CVE-2017- 11882

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: EXPLOITATION FOR CLIENT EXECUTION (T1203)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attackers exploited CVE-2017-11882, a vulnerability in Microsoft Office's Equation Editor component. This vulnerability allows for remote code execution when a specially crafted document is opened.

   TOOLS: -

   NOTE: -

 * Page #7:
   > They tried to deliver a new Trojan called OopsIE, via using a variant of the ThreeDollars delivery document

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The emails included a variant of the "ThreeDollars" delivery document, which is used to deliver the "OopsIE" Trojan.

   TOOLS: -

   NOTE: -

   LINK: 015

 * Page #7:
   > They sent two emails to two separate email addresses within the same organization

   ID: 015

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attackers used spearphishing emails, sending them to two separate email addresses within the same organization.

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #8:
   > they launched multiple attacks using spearphishing email (having attached PhpSpy and QuadAgent backdoor) to target an unnamed technology services provider, the Lebanese intelligence agency, and healthcare facilities in Saudi Arabia.

   ID: 016

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The attackers used spearphishing emails with malicious attachments to deliver malware to the target organizations.

   TOOLS: -

   NOTE: -

 * Page #9:
   > The malware was delivered via an Excel document

   ID: 017

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: The malware is delivered through an Excel document with malicious macros.

   TOOLS: -

   NOTE: -

 * Page #9:
   > They also created a new remote administration tool that supported HTTP and DNS communication

   ID: 018

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: The RAT communicates over HTTP, allowing it to send and receive commands or exfiltrate data through standard web traffic.

   TOOLS: -

   NOTE: -

   ---

   ID: 019

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: DNS (T1071.004)

   DESCRIPTION: The RAT also uses DNS for communication, which can help evade detection by blending with regular DNS traffic.

   TOOLS: -

   NOTE: -

   ---

   ID: 022

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: ENCRYPTED CHANNEL (T1573)

   SUB-TECHNIQUE: -

   DESCRIPTION: Created remote administration tools supporting HTTP and DNS communication with potential encryption.

   TOOLS: -

   NOTE: -

 * Page #9:
   > a phishing campaign was observed asking victims to join their social network. This time the group masqueraded as a Cambridge University lecturer, also setting up a LinkedIn page in order to gain victims' trust.

   ID: 020

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: he attackers impersonate a Cambridge University lecturer and use social networks like LinkedIn to gain the victims' trust.

   TOOLS: -

   NOTE: -

   LINK: 021

 * Page #9:
   > From there they asked victims to open malicious documents.

   ID: 021

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: Open a malicious document

   TOOLS: -

   NOTE: -

   LINK: 020

 * Page #10:
   > Twoface - A web shell, which is used to harvest credentials

   ID: 023

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005), PERSISTENCE (TA0003), PRIVILEGE ESCALATION (TA0004), INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Used tools like Twoface for credential harvesting from local system accounts.

   TOOLS: Twoface

   NOTE: -

 * Page #10:
   > Pickpocket - It is a browser credentialtheft tool.

   ID: 024

   SOURCE: TEXT

   TACTIC: RECONNAISSANCE (TA0043)

   TECHNIQUE: GATHER VICTIM IDENTITY INFORMATION (T1589)

   SUB-TECHNIQUE: CREDENTIALS (T1589.001)

   DESCRIPTION: Adversaries may gather credentials that can be used during targeting.

   TOOLS: Pickpocket

   NOTE: -

