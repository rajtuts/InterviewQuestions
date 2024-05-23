**What is Busy Spinning? Why Should You Use It in Java?**

By not releasing the CPU or suspending the thread, your thread retains all the cached data and instructions, which may be lost if the thread was suspended and resumed back in a different core of the CPU.

**What is Read-Write Lock? Does ConcurrentHashMap in Java Use the ReadWrite Lock?**

ReadWrite Lock is an implementation of a lock stripping technique where two separate locks are used for reading and writing operations. Since the read operation doesn't modify the state of the object, it's safe to allow multiple thread access to a shared object for reading without locking, and by splitting one lock into the read and write lock, you can easily do that.
Java provides an implementation of a read-write lock in the form of the ReentrantReadWritLock class in the java.util.concurrent.lock package. 

Also, the current implementation of java.util.ConcurrentHashMap doesn't use the ReadWriteLock; instead, it divides the Map into several segments and locks them separately using different locks. This means any given time, only a portion of the ConcurrentHashMap is locked, instead of the whole Map.

**How to Make an Object Immutable in Java? Why Should You Make an Object Immutable?**

when you mention String is Immutable, be ready with some reasons Why String is Immutable in Java.

Which Design Patterns have You Used in Your Java Project?
Always expect some design patterns-related questions for the Core Java Interview for the senior developer position. It's a better strategy to mention any GOF design pattern rather than Singleton or MVC, which almost every Java developer uses.
Your best bet can be a Decorator pattern or maybe a Dependency Injection Pattern, which is quite popular in the Spring Framework. It's also good to mention only the design patterns which you have used in your project and know their tradeoffs.
It's common that once you mention a particular design pattern, say Factory or Abstract Factory, Interviewer's next question would be, have you used this pattern in your project? So be ready with proper examples and explain why you choose a particular pattern.

**Do you know about Open Closed Design Principle or Liskov Substitution Principle?**

Design patterns are based on object-oriented SOLID design principles.


**Which Design Pattern Will You Use to Shield Your Code From a Third Party library? Which Another Will Likely replace in a Couple of Months?**

This is just one example of the scenario-based design pattern interview question. To test the practical experience of Java developers with more than five years of experience, companies ask this kind of question.
You can expect more real-world design problems in different formats, some with more detailed explanations with the context or some with only intent around.
One way to shield your code from a third-party library is to code against an interface rather than implementation and then use dependency injection to provide a particular implementation. This kind of question is also asked quite frequently by experienced and senior Java developers with 5 to 7 years of experience.

**How do you prevent SQL Injection in Java Code?**

This question is asked more by J2EE and Java EE developers than core Java developers, but it is still a good question to check the JDBC and Security skill of experienced Java programmers.

You can use PreparedStatement to avoid SQL injection in Java code. Use of the PreparedStatement for executing SQL queries not only provides better performance but also shields your Java and J2EE application from SQL Injection attacks.
On a similar note, If you are working more on Java EE or J2EE side, then you should also be familiar with other security issues, including Session Fixation attacks or Cross-Site Scripting attacks, and how to resolve them. These are some fields and questions where a good answer can make a lot of difference in your selection.

Tell me about different Reference types available in Java, e.g., WeakReference, SoftReference, or PhantomReference? and Why should you use them?
Well, they are different reference types coming from java.lang.ref package and provided to assist Java Garbage Collector in case of low memory issues. If you wrap an object with WeakReference, then it will be eligible for garbage collected if there are o strong references. They can later be reclaimed by the Garbage collector if JVM is running low on memory.
The java.util.WeakHashMap is a special Map implementation whose keys are the object of WeakReference, so if only Map contains the reference of any object and no other, those objects can be garbage collected if GC needs memory.

**How does the get method of HashMap work in Java?**

Yes, this is still one of the most popular core Java questions for senior developer interviews. You can also expect this question on a telephonic round, followed by lots of follow-up questions.

The short answer to this question is that HashMap is based upon hash table data structure and uses the hashCode() method to calculate hash code to find the bucket location on the underlying array and the equals() method to search the object in the same bucket in case of a collision.

**Which Two Methods HashMap key Object Should Implement?**

This is one of the follow-up questions I was talking about in the previous questions. Since the working of HashMap is based upon hash table data structure, any object which you want to use as a key for HashMap or any other hash-based collection, e.g., Hashtable or ConcurrentHashMap must implement equals() and hashCode() method.
The hashCode() is used to find the bucket location, i.e., the index of the underlying array, and the equals() method is used to find the right object in a linked list stored in the bucket in case of a collision.
By the way, from Java 8, HashMap also started using a tree data structure to store the object in case of a collision to reduce the worst-case performance of HashMap from O(n) to O(logN).

**Why Should an Object Used As the Key should be Immutable?**

This is another follow-up to the previous core Java interview questions. It's good to test the depth of technical knowledge of candidates by asking more and more questions on the same topic. If you know about Immutability, you can answer this question by yourself.
The short answer to this question is key should be immutable, so that hashCode() method always returns the same value.

Since the hash code returned by the hashCode(,) method depends on the content of the object, i.e., values of member variables. If an object is mutable, then those values can change, and so is the hash code. If the same object returns a different hash code once you insert the value in HashMap, you will end up searching in different bucket locations and will not be able to retrieve the object.
That's why the key objective should be immutable. It's not a rule enforced by the compiler, but you should take care of it as an experienced programmer.

**How does ConcurrentHashMap achieve its Scalability?**

Sometimes this multithreading + collection interview question is also asked as the difference between ConcurrentHashMap and Hashtable in Java. The problem with synchronized HashMap or Hashtable was that the whole Map is locked when a thread performs any operation with Map.
The java.util.ConcurrentHashMap class solves this problem by using a lock stripping technique, where the whole map is locked at different segments, and only a particular segment is locked during the write operation, not the whole map.
The ConcurrentHashMap also achieves its scalability by allowing lock-free reads as read is a thread-safe operation.

**How do you share an object between threads? Or How to pass an object from one thread to another?**

There are multiple ways to do that, like Queues, Exchanger, etc., but BlockingQueue using the Producer-Consumer pattern is the easiest way to pass an object from one thread to another.

**How do you find out if your program has a deadlock?**

By taking thread dump using kill -3, using JConsole or VisualVM), I suggest preparing this core java interview question in more detail, as the Interviewer definitely likes to go with more detail, e.g., they will press with questions like, have you really done that in your project or not?
