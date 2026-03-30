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

### Example 1: [In a video game]

**Description**: 
**Why Round-Robin works well here**: 
In a video game, like  Minecraft, the game engine runs multiple tasks simultaneously: rendering graphics, processing player input, updating AI, and handling network events. Each task can be managed by a separate thread. Using Round-Robin scheduling ensures that no single task dominates the CPU
### Example 2: [media player]

**Description**: 
**Why Round-Robin works well here**: 
In a media player, like  Spotify, multiple tasks run at the same time: decoding audio, decoding video, buffering data from the network, and updating the user interface. Each task can run in its own thread. Using Round-Robin scheduling ensures that no single task
---

## Summary

**Key concepts I understood through these questions:**
1. different  between thread and process 
2. the round robin and time quantum
3. therad lifecycle and move through different state

**Concepts I need to study more:**
1. 
2. 
