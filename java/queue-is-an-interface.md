> A Queue is an interface, which means you cannot construct a Queue directly.

The best option is to construct off a class that already implements the Queue interface,
like one of the following:

- AbstractQueue
- ArrayBlockingQueue
- ConcurrentLinkedQueue
- DelayQueue
- LinkedBlockingQueue
- LinkedList
- PriorityBlockingQueue
- PriorityQueue
- SynchronousQueue

```java
Queue<Integer> q = new LinkedList<Integer>();
```
