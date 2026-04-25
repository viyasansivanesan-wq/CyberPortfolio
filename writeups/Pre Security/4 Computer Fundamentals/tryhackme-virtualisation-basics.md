TryHackMe — Virtualisation Basics

Platform: TryHackMe

Room: Virtualisation Basics

Difficulty: Easy

Category: Cybersecurity 101 / Computing Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Virtualisation Basics room on TryHackMe. This room covers the core concepts of virtualisation — what it is, how hypervisors work, the difference between Type 1 and Type 2 hypervisors, and how containers differ from virtual machines. Ends with a practical task managing a simulated hypervisor dashboard.



Objectives



Understand what virtualisation is and why it's used

Learn what a hypervisor is and how it manages virtual machines

Understand the difference between Type 1 and Type 2 hypervisors

Understand what containers are and when to use them instead of VMs

Complete a practical hypervisor management exercise





Key Concepts

What is Virtualisation?

Virtualisation allows multiple applications or operating systems to share a single physical server by abstracting the hardware. Instead of needing separate physical machines for each workload, virtualisation creates isolated virtual environments on one host.



Hypervisors

A hypervisor is the software that manages and allocates resources (CPU, RAM, storage) to each virtual machine. There are two types:

TypeDescriptionUse CaseType 1 (Bare-metal)Runs directly on the physical hardware, no host OS requiredEnterprise servers, data centresType 2 (Hosted)Runs on top of an existing OS (e.g. VirtualBox, VMware Workstation)Study labs, personal use, cybersecurity practice



Type 2 hypervisors are what cybersecurity students use to run practice labs (e.g. Kali Linux in VirtualBox) — they run on top of Windows or macOS without needing dedicated hardware.





Virtual Machines vs Containers

FeatureVirtual MachineContainerIncludes full OS✅ Yes❌ No — shares host OS kernelIsolation levelHighModerateResource usageHigherLowerBest forRunning different OSes, full isolationMultiple small apps on the same OS

Containers are the right choice when a company wants to host multiple small applications on the same virtual machine — they are lightweight and share the host OS, making them efficient.



Practical Task — Hypervisor Dashboard

Used a simulated hypervisor management dashboard to inspect and manage running virtual machines.

QuestionAnswerVM running for the longest timeMonitoring-SYSVM using the biggest amount of memoryDB-Cluster-01VMs in running state after fixing Mail-SERVER8Physical machine hosting most of the VMsHV-PROD-02



Questions \& Answers

QuestionAnswerWhat does virtualisation enable multiple applications to share?physical serverWhat is the software that manages resources for each VM?hypervisorWhich hypervisor type would a student use for a cybersecurity study lab?type 2What should a company use to host multiple small apps in the same VM?containersVM running for the longest timeMonitoring-SYSVM using the most memoryDB-Cluster-01VMs in running state after fixing Mail-SERVER8Physical machine hosting most VMsHV-PROD-02



What I Learned

Virtualisation is fundamental to how modern infrastructure works — and directly relevant to cybersecurity labs. Every TryHackMe VM I've been attacking runs inside a virtualised environment. Understanding the difference between Type 1 and Type 2 hypervisors helps explain why enterprise environments use bare-metal hypervisors (performance, security) while students use Type 2 (convenience). The containers section was particularly useful — Docker and containerised applications are increasingly common targets in CTFs and real-world pentesting, so understanding how they differ from VMs matters.



Challenges

No major technical challenges. The hypervisor dashboard task required reading the VM stats carefully to identify which machine had been running longest and which was consuming the most memory.



Takeaways



Virtualisation lets one physical server run many isolated workloads — core to modern infrastructure

Hypervisors manage VM resources — Type 1 for enterprise, Type 2 for personal/study use

Containers share the host OS kernel — lighter than VMs but less isolated

Type 2 hypervisors (VirtualBox, VMware) are the standard tool for cybersecurity study labs

Understanding virtualisation is essential for cloud security and container-based pentesting





Next Steps



Continue with the Cybersecurity 101 pathway

Explore Docker and container security concepts

Begin Linux Fundamentals Part 1

