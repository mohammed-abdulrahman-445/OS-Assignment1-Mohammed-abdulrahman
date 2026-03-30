# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[process is independent program that has own memory space. thread is unit of execution withn process ,it has own program counter, in SchedulerSimulation.java each process run inside diffrent thread. differences between process and thread 
memory sharing:thread withn the same process share memory,process have separate memory spaces ,that make thread shared easily.
Creation Overhead and Speed: Creating threads is faster and uses less memory than creating separate processes.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling,each process given fixed time quantum and is max of CPU,if process doesn't finish its allocated time quantum and placed at the end of ready queue]

Example from my output:
```
[  ? P1 executing quantum [3000ms] 
  ? Quantum progress: [???????????????] 100%
  ? P1 completed quantum 3000ms ? Overall progress: [????????????????????] 60%
     Remaining time: 1958ms
  ? P1 yields CPU for context switch

  ? P1 (Priority: 1) added to ready queue ?]
```

**Explanation of example:**
[ ? P1 executing quantum [3000ms] 
  ? Quantum progress: [???????????????] 100%
  ? P1 completed quantum 3000ms ? Overall progress: [????????????????????] 60%
     Remaining time: 1958ms
  ? P1 yields CPU for context switch

  ? P1 (Priority: 1) added to ready queue ?]

  Why re-queueing is important:
 It makes sure no single process keeps the CPU all to itself

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state? after new thread is called addProcessToQueue(),object is created befor start ]

2. **Runnable**: [When does P1 become Runnable?when current Thread.start() is called in scheduling loop, and ready queue and is ready to be scheduled by the CPU ]

3. **Running**: [When is P1 Running? when os scheduler select and executing run() method and calculating runtime]

4. **Waiting**: [When/why would P1 be Waiting?when Thread.sleep is called during work process ,and when the main thread waits currentThread.join() to complete]

5. **Terminated**: [When is P1 Terminated?when the run() method returns normal after comleting and add runToCompletion.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
