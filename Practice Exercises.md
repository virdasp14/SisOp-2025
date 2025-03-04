# PRACTICE EXERCISES

## Virda Septina Putri

3124500058 / D3 IT B

---

### What are the three main purposes of an operating system?

**Answer:**

The operating system acts as a manager for all hardware and software resources in a computer system. This includes CPU scheduling, memory allocation, storage management, and device handling to ensure everything runs efficiently.

The operating system provides an interface between users and the computer hardware, making it easier for people to interact with the system. This could be through a graphical user interface (GUI) or a command-line interface (CLI).

One of the core jobs of an operating system is to load and execute programs, managing processes and handling input/output operations. It also provides essential services like file management, networking, and security.

---

### We have stressed the need for an operating system to forsake this principle and to "waste" resources? Why is such a system not really wasteful?

**Answer:**

The idea of an operating system "wasting" resources might seem counterintuitive, but in certain contexts, it is done to achieve higher-level goals such as performance optimization, user experience, or system reliability. Here's why such a system is not truly wasteful:

- **Improving Performance Through Redundancy**
- **Enhancing User Experience**
- **Ensuring Reliability and Fault Tolerance**
- **Future-Proofing and Scalability**
- **Trade-Offs for Efficiency**

While it may seem that the OS is "wasting" resources, these practices are strategic and purposeful. They are designed to optimize performance, enhance user experience, ensure reliability, and prepare for future demands.

---

### What is the main difficulty that a programmer must overcome in writing an operating system for a real-time environment?

**Answer:**

One of the biggest challenges in writing an operating system for a real-time environment is meeting strict timing constraints. Unlike general-purpose operating systems, which focus on maximizing resource utilization and responsiveness, real-time systems must guarantee that tasks are completed within a specific deadline. Failure to do so can lead to serious consequences, especially in critical applications like medical devices, automotive control systems, or industrial automation.

---

### Keeping in mind the various definitions of operating systems, consider whether the operating system should include applications such as web browsers and mail programs.

**Answer:**

#### Arguments for inclusion:
- Ease of use and integration.
- Built-in security features.
- Optimized performance for system applications.

#### Arguments against inclusion:
- OS should focus on core functionality.
- Increases system bloat.
- May discourage third-party innovation.

Ultimately, whether an OS should include applications depends on its purpose. Consumer operating systems often benefit from built-in apps for convenience and security, while more modular systems should remain minimalistic.

---

### How does the distinction between kernel mode and user mode function as a rudimentary form of protection (security)?

**Answer:**

The distinction between kernel mode and user mode is a fundamental security mechanism in operating systems. It enforces a strict separation between privileged operations (reserved for the OS kernel) and non-privileged operations (performed by user applications). This prevents user applications from directly accessing or interfering with critical system resources.

---

### Which of the following instructions should be privileged?

- **Privileged Instructions (Kernel Mode):**
  - Set value of timer.
  - Clear memory.
  - Turn off interrupts.
  - Modify entries in the device-status table.
  - Switch from user to kernel mode.
  - Access I/O device.

- **Non-Privileged Instructions (User Mode):**
  - Read the clock.
  - Issue a trap instruction.

---

### Some early computers protected the operating system by placing it in a memory partition that could not be modified. Describe two difficulties with such a scheme.

**Answer:**

1. **Lack of Flexibility for Updates and Bug Fixes:** OS updates and patches would be nearly impossible, requiring inefficient workarounds like replacing memory modules.
2. **Difficulty in Managing Dynamic OS Components:** Modern OS functionalities like device drivers and runtime configurations require modifications, which would be difficult under this scheme.

---

### Some CPUs provide for more than two modes of operation. What are two possible uses of these multiple modes?

**Answer:**

1. **Enhanced Security Through Privilege Levels:** Hierarchical security models can assign different privilege levels to different software components.
2. **Specialized Performance Optimization:** Certain modes can optimize performance for specific tasks.

---

### Timers could be used to compute the current time. Provide a short description of how this could be accomplished.

**Answer:**

1. **System Initialization:** OS sets an initial time based on hardware clocks or NTP servers.
2. **Timer Interrupts:** OS configures a hardware timer to generate periodic interrupts.
3. **Time Computation:** The OS maintains a global time variable that updates on each timer tick.

---

### Give two reasons why caches are useful. What problems do they solve? What problems do they cause?

**Answer:**

**Why caches are useful:**
- **Speed Improvement:** Reduces latency by keeping frequently accessed data close to the processor.
- **Reduced Bottlenecks:** Helps minimize slow disk or memory access.

**Problems caches solve:**
- Minimize delays.
- Reduce I/O operations.

**Problems caches cause:**
- **Coherency Issues:** Ensuring data consistency across multiple processors.
- **Increased Complexity:** Requires intelligent cache management algorithms.

**Why not make the cache as large as the device?**
- **Cost:** Large cache memory is expensive.
- **Volatility:** Most cache memory is volatile, unlike persistent storage.

---

### Distinguish between the client-server and peer-to-peer models of distributed systems.

**Answer:**

| Feature        | Client-Server | Peer-to-Peer |
|---------------|--------------|-------------|
| **Control**    | Centralized  | Decentralized |
| **Scalability** | Can become overloaded | More scalable |
| **Reliability** | Server failure disrupts system | More fault-tolerant |
| **Security**   | Easier to enforce | Harder to secure |

The client-server model works well for centralized management, while peer-to-peer is better for decentralized applications requiring flexibility and resilience.
