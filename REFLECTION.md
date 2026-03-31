# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[in Java. I understood how each process in the simulation was represented as a thread using the Runnable interface. I also learned about different thread states such as New, Runnable, Running, Waiting, and Terminated, and how a thread transitions between them during execution. One important concept I learned was how threads can execute concurrently, giving the impression of parallel execution even on a single CPU. I also gained a better understanding of how context switching works when multiple threads share CPU time. What surprised me was how easy it is to simulate real CPU scheduling using threads, but also how careful we need to be when managing timing and execution order. Overall, this assignment helped me connect theoretical concepts of operating systems with practical implementation.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[The most challenging part of this assignment was implementing and correctly tracking the waiting time for each process. It was difficult because it required precise timing and understanding exactly when a process enters and leaves the ready queue. I had to carefully manage variables like lastQueueEnterTime and update the total waiting time at the correct moment before execution. Another challenge was understanding how threads behave when they are paused and resumed, especially with the use of Thread.sleep() and join(). Debugging was also challenging because small mistakes in timing logic could lead to incorrect results. Additionally, ensuring that processes were re-added to the queue correctly without breaking the scheduling logic required careful attention. This part of the assignment really tested my understanding of both scheduling and thread behavior.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[To overcome these challenges, I approached the problem step by step and focused on understanding the flow of the program. I reviewed the code multiple times to track how each process moves through the ready queue and how its state changes. I also used print statements and output analysis to verify whether the waiting times and execution order were correct. When I encountered issues, I broke the problem into smaller parts and tested each part individually. I referred to Java documentation to better understand thread methods like start() and join(). Additionally, I compared the expected behavior of Round-Robin scheduling with my program output to identify inconsistencies. This systematic debugging approach helped me fix errors and improve the accuracy of my implementation.]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Multithreading is widely used in many real-world applications to improve performance and responsiveness. For example, web browsers use multiple threads to load web pages, process JavaScript, and handle user interactions simultaneously. This ensures that the user interface remains responsive even while heavy tasks are running in the background. Another example is in mobile applications, where background threads are used to fetch data from the internet without freezing the app. In gaming, threads are used to handle graphics rendering, physics calculations, and user input at the same time. Multithreading is also used in servers to handle multiple client requests efficiently. This assignment helped me understand how these real-world systems manage multiple tasks using threads.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
