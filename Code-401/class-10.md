# Class 10

## Stacks and Queues

| Aspect           | Stack                                      | Queue                                      |
|------------------|--------------------------------------------|--------------------------------------------|
| Basic Concept    | LIFO (Last In First Out)                    | FIFO (First In First Out)                  |
| Operations       | Push, Pop, Peek, IsEmpty                    | Enqueue, Dequeue, Peek, IsEmpty            |
| Push/Enqueue     | Adds an item to the top of the stack        | Adds an item to the end of the queue       |
| Pop/Dequeue      | Removes an item from the top of the stack   | Removes an item from the front of the queue|
| Top/Front        | Top refers to the top item in the stack     | Front refers to the front item in the queue|
| Rear             | Not applicable in stacks                    | Rear refers to the end item in the queue   |
| Peek             | Views the value of the top item             | Views the value of the front item          |
| Order of Access  | The most recent item added is accessed first| The oldest item added is accessed first    |
| Complexity       | O(1) for push, pop, peek, and isEmpty       | O(1) for enqueue, dequeue, peek, and isEmpty|
| Underlying Structure | Often implemented using linked lists or arrays | Often implemented using linked lists or arrays |
| Use Cases        | Undo mechanisms, parsing expressions       | Queuing systems, breadth-first search      |

### Stack and Queue Visualization:
- **Stack**: Imagine a stack of plates. The last plate you put on top is the first one you take off.
- **Queue**: Think of a line of people. The first person in line is the first one to be served.

### Key Points:
- Both stacks and queues are linear data structures.
- Stacks operate on a LIFO basis, making them ideal for tasks where the most recent addition is the first to be removed, like undo operations in text editors.
- Queues operate on a FIFO basis, suitable for scenarios where the first added item needs to be processed first, like in printer spooling or call center systems.
- Both can be efficiently implemented to have O(1) time complexity for their primary operations.