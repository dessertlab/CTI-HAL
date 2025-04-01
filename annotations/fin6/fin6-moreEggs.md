## Detailed comments

 * Page #1:
   > the actor uses a fraudulent, but legitimately created LinkedIn proWle to initiate contact with individuals at the targeted company by sending invitations with a short message (Figure 1). This appears as a benign email

   ID: 001

   SOURCE: TEXT

   TACTIC: RECONNAISSANCE (TA0043)

   TECHNIQUE: GATHER VICTIM IDENTITY INFORMATION (T1589)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may gather information about the victim's identity that can be used during targeting. Information about identities may include a variety of details, including personal data (ex: employee names, email addresses).

   TOOLS: -

   NOTES: -

 * Page #2:
   > often suggests the recipient click on a link

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING LINK (T1566.002)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious link in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #2:
   > this actor used an attached PDF with embedded URLs or other malicious attachments.

   ID: 003

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTES: -

 * Page #3:
   > The landing page initiates a download of a Microsoft Word Wle (Figure 4) with malicious macros

   ID: 004

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Tools or files may be copied from an external adversary-controlled system to the victim network through the command and control channel.

   TOOLS: -

   NOTES: -

 * Page #3:
   > If the recipient enables macros, the "More_eggs" payload will be downloaded and executed.

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: USER EXECUTION (T1204)

   SUB-TECHNIQUE: MALICIOUS FILE (T1204.002)

   DESCRIPTION: An adversary may rely upon a user opening a malicious file in order to gain execution. Users may be subjected to social engineering to get them to open a file that will lead to code execution.

   TOOLS: Taurus Builder, VenomKit

   NOTES: -

 * Page #3:
   > the landing page may initiate the download of a JScript loader instead, but this intermediate malware still ultimately results in the delivery of More_eggs.

   ID: 006

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: JAVASCRIPT (T1059.007)

   DESCRIPTION: Adversaries may abuse various implementations of JavaScript for execution.

   TOOLS: -

   NOTES: -

 * Page #7:
   > its ability to download additional payloads, More_eggs has extensive capabilities to proWle the infected machine

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: INGRESS TOOL TRANSFER (T1105)

   SUB-TECHNIQUE: -

   DESCRIPTION: Tools or files may be copied from an external adversary-controlled system to the victim network through the command and control channel.

   TOOLS: More_eggs (S0284)

   NOTES: -

   ID: 008

   SOURCE: TEXT

   TACTIC: COLLECTION (TA0009)

   TECHNIQUE: DATA FROM LOCAL SYSTEM (T1005)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may search local system sources.

   TOOLS: More_eggs (S0284)

   NOTES: -