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


# Intro to Asynchronous JS
• JavaScript stands out with its heavy use of callbacks
• Callbacks execute commands at later times, but their exact timing isn't guaranteed
• We'll explore how to use callbacks asynchronously

* Synchronous Code:
    • Commands execute in a guaranteed order
    • Example:

    ```javascript
    console.log("one");
    console.log("two");
    console.log("three");
    ```
* Asynchronous Code:
    • Commands don't have a guaranteed order of execution
    • Example using __'setTimeout'__:

    ```js
    console.log("start");

    setTimeout(function() {
        console.log("time is up!");
    }, 1500);

    console.log("end");
    ```
    • Output order: "start", "end", "time is up!"

* Why Asynchronous Code?
    • In the real world, events don't always happen predictably
    • Examples:
        - When fetching data from a server, response time varies due to network latency
        - User interactions like key presses or clicks occur unpredictably
    • Asynchronous code handles such uncertainty during program runtime

* Key Takeaways
    • Introduced asynchronous code
    • Compared synchronous and asynchronous behaviour using __'setTimeout'__
    • Asynchronous code handles unpredictable timing scenarios during program execution


# Timeouts and Intervals
• Asynchronous nature illustrated through 'setTimeout'
• Familiarise with 'setTimeout usage for async concepts

* setTimeout Basics:
    • Accepts callback and time delay in milliseconds
    • Non-blocking nature; code after 'setTimeout' runs without waiting
    • Optional delay; defaults to zero if not specified

* Predicting Execution Order:
    • Common interview question: understanding code execution order
    • 'setTimeout' execution doesn't block further lines

* Additional Arguments:
    • 'setTimeout' can take unlimited additional arguments
    • Callback executes with provided arguments after the delay

* Cancelling Timeouts:
    • 'setTimeout' returns a special Timeout object
    • Use 'clearTimeout' to cancel a pending timeout
    • Variation in return value between NodeJS and browser environments

* Running Intervals:
    • 'setInterval' executes a callback repeatedly at a specified delay
    • Similar arguments to 'setTimeout'
    • Use 'clearInterval' to cancel an interval
