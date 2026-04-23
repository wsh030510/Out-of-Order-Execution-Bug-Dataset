**MGO-OOO-Bugs**: A Benchmark of Multi-Granularity Out-of-Order Concurrency Bugs﻿

This repository contains the dataset for our paper on "Out-of-Order (OOO) Execution Bugs" under Weak Memory Models (WMM). We propose a Multi-Granularity Ordering (MGO) taxonomy and collect 58 OOO bug samples across different system abstraction layers.

📂 Repository Structure (MGO Taxonomy)
Our dataset is strictly categorized into three layers based on the triggering level of the concurrency bugs:
* **[Layer1](./Layer1)**: Micro-Instruction Level (32 Samples). Focuses on pure hardware-sensitive reorderings (Store-Store, Store-Load) in fundamental lock-free data structures (e.g., Spinlocks, Ring Buffers).
* **[Layer2](./Layer2)**: Resource Lifecycle Level (24 Samples). Focuses on hardware-agnostic and OS-level reorderings, typically manifesting as Use-After-Free (UAF) or Kernel Panics driven by thread scheduling or interrupts (e.g., Linux Kernel, Drivers).
* **[Layer3](./Layer3)**: Semantic Logic Level (2 Samples). Focuses on complex state machine or protocol disruptions in high-performance distributed systems and networking frameworks (e.g., MySQL, DPDK, sofa-pbrpc).

🏷️ Label Definitions
* **Bug Id**: Our own defined internal reference number for the bug (e.g., L1-01).
* **Source**: The source of the vulnerability or the submission number of the vulnerability.
* **Target System**: The software project or framework where the bug is located (e.g., MySQL, Linux Kernel, DPDK).
* **Type**: The specific manifestation or category of the concurrency error (e.g., UAF, Deadlock, Store-Load reordering).
* **Registered**: The date the bug was initially reported or raised by the community.
* **Resolved**: The date the bug was officially fixed or closed by the developers.

**Layer 1: Micro-Instruction Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L1-01 | [#123]() | Closed | Store-Load Reordering | Jan 10, 2025 | Jan 15, 2025 |
| L1-02 | [CVE-202X-XXXX]() | Resolved | Store-Store Reordering | Feb 05, 2025 | Feb 10, 2025 |

**Layer 2: Resource Lifecycle Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L2-01 | [#456]() | Closed | Use-After-Free (UAF) | Nov 20, 2024 | Dec 01, 2024 |
| L2-02 | [#789]() | Resolved | Kernel Panic | Mar 12, 2025 | Mar 15, 2025 |

**Layer 3: Semantic Logic Level**
| Bug Id | Source | Target System | Type | Registered | Resolved |
| :--- | :--- | :--- | :--- | :--- | :--- |
| L3-01 | [#999]() | Open | State Machine Error | Apr 01, 2026 | --- |
