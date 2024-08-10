# Explanation

1. When we Run Synchronous Code: It goes to _callstack_ with no waiting
2. When we run _Asynchronous code_ it is executed in the _web API_ Environment
    1. If takes time, Won't Block call stack
    2. This is How A _single Thread_ language behave as a multithreaded
3. When Asynchronous code is Finished, It Fires up and _event_
    1. Manual Event: (i.e. me typing load event)
    1. Others types
4. Events will be added to [microtasks Queue](Definitions/microtasks%20Queue.md)
5. and then added to callstack when it have space
