# OS Topic 2: Processes vs. Threads

## 1. What is a Program?

A **program** is a set of instructions saved on a disk. It does not perform any operations until it is executed.

**Example:** A recipe book lying on a shelf. It contains the instructions, but nobody is cooking yet.

## 2. What is a Process?

A **process** is a program that is currently running.

**Example:** When someone opens a recipe book and starts cooking, it is like a process. When you double-click Chrome, the OS creates a Chrome process.

### Program vs. Process

| Feature | Program | Process |
|---|---|---|
| **State** | Stored on disk | Running in memory |
| **Example** | `chrome.exe` file | Chrome running on your screen |
| **Real-life Example** | Recipe book on a shelf | Cooking happening now |

You can run **one program multiple times**. For example, opening Notepad twice can create two separate processes, like two people cooking from the same recipe in different kitchens.

## 3. What Resources Does a Process Get?

When the OS creates a process, it provides the process with its own resources and address space.

- **Memory:** Its own address space containing code, data, stack, and heap.
- **Process ID (PID):** A unique identifier assigned to the process.
- **Open Files and Resources:** Resources used by the process.

Because each process has its own memory, **one process cannot easily interfere with another process**.

For example, if Chrome crashes, your music player can continue playing.

## 4. Process States (Life Cycle of a Process)

A process goes through different stages during its execution, similar to a student moving through different stages in an exam hall.

1. **New:** The process has just been created.
2. **Ready:** The process is waiting for CPU time.
3. **Running:** The CPU is executing the process.
4. **Waiting:** The process is waiting for an event, such as a file operation or user input.
5. **Terminated:** The process has finished execution.

### Example

A game process is running. When you press Save, it may enter the **Waiting** state while waiting for the disk operation to complete. Once the operation finishes, it can return to the **Ready** state and then move to the **Running** state when scheduled by the CPU.

## 5. What is a Thread?

A **thread** is a small unit of execution within a process.

### Real-Life Example: Cooking Dinner

Imagine you are preparing dinner with three helpers:

- One person chops vegetables (**Thread 1**).
- One person boils rice (**Thread 2**).
- One person prepares curry (**Thread 3**).

It is one kitchen, one dinner, but three workers. Similarly, a single process can contain multiple threads that perform different tasks.

### Real-World Example: A Browser

In a browser, different threads may handle tasks such as loading a page, playing a video, and responding to user input. This allows multiple tasks to make progress without necessarily blocking one another.

## 6. What Do Threads Share and What Do They Keep Private?

Threads belonging to the same process share certain resources but maintain their own execution state.

| Shared by All Threads of a Process | Private to Each Thread |
|---|---|
| Code | Stack |
| Data | Registers |
| Heap memory | Program counter |
| Open files | |

Since threads share the same memory, they can exchange information easily and quickly.

However, if two threads try to modify the same data simultaneously, problems can occur. These issues are addressed through **thread synchronization**.

## 7. Process vs. Thread

| Feature | Process | Thread |
|---|---|---|
| **Meaning** | A running program | A unit of execution within a process |
| **Memory** | Has its own separate address space | Shares memory with other threads in the same process |
| **Creation Time** | Generally slower and more resource-intensive | Generally faster and less resource-intensive |
| **Communication** | Requires inter-process communication (IPC) mechanisms | Can communicate through shared memory |
| **If One Crashes** | Other independent processes are usually unaffected | A thread failure can affect the entire process |
| **Example** | Chrome and VS Code running as separate processes | Different tasks performed by threads within Chrome |

## 8. Quick Recap

- **Program:** Instructions stored on disk.
- **Process:** A program in execution.
- **PID:** A unique identifier assigned to a process.
- **Process States:** New → Ready → Running → Waiting → Terminated.
- **Thread:** A lightweight unit of execution within a process.
- **Shared Resources:** Threads of the same process share code, data, heap memory, and open files.
- **Private Resources:** Each thread maintains its own stack, registers, and program counter.
- **Processes:** Provide isolation between applications.
- **Threads:** Are generally lighter and faster to create than processes.

## 9. Common Interview Questions

1. What is the difference between a program and a process?
2. What is the difference between a process and a thread?
3. What are the different states of a process?
4. Why are threads called lightweight?
5. What resources do threads of the same process share?

## 10. Quick Check

### Question 1: You open Notepad three times. How many processes are created?

**Answer:** Three separate processes can be created when each instance runs as a separate process.

### Question 2: Which is faster to create: a process or a thread? Why?

**Answer:** A thread is generally faster to create because it shares the existing process's memory and resources instead of requiring a separate process address space.

---

**Next Topic:** OS Topic 3 — CPU Scheduling
