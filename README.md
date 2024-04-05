# TexTide: A Case Study Analyzing The Arch Linux Operating System Versatility from Desktop to Cloud

**Word count:**  

# Table of Contents

1. [Executive Summary](#executive-summary)
2. [Glossary](#glossary)
6. [Introduction](#introduction)
    - [Criteria for Choosing the Operating Systems in Parts 1 & 2](#criteria)
    - [Background Information](#background-information)
        - [The Man & The Penguin](#)
        - [Linux History](#linux)
        - [Arch Linux History](#arch-linux)
    - [Understanding Operating Systems](#understanding-operating-systems)
        - [Kernel vs. CPU](#kernel-vs-cpu)
        - 
7. [Part 1: Daily Driver OS (Arch Linux)](#operating-system-one)
    - [Process and Threads](#process-and-threads)
    - [Process Scheduling](#process-scheduling)
    - [Synchronization](#synchronization)
    - [Deadlock](#deadlock)
    - [Memory Management](#memory-management)
    - [File Management](#file-management)
8. [Part 2: Cloud Computing OS (Arch Linux)](#operating-system-two-cloud-os)
   - [Trends in Operating Systems](#)
   - [What Constitutes a Cloud Computing OS?](#)
   - [Comparison with OS of Part 1](#comparison-with-os-one)
       - [Implementation-wise](#)
       - [Performance-wise](#)
       - [Hardware Support](#)
       - [Community and Support](#)
       - [Updates and Stability](#)
       - [Licensing and Cost](#)
10. [Part 3: Additional Considerations (Best Practices in OS)](#)
    - [Legal and Ethical Issues](#legal-and-ethical-issues)
    - [Solutions to Issues](#solutions-to-issues)
11. [Conclusion](#conclusion)
    - [Overview](#overview)
    - [Linux vs. Our Current Daily Drivers](#)
        - [Linux vs. Windows](#)
        - [Linux vs. macOS](#)
    - [Further Research](#further-research)
    - [Building Our Own Distro!](#building-our-own-distro)
12. [Work Distribution Among Team](#work-graph)
19. [Acknowledgments](#acknowledgments)
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


# Terms of Use
Copyright © 2024 All Contributors

This case study is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License (CC BY-NC-ND 4.0). Individuals are permitted to share and distribute the work non-commercially, provided proper attribution is given to all contributors. However, derivative works based on this material are not allowed without prior permission from [@Nour-MK.](https://github.com/Nour-MK), even if they comply with the terms of the CC BY-NC-ND 4.0 license.

This publication adheres to all regulatory laws and guidelines established by the American University of Ras Al Khaimah (AURAK) regarding the dissemination of academic materials.
