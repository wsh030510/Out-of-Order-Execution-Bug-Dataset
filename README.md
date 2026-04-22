MGO-OOO-Bugs: A Benchmark of Multi-Granularity Out-of-Order Concurrency Bugs﻿

This repository contains the dataset for our paper on "Out-of-Order (OOO) Execution Bugs" under Weak Memory Models (WMM). We propose a Multi-Granularity Ordering (MGO) taxonomy and collect 58 OOO bug samples across different system abstraction layers.

📂 Repository Structure (MGO Taxonomy)
Our dataset is strictly categorized into three layers based on the triggering level of the concurrency bugs:
* **[Layer1](./Layer1)**: Micro-Instruction Level (32 Samples). Focuses on pure hardware-sensitive reorderings (Store-Store, Store-Load) in fundamental lock-free data structures (e.g., Spinlocks, Ring Buffers).
* **[Layer2](./Layer2)**: Resource Lifecycle Level (24 Samples). Focuses on hardware-agnostic and OS-level reorderings, typically manifesting as Use-After-Free (UAF) or Kernel Panics driven by thread scheduling or interrupts (e.g., Linux Kernel, Drivers).
* **[Layer3](./Layer3)**: Semantic Logic Level (2 Samples). Focuses on complex state machine or protocol disruptions in high-performance distributed systems and networking frameworks (e.g., MySQL, DPDK, sofa-pbrpc).

🏷️ Label Definitions
* **Bug Id**: Our own defined internal reference number for the bug (e.g., L1-01).
* **Issue No**: The official bug tracking number, CVE ID, or discussion thread (e.g., GitHub issue #XXXXX).
* **Status**: The current resolution status of the bug in its original repository.
* **Type**: The specific manifestation or category of the concurrency error (e.g., UAF, Deadlock, Store-Load reordering).
* **Registered**: The date the bug was initially reported or raised by the community.
* **Resolved**: The date the bug was officially fixed or closed by the developers.
