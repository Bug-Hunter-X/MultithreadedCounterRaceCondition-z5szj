# Java Multithreaded Counter Race Condition

This repository demonstrates a classic race condition in Java involving a simple counter incremented by multiple threads. The `Counter` class is not thread-safe, resulting in an incorrect final count when multiple threads access and modify the `count` variable concurrently.

## How to Reproduce

1.  Clone this repository.
2.  Compile and run `Main.java`.
3.  Observe that the final count is less than 2000, even though 2000 increments are attempted.

## Solution

The solution involves making the `increment()` method thread-safe by using appropriate synchronization mechanisms (e.g., `synchronized` keyword or `AtomicInteger`).