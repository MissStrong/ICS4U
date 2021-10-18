## Note – Queue

The **queue** (pronounced like the letter "Q") is an abstract data type (ADT). It is a collection of elements that are "lined up", as though they are waiting in line. Elements get added to the back of the queue and removed from the front of the queue. The queue ADT is also known as FIFO (first in, first out) system. 

These are some the typical operations of a queue ADT:

* retrieve the item at the front of the queue
* remove the item at the front of the queue
* add an item to the back of the queue
* check whether the queue is empty

An example of a usage of a queue is prioritizing requests from users when maintaining software. Requests are typically done on a first-come first-serve basis, although more important requests (e.g. vulnerability issues) may "cut in line". 

Java has an **interface** called `Queue`. The `PriorityQueue` class, among other classes, `implement` `Queue`.

You need to import `java.util.Queue` in order to use these classes. Here are some of the methods you can use. 

| Method | Explanation | Example | Explanation |
| --- | --- | --- | --- |
| `PriorityQueue()` | Creates a new (empty) priority queue. | `Queue<Integer> queueExample = new PriorityQueue();` | Creates a new priority queue of integers called `queueExample`. It is initialized to the empty queue. |
| `add()` | Adds an element to the queue, if possible. Returns `true` or throws `IllegalStateException`. | `queueExample.add(1234);` | Adds `1234` to the top of `queueExample`. |
| `offer()` | Adds an element to the queue, if possible. Returns `true` (success) or `false` (failure).| `queueExample.offer(5678);` | Adds `5678` to the top of `queueExample`. | | 
| `element()` | Returns the element at the front of the queue or throws `EmptyQueueException` if the queue is empty. | `queueExample.element();` | Returns `5678`. |
| `peek()` | Returns the element at the front of the queue or returns `null` if the queue is empty. | `queueExample.peek();` | Returns `5678`. |
| `remove()` | Removes and returns the element at the front of the queue or throws `NoSuchElementException` if the queue is empty. | `queueExample.remove();` | Removes `5678`. Now, `queueExample` contains only `1234`. | 
| `poll()` | Removes and returns the element at the front of the queue or returns `null` if the queue is empty. | `queueExample.poll();` | `Removes 1234`. Now, queueExample is empty again. |
| `isEmpty()` | Returns `true` if the queue is empty, and `false` otherwise. | `queueExample.isEmpty()` | Returns `true`, since `queueExample` is currently empty. |

