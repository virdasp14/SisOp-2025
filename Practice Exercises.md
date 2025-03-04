**PRACTICE EXERCISES**

Virda Septina Putri

3124500058 / D3 IT B

1.1 What are the three main purposes of an operating system?

   Answer:

1. The operating system acts as a manager for all hardware and software resources in a computer system. This includes CPU scheduling, memory allocation, storage management, and device handling to ensure everything runs efficiently.
2. The operating system provides an interface between users and the computer hardware, making it easier for people to interact with the system. This could be through a graphical user interface (GUI) or a command-line interface (CLI).
3. One of the core jobs of an operating system is to load and execute programs, managing processes and handling input/output operations. It also provides essential services like file management, networking, and security.

1.2 We have stressed the need for an operating system to forsake this principle and to "waste" resources? Why is such a system not really wasteful?

Answer: 

 `	`The idea of an operating system "wasting" resources might seem counterintuitive, but in certain contexts, it is done to achieve higher-level goals such as performance optimization, user experience, or system reliability. Here's why such a system is not truly wasteful:

1. Improving Performance Through Redundancy
2. Enhancing User Experience
3. Ensuring Reliability and Fault Tolerance
4. Future-Proofing and Scalability
5. Trade-Offs for Efficiency

While it may seem that the OS is "wasting" resources, these practices are strategic and purposeful. They are designed to optimize performance, enhance user experience, ensure reliability, and prepare for future demands. In this sense, the system is not truly wasteful but rather making intelligent trade-offs to achieve broader goals.

1.3 What is the main difficulty that a programmer must overcome in writing an operating system for a real-time environment?

   Answer:

   `	`One of the biggest challenges in writing an operating system for a real-time environment, is meeting strict timing constraints. Unlike general-purpose operating systems, which focus on maximizing resource utilization and responsiveness, real-time systems must guarantee that tasks are completed within a specific deadline-failure to do so can lead to serious consequences, especially in critical applications like medical devices, automotive control systems, or industrial automation. The main difficulty comes from ensuring that the OS can handle unpredictable workloads while still meeting these deadlines. This requires precise scheduling algorithms, efficient resource management, and handling external inputs in a way that avoids delays. Hard real-time systems, in particular, can’t afford even minor timing variations, so programmers need to design for predictability rather than just raw speed.

1.4 Keeping in mind the various definitions of operating system, consider whether the operating system should include applications such as web browsers and mail programs. Argue both that it should and that it should not, and support your answer.

   Answer:

   Why an operating system should include applications like web browsers and mail programs. One argument in favor of including applications like web browsers and mail clients within the OS is ease of use and integration. If these applications are built directly into the OS, users get a seamless experience without needing to install additional software. This approach is common in consumer-focused operating systems like Windows and macOS, where built-in apps like Edge or Mail provide a default solution right out of the box. Another benefit is better security and system optimization. Since the OS has complete control over built-in applications, it can ensure they are tightly integrated with system security features, such as sandboxing or automatic updates. For instance, an OS-managed browser can be optimized to work efficiently with the system’s networking stack and security policies, reducing vulnerabilities compared to third-party applications.

   Why an operating system should not include these application. On the other hand, there’s a strong argument that an operating system should remain lean and focused on core functionality, such as managing hardware, running processes, and handling security. Including applications like web browsers and email clients risks bloating the OS with unnecessary features that users may not even want. A more modular approach, as seen in Linux distributions, allows users to install the software they need rather than being forced to use built-in applications. This promotes freedom of choice and flexibility, letting users pick the best tools for their needs rather than being locked into whatever the OS provides. Another key issue is competition and innovation. If an OS comes preloaded with applications, it could discourage third-party developers from creating alternatives, potentially stifling innovation. This was a major concern in cases like Microsoft’s bundling of Internet Explorer, which led to antitrust lawsuits.

   Ultimately, whether an OS should include applications depends on its purpose. Consumer operating systems often benefit from built-in apps for convenience and security, while more modular or professional systems should remain minimalistic, giving users the freedom to choose their software. In other words, there’s no single right answer—it depends on what kind of user experience the OS is designed to provide.

1.5 How does the distinction between kernel mode and user mode function as a rudimentary from of protection (security)?

   Answer:

   `	`The distinction between kernel mode and user mode is a fundamental security mechanism in operating systems. It enforces a strict separation between privileged operations (reserved for the OS kernel) and non-privileged operations (performed by user applications). This separation acts as a rudimentary form of protection by preventing user applications from directly accessing or interfering with critical system resources.

1.6 Which of the following instructions should be privileged?

   a. Set value of timer.

   b. Read the clock.

   c. Clear memory.

   d. Issue a trap instruction.

   e. Turn off interrupts.

   f. Modify entries in device-status table.

   g. Switch from user to kernel mode.

   h. Access I/O device.

   Answer:

   `	`privileged instructions are those that can only be executed in kernel mode because they directly impact system resources, security, or overall stability. These instructions must be restricted to prevent user applications from causing crashes, security breaches, or unintended behavior. 

   `	`Priveleged Instructions (must be executed in kernel mode):

a. Set value of timer: The operating system uses a timer to regain control of the CPU (preemptive multitasking). Allowing a user program to change it could let processes run indefinitely, bypassing scheduling policies.
b. Clear memory: Directly modifying memory could lead to data corruption or security issues. Only the operating system should handle memory management.
c. Turn off interrupts: Interrupts ensure the CPU can respond to external events (e.g., I/O operations). If a user program could disable them, it could prevent the system from functioning properly.
d. Modify entries in the device-status table: The device-status table keeps track of hardware interactions. If user programs could modify it, they might interfere with device operations or access restricted hardware.
e. Switch from user to kernel mode: A process should only enter kernel mode through controlled system calls. If any program could switch modes at will, it could bypass security measures and take full control of the system.
f. Access I/O device: Direct access to I/O devices (e.g., disk, printer, network) must be regulated by the to ensure fair access, prevent conflicts, and protect data integrity.

