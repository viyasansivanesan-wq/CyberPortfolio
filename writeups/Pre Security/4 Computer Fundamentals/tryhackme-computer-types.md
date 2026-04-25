TryHackMe — Computer Types

Platform: TryHackMe

Room: Computer Types

Difficulty: Easy

Category: Cybersecurity 101 / Computing Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Computer Types room on TryHackMe. This room explores the different types of computers that exist beyond the traditional desktop or laptop — from servers and workstations to smartphones, IoT devices, and embedded computers. Includes an interactive challenge to identify hidden computers in everyday objects.



Objectives



Understand the different categories of computer types

Learn what distinguishes servers, workstations, and personal computers

Understand what smartphones, tablets, IoT devices, and embedded computers are

Complete an interactive challenge identifying computers hidden in everyday objects





Key Concepts

Traditional Computer Types

TypeDescriptionDesktopStandard personal computer with separate monitor, keyboard, and mouseLaptopPortable all-in-one personal computerServerRuns without a dedicated screen or keyboard; provides services to other devices on a networkWorkstationHigh-spec computer with specialised components built for precision or intensive work (e.g. 3D rendering, engineering)



Hidden Computers — Everyday Devices

TypeDescriptionExamplesSmartphonePocket-sized computer optimised for battery life and connectivityiPhone, Android phoneTabletTouch-first computer with a larger screeniPad, drawing tabletIoT DeviceNetwork-connected device with a single purposeSmart thermostat, smart doorbell, fitness trackerEmbedded ComputerComputer built into another device; may not connect to any networkCoffee maker controller, automatic door sensor, lamp dimmer chip

IoT vs Embedded: Both are small and single-purpose. The key difference is connectivity — IoT devices connect to a network to send/receive data, while embedded computers operate independently inside a machine, often invisibly for years.



Practical Task — Hidden Computers Challenge

Used the interactive static site to identify 8 hidden computers among everyday objects in a room, with a maximum of 3 wrong clicks allowed.

Hidden computers found: Smart TV, Smart Fridge, Security Cam, WiFi Router, Thermostat, Smartwatch, Smart Speaker, Robot Vacuum.

Flag: THM{8\_computer\_types}



Questions \& Answers

QuestionAnswerWhich computer type runs without a dedicated screen and keyboard?serverWhat kind of computer with specialised components is used for precision work?workstationWhat is the most popular pocket-sized computer?smartphoneWhat kind of computer would you find in a coffee machine?embedded computerFlag from the hidden computers challengeTHM{8\_computer\_types}



What I Learned

This room expanded my definition of what a "computer" is. Embedded computers are everywhere — inside appliances, vehicles, industrial equipment — and most people never think of them as computers at all. From a security perspective this matters enormously: IoT devices are frequently under-secured, rarely updated, and often overlooked in security assessments. Smart TVs, routers, thermostats, and doorbells are all attack surfaces. The distinction between IoT and embedded is also relevant — an IoT device is network-connected and therefore reachable remotely, making it a much higher-risk target.



Challenges

No major technical challenges. The hidden computers game required thinking broadly about what qualifies as a computer — the Smart TV and Smartwatch were obvious, but items like the Security Cam and Robot Vacuum required applying the definition carefully.



Takeaways



Computers are everywhere — not just desktops and laptops

Servers run headlessly and provide services across networks — a core concept for pentesting infrastructure

IoT devices are network-connected and frequently insecure — a major real-world attack surface

Embedded computers are invisible by design — but still run code that can contain vulnerabilities

Workstations differ from desktops by having specialised, high-performance components





Next Steps



Continue with the Cybersecurity 101 pathway

Explore IoT security and common vulnerabilities in networked devices

Begin Linux Fundamentals

