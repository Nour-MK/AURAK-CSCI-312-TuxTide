# <p align="center">TuxTide[^*]: An OS Case Study</p>
## <p align="center">Analyzing Arch Linux's Versatility from Desktop to Cloud</p>
[^*]: The title "TuxTide" (i.e. Tux Tide) represents a convergence associated with Tux, the Linux mascot. It implies a surge or wave of activity, innovation, or prominence related to Linux or open-source technology and suggests the powerful force and momentum driven by the Linux community (both developers and users), with Tux as its emblem.

![](Assets/banner.png)
<!-- Badge icons found at https://feathericons.com/ and view stats at https://yhype.me/github/accounts/Nour-MK/TuxTide/traffic -->
<p align="center">
  <a href="https://custom-icon-badges.demolab.com/badge/Project%20Status-Work%20in%20Progress-1793d1?style=for-the-badge&logo=activity&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Project%20Status-Work%20in%20Progress-1793d1?style=for-the-badge&logo=activity&logoSource=feather&logoColor=white" alt="Project Status" title="Project Status" style="vertical-align:top; margin:4px"></a>
  <a href="https://custom-icon-badges.demolab.com/badge/Word%20Count-5k-1793d1?style=for-the-badge&logo=type&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Word%20Count-5k-1793d1?style=for-the-badge&logo=type&logoSource=feather&logoColor=white" alt="Word Count" title="Word Count" style="vertical-align:top; margin:4px"></a>
  <a href="https://custom-icon-badges.demolab.com/badge/Views%20Count-5k-1793d1?style=for-the-badge&logo=eye&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Views%20Count-288-1793d1?style=for-the-badge&logo=eye&logoSource=feather&logoColor=white" alt="Views Count" title="Views Count" style="vertical-align:top; margin:4px"></a>
</p>

This study aims to academically investigate operating systems, focusing on Arch Linux. It begins with an Executive Summary and Glossary to provide brief insights and clarify technical terms used throughout the study. The Introduction section outlines the criteria for selecting operating systems and presents background information on Linux and Arch Linux history. Parts 1 and 2 discuss Arch Linux's functionality as both a Daily Driver OS and a Cloud Computing OS. Additionally, Part 2 compares Arch Linux's roles in daily usage and cloud computing environments, analyzing factors such as implementation, performance, hardware support, community and support, updates and stability, as well as licensing and cost considerations. Part 3 addresses Additional Considerations, including legal and ethical issues related to operating systems and proposing potential solutions. The study concludes by giving an overview to recap all discussed findings, comparing Linux with mainstream operating systems like Windows and macOS, suggesting avenues for further research, and considering the possibility of constructing a custom Linux distribution of our own! Finally, a list of resources is provided for reference and further exploration.

