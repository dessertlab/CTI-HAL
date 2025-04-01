## Detailed comments

 * Page #2:
   > The a!empts involved a phishing email appearing to be from the U.S. Depa"ment of State with links to zip #les

   ID: 001

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Phishing emails that contain links to malicious zipper files.

   TOOLS: -

   NOTE: -

   LINK: 002

 * Page #2:
   > containing malicious Windows sho"cuts that delivered Cobalt Strike Beacon.

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Malicious zipper files disguised as legitimate Windows shortcuts.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 001

 * Page #2:
   > The a!acker appears to have compromised the email server of a hospital and the corporate website of a consulting company

   ID: 019

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: -

   DESCRIPTION: The attacker appears to have compromised the email server of a hospital and the corporate website of a consulting company in order to use their infrastructure to send phishing emails.

   TOOLS: -

   NOTE: -

 * Page #3:
   > The a!acker used unique links in each phishing email

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Phishing emails that contain links to malicious zipper files.

   TOOLS: -

   NOTE: -

   LINK: 004

 * Page #3:
   > the links that FireEye observed were used to download a ZIP archive that contained a weaponized Windows sho"cut #le, launching both a benign decoy document and a Cobalt Strike Beacon backdoor, customized by the a!acker to blend in with legitimate network tra%c.

   ID: 004

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Malicious zipper files disguised as legitimate Windows shortcuts.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 003

 * Page #5:
   > The threat actor cra&ed the phishing emails to masquerade as a U.S. Depa"ment of State Public A$airs o%cial sharing an o%cial document

   ID: 005

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Phishing emails that contain links to malicious zipper files.

   TOOLS: -

   NOTE: -

   LINK: 006

 * Page #5:
   > The links led to a ZIP archive that contained a weaponized Windows sho"cut #le hosted on a likely compromised legitimate domain, jmj[.].com.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Malicious zipper files disguised as legitimate Windows shortcuts.

   TOOLS: -

   NOTE: -

   LINK: 005, 007

 * Page #6:
   > execute a PowerShell command that read, decoded, and executed additional code from within the sho"cut #le.

   ID: 007

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The use of a malicious shortcut file to execute the code.

   TOOLS: -

   NOTE: -

   LINK: 006, 008

   ---

   ID: 008

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.002)

   DESCRIPTION: The use of a PowerShell command to execute additional code.

   TOOLS: -

   NOTE: -

   LINK: 007, 009

 * Page #6:
   > the sho"cut #le dropped a benign, publicly available, U.S. Depa"ment of State form and Cobalt Strike Beacon

   ID: 009

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malicious shortcut file drops a seemingly innocuous U.S. State Department form to confuse and distract the user.

   TOOLS: COBALT STRIKE (S0154)

   NOTE: -

   LINK: 010

 * Page #6:
   > The BEACON payload was con#gured with a modi#ed variation of the publicly available "Pandora" Malleable C2 Pro#le and used a command and control (C2) domain – pandorasong[.]com – assessed to be a masquerade of the Pandora music streaming service.

   ID: 010

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Use of a C2 domain that mimics a legitimate service, in this case Pandora music streaming service.

   TOOLS: -

   NOTE: -

   LINK: 009

 * Page #9:
   > Each phishing email contained a unique malicious URL

   ID: 011

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Sending phishing emails containing malicious URLs.

   TOOLS: -

   NOTE: -

 * Page #10:
   > two variants

   ID: 012

   LINK: T01 OR T02

 * Page #10:
   > The #rst variant

   ID: T01

   LINK: 012, 013, 014, 015

 * Page #10:
   > ds7002.lnk was a malicious sho"cut (LNK) #le that contained an embedded BEACON DLL and decoy PD

   ID: 012

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malicious shortcut file (LNK) is disguised as a legitimate file

   TOOLS: -

   NOTE: -

   LINK: 013

 * Page #10:
   > to launch a PowerShell command

   ID: 013

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: POWERSHELL (T1059.002)

   DESCRIPTION: Using a PowerShell command launched from the shortcut file (LNK).

   TOOLS: -

   NOTE: -

   LINK: 012, 014

 * Page #10:
   > the PowerShell command extracted and executed the Cobalt Strike BEACON backdoor and decoy PDF

   ID: 015

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: The malicious shortcut file (LNK) is disguised as a legitimate file

   TOOLS: -

   NOTE: -

   LINK: 014

 * Page #10:
   > On execution

   ID: 014

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: The malicious shortcut file (LNK) is executed by the user.

   TOOLS: -

   NOTE: -

   LINK: 015

 * Page #10:
   > The other observed variant

   ID: T02

   LINK:

 * Page #13:
   > This command included some speci#c obfuscation, which may indicate a!empts to bypass speci#c detection logic.

   ID: 016

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique includes the use of obfuscation techniques to hide the malicious behavior of the malware. In the context described, the command included a specific type of obfuscation that may have been used to evade detection.

   TOOLS: -

   NOTE: -

 * Page #14:
   > The PowerShell loader code is obfuscated

   ID: 017

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: This technique is applied when executable files or data are made less readable to avoid detection by security tools

   TOOLS: -

   NOTE: -

 * Page #16:
   > The dropped BEACON loader DLL was executed by RunDll32.exe using the expo" function "PointFunctionCall

   ID: 018

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: SIGNED BINARY PROXY EXECUTION (T1218)

   SUB-TECHNIQUE: RUNDLL32 (T1218.011)

   DESCRIPTION: rubdll32.exe was used

   TOOLS: -

   NOTE: -