Non-Privileged Instructions (can be executed in user mode):

a. Read the clock: Simply reading the system clock does not pose a security risk. Many applications, like calendars and logs, need access to the current time.
b. Issue a trap instruction: Traps (such as system calls) are a controlled way for user programs to request services from the operating system. Since they transition execution to kernel mode safely, they are allowed in user mode.

1.7 Some early computers protected the operating system by placing it in a memory partition that could not be modified by either the user job or the operating system itself. Describe two difficulties that you think could arise with such a scheme.

Answer: 

1. Lack of Flexibility for Updates and Bug Fixes

   If the OS is locked in an unmodifiable memory partition, fixing bugs, applying security patches, or upgrading the system becomes nearly impossible. Modern operating systems frequently receive updates to improve security, add new features, or fix vulnerabilities. Without the ability to modify the OS, administrators would have to find workarounds-like replacing the entire memory module or relying on external boot mechanisms-which is inefficient and impractical.

2. Difficulty in Managing Dynamic OS Components

   Many modern OS functionalities, such as device drivers, kernel extensions, and runtime configurations, require modifications to system memory. If the OS cannot modify its own code or data structures, adapting to new hardware, loading drivers, or even managing system resources efficiently becomes a challenge. For example, if a new peripheral device is introduced, the OS might need to load a driver into memory-but with this restrictive protection in place, it wouldn't be able to do so.

1.8 Some CPUs provide for more than two modes of operation. What are two possible uses of these multiple modes?

Answer: 

1. Enhanced Security Through Privilege Levels

   Multiple modes can be used to implement a hierarchical security model, where different levels of privilege are assigned to different types of software.

2. Specialized Performance Optimization

   Multiple modes can be used to optimize performance for specific tasks or workloads.

1.9 Timers could be used to compute the current time. Provide a short description of how this could be accomplished.

Answer:

`	`Timers play a crucial role in an operating system, including keeping track of the current time. Here's how a timer can be used to compute the current time:

1. System Initialization: When the OS starts, it sets an initial time value, usually based on hardware clocks, a real-time clock (RTC) chip, or a network time protocol (NTP) server.
2. Timer Interrupts: The OS configures a hardware timer to generate periodic interrupts at a fixed interval (e.g., every millisecond). Each time the timer generates an interrupt, the OS increments a counter that represents the passage of time.
3. Time Computation:
   a. The OS maintains a global time variable, which updates every timer interrupt.
   b. By counting the number of timer ticks since startup, the OS can calculate the current time by converting ticks into seconds, minutes, and hours.
4. Providing the Current Time:
   a. When an application requests the current time, the OS reads the stored value from the global time variable and returns the computed time.
   b. If necessary, the OS can also adjust the time based on an external source (e.g., NTP servers) to maintain accuracy.

1.10. Give two reasons why caches are useful. What problems do they solve? What problems do they cause? If a cache can be made as large as the device for which it is caching (for instance, a cache as large as a disk), why not make it that large and eliminate the device?

Answer: 

`	`Caches play a crucial role in improving system performance by storing frequently accessed data closer to the processor.

Why caches are useful: 

1. Speed Improvement: accessing data from main memory (RAM) or disk storage is significantly slower than accessing it from a cache. By keeping frequently used data in a smaller, faster memory location, caches reduce latency and improve system performance.
2. Reduced Bottlenecks: Since caches store copies of recently accessed data, they help reduce the load on slower storage devices like hard drives or even RAM. This improves the overall efficiency of the system and prevents unnecessary delays.

Problems caches solve:

1. Minimize Delays: Caches reduce the time gap between CPU execution speed and memory access speed.
2. Decrease I/O Operations: Frequent disk access can slow down performance. Caching reduces the number of reads/writes needed, improving responsiveness.

Problems caches cause:

1. Coherency Issues: If multiple processors or systems are using the same data, ensuring they all have the most up-to-date version becomes challenging. This is known as the cache coherence problem and requires complex mechanisms to resolve.
2. Increased Complexity: Managing cache replacement (deciding what stays in the cache and what gets removed) requires intelligent algorithms like LRU (Least Recently Used) or FIFO (First In, First Out). Poor cache management can actually slow down performance instead of improving it.

But, Why not just make the cache as large as the device?

1. Cost: Cache memory (such as SRAM or high-speed DRAM) is much more expensive than traditional storage. A large cache the size of a hard drive would be financially impractical.
2. Volatility: Most caches use volatile memory, meaning they lose their data when the system is powered off. A hard disk or SSD, on the other hand, provides persistent storage, which is essential for long-term data retention.

1.11 Distinguish between the client-server and peer-to-peer models of dis-tributed systems.

Answer:

`	`The client-server model works well for systems needing central management and security, while peer-to-peer is better for decentralized applications that require flexibility and resilience. Many modern systems, like cloud computing and hybrid networks, actually use a mix of both to balance efficiency and reliability.

	

|Feature|Client-server|Peer-to-peer|
| :- | :- | :- |
|Control|Centralized (server manages everything)|Decentralized (all peers are equal)|
|Scalability|Can become overloaded|More scalable as peers share the load|
|Reliability|Server failure disrupts the system|More fault-tolerant|
|Security|Easier to enforce security policies|Harder to secure due to lack of central control|