## Work Distribution & Acknowledgements
| | Member            | ID        | Contact                                                                                        | Task |
|-|-------------------|-----------|------------------------------------------------------------------------------------------------|------|
|1| Urita Sadallah    | 2021004899| [Email](mailto:urita.sadallah@aurak.ac.ae), [Github](https://github.com/uritaaquila)         | 1. Conducted research on synchronization. <br> 2. Conducted research on deadlock. <br> 3. Prepared presentation slides. |
|2| Mohamed Abouissa  | 2021005188| [Email](mailto:mohamed.abouissa@aurak.ac.ae), [Github](https://github.com/Mohamed-Abouissa)   | 1. Conducted research on introduction. <br> 2. Conducted research on memory management. <br> 3. Conducted research on file management. |
|3| Khawla Alhammadi  | 2021004956| [Email](mailto:khawla.alhammadi@aurak.ac.ae), [Github](https://github.com/Khawlaalh)                                                  | 1. Prepared executive summary. <br> 2. Compiled glossary. <br> 3. Conducted research on OS trends. |
|4| Sarah Alsuwaidi   | 2021004782| [Email](mailto:sarah.alsuwaidi@aurak.ac.ae), [Github](https://github.com/SarahAlsuwaidi)                                                   | 1. Conducted research on cloud computing OSes. <br> 2. Compared OS of Part 1 with OS of Part 2. <br> 3. Conducted research on legal and ethical issues.  |
|5| Ahmad Hammoudeh   | 2021004915| [Email](mailto:ahmad.hammoudeh@aurak.ac.ae), [Github](https://github.com/ahmaadmohd)          | 1. Provided solutions to issues identified. <br> 2. Wrote the conclusion. <br> 3. Formatted resources in APA 7th edition style. |
|6| Nour Mohamed      | 2021004938| [Email](mailto:nour.mohamed@aurak.ac.ae), [Github](https://github.com/Nour-MK)                  | 1. Conducted research on process and threads. <br> 2. Conducted research on process scheduling. <br> 3. Exported case study to various formats. |


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
Choosing an operating system (OS) for our research and case study is a critical decision that warrants careful consideration. In selecting the operating system (OS) for our study, several key criteria were considered to ensure an immersive and engaging research experience. Firstly, the OS should not be widely recognized or mainstream to avoid duplication of efforts with classmates, fostering a unique and stimulating exploration and presentation of key findings. This requirement eliminates OSes such as Windows, macOS, Ubuntu, and Android. Secondly, the OS must be fully open-source as this allows us to freely inspect the source code, providing a firsthand understanding of its underlying architecture and infrastructure. This transparency empowers us to delve deeper into the OS's mechanisms, gaining insights that may not be readily available with closed-source alternatives. Additionally, the vast community surrounding open-source OSes serves as a valuable resource. Many community members have likely encountered and addressed the same questions and challenges we will face, offering a wealth of knowledge and expertise to draw from. This collaborative ecosystem enhances our learning process, enabling us to leverage the collective wisdom and experiences of those who have traversed similar paths before us. Additionally, the chosen OS must demonstrate maturity, offering comprehensive documentation and resources for thorough research. This requirement eliminates new or incomplete OS releases like Fuchsia, dahliaOS, ChromeOS, and Rhino Linux ensuring a stable foundation for our study. Furthermore, the OS should serve as a daily driver for personal devices, capable of supporting a wide range of tasks commonly performed by average or power users. This criterion excludes toy or meme OSes as well as specialized distributions like Temple OS, Hannah Montana Linux, AmogOS, Kali Linux, BlackArch Linux, and Garuda Linux ensuring relevance and practicality in our investigation. Finally, accessibility is crucial, necessitating the availability of a virtual machine (VM) image to facilitate experimental demonstrations and testing. By adhering to these criteria, we aimed to select an OS that piques the interest of all contributors and enables us to conduct a comprehensive and meaningful study.

### Why Arch Linux?
A kernel is a software component that serves as the core of an operating system (OS). It acts as an intermediary between the hardware and the software applications running on the computer. The kernel manages system resources, such as memory, CPU, and input/output devices, and provides essential services to applications, such as process management, memory management, and device drivers. While the kernel itself is a software component, it interacts closely with the hardware of the computer. A kernel can be downloaded, as it is typically distributed as part of an operating system package. Many popular operating systems, such as Linux, macOS, and Windows, provide the kernel as part of their installation packages. In terms of the metaphor of the "heart" and "mind" of the operating system, the CPU can be likened to the "heart," as it is responsible for executing instructions and performing computations. However, the kernel serves as the "mind" of the operating system. It controls and coordinates the activities of the CPU and other hardware components, manages system resources, and provides a platform for executing software applications. Without the kernel, the CPU would lack the necessary instructions and management to operate effectively, much like a body without a brain would lack the ability to function cohesively. Therefore, while the CPU is essential for executing instructions, the kernel serves as the central intelligence that orchestrates the operations of the entire operating system.

The Linux kernel stands as a remarkable testament to the power of open-source development, serving as the foundational bedrock upon which a diverse array of Linux distributions (distros) thrive. At the heart of the Linux kernel's extraordinary versatility and capability lies a set of foundational characteristics that make it an ideal base for a multitude of diverse operating systems. Firstly, its modular architecture allows for unparalleled flexibility and customization. The Linux kernel is composed of numerous modules that can be dynamically loaded or unloaded, enabling developers to tailor the operating system to specific requirements without compromising its integrity. This modular design also facilitates efficient resource management and scalability, making it well-suited for a wide range of hardware environments, from embedded devices to supercomputers. Additionally, the Linux kernel is renowned for its stability, reliability, and robustness. Its rigorous development process, which involves thousands of contributors worldwide scrutinizing and improving the code, ensures that it adheres to high standards of quality and security. This stability forms the cornerstone of Linux's reputation as a dependable platform for mission-critical systems and enterprise-level applications. Furthermore, the Linux kernel boasts exceptional performance and efficiency, thanks to its optimized design and emphasis on resource utilization. Its lightweight footprint and support for preemptive multitasking enable it to efficiently manage system resources, ensuring responsive and smooth operation even under heavy workloads. Moreover, the Linux kernel is characterized by its extensive hardware support and compatibility. Its open architecture and standardized interfaces make it easy to port to a wide range of hardware platforms, enabling Linux-based operating systems to run on virtually any device imaginable. This broad compatibility extends to diverse peripherals and devices, further enhancing the versatility and applicability of Linux-based systems. Its modular, adaptable design embodies technical excellence. This flexibility fuels a flourishing ecosystem where creativity knows no bounds. Moreover, the Linux kernel's robustness and reliability underpin the stability and performance of these distros, instilling confidence in users and developers alike. The sheer diversity and ingenuity of Linux distros exemplify the boundless potential of open-source software, demonstrating how a single kernel can inspire an endless tapestry of innovation and empowerment within the technology landscape.

Linux, as a kernel, forms the foundation for a plethora of distributions tailored to diverse needs and preferences. Each distribution is a manifestation of a community's vision, ranging from everyday use to specialized applications like cybersecurity or gaming. In this landscape, Arch Linux stands out as a robust and versatile option. Although its popularity clashes with our first criteria about potential duplication or the likelihood of others selecting it for similar projects, and while alternatives like Debian or Ubuntu exist, Arch's power and flexibility cannot be overlooked. Arch Linux is often esteemed for its robustness and flexibility, setting it apart from counterparts like Ubuntu or Debian. At the heart of its potency lies a distinctive rolling release model, ensuring users have access to the latest software updates seamlessly. This contrasts with the fixed release cycles of Ubuntu and Debian, which may lag behind in incorporating cutting-edge features. Another hallmark of Arch Linux is its unparalleled customizability, empowering users to craft their systems precisely to their specifications. The Arch User Repository (AUR) further enhances this flexibility, offering a vast array of user-contributed packages to expand functionality beyond the standard repository offerings. Moreover, Arch embraces a minimalist philosophy, starting users with a command-line interface (CLI) provides a bare-bones installation that serves as a blank canvas for users to build upon. This minimalist approach not only fosters a deeper understanding of the system's intricacies but also allows for a more optimized and efficient computing experience. The comprehensive documentation and active community support surrounding Arch Linux ensures a rich research experience. The Arch Wiki and forums serve as invaluable resources for troubleshooting, in-depth learning, and sharing knowledge among users. While Arch Linux may present a steeper learning curve compared to Ubuntu or Debian, many users find the challenge rewarding, as it empowers them with a greater mastery over their computing environment. Moreover, Arch serves as a solid foundation for exploring various distributions based on it, such as BlackArch or Garuda, each offering its own spin and specialization. By delving into Arch's ecosystem and its derivatives, we can uncover nuances in performance, usability, and adaptability across different environments. And, while exploring specific distributions of Arch on their own might seem tempting, it could potentially limit the breadth of our study and hinder resource accessibility. The notion that Arch Linux is built upon the Linux kernel is intriguing, but what truly captures attention is the realization that there exist operating systems derived from Arch Linux, which in turn, is derived from the Linux kernel. This phenomenon of operating systems emerging from a derivative of another, essentially forming a "fork of a fork," is nothing short of remarkable and deserves significant recognition. In summary, Arch Linux emerges as an ideal choice for our research endeavor. Its versatility, extensive documentation, and potential for unique exploration make it a compelling option despite the challenges it presents. Through our study, we aim to shed light on the dynamic nature of operating systems and their adaptability to diverse computing environments.


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
