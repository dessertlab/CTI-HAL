## Detailed comments

* Page #10:
    > BLACKENERGY

    ID: S01

    SOURCE: TEXT

    TOOLS: BlackEnergy (S0089)


* Page #10:
   > wiping of Windows systems through the KillDisk malware

   ID: 001

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DISK WIPE (T1561)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may wipe or corrupt raw disk data on specific systems or in large numbers in a network to interrupt availability to system and network resources.

   TOOLS: KillDisk (S0607)

   NOTE: -

* Page #10:
   > destruction of serial-to-Ethernet devices through malicious firmware updates

   ID: 002

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: FIRMWARE CORRUPTION (T1495)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may overwrite or corrupt the flash memory contents of system BIOS or other firmware in devices attached to a system in order to render them inoperable or unable to boot, thus denying the availability to use the devices and/or the system.

   TOOLS: -

   NOTE: -

* Page #12:
    > CRASHOVERRIDE

    ID: S02

    SOURCE: TEXT

    TOOLS: CRASHOVERRIDE/Industroyer (S0604)

* Page #13:
   > After authentication opens HTTP channel to external command and control server (C2) through internal proxy

   ID: 003

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: APPLICATION LAYER PROTOCOL: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries may communicate using application layer protocols associated with web traffic to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTE: The backdoor opens an HTTP channel to an external C2 server through an internal proxy.

* Page #13:
   > Overwrites an existing service to point to the backdoor so the malware persists between reboots

   ID: 004

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

* Page #13:
   > On execution, the malware attempts to contact a hard-coded proxy address located within the local network.

   ID: 005

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: PROXY (T1090)

   SUB-TECHNIQUE: PROXY: INTERNAL PROXY (T1090.001)

   DESCRIPTION: Adversaries may use a connection proxy to direct network traffic between systems or act as an intermediary for network communications to a command and control server to avoid direct connections to their infrastructure.

   TOOLS: -

   NOTE: The malware contacts a hard-coded proxy address on the local network as part of its C2 communication strategy.

* Page #13:
   > The backdoor then sends a series of HTTP POST requests with the victim's Windows GUID (a unique identifier set with every Windows installation) in the HTTP body. This information authenticates the targeted machine to the command and control (C2) server.

   ID: 006

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: APPLICATION LAYER PROTOCOL: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries may communicate using application layer protocols associated with web traffic to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTE: -

* Page #14:
   > If the authentication is successful to the internal proxy, the malware attempts to perform an HTTP CONNECT to an external C2 server via the internal proxy.

   ID: 007

   SOURCE: TEXT

   TACTIC: COMMAND AND CONTROL (TA0011)

   TECHNIQUE: APPLICATION LAYER PROTOCOL (T1071)

   SUB-TECHNIQUE: APPLICATION LAYER PROTOCOL: WEB PROTOCOLS (T1071.001)

   DESCRIPTION: Adversaries may communicate using application layer protocols associated with web traffic to avoid detection/network filtering by blending in with existing traffic.

   TOOLS: -

   NOTE: -

   LINK: #005 THEN #006 THEN #007


* Page #14:
   > Create a new process as logged in user •Create a new process as specified user via CreateProcessWithLogon

   ID: 008

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads.

   TOOLS: -

   NOTE: -

* Page #14:
   > Write a file •Copy a file •Execute a command as logged in user •Execute a command as specified user •Kill the backdoor

   ID: 009

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: COMMAND AND SCRIPT INTERPRETER (T1059)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries.

   TOOLS: -

   NOTE: -

* Page #14:
   > Stop a service •Specify a user (log in as user) and stop a service •Specify a user (log in as user) and start a service •Alter an existing service to point to specified process and change to start at boot

   ID: 010

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

* Page #15:
   > The service manipulation process is the only persistence mechanism for the malware. When used, the adversary can select an arbitrary system service, direct it to refer to CRASHOVERRIDE, and ensure it is loaded on system boot.

   ID: 011

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

* Page #15:
   > Loads payload modules which manipulate the ICS and cause destruction via the wiper

   ID: 012

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may execute malicious payloads via loading shared modules.

   TOOLS: -

   NOTE: -

* Page #15:
   > Starts itself as a service likely to hide better

   ID: 013

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

* Page #15:
   > Launches the payload and begins either 1 or 2 hours countdown before launching the data wiper

   ID: 014

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: -

   NOTE: -

