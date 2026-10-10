# Operating System (OS)

## 1. What is an Operating System?

An **Operating System (OS)** is software that sits between **you (and your applications)** and the **hardware**.

**Examples:** Windows, Linux, macOS, Android.

### Example: A School Principal 🏫

Think of the OS as the **principal** of a school.

- Students (apps like Chrome, WhatsApp, and games) all need resources such as classrooms, the playground, and the library.
- The school's resources (CPU, RAM, storage, and printer) are limited.
- The principal decides **who gets what, when, and for how long**, so everything runs smoothly without conflicts.

Without a principal, the school would be chaotic. Similarly, without an OS, applications would compete for hardware resources.

## 2. Functions of an Operating System

| Function | School Example | Computer Example |
|---|---|---|
| **Process Management** | Deciding which class uses the playground | Deciding which application gets the CPU |
| **Memory Management** | Giving each class its own room | Giving each application its own part of RAM |
| **File Management** | A library that stores books in an organised way | Managing folders, files, saving, and opening files |
| **Device Management** | Controlling the school bell and printer | Communicating with the keyboard, mouse, and printer through drivers |
| **Security** | Gate passes and ID cards | Passwords and user permissions |
| **User Interface** | A reception desk where you ask for things | Desktop, icons, and command line |

## 3. Ways to Interact with an Operating System

There are two common ways to interact with an OS.

### 3.1 Graphical User Interface (GUI)

A **GUI** allows users to interact with the operating system using graphical elements such as icons, windows, and buttons.

**Example:** The Windows desktop.

### 3.2 Command Line Interface (CLI)

A **CLI** allows users to interact with the operating system by typing commands.

**Examples:** Linux terminal commands such as `ls` and `cd`.

## 4. What is a Kernel?

The **kernel** is the core and most important part of an operating system. It runs from the moment the computer starts and directly manages the CPU, memory, and devices.

**Example:** If the OS is the principal's office, the kernel is the principal's brain—the part that makes the decisions.

Everything else, such as the desktop, icons, and settings application, is built around it.

## 5. User Mode vs. Kernel Mode

The CPU operates in two modes: **user mode** and **kernel mode**.

| Feature | User Mode | Kernel Mode |
|---|---|---|
| **Who runs here?** | Normal applications (Chrome, Notepad) | The kernel |
| **Access** | Limited access; cannot directly access hardware | Full access to system resources |
| **If something crashes** | Usually, only that application crashes | The entire system can crash |

### Why is this separation necessary?

Imagine if any student could open the principal's cupboard and change the exam papers. That would be dangerous.

Therefore, students can only request things from the principal. Similarly, applications must request privileged operations from the kernel instead of accessing hardware directly.

## 6. What is a System Call?

A **system call** is a mechanism through which an application requests a service from the operating system's kernel.

Applications running in user mode cannot directly perform certain privileged operations, so they use system calls to request these services.

### Example: Saving a File in Notepad

1. Notepad runs in user mode and cannot directly perform the required disk operation.
2. It makes a system call to the kernel, requesting that the file be written.
3. The CPU switches to kernel mode.
4. The kernel performs the file-writing operation.
5. The CPU switches back to user mode and returns the result to Notepad.

### Common System Calls

- Opening a file
- Reading a file
- Writing a file
- Creating a process
- Allocating memory

## 7. Quick Recap

- **Operating System (OS):** Manages the interaction between applications and hardware.
- **Main Functions:** Process management, memory management, file management, device management, and security.
- **Kernel:** The core part of the OS that manages hardware and system resources.
- **User Mode:** A restricted execution mode for normal applications.
- **Kernel Mode:** A privileged execution mode that allows the kernel to manage system resources.
- **System Call:** A mechanism through which an application requests a service from the kernel.

## 8. Common Interview Questions

1. What is an operating system, and what are its main functions?
2. What is a kernel?
3. What is the difference between user mode and kernel mode?
4. What is a system call? Give an example.
5. What is the difference between a GUI and a CLI?

## 9. Quick Check

### Question 1: Why can't Chrome directly write to your hard disk?

**Answer:** Applications run in user mode, which restricts direct hardware access. Therefore, Chrome must make a system call and let the kernel perform the required operation.

### Question 2: If an application in user mode crashes, does the whole computer crash?

**Answer:** No. Usually, only that application crashes while the kernel continues running.

---
