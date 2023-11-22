# Queue Interface
- Queue interface maintains the first-in-first-out order.
- It can be defined as an ordered list that is used to hold the elements which are about to be processed.

  ### PriorityQueue:
   - It holds the elements or objects which are to be processed by their priorities.
   - PriorityQueue doesn't allow null values to be stored in the queue.

  ### Deque:
   - Deque interface extends the Queue interface.
   - In Deque, we can remove and add the elements from both sides.
   - Deque stands for a double-ended queue which enables us to perform operations at both ends.

  ### ArrayDeque:
   - ArrayDeque class implements the Deque interface.
  - We can add or delete the elements from both ends.
   - ArrayDeque is faster than ArrayList and Stack and has no capacity restrictions.

* * *

**ChatGPT:**

Sure, let's go through each data structure and provide a brief description along with example codes for their operations.

### 1. **Queue:**

#### Description:

* A queue is a data structure that follows the First-In-First-Out (FIFO) principle.
* Elements are added at the rear (enqueue) and removed from the front (dequeue).
* It represents a waiting line.

#### Example Code:

```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();

        // Enqueue
        queue.offer("Element 1");
        queue.offer("Element 2");
        queue.offer("Element 3");

        // Dequeue
        String removedElement = queue.poll();
        System.out.println("Removed Element: " + removedElement);

        // Peek (retrieve but not remove)
        String frontElement = queue.peek();
        System.out.println("Front Element: " + frontElement);

        // Display all elements
        System.out.println("Queue: " + queue);
    }
}
```

### 2. **PriorityQueue:**

#### Description:

* A PriorityQueue stores elements based on their priorities.
* The element with the highest priority is served before others.
* Elements are ordered using their natural ordering or by a comparator.

#### Example Code:

```java
import java.util.PriorityQueue;

public class PriorityQueueExample {
    public static void main(String[] args) {
        PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();

        // Enqueue
        priorityQueue.offer(30);
        priorityQueue.offer(20);
        priorityQueue.offer(40);

        // Dequeue (highest priority first)
        int removedElement = priorityQueue.poll();
        System.out.println("Removed Element: " + removedElement);

        // Display all elements
        System.out.println("PriorityQueue: " + priorityQueue);
    }
}
```

### 3. **Deque:**

#### Description:

* Deque (Double-ended queue) allows insertion and removal of elements from both ends.
* Extends the Queue interface.

#### Example Code:

```java
import java.util.ArrayDeque;
import java.util.Deque;

public class DequeExample {
    public static void main(String[] args) {
        Deque<String> deque = new ArrayDeque<>();

        // Add elements at the rear
        deque.offerLast("Element 1");
        deque.offerLast("Element 2");

        // Add elements at the front
        deque.offerFirst("Element 3");

        // Remove element from the front
        String removedFromFront = deque.pollFirst();
        System.out.println("Removed from Front: " + removedFromFront);

        // Remove element from the rear
        String removedFromRear = deque.pollLast();
        System.out.println("Removed from Rear: " + removedFromRear);

        // Display all elements
        System.out.println("Deque: " + deque);
    }
}
```

### 4. **ArrayDeque:**

#### Description:

* ArrayDeque is a resizable-array implementation of the Deque interface.
* Elements can be added or removed from both ends efficiently.
* It is faster than ArrayList and Stack.

#### Example Code:

```java
import java.util.ArrayDeque;

public class ArrayDequeExample {
    public static void main(String[] args) {
        ArrayDeque<String> arrayDeque = new ArrayDeque<>();

        // Add elements at the rear
        arrayDeque.offerLast("Element 1");
        arrayDeque.offerLast("Element 2");

        // Add elements at the front
        arrayDeque.offerFirst("Element 3");

        // Remove element from the front
        String removedFromFront = arrayDeque.pollFirst();
        System.out.println("Removed from Front: " + removedFromFront);

        // Remove element from the rear
        String removedFromRear = arrayDeque.pollLast();
        System.out.println("Removed from Rear: " + removedFromRear);

        // Display all elements
        System.out.println("ArrayDeque: " + arrayDeque);
    }
}
```

These examples should give you a good understanding of how to use Queue, PriorityQueue, Deque, and ArrayDeque in Java.

* * *

**You:**

give me all this methods in separate table in markdown

* * *

**ChatGPT:**

Certainly! Here are the methods for each data structure in a separate markdown table:

### 1. **Queue:**

| Method | Description |
| --- | --- |
| `offer(E e)` | Inserts the specified element into the queue. |
| `poll()` | Retrieves and removes the head of the queue. |
| `peek()` | Retrieves, but does not remove, the head of the queue. |
| `size()` | Returns the number of elements in the queue. |
| `isEmpty()` | Returns true if the queue is empty; otherwise, false. |

### 2. **PriorityQueue:**

| Method | Description |
| --- | --- |
| `offer(E e)` | Inserts the specified element into the queue. |
| `poll()` | Retrieves and removes the head of the queue. |
| `peek()` | Retrieves, but does not remove, the head of the queue. |
| `size()` | Returns the number of elements in the queue. |
| `isEmpty()` | Returns true if the queue is empty; otherwise, false. |

### 3. **Deque:**

| Method | Description |
| --- | --- |
| `offerFirst(E e)` | Inserts the specified element at the front of the deque. |
| `offerLast(E e)` | Inserts the specified element at the end of the deque. |
| `pollFirst()` | Retrieves and removes the first element of the deque. |
| `pollLast()` | Retrieves and removes the last element of the deque. |
| `peekFirst()` | Retrieves, but does not remove, the first element of the deque. |
| `peekLast()` | Retrieves, but does not remove, the last element of the deque. |
| `size()` | Returns the number of elements in the deque. |
| `isEmpty()` | Returns true if the deque is empty; otherwise, false. |

### 4. **ArrayDeque:**

| Method | Description |
| --- | --- |
| `offerFirst(E e)` | Inserts the specified element at the front of the deque. |
| `offerLast(E e)` | Inserts the specified element at the end of the deque. |
| `pollFirst()` | Retrieves and removes the first element of the deque. |
| `pollLast()` | Retrieves and removes the last element of the deque. |
| `peekFirst()` | Retrieves, but does not remove, the first element of the deque. |
| `peekLast()` | Retrieves, but does not remove, the last element of the deque. |
| `size()` | Returns the number of elements in the deque. |
| `isEmpty()` | Returns true if the deque is empty; otherwise, false. |

These tables provide a quick reference for the methods associated with each data structure.