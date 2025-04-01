## Detailed comments

 * Page #1:
   > Magecart operators registered a domain called neweggstats.com with the intent of blending in with Newegg's primary domain, newegg.com

   ID: 001

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: ACQUIRE INFRASTRUCTURE (T1583)

   SUB-TECHNIQUE: DOMAINS (T1583.001)

   DESCRIPTION: Adversaries may acquire domains that can be used during targeting. Domain names are the human readable names used to represent one or more IP addresses. They can be purchased or, in some cases, acquired for free.

   TOOLS: -

   NOTES: -

   ID: 002

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: IMPERSONATION (T1656)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may impersonate a trusted person or organization in order to persuade and trick a target into performing some action on their behalf.

   TOOLS: -

   NOTES: -

 * Page #1:
   > a Magecart drop server where their skimmer backend runs to receive skimmed credit card information

   ID: 003

   SOURCE: TEXT

   TACTIC: EXFILTRATION (TA0010)

   TECHNIQUE: EXFILTRATION OVER C2 CHANNEL (T1041)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may steal data by exfiltrating it over an existing command and control channel.

   TOOLS: -

   NOTES: -

 * Page #1:
   > these actors acquired a certificate issued for the domain by Comodo to lend an air of legitimacy to their page

   ID: 004

   SOURCE: TEXT

   TACTIC: RESOURCE DEVELOPMENT (TA0042)

   TECHNIQUE: OBTAIN CAPABILITIES (T1588)

   SUB-TECHNIQUE: DIGITAL CERTIFICATES (T1588.004)

   DESCRIPTION: Adversaries may buy and/or steal SSL/TLS certificates that can be used during targeting. SSL/TLS certificates are designed to instill trust.

   TOOLS: -

   NOTES: -

 * Page #2:
   > the attackers placed the skimmer code on Newegg

   ID: 005

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPTING INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTES: -

 * Page #2:
   > The skimmer was put on the payment processing page itself, not in a script, so it would not show unless the payment page was hit.

   ID: 006

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: OBFUSCATED FILES OR INFORMATION (T1027)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to make an executable or file difficult to discover.

   TOOLS: -

   NOTES: -
