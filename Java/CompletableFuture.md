**What is completablefuture in java? how many ways we can use it?**
* `CompletableFuture` is a class in Java that was introduced in Java 8 as part of the `java.util.concurrent` package. It represents a future result of an asynchronous computation, providing a flexible and powerful way to handle asynchronous programming in Java.

### What is `CompletableFuture`?

A `CompletableFuture` can be used to write non-blocking, asynchronous code. It allows you to perform tasks asynchronously and later combine the results, wait for them, or handle any exceptions that occur during their execution. `CompletableFuture` builds on the `Future` interface but provides a more feature-rich API, enabling easier and more intuitive composition of asynchronous tasks.

### Key Features

- **Completion Stage**: Methods to create and combine multiple `CompletableFuture` instances.
- **Non-blocking**: Operations can be chained and composed without blocking the main thread.
- **Exception Handling**: Built-in methods to handle exceptions in asynchronous pipelines.
- **Functional Programming**: Utilizes functional programming concepts, allowing lambda expressions and method references for callbacks.

### Ways to Use `CompletableFuture`

There are various ways to create, run, and combine `CompletableFuture` instances. Here are some of the most common usage patterns:

#### 1. Creating a `CompletableFuture`

- **Supply Async**: Runs a task asynchronously and returns a result.
  ```java
  CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> "Hello, World!");
  ```

- **Run Async**: Runs a task asynchronously that does not return a result.
  ```java
  CompletableFuture<Void> future = CompletableFuture.runAsync(() -> {
      // perform some action
  });
  ```

#### 2. Completing a `CompletableFuture`

- **Manual Completion**: Complete the future manually.
  ```java
  CompletableFuture<String> future = new CompletableFuture<>();
  future.complete("Manual Completion");
  ```

- **Complete Exceptionally**: Complete the future with an exception.
  ```java
  CompletableFuture<String> future = new CompletableFuture<>();
  future.completeExceptionally(new RuntimeException("Exception occurred"));
  ```

#### 3. Chaining `CompletableFuture` Instances

- **ThenApply**: Transforms the result of a future when it completes.
  ```java
  CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> "Hello")
                                                      .thenApply(result -> result + ", World!");
  ```

- **ThenAccept**: Consumes the result of a future when it completes.
  ```java
  CompletableFuture.supplyAsync(() -> "Hello")
                   .thenAccept(result -> System.out.println(result));
  ```

- **ThenRun**: Runs a runnable after the future completes, without using the result.
  ```java
  CompletableFuture.supplyAsync(() -> "Hello")
                   .thenRun(() -> System.out.println("Done!"));
  ```

- **ThenCompose**: Composes another future based on the result of the first future.
  ```java
  CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> "Hello")
                                                      .thenCompose(result -> CompletableFuture.supplyAsync(() -> result + ", World!"));
  ```

#### 4. Combining `CompletableFuture` Instances

- **ThenCombine**: Combines two futures and processes their results together.
  ```java
  CompletableFuture<String> future1 = CompletableFuture.supplyAsync(() -> "Hello");
  CompletableFuture<String> future2 = CompletableFuture.supplyAsync(() -> "World");
  CompletableFuture<String> combinedFuture = future1.thenCombine(future2, (result1, result2) -> result1 + " " + result2);
  ```

- **AllOf**: Waits for all futures to complete.
  ```java
  CompletableFuture<Void> allOfFuture = CompletableFuture.allOf(future1, future2);
  ```

- **AnyOf**: Waits for any one of the futures to complete.
  ```java
  CompletableFuture<Object> anyOfFuture = CompletableFuture.anyOf(future1, future2);
  ```

#### 5. Handling Exceptions

- **Exceptionally**: Provides a fallback result in case of an exception.
  ```java
  CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> {
      if (new Random().nextBoolean()) {
          throw new RuntimeException("Failed!");
      }
      return "Success";
  }).exceptionally(ex -> "Failure");
  ```

- **Handle**: Handles both the result and exception.
  ```java
  CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> {
      if (new Random().nextBoolean()) {
          throw new RuntimeException("Failed!");
      }
      return "Success";
  }).handle((result, ex) -> {
      if (ex != null) {
          return "Failure";
      }
      return result;
  });
  ```

### Example: Combining and Handling Results

```java
import java.util.concurrent.CompletableFuture;
import java.util.concurrent.ExecutionException;

public class CompletableFutureExample {
    public static void main(String[] args) {
        CompletableFuture<String> future1 = CompletableFuture.supplyAsync(() -> "Hello");
        CompletableFuture<String> future2 = CompletableFuture.supplyAsync(() -> "World");

        CompletableFuture<String> combinedFuture = future1
            .thenCombine(future2, (result1, result2) -> result1 + " " + result2)
            .thenApply(result -> result + "!")
            .exceptionally(ex -> "An error occurred: " + ex.getMessage());

        try {
            System.out.println(combinedFuture.get());  // Output: Hello World!
        } catch (InterruptedException | ExecutionException e) {
            e.printStackTrace();
        }
    }
}
```

### Conclusion

`CompletableFuture` is a powerful tool for managing asynchronous programming in Java. It provides numerous methods to create, chain, and combine asynchronous tasks, handle exceptions, and more, making it easier to write non-blocking, efficient, and maintainable code. Understanding how to use `CompletableFuture` effectively can greatly enhance your ability to handle concurrency and asynchronous operations in Java applications.
