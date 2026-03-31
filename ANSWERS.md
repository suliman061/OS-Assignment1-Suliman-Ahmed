# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A process is an independent program in execution that has its own memory space and system resources. Each process runs separately and does not share memory with other processes. In contrast, a thread is a smaller unit of execution داخل the same process and shares the same memory and resources with other threads.

Threads are lighter and faster to create compared to processes, which require more overhead for memory allocation and management. In this assignment, threads were used because they allow efficient simulation of multiple processes with fast context switching. Using threads also simplifies communication and resource sharing within the program.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:n Round-Robin scheduling, when a process does not finish within its assigned time quantum, it is paused and moved to the end of the ready queue. This allows other processes to get CPU time, ensuring fairness among all processes.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```P1 executing quantum [2000ms]
Remaining time: 3000ms
P1 yields CPU for context switch

Ready Queue: [P2 → P3 → P1]
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example: In this example, process P1 did not finish during its time quantum, so it was stopped and re-added to the end of the queue. This means P1 will wait while P2 and P3 execute. After that, P1 will get another chance to run. This cycle continues until the process completes execution.**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer: New:
P1 is in the New state when the thread is created using new Thread(process) but has not started yet.
Runnable:
P1 enters the Runnable state after calling the start() method, making it ready to be executed by the CPU.
Running:
P1 is in the Running state when the CPU begins executing its run() method.
Waiting:
P1 enters the Waiting state when Thread.sleep() is called inside the run() method, simulating execution delay.
Terminated:
P1 reaches the Terminated state after completing its execution when remainingTime becomes zero**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]
A web server processes multiple client requests simultaneously, such as loading web pages or handling API calls.
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round-Robin scheduling ensures that each request gets a fair share of CPU time. This prevents any single request from blocking others and improves system responsiveness, especially when many users are connected at the same time.
### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]
An operating system manages multiple running applications like browsers, editors, and background services.
**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round-Robin allows each application to receive CPU time in a fair and predictable manner. This ensures smooth multitasking and prevents any program from monopolizing the CPU.
---

## Summary

**Key concepts I understood through these questions:**
1. The difference between processes and threads and their performance impact
2. How Round-Robin scheduling manages process execution fairly
3. The lifecycle and states of a thread during execution

**Concepts I need to study more:**
1. Advanced CPU scheduling algorithms such as Priority Scheduling and Multilevel Queues
2. Thread synchronization and concurrency control
