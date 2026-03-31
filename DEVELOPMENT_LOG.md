# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 29, 3:00 PM]
**What I did**: Read and analyzed the provided code.

**Details**: Carefully went through the entire Java code
Identified the main classes: Process and SchedulerSimulation
Tried to understand how Round-Robin scheduling is implemented
Focused on how threads are created and managed in the queu

**Challenges**: The code structure was initially confusing, especially the relationship between threads and processes using the Map<Thread, Process>. It was also difficult to understand how the scheduling loop works and how processes move in and out of the ready queue. Additionally, tracking where each feature (like waiting time and context switching) should be implemented was not clear at first.

**Solution**: I broke the code into smaller parts and analyzed each section separately. I focused on understanding the flow of execution step by step, especially inside the main scheduling loop. I also wrote notes to track how data moves between the queue and the process map.

**Time spent**: 30 minute 

---

### Entry 2 - [March 30, 4:00 AM]
**What I did**: Ran the code and started understanding the execution behavior.

**Details**: Compiled and executed the program
Observed how processes are added to the ready queue
Watched how threads execute in a Round-Robin manner
Analyzed the output step by step

**Challenges**: It was difficult to follow the execution order because multiple threads were involved. The output was also complex due to the formatted printing, which made it harder to track each process.

**Solution**: I focused on one process at a time and tracked its lifecycle through the output. I also ignored the colors at first and concentrated only on the logic.

**Time spent**: 1 hour

---

### Entry 3 - [March 30, 1:00 PM]
**What I did**: Implemented Feature 1 (process priority).

**Details**: Added a priority field to the Process class
Generated random priority values between 1 and 5
Displayed priority when adding processes to the queue

**Challenges**: I was unsure where to initialize the priority and how to print it without affecting existing functionality.

**Solution**: I added the priority inside the constructor and used a getter method to display it in the output.

**Time spent**: 2 hours

---

### Entry 4 - [March 30, 4:00 PM]
**What I did**: Implemented Feature 2 (context switch counter).

**Details**: Added a static variable to count context switches 
Incremented it every time a process starts execution 
Printed the total at the end of the simulation

**Challenges**: At first, the counter was incorrect because I placed it in the wrong location.

**Solution**: I moved the increment to just before currentThread.start() to correctly count each execution cycle.

**Time spent**: 1:30 hours

---

### Entry 5 - [March 31, 3:00 PM]
**What I did**: Implemented Feature 3 (waiting time calculation).

**Details**: Added variables to track waiting time
Calculated waiting time before each execution
Updated waiting time when processes re-enter the queue

**Challenges**: This was the most difficult part because it required precise timing and correct placement of calculations.

**Solution**: I used System.currentTimeMillis() and carefully updated the waiting time before execution and when re-adding processes.

**Time spent**: 3 hours

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [8 hours]

**Most challenging part**: The most challenging part was implementing the waiting time feature because it required accurate tracking of time and understanding the exact flow of processes in the queue.

**Most interesting learning**: The most interesting part was seeing how Round-Robin scheduling works in practice and how threads simulate real CPU scheduling behavior.

**What I would do differently next time**: Next time, I would test each feature immediately after implementing it instead of waiting until the end, to reduce debugging time.
