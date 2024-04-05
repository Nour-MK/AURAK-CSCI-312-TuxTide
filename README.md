# TexTide: A Case Study Analyzing The Arch Linux Operating System Versatility from Desktop to Cloud
![](Assets/logo.png)

**Word count:** TBC

# Work Distribution & Acknowledgements
| | Member            | ID        | Contact                                                                                        | Task |
|-|-------------------|-----------|------------------------------------------------------------------------------------------------|------|
|1| Urita Sadallah    | 2021004899| [Email](mailto:urita.sadallah@aurak.ac.ae), [Github](https://github.com/uritaaquila)         |      |
|2| Mohamed Abouissa  | 2021005188| [Email](mailto:mohamed.abouissa@aurak.ac.ae), [Github](https://github.com/Mohamed-Abouissa)   |      |
|3| Khawla Alhammadi  | 2021004956| [Email](mailto:khawla.alhammadi@aurak.ac.ae),                                                                                               |      |
|4| Sarah Alsuwaidi   | 2021004782| [Email](mailto:sarah.alsuwaidi@aurak.ac.ae),                                                                                               |      |
|5| Ahmad Hammoudeh   | 2021004915| [Email](mailto:ahmad.hammoudeh@aurak.ac.ae), [Github](https://github.com/ahmaadmohd)    |      |
|6| Nour Mohamed      | 2021004938| [Email](mailto:nour.mohamed@aurak.ac.ae), [Github](https://github.com/Nour-MK)                |      |


We extend our sincere appreciation to Dr. Zubaidah Al-Hazza for her invaluable guidance, encouragement, and support throughout this research project. Her expertise and insightful feedback have significantly contributed to the completion of this study.


# Table of Contents

1. [Executive Summary](#executive-summary)
2. [Glossary](#glossary)
6. [Introduction](#introduction)
    1. [Criteria for Choosing the Operating Systems in Parts 1 & 2](#criteria-for-choosing-the-operating-systems-in-parts-1--2)
    2. [Background Information](#background-information)
        1. [The Man & The Penguin](#the-man--the-penguin)
        2. [Linux History](#linux-history)
        3. [Arch Linux History](#arch-linux-history)
7. [Part 1: Daily Driver OS (Arch Linux)](#part-1-daily-driver-os-arch-linux)
    1. [Process and Threads](#process-and-threads)
    2. [Process Scheduling](#process-scheduling)
    3. [Synchronization](#synchronization)
    4. [Deadlock](#deadlock)
    5. [Memory Management](#memory-management)
    6. [File Management](#file-management)
8. [Part 2: Cloud Computing OS (Arch Linux)](#part-2-cloud-computing-os-arch-linux)
    1. [Trends in Operating Systems](#trends-in-operating-systems)
    2. [What Constitutes a Cloud Computing OS?](#what-constitutes-a-cloud-computing-os)
    3. [Comparison with OS of Part 1](#comparison-with-os-of-part-1)
        1. [Implementation-wise](#implementation-wise)
        2. [Performance-wise](#performance-wise)
        3. [Hardware Support](#hardware-support)
        4. [Community and Support](#community-and-support)
        5. [Updates and Stability](#updates-and-stability)
        6. [Licensing and Cost](#licensing-and-cost)
10. [Part 3: Additional Considerations (Best Practices in OS)](#part-3-additional-considerations-best-practices-in-os)
    1. [Legal and Ethical Issues](#legal-and-ethical-issues)
    2. [Solutions to Issues](#solutions-to-issues)
11. [Conclusion](#conclusion)
    1. [Overview](#overview)
    2. [Linux vs. Our Current Daily Drivers](#linux-vs-our-current-daily-drivers)
        1. [Linux vs. Windows](#linux-vs-windows)
        2. [Linux vs. macOS](#linux-vs-macos)
    3. [Further Research](#further-research)
    4. [Building Our Own Distro!](#building-our-own-distro)
14. [Resources](#resources)
18. [Terms of Use](#terms-of-use)


# Executive Summary

# Glossary
1. **Daily Driver**: A computer or operating system that is used regularly for everyday tasks, such as web browsing, email, document editing, etc. It is the primary system relied upon by the user for their computing needs.

2. **Bare Metal**: Refers to a computer system or software that operates directly on the underlying hardware without the need for an intervening operating system or virtualization layer.

3. **Shell**: A program that serves as the interface between the user and the operating system, allowing users to interact with the system by interpreting commands and executing them. Shells can be command-line interfaces (CLI) or graphical user interfaces (GUI), providing users with different ways to interact with the system.

4. **Kernel**: The core component of an operating system that manages system resources, such as memory, CPU, and input/output devices. It acts as an intermediary between the hardware and the software layers of the system.

5. **Vanilla**: In the context of software, "vanilla" refers to the original, unmodified version of a program or operating system, without any additional features or customizations.

6. **Ricing**: An acronym/term that originated in the Unix and Linux communities, particularly within the desktop customization (often called "desktop theming") subculture. It stands for Race Inspired Cosmetic Enhancements and it's the practice of customizing the appearance and functionality of a computer system, typically through the use of themes, icons, and configuration settings, to achieve a desired aesthetic or performance.

7. **Flavors**: Variants or different versions of a software or operating system that are tailored to specific use cases or preferences. They may include different configurations, packages, or default settings.

8. **Fork of a Fork**: A software project that is derived from another project, which itself was originally derived from a separate project. It represents a further divergence in the development path, typically resulting in significant differences from the original codebase.

9. **Distribution**: A complete operating system package that includes the kernel, system utilities, libraries, and applications, pre-configured and packaged for easy installation and use. Linux distributions, such as Ubuntu and Fedora, are examples of this.

10. **Distro Hopping**: The practice of frequently switching between different Linux distributions, often motivated by a desire to explore different features, performance characteristics, or software availability.

11. **Desktop Environment**: A graphical user interface (GUI) that provides users with a visual way to interact with their computer, including windows, icons, menus, and other graphical elements. Examples include GNOME, KDE, and Xfce.

12. **Bloatware**: Software that includes unnecessary features, functions, or components, often resulting in excessive resource usage, decreased performance, or decreased usability. It may be pre-installed on systems or bundled with other software packages.

13. **GUI**: A graphical user interface, a type of user interface that allows users to interact with electronic devices through graphical icons and visual indicators, as opposed to text-based interfaces, such as command-line interfaces.

14. **CLI**: Command-Line Interface, a text-based interface used for entering commands to communicate with a computer system. It provides users with direct access to system functions and utilities through typed commands.

15. **Virtual Machine**: A software-based emulation of a physical computer system that allows multiple operating systems to run simultaneously on the same hardware. It provides isolation and encapsulation of resources, enabling efficient utilization of hardware resources.

16. **Dual Boot**: The practice of installing and running two different operating systems on the same computer, allowing users to choose which operating system to boot into when starting the system.

17. **Documentation**: Comprehensive information and instructions provided with software or hardware products, including user manuals, guides, tutorials, and technical specifications. It helps users understand and utilize the features and capabilities of the product.

# Introduction
## Criteria for Choosing the Operating Systems in Parts 1 & 2
## Background Information
### The Man & The Penguin
### Linux History
### Arch Linux History

# Part 1: Daily Driver OS (Arch Linux)
## Process and Threads
## Process Scheduling
## Synchronization
## Deadlock
## Memory Management
## File Management

# Part 2: Cloud Computing OS (Arch Linux)
## Trends in Operating Systems
## What Constitutes a Cloud Computing OS?
## Comparison with OS of Part 1
### Implementation-wise
### Performance-wise
### Hardware Support
### Community and Support
### Updates and Stability
### Licensing and Cost

# Part 3: Additional Considerations (Best Practices in OS)
## Legal and Ethical Issues
## Solutions to Issues

# Conclusion
## Overview
## Linux vs. Our Current Daily Drivers
### Linux vs. Windows
### Linux vs. macOS
## Further Research
## Building Our Own Distro!

# Resources

# Terms of Use
Copyright © 2024 All Contributors

This case study is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://github.com/Nour-MK/TuxTide/blob/main/LICENSE.txt). Individuals are permitted to share and distribute the work non-commercially, provided proper attribution is given to all contributors. However, derivative works based on this material are not allowed without prior permission from [@Nour-MK.](https://github.com/Nour-MK), even if they comply with the terms of the CC BY-NC-ND 4.0 license.

This publication adheres to all regulatory laws and guidelines established by the American University of Ras Al Khaimah (AURAK) regarding the dissemination of academic materials.
