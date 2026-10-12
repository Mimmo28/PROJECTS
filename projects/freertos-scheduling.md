# 🚀 Real-Time Scheduling for Embedded Systems (FreeRTOS)
> **Architecture:** Embedded Real-Time Operating System | **Tech Stack:** C, FreeRTOS, Microcontroller Toolchains | **Status:** Completed (Academic / Politecnico di Torino)

## 📋 Project Overview
This project explores real-time task scheduling and deterministic execution in resource-constrained embedded systems using **FreeRTOS** and **C**. Developed as part of the advanced curriculum at **Politecnico di Torino**, the project focuses on designing, implementing, and validating both time-triggered and priority-based real-time schedulers capable of satisfying stringent timing constraints.

---

## 🏗️ Architectural Decisions

### 1. Hybrid Scheduling Paradigms
- **Time-Triggered Architectures (TTA):** Designed deterministic cyclic executive schedulers for safety-critical tasks with strictly periodic deadlines.
- **Priority-Based Preemptive Scheduling:** Implemented Fixed-Priority Preemptive (Rate Monotonic / Deadline Monotonic) tasksets under FreeRTOS preemptive kernel configurations.
- **Cooperative & Background Tasks:** Managed non-critical telemetry and diagnostic routines in idle or background priorities without starving hard real-time threads.

### 2. Task Synchronization & Inter-Process Communication (IPC)
- **Bounded Resource Sharing:** Employed FreeRTOS binary semaphores, counting semaphores, and mutexes with **Priority Inheritance** protocols to eliminate unbounded Priority Inversion.
- **Deterministic Queues:** Message queues with non-blocking timeouts used for zero-copy inter-task communication.

---

## 🛡️ Real-Time Safety & Timing Analysis

*   **Schedulability & Worst-Case Execution Time (WCET):** Conducted analytical feasibility verification (Liu & Layland utilization bounds, Response Time Analysis - RTA).
*   **Deadline Enforcement & Jitter Minimization:** Optimized interrupt service routines (ISRs) using deferred interrupt processing (task notifications / FreeRTOS software timers).
*   **Memory Safety in Embedded Systems:** Static memory allocation (`configSUPPORT_STATIC_ALLOCATION = 1`) to eliminate heap fragmentation and non-deterministic `malloc` delays during mission-critical phases.
*   **Stack Overflow Protection:** Enabled hardware stack monitoring and canary checks (`configCHECK_FOR_STACK_OVERFLOW = 2`).

---

## 📈 Key Outcomes
- Zero missed deadlines across simulated maximum-load stress tests.
- Formally verified latency margins and bounded interrupt latency.
- Robust handling of preemptive context switches on constrained embedded architectures.

---

> **Developer:** Domenico Filippo Innamorato  
> **Team Project:** Politecnico di Torino (MSc Cybersecurity Engineering)
