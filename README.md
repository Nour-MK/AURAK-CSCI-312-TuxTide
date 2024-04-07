# <p align="center">TuxTide[^1]: An OS Case Study</p>
## <p align="center">Analyzing Arch Linux's Versatility from Desktop to Cloud</p>
[^1]: The title "TuxTide" (i.e. Tux Tide) represents a convergence associated with Tux, the Linux mascot. It implies a surge or wave of activity, innovation, or prominence related to Linux or open-source technology and suggests the powerful force and momentum driven by the Linux community (both developers and users), with Tux as its emblem.

![](Assets/banner.png)
<!-- Badge icons found at https://feathericons.com/ and view stats at https://yhype.me/github/accounts/Nour-MK/TuxTide/traffic -->
<p align="center">
  <a href="https://custom-icon-badges.demolab.com/badge/Project%20Status-Work%20in%20Progress-1793d1?style=for-the-badge&logo=activity&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Project%20Status-Work%20in%20Progress-1793d1?style=for-the-badge&logo=activity&logoSource=feather&logoColor=white" alt="Project Status" title="Project Status" style="vertical-align:top; margin:4px"></a>
  <a href="https://custom-icon-badges.demolab.com/badge/Word%20Count-5k-1793d1?style=for-the-badge&logo=type&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Word%20Count-5k-1793d1?style=for-the-badge&logo=type&logoSource=feather&logoColor=white" alt="Word Count" title="Word Count" style="vertical-align:top; margin:4px"></a>
  <a href="https://custom-icon-badges.demolab.com/badge/Views%20Count-5k-1793d1?style=for-the-badge&logo=eye&logoSource=feather&logoColor=white">
    <img src="https://custom-icon-badges.demolab.com/badge/Views%20Count-386-1793d1?style=for-the-badge&logo=eye&logoSource=feather&logoColor=white" alt="Views Count" title="Views Count" style="vertical-align:top; margin:4px"></a>
</p>

This study aims to academically investigate operating systems, focusing on Arch Linux. It begins with an Executive Summary and Glossary to provide brief insights and clarify technical terms used throughout the study. The Introduction section outlines the criteria for selecting operating systems and presents background information on Linux and Arch Linux history. Parts 1 and 2 discuss Arch Linux's functionality as both a Daily Driver OS and a Cloud Computing OS. Additionally, Part 2 compares Arch Linux's roles in daily usage and cloud computing environments, analyzing factors such as implementation, performance, hardware support, community and support, updates and stability, as well as licensing and cost considerations. Part 3 addresses Additional Considerations, including legal and ethical issues related to operating systems and proposing potential solutions. The study concludes by giving an overview to recap all discussed findings, comparing Linux with mainstream operating systems like Windows and macOS, suggesting avenues for further research, and considering the possibility of constructing a custom Linux distribution of our own! Finally, a list of resources is provided for reference and further exploration.

