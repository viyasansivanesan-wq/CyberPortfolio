TryHackMe — Operating Systems: Introduction

Platform: TryHackMe

Room: Operating Systems: Introduction

Difficulty: Easy

Category: Cybersecurity 101 / Computing Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Operating Systems: Introduction room on TryHackMe. This room covers what an operating system is, its core responsibilities, the difference between kernel space and user space, and hands-on investigation of a live Ubuntu Linux system using system tools like About This Computer and System Monitor.



Objectives



Understand what an operating system is and what it does

Learn the difference between kernel space and user space

Understand the core responsibilities of an OS

Investigate a live Linux system to gather hardware and filesystem information

Navigate the Linux file system to find a hidden flag





Key Concepts

What is an Operating System?

An Operating System (OS) is the software that manages hardware resources and provides services for applications to run. It acts as the intermediary between the user/applications and the physical hardware.

Common operating systems: Windows, Linux (Ubuntu, Kali, Debian), macOS.



Kernel Space vs User Space

SpaceAccess LevelDescriptionKernel SpaceUnrestrictedHas direct, unrestricted access to hardware — runs the OS kernelUser SpaceRestrictedWhere user applications run — cannot directly access hardware

The kernel manages communication between user applications and hardware through controlled interfaces called system calls.



Core OS Responsibilities



Process Management — scheduling and managing running programs

Memory Management — allocating and tracking RAM usage across processes

File System Management — organising and controlling access to stored data

Device Management — communicating with hardware via drivers

User Management — managing user accounts, authentication, and permissions

Security \& Access Control — enforcing permissions and protecting system resources





Linux File System Basics

Linux organises everything under a single root directory /. Key directories:



/home — contains user home directories

/dev — contains device files (e.g. /dev/root for the root filesystem)

/etc — system configuration files

/var — variable data (logs, databases)



The root filesystem device /dev/root uses the ext4 filesystem type — the standard Linux filesystem format.



Practical Tasks

System Investigation — About This Computer

Opened the About This Computer shortcut on the Ubuntu Mate desktop to gather system information:



Ubuntu Mate version running: 1.26.2

Memory allocated to the machine: 1.9 GiB



System Monitor — File Systems Tab

Opened System Monitor and navigated to the File Systems tab:



Filesystem type for /dev/root: ext4



Home Directory Investigation

Opened the Home directory from the Desktop:



Number of user directories found: 3



Navigated to Alex's home directory → Documents folder → opened note.txt:

Flag: THM{new\_pc\_for\_free!}



Questions \& Answers

QuestionAnswerWhich OS space has unrestricted access to hardware?Kernel SpaceWhich OS responsibility manages user accounts and permissions?User ManagementWhat version of Ubuntu Mate is the computer running?1.26.2How much memory is allocated to the machine?1.9 GiBWhat filesystem type is listed for /dev/root?ext4How many user directories exist in the Home directory?3What is the flag in Alex's note.txt?THM{new\_pc\_for\_free!}



What I Learned

This room gave me hands-on experience with a live Linux system for the first time in a structured way. Navigating the file system, checking system specs through the GUI, and finding a flag hidden in a text file are all directly transferable skills — in real penetration testing, post-exploitation involves exactly this kind of system investigation: finding user directories, reading sensitive files, and understanding what OS and hardware you're working with. The kernel space vs user space distinction is also foundational for understanding privilege escalation — moving from user space to kernel space is the goal of many local privilege escalation exploits.



Challenges

No major technical challenges. Navigating to Alex's Documents folder required understanding the Linux home directory structure — /home/alex/Documents/note.txt.



Takeaways



The OS manages all hardware and software interactions — understanding it is foundational for security

Kernel space has unrestricted hardware access — kernel exploits are the highest-impact privilege escalation

Linux organises everything under / — knowing the directory structure is essential for pentesting

ext4 is the standard Linux filesystem — relevant for forensics and disk analysis

Post-exploitation on Linux starts with exactly this kind of system reconnaissance





Tools Used



About This Computer (Ubuntu Mate GUI)

System Monitor — File Systems tab

Linux file manager (Home directory navigation)





Next Steps



Continue with Linux Fundamentals Part 1

Start learning Linux command line navigation (ls, cd, cat, find)

Explore Linux privilege escalation techniques

