# Concurrent Railway Reservation System
### Mini Operating System Simulator (Operating Systems Lab Project)

A C++-based Mini Operating System Simulator that demonstrates core Operating System concepts such as process management, CPU scheduling, synchronization, inter-process communication, resource allocation, and user vs kernel mode operations.

The main application running inside this simulated operating system is a **Concurrent Railway Reservation System**, where multiple users can book, cancel, and inquire about train tickets simultaneously while sharing limited system resources.

---

## Project Objectives

This project was developed to provide practical understanding of fundamental Operating System concepts through a real-world concurrent application.

### Operating System Concepts Implemented
- Process Creation and Termination
- Process States (New, Ready, Running, Blocked, Terminated)
- Multitasking and Multithreading
- Concurrency
- Critical Section Handling
- Synchronization using Mutex/Semaphores
- Inter-Process Communication (IPC)
- CPU Scheduling (FCFS, Round Robin, Priority)
- Resource Allocation (CPU, RAM, Disk)
- Ready Queue Management
- User Mode vs Kernel Mode
- Interrupt Handling
- Logging and File Persistence

---

## Simulated System Configuration

| Resource | Default Value |
|--------|--------:|
| RAM | 2 GB |
| Secondary Storage | 256 GB |
| CPU Cores | 8 |

These values can be configured during system startup.

---

## System Architecture

The Mini OS consists of the following major subsystems:

### Boot Manager
- Simulates system boot sequence
- Loads hardware configuration
- Initializes all OS subsystems

### Process Manager
- Creates and terminates processes
- Maintains Process Control Blocks (PCBs)
- Tracks process states

### Scheduler
- Implements FCFS
- Implements Round Robin
- Supports Priority Scheduling

### Resource Manager
- Allocates and deallocates RAM, CPU cores, and storage

### Synchronization Module
- Uses mutexes and semaphores
- Protects critical sections

### IPC Module
- Message queues/shared data structures

### Interrupt Handler
- Handles booking timeout
- Handles cancellation interrupt
- Handles system shutdown

### Railway Reservation Application
- Ticket booking
- Ticket cancellation
- Seat inquiry
- Passenger information

---

## Railway Reservation Features

- Book Tickets
- Cancel Tickets
- View Available Seats
- View Booking Status
- Passenger Information Management
- Prevent Double Booking
- Concurrent Access Support

---

## Process Lifecycle

Each user request is treated as an independent process.

```text
New → Ready → Running → Blocked → Ready → Terminated
