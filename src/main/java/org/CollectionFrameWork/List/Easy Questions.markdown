### List Interface Interview Questions (easy to medium)

1. **What is the `List` interface in Java?**

    * The `List` interface is an ordered collection that allows duplicate elements and is index-based.

2. **Explain the difference between `ArrayList` and `LinkedList`.**

    * `ArrayList` uses an array for dynamic sizing, providing fast random access. `LinkedList` uses a doubly-linked list and is suitable for frequent insertions and removals.

3. **Why is `Vector` considered legacy, and what is its alternative?**

    * `Vector` is considered legacy due to its synchronization overhead. `ArrayList` is a preferred alternative unless thread safety is required.

4. **What is the purpose of the `Stack` class in Java?**

    * The `Stack` class represents a last-in, first-out (LIFO) stack of objects and includes standard push and pop operations.

5. **How do you iterate through elements in a `List`?**

    * You can use an iterator, enhanced for loop, or Java 8 streams to iterate through elements in a `List`.

6. **Can you store different data types in a `List`?**

    * Yes, a `List` in Java can store elements of different data types.

7. **Explain the difference between `remove(int index)` and `remove(Object o)` methods.**

    * `remove(int index)` removes the element at the specified index, while `remove(Object o)` removes the first occurrence of the specified object.

8. **What is the significance of the `add(int index, E element)` method in a `List`?**

    * This method inserts the specified element at the specified position in the list, shifting the existing elements to make room.

9. **How do you check if a specific element is present in a `List`?**

    * You can use the `contains(Object o)` method to check if a specific element is present in a `List`.

10. **When would you choose `ArrayList` over `LinkedList` and vice versa?**

    * Choose `ArrayList` when you need fast random access and read-heavy operations. Choose `LinkedList` for frequent insertions and removals.

11. **Can a `List` contain `null` elements?**

    * Yes, a `List` in Java can contain `null` elements.

12. **Explain the difference between the `addFirst` and `addLast` methods in `LinkedList`.**

    * `addFirst` inserts the specified element at the beginning of the list, while `addLast` appends it to the end.

13. **What is the purpose of the `clear()` method in a `List`?**

    * The `clear()` method removes all elements from the list, making it empty.

14. **How does the `ArrayList` dynamically resize itself?**

    * `ArrayList` dynamically resizes itself by creating a new array with a larger capacity and copying the elements from the old array.

15. **What is the time complexity of the `get` operation in `ArrayList` and `LinkedList`?**

    * The time complexity of the `get` operation is O(1) for `ArrayList` and O(n) for `LinkedList`.

16. **How does the `Stack` class relate to the `Vector` class in terms of inheritance?**

    * The `Stack` class extends the `Vector` class, inheriting its properties and methods.

17. **Can you use the `add` method to insert an element at a specific index in a `List`?**

    * Yes, the `add` method can be used to insert an element at a specific index by providing the index as an argument.

18. **What is the role of the `pop` method in the `Stack` class?**

    * The `pop` method removes and returns the element at the top of the stack.

19. **How would you check if a `List` is empty?**

    * You can use the `isEmpty()` method to check if a `List` is empty.

20. **What is the purpose of the `peek` method in the `Stack` class?**

    * The `peek` method returns the element at the top of the stack without removing it.
