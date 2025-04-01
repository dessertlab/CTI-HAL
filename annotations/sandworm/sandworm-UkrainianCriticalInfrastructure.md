## Detailed comments

 * Page #2:
   > malicious remote operation of the breakers was conducted by multiple external humans using either existing remote administration tools at the operating system level or remote industrial control system (ICS) client so"ware via virtual private network (VPN) connections.

   ID: 001

   SOURCE: TEXT

   TACTIC: LATERAL MOVEMENT (TA0008)

   TECHNIQUE: REMOTE SERVICES (T1021)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may use Valid Accounts to log into a service that accepts remote connections, such as telnet, SSH, and VNC. The adversary may then perform actions as the logged-on user.

   TOOLS: VPN, Remote Administration Tools, ICS Software

   NOTE: The attackers used VPN connections and remote administration tools to control the breakers and operate industrial systems maliciously.

 * Page #2:
   > The companies believe that the actors acquired legitimate credentials prior to the cyber-attack to facilitate remote access.

   ID: 002

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts as a means of gaining Persistence.

   TOOLS: -

   NOTES: -

 * Page #2:
   > The KillDisk malware erases selected files on target systems and corrupts the master boot record, rendering systems inoperable.

   ID: 003

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DISK WIPE (T1561)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may wipe or corrupt raw disk data on specific systems or in large numbers in a network to interrupt availability to system and network resources.

   TOOLS: KillDisk (S0607)

   NOTE: -

 * Page #2:
   > It was further reported that in at least one instance, Windows-based human-machine interfaces (HMIs) embedded in remote terminal units were also overwritten with KillDisk.

   ID: 004

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: KillDisk (S0607)

   NOTE:

 * Page #2:
   > The actors also rendered Serial-to-Ethernet devices at substations inoperable by corrupting their firmware.

   ID: 005

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: FIRMWARE CORRUPTION (T1495)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may overwrite or corrupt the flash memory contents of system BIOS or other firmware in devices attached to a system in order to render them inoperable or unable to boot, thus denying the availability to use the devices and/or the system.

   TOOLS: -

   NOTE: -

 * Page #2:
   > the actors reportedly scheduled disconnects for server Uninterruptable Power Supplies (UPS) via the UPS remote management interface.

   ID: 006

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SYSTEM SHUTDOWN/REBOOT (T1529)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may shutdown/reboot systems to interrupt access to, or aid in the destruction of, those systems.

   TOOLS: KillDisk (S0607)

   NOTE:

 * Page #2:
   > The malware was reportedly delivered via spear phishing emails with malicious Microso" O!ice attachments.

   ID: 007

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: PHISHING (T1566)

   SUB-TECHNIQUE: SPEARPHISHING ATTACHMENT (T1566.001)

   DESCRIPTION: Adversaries may send spearphishing emails with a malicious attachment in an attempt to gain access to victim systems.

   TOOLS: -

   NOTE: -

 * Page #2:
   > It is suspected that BlackEnergy may have been used as an initial access vector to acquire legitimate credentials;

   ID: 008

   SOURCE: TEXT

   TACTIC: INITIAL ACCESS (TA0001)

   TECHNIQUE: VALID ACCOUNTS (T1078)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may obtain and abuse credentials of existing accounts as a means of gaining Persistence.

   TOOLS: -

   NOTES: -