## Work Distribution & Acknowledgements
| | Member            | ID        | Contact                                                                                        | Task |
|-|-------------------|-----------|------------------------------------------------------------------------------------------------|------|
|1| Urita Sadallah    | 2021004899| [Email](mailto:urita.sadallah@aurak.ac.ae), [Github](https://github.com/uritaaquila)         | 1. Conducted research on synchronization. <br> 2. Conducted research on deadlock. <br> 3. Prepared presentation slides. |
|2| Mohamed Abouissa  | 2021005188| [Email](mailto:mohamed.abouissa@aurak.ac.ae), [Github](https://github.com/Mohamed-Abouissa)   | 1. Conducted research on introduction. <br> 2. Conducted research on memory management. <br> 3. Conducted research on file management. |
|3| Khawla Alhammadi  | 2021004956| [Email](mailto:khawla.alhammadi@aurak.ac.ae), [Github](https://github.com/Khawlaalh)                                                  | 1. Prepared executive summary. <br> 2. Compiled a glossary in the footnotes. <br> 3. Conducted research on OS trends. |
|4| Sarah Alsuwaidi   | 2021004782| [Email](mailto:sarah.alsuwaidi@aurak.ac.ae), [Github](https://github.com/SarahAlsuwaidi)                                                   | 1. Conducted research on cloud computing OSes. <br> 2. Compared OS of Part 1 with OS of Part 2. <br> 3. Conducted research on legal and ethical issues.  |
|5| Ahmad Hammoudeh   | 2021004915| [Email](mailto:ahmad.hammoudeh@aurak.ac.ae), [Github](https://github.com/ahmaadmohd)          | 1. Provided solutions to issues identified. <br> 2. Wrote the conclusion. <br> 3. Formatted resources in APA 7th edition style. |
|6| Nour Mohamed      | 2021004938| [Email](mailto:nour.mohamed@aurak.ac.ae), [Github](https://github.com/Nour-MK)                  | 1. Conducted research on process and threads. <br> 2. Conducted research on process scheduling. <br> 3. Exported case study to various formats. |


We extend our sincere appreciation to Dr. Zubaidah Al-Hazza for her invaluable guidance, encouragement, and support throughout this research project. Her expertise and insightful feedback have significantly contributed to the completion of this study.


## Table of Contents
<details>
  <summary> Click to expand/collapse</summary>

1. [Executive Summary](#executive-summary)
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

</details>


## Executive Summary

<details>
  <summary> Click to expand/collapse</summary>

</details>

## Introduction

<details>
  <summary> Click to expand/collapse</summary>

### Criteria for Choosing the Operating Systems in Parts 1 & 2
Choosing an operating system (OS) for our research and case study is a critical decision that warrants careful consideration. In selecting the operating system (OS) for our study, several key criteria were considered to ensure an immersive and engaging research experience. Firstly, the OS should not be widely recognized or mainstream to avoid duplication of efforts with classmates, fostering a unique and stimulating exploration and presentation of key findings. This requirement eliminates OSes such as Windows, macOS, Ubuntu, and Android. Secondly, the OS must be fully open-source as this allows us to freely inspect the source code, providing a firsthand understanding of its underlying architecture and infrastructure. This transparency empowers us to delve deeper into the OS's mechanisms, gaining insights that may not be readily available with closed-source alternatives. Additionally, the vast community surrounding open-source OSes serves as a valuable resource. Many community members have likely encountered and addressed the same questions and challenges we will face, offering a wealth of knowledge and expertise to draw from. This collaborative ecosystem enhances our learning process, enabling us to leverage the collective wisdom and experiences of those who have traversed similar paths before us. Additionally, the chosen OS must demonstrate maturity, offering comprehensive documentation and resources for thorough research. This requirement eliminates new or incomplete OS releases like Fuchsia, dahliaOS, ChromeOS, and Rhino Linux ensuring a stable foundation for our study. Furthermore, the OS should serve as a daily driver for personal devices, capable of supporting a wide range of tasks commonly performed by average or power users. This criterion excludes toy or meme OSes as well as specialized distributions like Temple OS, Hannah Montana Linux, AmogOS, Kali Linux, BlackArch Linux, and Garuda Linux ensuring relevance and practicality in our investigation. Finally, accessibility is crucial, necessitating the availability of a virtual machine (VM) image to facilitate experimental demonstrations and testing. By adhering to these criteria, we aimed to select an OS that piques the interest of all contributors and enables us to conduct a comprehensive and meaningful study.

#### Why Arch Linux?
A kernel is a software component that serves as the core of an operating system (OS). It acts as an intermediary between the hardware and the software applications running on the computer. The kernel manages system resources, such as memory, CPU, and input/output devices, and provides essential services to applications, such as process management, memory management, and device drivers. While the kernel itself is a software component, it interacts closely with the hardware of the computer. A kernel can be downloaded, as it is typically distributed as part of an operating system package. Many popular operating systems, such as Linux, macOS, and Windows, provide the kernel as part of their installation packages. In terms of the metaphor of the "heart" and "mind" of the operating system, the CPU can be likened to the "heart," as it is responsible for executing instructions and performing computations. However, the kernel serves as the "mind" of the operating system. It controls and coordinates the activities of the CPU and other hardware components, manages system resources, and provides a platform for executing software applications. Without the kernel, the CPU would lack the necessary instructions and management to operate effectively, much like a body without a brain would lack the ability to function cohesively. Therefore, while the CPU is essential for executing instructions, the kernel serves as the central intelligence that orchestrates the operations of the entire operating system.

The Linux kernel stands as a remarkable testament to the power of open-source development, serving as the foundational bedrock upon which a diverse array of Linux distributions (distros) thrive. At the heart of the Linux kernel's extraordinary versatility and capability lies a set of foundational characteristics that make it an ideal base for a multitude of diverse operating systems. Firstly, its modular architecture allows for unparalleled flexibility and customization. The Linux kernel is composed of numerous modules that can be dynamically loaded or unloaded, enabling developers to tailor the operating system to specific requirements without compromising its integrity. This modular design also facilitates efficient resource management and scalability, making it well-suited for a wide range of hardware environments, from embedded devices to supercomputers. Additionally, the Linux kernel is renowned for its stability, reliability, and robustness. Its rigorous development process, which involves thousands of contributors worldwide scrutinizing and improving the code, ensures that it adheres to high standards of quality and security. This stability forms the cornerstone of Linux's reputation as a dependable platform for mission-critical systems and enterprise-level applications. Furthermore, the Linux kernel boasts exceptional performance and efficiency, thanks to its optimized design and emphasis on resource utilization. Its lightweight footprint and support for preemptive multitasking enable it to efficiently manage system resources, ensuring responsive and smooth operation even under heavy workloads. Moreover, the Linux kernel is characterized by its extensive hardware support and compatibility. Its open architecture and standardized interfaces make it easy to port to a wide range of hardware platforms, enabling Linux-based operating systems to run on virtually any device imaginable. This broad compatibility extends to diverse peripherals and devices, further enhancing the versatility and applicability of Linux-based systems. Its modular, adaptable design embodies technical excellence. This flexibility fuels a flourishing ecosystem where creativity knows no bounds. Moreover, the Linux kernel's robustness and reliability underpin the stability and performance of these distros, instilling confidence in users and developers alike. The sheer diversity and ingenuity of Linux distros exemplify the boundless potential of open-source software, demonstrating how a single kernel can inspire an endless tapestry of innovation and empowerment within the technology landscape.

Linux, as a kernel, forms the foundation for a plethora of distributions tailored to diverse needs and preferences. Each distribution is a manifestation of a community's vision, ranging from everyday use to specialized applications like cybersecurity or gaming. In this landscape, Arch Linux stands out as a robust and versatile option. Although its popularity clashes with our first criteria about potential duplication or the likelihood of others selecting it for similar projects, and while alternatives like Debian or Ubuntu exist, Arch's power and flexibility cannot be overlooked. Arch Linux is often esteemed for its robustness and flexibility, setting it apart from counterparts like Ubuntu or Debian. At the heart of its potency lies a distinctive rolling release model, ensuring users have access to the latest software updates seamlessly. This contrasts with the fixed release cycles of Ubuntu and Debian, which may lag behind in incorporating cutting-edge features. Another hallmark of Arch Linux is its unparalleled customizability, empowering users to craft their systems precisely to their specifications. The Arch User Repository (AUR) further enhances this flexibility, offering a vast array of user-contributed packages to expand functionality beyond the standard repository offerings. Moreover, Arch embraces a minimalist philosophy, starting users with a command-line interface (CLI) provides a bare-bones installation that serves as a blank canvas for users to build upon. This minimalist approach not only fosters a deeper understanding of the system's intricacies but also allows for a more optimized and efficient computing experience. The comprehensive documentation and active community support surrounding Arch Linux ensures a rich research experience. The Arch Wiki and forums serve as invaluable resources for troubleshooting, in-depth learning, and sharing knowledge among users. While Arch Linux may present a steeper learning curve compared to Ubuntu or Debian, many users find the challenge rewarding, as it empowers them with a greater mastery over their computing environment. Moreover, Arch serves as a solid foundation for exploring various distributions based on it, such as BlackArch or Garuda, each offering its own spin and specialization. By delving into Arch's ecosystem and its derivatives, we can uncover nuances in performance, usability, and adaptability across different environments. And, while exploring specific distributions of Arch on their own might seem tempting, it could potentially limit the breadth of our study and hinder resource accessibility. The notion that Arch Linux is built upon the Linux kernel is intriguing, but what truly captures attention is the realization that there exist operating systems derived from Arch Linux, which in turn, is derived from the Linux kernel. This phenomenon of operating systems emerging from a derivative of another, essentially forming a "fork of a fork," is nothing short of remarkable and deserves significant recognition. In summary, Arch Linux emerges as an ideal choice for our research endeavor. Its versatility, extensive documentation, and potential for unique exploration make it a compelling option despite the challenges it presents. Through our study, we aim to shed light on the dynamic nature of operating systems and their adaptability to diverse computing environments.


### Background Information
#### The Man & The Penguin
> Only wimps use tape backup. Real men just upload their [important stuff](https://github.com/torvalds/linux) on ftp and let the rest of the world mirror it. **— Linus Torvalds**
#### Linux History
Linux is a popular open-source operating system, it was created by Linus Torvalds in 1991, at that time, Torvalds was a computer science student at the University of Helsinki, Finland, and started working on the Linux project as a personal enterprise. The name Linux is a combination of his name, Linus, and Unix, the operating system that inspired his projects. At that time, most operating systems were proprietary and expensive, Torvalds wanted to create an operating system that could be made freely available to anyone who wanted to use it. It initially released Linux as free software under the GNU General Public License (GPL), which means anyone can use, modify and redistribute its source code. The first versions of Linux were mainly used by technology enthusiasts and software developers, but over time it has gained popularity and is used in many different types of devices such as computers, servers, smartphones and embedded systems. Linux is considered one of the most stable, secure, and reliable operating systems and is widely used in servers, supercomputers, and enterprise environments. Today, Linux is one of the most widely used operating systems in the world, with an estimated 5.53% of all desktop computers and more than 90% of the world’s top supercomputers running on Linux, and approx. 71.85% of all mobile devices run on Android, which is Linux-based. The Linux community has grown with thousands of developers and users working to create and maintain the operating system.

The Linux operating system is a type of operating system similar to Unix and based on the Linux kernel, but the Linux kernel alone is not enough to create a complete operating system. A complete Linux system package is called a distribution, many Linux distributions are available to satisfy almost any of your computing needs, and most distributions are customized for a specific user group, such as professional users, multimedia enthusiasts, software developers, or casual home users, each custom distribution includes the necessary software packages to support specialized features, such as audio and video editing software for multimedia enthusiasts or compilers and environments, integrated development for software developers. Linux distributions are commonly categorized into three main types, each catering to distinct user preferences and needs. Firstly, there are the "Rolling Release" distributions, characterized by their continuous and incremental updates, offering users access to the latest software versions as soon as they are available. These distributions prioritize cutting-edge features and frequent updates, appealing to users who desire the latest software advancements and are comfortable with potential instability. On the other end of the spectrum are the "Fixed Release" distributions, which adhere to a scheduled release cycle, typically offering long-term support (LTS) versions with extended stability and security updates. These distributions prioritize reliability and predictability, making them suitable for production environments and users who prioritize stability over bleeding-edge features. Lastly, there are the "Specialized" distributions, which are tailored to specific use cases or target audiences, such as gaming, cybersecurity, multimedia production, or education. These distributions often come pre-configured with specialized software and tools optimized for their intended purpose, providing users with a focused and streamlined experience. Overall, these three categories encompass the diverse array of Linux distributions available, each offering unique benefits and catering to a broad spectrum of user needs and preferences. Furthermore, different Linux distributions are often divided into three main categories based on their installation medium: Live CD, Installation CD, and Network Installation. Live CDs allow users to boot directly into a fully functional Linux environment without needing to install anything on their system. They are commonly used for testing and demonstration purposes. Installation CDs, on the other hand, are used to install the Linux distribution onto a hard drive or other storage device. They typically include an installer that guides users through the installation process. Network Installation involves downloading the necessary files from the internet during the installation process. This method is useful for systems without optical drives or for users who want to ensure they have the latest software versions during installation. Each of these categories offers different advantages and is suited to different use cases, providing users with flexibility and choice when installing Linux.

The Linux architecture can be depicted as a layered structure. Starting from the bottom, these layers are hardware, kernel, shell, and applications. The lowest level of the Linux architecture is the hardware layer. This layer comprises the physical components of a computer, such as the hard drive, RAM, motherboard, CPU, network interfaces, and peripherals. These components are the tangible pieces of your system on which the rest of the architecture is built. As the core of the system, the kernel performs important low-level tasks including disk management, task scheduling, memory allocation, and peripheral operations which are fundamental to efficient mining operations and system stability, the Linux kernel is designed as a monolithic entity, integrating device drivers, file systems, system server calls, and countless other important components into a single static binary, this design choice facilitates direct and efficient execution of processes granting the kernel a high degree of control over system resources and thus ensuring strong performance and reliability. Communicating directly with the system hardware, the kernel’s role is essential in optimizing system performance and stability as it translates high-level application requirements into low-level hardware instructions ensuring that the software operates efficiently while making the best use of available resources, the kernel’s architecture not only promotes seamless interaction with hardware but also supports the system’s ability to support a variety of computing tasks from everyday desktop use to managing applications, complex computer and server environments, continuously refined and enhanced by a global community of developers the Linux kernel evolves to meet the needs of modern computing maintaining its position as the foundation of the Linux operating system known for its efficiency, stability and adaptability. Just above the kernel in the Linux hierarchy is the shell; an essential component that serves as the main interface between the user and the underlying operating system. At its core, the shell provides a user-friendly platform through which commands are issued and executed allowing users to interact with the kernel and perform a variety of tasks. Although most shell interactions occur in the command line interface (CLI), where the user enters commands for the shell to interpret, it is important to note that the shell can also display itself in a graphical user interface (GUI) providing other means of interaction. Linux offers a wide variety of shell options each offering its own set of features and syntax to meet different user preferences and requirements. Among the most widely used shells is Bourne Again Shell (bash), known for its flexibility and extensive functionality making it the default choice for many Linux distributions. Additionally, users have the option to explore alternatives such as C Shell (csh) which has a C-like syntax, and Z Shell (zsh), known for its advanced customization options and interoperability. Choosing a shell often depends on factors such as script ability ease of use and compatibility with existing workflows allowing users to tailor their Linux experience to their individual needs. At the top of the Linux architecture is the application layer which represents the software that directly engages users in their computing experience. These applications include many features, meeting the diverse needs and preferences of users from essential system utilities like file managers, text editors, and network managers to apps like web browsers and productivity tools. Although applications serve as the primary interface for user interaction, their functionality relies on transparent communication with the underlying hardware and middleware. When users interact with applications, by issuing commands to open files, for example, this process requires coordinated effort across multiple layers of the Linux architecture. The shell interprets user commands and acts as a channel through which instructions are relayed to the kernel, which, in turn, coordinates the retrieval and manipulation of data from the hardware. Ultimately, the application performs the desired action whether it's displaying a file in a text editor or displaying a web page in a browser, making it easier for users to interact with the system. This complex interaction between applications, shell, and kernel highlights the cohesive nature of the Linux ecosystem where each layer works in harmony with the other to deliver a seamless and responsive computing experience. By leveraging the capabilities of applications users can exploit the full potential of the Linux operating system opening up countless possibilities for productivity, creativity, and exploration. Linux’s rich application ecosystem allows users to tailor their computing environment to their personal needs, promoting a user experience that is smooth, dynamic, and attractive to use.


#### Arch Linux History


</details>


## Part 1: Daily Driver OS (Arch Linux)

<details>
  <summary> Click to expand/collapse</summary>

### Process and Threads
### Process Scheduling
### Synchronization
Arch Linux, being a distribution of Linux, utilizes various synchronization mechanisms provided by the Linux kernel. These mechanisms include (but are not limited to):
1. **Mutexes and Semaphores:** Arch Linux uses mutexes and semaphores to control access to shared resources among processes. Mutexes allow exclusive access to a resource, while semaphores allow both exclusive and shared access based on a count. The Linux kernel provides an implementation of semaphores, which are declared and initialized using the `struct semaphore` type. Semaphores can be created directly and initialized using `void sema_init(struct semaphore *sem, int val);` where `val` is the initial value to assign to a semaphore. Another way is using helper functions and macros like `DECLARE_MUTEX(name);` and `DECLARE_MUTEX_LOCKED(name);`. In this scenario, the outcome is a semaphore variable named `name` that gets initialized to 1 via `DECLARE_MUTEX` or 0 via `DECLARE_MUTEX_LOCKED`. In the latter scenario, the mutex commences in a locked state, necessitating explicit unlocking before any thread can gain access. For cases where the mutex needs to be initialized during runtime, such as when dynamically allocated, utilize either of the functions `void init_MUTEX(struct semaphore *sem);` or `void init_MUTEX_LOCKED(struct semaphore *sem);`. Further, the `down` function decrements the value of the semaphore, while `down_interruptible` allows interruption and `down_trylock` returns immediately if the semaphore is unavailable. There are three versions of down: `void down(struct semaphore *sem);`, `int down_interruptible(struct semaphore *sem);`, and `int down_trylock(struct semaphore *sem);`. After a thread has effectively invoked one of the variants of `down`, it's considered to be "holding" the semaphore. Subsequently, that thread is granted access to the critical section guarded by the semaphore. Upon completing operations necessitating mutual exclusion, the semaphore must be relinquished. The `void up(struct semaphore *sem);` function is used to increment the value of a semaphore, effectively releasing a resource. When you call `up()` on a semaphore, it increases the semaphore count, which indicates that a resource has become available. This allows other processes or threads waiting on that semaphore to proceed, potentially accessing the shared resource it guards. Proper handling of semaphores, especially in error paths, is crucial to prevent processes from hanging and ensure system stability. [Tap to view figures](Assets/banner.png)
2. **Spinlocks:** are used to protect critical sections of code from simultaneous access by multiple threads. When a thread tries to acquire a spinlock that is already held by another thread, it spins in a loop until the lock becomes available. Semaphores and spinlocks are essential mechanisms in the Linux kernel for ensuring mutual exclusion. While semaphores are versatile and can handle sleeping processes, spinlocks are primarily used in non-sleeping contexts like interrupt handlers, offering higher performance. Spinlocks operate by repeatedly checking for lock availability, with atomic operations ensuring thread safety and deadlock avoidance. They are typically employed in multiprocessor systems but are also relevant for uniprocessor systems with preemptive kernels due to concurrency concerns. Proper locking mechanisms are crucial even in uniprocessor systems without preemption to prevent infinite spinning. The necessary header file for the spinlock primitives is `<linux/spinlock.h>`. A spinlock is represented by the data type `spinlock_t`. Similar to other data structures, a spinlock needs initialization. This can occur during compilation using `spinlock_t my_lock = SPIN_LOCK_UNLOCKED;` or during runtime using `void spin_lock_init(spinlock_t *lock);`. Prior to entering a critical section, the code must acquire the required lock through `void spin_lock(spinlock_t *lock);`. It's important to note that all spinlock waits are inherently uninterruptible. Once `spin_lock` is called, the code will spin until the lock becomes available. To release a previously obtained lock, use `void spin_unlock(spinlock_t *lock);`.
3. **Read-Write Locks:** Arch Linux employs read-write locks to allow concurrent read access to a resource while ensuring exclusive write access. This mechanism enhances performance by permitting multiple readers simultaneously but ensuring only one writer at a time. The Linux kernel offers a specialized semaphore type known as `rwsem`, or "reader/writer semaphore," which is occasionally beneficial in driver development. Including `<linux/rwsem.h>` is necessary for code utilizing rwsems. The relevant data structure for reader/writer semaphores is `struct rw_semaphore`, requiring explicit initialization at runtime with `void init_rwsem(struct rw_semaphore *sem);`. A freshly initialized rwsem is ready for the next task (either reader or writer). For read-only access, code interfaces with `void down_read(struct rw_semaphore *sem);`, `int down_read_trylock(struct rw_semaphore *sem);`, and `void up_read(struct rw_semaphore *sem);` such that `down_read` grants read-only access to protected resources, possibly concurrently with other readers and `down_read_trylock` returns nonzero if access was granted immediately, else 0. Success with `down_read` necessitates releasing the rwsem with `up_read`. Similarly, for writers, the functions `void down_write(struct rw_semaphore *sem);`, `int down_write_trylock(struct rw_semaphore *sem);`, `void up_write(struct rw_semaphore *sem);`, and `void downgrade_write(struct rw_semaphore *sem);` are used. These functions behave akin to their reader counterparts, providing write access. `downgrade_write` allows other readers in after performing quick changes. An `rwsem` permits either one writer or numerous readers to hold the semaphore. Writers take precedence, halting reader access until all writers conclude their tasks. This design can result in reader starvation if many writers contend for the semaphore, thus rwsems are best suited for scenarios where write access is infrequent and short-lived.
4. **Atomic Operations:** ensure that certain operations on shared data structures are performed indivisibly, without interruption. Arch Linux utilizes atomic operations extensively for synchronization purposes. Linux offers two categories of atomic operations: those involving integer variables and those focusing on individual bits within variables. Atomic operations on integer variables in C, such as `a = a + 1`, don't guarantee atomicity in the Linux kernel. To address this, Linux introduces the `atomic_t` data type to distinguish between atomic and non-atomic operations. Declaration of an `atomic_t` variable follows the format `atomic_t variable;`, indicating that this variable is intended for atomic operations only. The Linux kernel provides various functions for atomic operations on atomic variables, including:
    1. `atomic_set(atomic_t *a, int value);` // Sets the value at memory location a
    2. `atomic_add(int val, atomic_t *a);` // Adds val to the value at memory location a
    3. `atomic_read(const atomic_t *a);` // Reads the value of the atomic_t at a
    4. `atomic_inc(atomic_t *a);` // Increments the value at a atomically
    5. `atomic_dec(atomic_t *a);` // Decrements the value at a atomically
    6. `atomic_sub(int val, atomic_t *a);` // Subtracts the value at a by the amount val
5. **Lightweight PI-futexes:** Lightweight Priority Inheritance Futexes (Fast User-space Mutex) are an advanced synchronization mechanism in the Linux kernel designed for efficient user-space synchronization. Arch Linux harnesses Lightweight PI-futexes to implement sophisticated synchronization constructs within user-space applications, ensuring optimal performance and reliability. The reason we use Priority Inheritance is that implementing PI in user-space aids determinism for applications, optimizing latencies. In user-space, PI-enabled pthread mutexes work similarly to futex-based locks, with atomic operations handling locking and unlocking without kernel involvement. For the slow path, two new futex operations are introduced: `FUTEX_LOCK_PI` and `FUTEX_UNLOCK_PI`. If lock acquisition fails, `FUTEX_LOCK_PI` is invoked, initiating kernel tasks to establish a futex queue and assign a 'PI state' structure. Once acquired, the task updates the futex value and returns ownership to user-space. If unlock succeeds, no kernel operations occur. If it fails due to the `FUTEX_WAITERS` bit being set, `FUTEX_UNLOCK_PI` is called, unlocking the futex and releasing associated resources in the kernel. In Linux, PI-futexes are used to prevent priority inversion in synchronization scenarios. Priority inversion occurs when a low-priority thread holds a lock needed by a high-priority thread, causing the high-priority thread to wait unnecessarily. With PI-futexes, the priority of the holder of a lock is temporarily boosted to the priority of the waiting thread, thus preventing priority inversion. 'Robustness' and 'PI' are independent futex properties: This indicates that the properties of being "robust" (ensuring proper behavior even if a thread is terminated abruptly) and being a PI-futex are separate attributes. In other words, a futex can be either robust or PI, or it can possess both properties simultaneously, or none of them. Futexes can have the following combinations of properties: (Not robust, not PI), (Robust, not PI), (Not robust, PI), or (Robust, PI). They are called "lightweight" for three main reasons:
    1. In user-space fast paths, PI-enabled futexes require no kernel intervention or additional complexity. There are no registration or extra kernel calls; just fast atomic operations in user-space.
    2. Even in slow paths, the system call and scheduling pattern closely resemble regular futexes, maintaining efficiency.
    3. The in-kernel PI implementation simplifies around the mutex abstraction, with strict rules like single ownership and no recursive locking.

### Deadlock
Arch Linux, like other Unix-like operating systems, employs various strategies to prevent and handle deadlocks, ensuring system stability and reliability. These strategies include (but are not limited to):
1. **Resource Ordering:** Arch Linux encourages developers to adhere to a strict order when acquiring multiple resources. By consistently acquiring resources in the same predetermined order, the system reduces the likelihood of circular dependencies that can lead to deadlocks. For example, if a process requires both resource A and resource B, it should always acquire resource A before attempting to acquire resource B.
2. **Timeouts:** In scenarios where deadlocks cannot be entirely prevented, Arch Linux may implement timeout mechanisms. Threads attempting to acquire resources may be subject to a specified time limit. If a thread is unable to obtain the necessary resources within this timeframe, it releases the resources it currently holds and retries later. This approach prevents threads from indefinitely blocking due to deadlock situations, promoting system responsiveness.
3. **Deadlock Detection:** Arch Linux may utilize deadlock detection algorithms to proactively identify and resolve deadlocks. These algorithms periodically analyze the resource allocation graph to detect cycles indicative of potential deadlocks. Upon detection, the system takes appropriate measures to break the deadlock, such as releasing resources or forcibly terminating processes involved in the deadlock. By swiftly addressing deadlock conditions, Arch Linux minimizes their impact on system performance and user experience.
4. **Resource Preemption:** In critical scenarios, Arch Linux may employ resource preemption to break potential deadlocks. This involves preemptively revoking resources from processes to resolve deadlock situations. For instance, if a process holds a resource required by another process to progress, Arch Linux may forcibly reclaim the resource from the holding process, allowing the dependent process to proceed. Resource preemption ensures the timely resolution of deadlocks, preventing prolonged system stagnation and facilitating continuous operation.

### Memory Management
### File Management

</details>

## Part 2: Cloud Computing OS (Arch Linux)

<details>
  <summary> Click to expand/collapse</summary>

### Trends in Operating Systems
### What Constitutes a Cloud Computing OS?
### Comparison with OS of Part 1
#### Implementation-wise
#### Performance-wise
#### Hardware Support
#### Community and Support
#### Updates and Stability
#### Licensing and Cost

</details>


## Part 3: Additional Considerations (Best Practices in OS)

<details>
  <summary> Click to expand/collapse</summary>

### Legal and Ethical Issues
> A lot of that momentum comes from the fact that Linux is free. **— Nat Friedman**
### Solutions to Issues

</details>


## Conclusion

<details>
  <summary> Click to expand/collapse</summary>

### Overview
### Linux vs. Our Current Daily Drivers
#### Linux vs. Windows
> If Microsoft ever does applications for Linux it means I've won. **— Linus Torvalds**
#### Linux vs. macOS
### Further Research
### Building Our Own Distro!

</details>


## Resources

<details>
  <summary> Click to expand/collapse</summary>

</details>

## Terms of Use
Copyright © 2024 All Contributors

This case study is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://github.com/Nour-MK/TuxTide/blob/main/LICENSE.txt). Individuals are permitted to share and distribute the work non-commercially, provided proper attribution is given to all contributors. However, derivative works based on this material are not allowed without prior permission from [@Nour-MK.](https://github.com/Nour-MK), even if they comply with the terms of the CC BY-NC-ND 4.0 license.

This publication adheres to all regulatory laws and guidelines established by the American University of Ras Al Khaimah (AURAK) regarding the dissemination of academic materials.
