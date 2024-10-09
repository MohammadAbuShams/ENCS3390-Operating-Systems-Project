# Multilevel Feedback Queue Scheduling Simulator

## Overview
This project simulates a multilevel feedback queue (MFQ) scheduling algorithm, commonly used in operating systems to manage processes dynamically. It includes a workload generator to create random process workloads and a simulator that implements the MFQ with varying scheduling strategies across multiple queues.

## Project Components

### 1. Workload Generator
This component generates a random set of process workloads based on user-specified parameters and saves them to a file. Each process is defined by its PID, arrival time, and alternating CPU and IO bursts.

#### Parameters for Generation:
- **Number of Processes**: Total processes to generate.
- **Max Arrival Time**: Maximum possible arrival time for processes.
- **Max Number of CPU Bursts**: Maximum CPU bursts a process can have.
- **IO Burst Duration Range**: [Min IO, Max IO] duration.
- **CPU Burst Duration Range**: [Min CPU, Max CPU] duration.

### 2. Simulator
This component reads the workload file and simulates a scheduling environment using a multilevel feedback queue mechanism with the following queues:
- **Queue #1**: Round Robin with time quantum `q1`.
- **Queue #2**: Round Robin with time quantum `q2`.
- **Queue #3**: Shortest-remaining-time first.
- **Queue #4**: First-come, first-served (FCFS).

Processes are moved between queues based on their execution state and the rules defined for each queue.

## Features
- Generate workloads with random process attributes.
- Simulate different scheduling strategies.
- Dynamic process handling between multiple queues.
- Real-time control over the simulation to pause and inspect the state.
- Output important statistics like CPU utilization and average waiting time.
- Visual Gantt chart representation of process execution.

## Contributors

- [Mohammad AbuShams](https://github.com/MohammadAbuShams)
- [Mohammed Owda](https://github.com/M7mdOdeh1).
