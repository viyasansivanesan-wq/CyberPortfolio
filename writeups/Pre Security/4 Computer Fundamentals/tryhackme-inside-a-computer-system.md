TryHackMe — Inside a Computer System

Platform: TryHackMe

Room: Inside a Computer System

Difficulty: Easy

Category: Cybersecurity 101 / Computing Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Inside a Computer System room on TryHackMe. This room covers the core hardware components that make up a computer, what each component does, and the step-by-step boot process that occurs when a computer is powered on. Includes two hands-on static site exercises.



Objectives



Identify and understand the role of each core hardware component

Learn the human body analogy used to describe PC components

Understand the full boot process from power button to OS

Complete interactive exercises on components and the boot sequence





Key Concepts

Core Hardware Components

ComponentAnalogyRoleCPUThe BrainProcesses all instructions and computationsRAMShort-term MemoryTemporarily stores data currently in useHDD / SSDLong-term MemoryPermanently stores files, OS, and programsMotherboardSkeleton and NervesConnects all components and allows communicationPSUHeart and LungsSupplies power to all componentsGPUVisual CortexHandles graphical processing and display output



The Boot Process

When the power button is pressed, the following steps occur before the OS loads:



Press Power Button — signal sent to PSU, power flows to all components

Firmware Starts — UEFI (or legacy BIOS) initialises and prepares core components

POST (Power-On Self Test) — checks that all required components are present and functioning correctly; triggers alerts if something is wrong

Select Boot Device — UEFI checks its ordered boot list to find the device containing the bootloader

Start Bootloader — the bootloader loads the Operating System from the boot device into RAM, then hands control to the OS





Note: BIOS and UEFI serve the same purpose — UEFI is the modern replacement for BIOS.





Practical Tasks \& Flags

TaskDescriptionFlagInside a Computer SystemMatch components to their roles on the static siteTHM{4llpccomp0n3nts1d3nt1f13d}What Happens When You Press the Start Button?Complete the boot process exercise on the static siteTHM{pc5ucce55fullyStart3d}



Questions \& Answers

QuestionAnswerFlag after completing the components exerciseTHM{4llpccomp0n3nts1d3nt1f13d}Flag after completing the boot process exerciseTHM{pc5ucce55fullyStart3d}



What I Learned

This room gave me a clearer mental model of how a computer actually functions at the hardware level. The human body analogy made it easy to remember what each component does — the CPU as the brain, RAM as short-term memory, and HDD/SSD as long-term memory maps well to how they actually behave. The boot process was more detailed than I expected — understanding POST and UEFI is directly relevant to security, since firmware-level attacks (like UEFI rootkits) target this exact stage before the OS even loads.



Challenges

No major technical challenges — the static site exercises were straightforward once the content was read carefully.



Takeaways



Every computer has the same core building blocks regardless of form factor

The CPU, RAM, and storage work together — speed bottlenecks usually come from one of these three

UEFI replaced BIOS but serves the same purpose — firmware-level security matters

POST is the system's self-check — if a component fails, POST catches it before the OS loads

Understanding hardware is foundational for both systems administration and security





Next Steps



Continue with the Cybersecurity 101 pathway

Explore operating system fundamentals (Linux and Windows)

Look into firmware-level security and UEFI vulnerabilities

