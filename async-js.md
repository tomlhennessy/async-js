# Threading

* Overview:
    - A program's birth (coding) is followed by its lifetime (execution), known byt its runtime

* Single-threaded vs Multi-threaded:
    Single-threaded:
        - Executes one command at a time
        - Analogous to a kitchen with one chef, where dishes are prepared sequentially
        - JavaScript operates on this model
    Multi-threaded:
        - Executes multiple commands simultaneously
        - Like a kitchen with several chefs working on different dishes

    JavaScript's Single-threaded nature:
        - Only one command runs at a time
        - Potential for unresponsiveness if a command takes too long

# Runtime Environment

## The Message Queue and Event Loop

* Overview:
    - JavaScript's asynchronous nature empowers interactive web experiences
    - Understanding the runtime's mechanics enhances our coding prowess

* Event Loop Model:
    • Call Stack:
        - Tracks ongoing function execution
        - Represents the current task being processed
    • Message Queue:
        - Stores tasks awaiting execution
        - Tasks are processed sequentially, ensuring no interruption

* Message Queue Structure:
    • Utilises the queue data structure
    • Characteristics:
        - New items added at the back (enqueueing)
        - Items processed from the front (deqeueueing)

* Illustration with Code:
    • Shows runtime behaviour through code execution
    • Demonstrates how tasks interact with the call stack and message queue

* Runtime Tracing:
    • Traces execution timeline of synchronous and asynchronous tasks
    • Illustrates how stack and queue operations occur over time

* Key Takeaways:
    • Synchronous tasks processed on the stack
    • Asynchronous tasks wait in the queue
    • Queue ensures sequential handling of events
    • Event loop orchestrates this continous process
