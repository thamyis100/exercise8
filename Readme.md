# STM32 FreeRTOS - Demonstrate how to eliminate resource contention in a selective manner - using a semaphore to protect the critical code section

## Overview
Exercise 8 aims to demonstrate how to use a semaphore as a synchronization mechanism to protect critical code sections from resource contention in a selective manner within a multitasking system. This approach ensures that only one task can access shared resources at a time.

## Project Setup
1. Hardware: STM32F4 Discovery Board.  
2. Software Tools: STM32CubeMX for hardware configuration and FreeRTOS as the RTOS used.  
3. Development Environment: A compatible IDE such as Keil MDK-ARM or IAR EWARM.

## Task Implementation
1. Create Tasks: Define two or more tasks to access shared resources simultaneously.  
2. Integrate Semaphore: Create a binary semaphore to manage access to shared resources.  
3. Access Critical Section: Use FreeRTOS functions like `xSemaphoreTake` and `xSemaphoreGive` to ensure only one task accesses the critical resource at a time.

## Resource Contention Detection
- Identify potential conflicts by allowing tasks to access resources without synchronization.  
- Observe symptoms such as data anomalies or other undesired behaviors.

## Explanation
- A semaphore acts as a locking mechanism to prevent simultaneous access.  
- This implementation is more efficient than global suspension because it selectively protects specific resources.

## Prerequisites
1. Basic understanding of multitasking and resource management in FreeRTOS.  
2. Knowledge of hardware configuration using STM32CubeMX.  
3. Familiarity with the concept of semaphores in real-time programming.

## Usage
1. Initialize the semaphore in the `main()` function.  
2. Add code to protect critical resources using the semaphore in each task.  
3. Compile, upload to hardware, and execute.

## Expected Outcome
- No resource contention occurs during testing.  
- The multitasking system operates stably without data loss or other undesirable behaviors.

## Conclusion
Using a semaphore to protect critical code sections is an efficient solution to avoid resource contention in multitasking systems. This approach can be adapted to various scenarios where shared resources are managed by multiple tasks.

## Video Demo Project Exercise 8
https://github.com/user-attachments/assets/46460c90-9664-4a37-8000-cba912f0ff24