* Page #16:
   > the ICS payload modules and data wiper module must be loaded by a separate loader EXE.

   ID: 015

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may execute malicious payloads via loading shared modules.

   TOOLS: -

   NOTE: -

* Page #16:
   > It then loads the module DLL via an exported function named Crash

   ID: 017

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SHARED MODULES (T1129)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may execute malicious payloads via loading shared modules.

   TOOLS: -

   NOTE: -

* Page #16:
   > the sample analyzed starts a service named  defragsvc

   ID: 016

   SOURCE: TEXT

   TACTIC: PERSISTENCE (TA0003)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads as part of persistence.

   TOOLS: -

   NOTE: -

* Page #16:
   > Control then passes from the launcher to the loaded module while the launcher waits two hours before executing the data wiper.

   ID: 018

   SOURCE: TEXT

   TACTIC: EXECUTION (TA0002)

   TECHNIQUE: SCHEDULED TASK/JOB (T1053)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may abuse task scheduling functionality to facilitate initial or recurring execution of malicious code.

   TOOLS: -

   NOTE: -

* Page #16:
   > Clears all registry keys associated with system services •Overwrites all ICS configuration files across the hard drives and all mapped network drives specifically targeting ABB PCM600 configuration files in this sample •Overwrites generic Windows files

   ID: 019

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: -

   NOTE: -

* Page #16:
   > Renders the system unusable

   ID: 020

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: SERVICE STOP (T1489)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may stop or disable services on a system to render those services unavailable to legitimate users.

   TOOLS: -

   NOTE: -

* Page #16:
   > Once executed, the data wiper module clears registry keys, erase files, and kill processes running on the system.

   ID: 021

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: -

   NOTE: -

* Page #16:
   > The first task of the wiper writes zeros into all of the registry keys in: SYSTEM\CurrentControlSet\Services

   ID: 022

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: DATA DESTRUCTION (T1485)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.

   TOOLS: -

   NOTE: -

* Page #17:
   > 'Kills' legitimate the master process on the victim host

   ID: 023

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads.

   TOOLS: -

   NOTE: -

* Page #17:
   > Masquerades as the new master

   ID: 024

   SOURCE: TEXT

   TACTIC: DEFENSE EVASION (TA0005)

   TECHNIQUE: MASQUERADING (T1036)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may attempt to manipulate features of their artifacts to make them appear legitimate or benign to users and/or security tools.

   TOOLS: -

   NOTE: -

* Page #20:
   > the first action is to try to kill the communications service process which acts as the master process

   ID: 025

   SOURCE: TEXT

   TACTIC: PRIVILEGE ESCALATION (TA0004)

   TECHNIQUE: CREATE OR MODIFY SYSTEM PROCESS (T1543)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may create or modify system-level processes to repeatedly execute malicious payloads.

   TOOLS: -

   NOTE: -

* Page #23:
   > In some circumstances, it may have no immediate impact while in others it could put customers into an outage. It is important to note that grid operations encompass failure modes and operations can normally compensate.

   ID: 026

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE:SERVICE STOP (T1489)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may stop or disable services on a system to render those services unavailable to legitimate users.

   TOOLS: -

   NOTE: -

* Page #24:
   > The outcome of the action infers that various systems can either perform actions on wrong information or report incorrect information to system operators. This Denial of Visibility will amplify misunderstanding and confusion while system operators troubleshoot the problem as their system view will show breakers closed when they are open.

   ID: 027

   SOURCE: TEXT

   TACTIC: IMPACT (TA0040)

   TECHNIQUE: MANIPULATION OF CONTROL (T0833)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may manipulate physical process control within the industrial environment. Methods of manipulating control can include changes to set point values, tags, or other parameters. Adversaries may manipulate control systems devices or possibly leverage their own, to communicate with and command physical control processes. The duration of manipulation may be temporary or longer sustained, depending on operator detection.

   TOOLS: -

   NOTE: The manipulation of control systems results in incorrect reporting and actions based on false data, leading to operational confusion and a Denial of Visibility for system operators.

* Page #25:
   > A second, and more severe, amplifying attack would be to neutralize the automated protective system by creating a Denial of Service against some or all of the protective relays.

   ID: 028

   SOURCE: TEXT

   TACTIC: INHIBIT REPONSE FUNCTION (TA0107)

   TECHNIQUE: DENIAL OF SERVICE (T0814)

   SUB-TECHNIQUE: -

   DESCRIPTION: Adversaries may perform Denial-of-Service (DoS) attacks to disrupt expected device functionality.

   TOOLS: -

   NOTE: -