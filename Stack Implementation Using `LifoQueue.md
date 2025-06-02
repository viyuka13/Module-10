# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program
      from queue import LifoQueue
      
      stack = LifoQueue(maxsize=7)
      n = int(input())
      
      for _ in range(n):
          if not stack.full():
              value = input()
              stack.put(value)
      
      print(stack.full())
      
      while not stack.empty():
          print(stack.get())

## 🧪 Sample Input and Output
![image](https://github.com/user-attachments/assets/667f9885-7a17-4b67-ae6e-b409289a87f7)

## Result:
The program successfully creates a stack with a maximum size of 7, reads 5 input elements, pushes them onto the stack, confirms the stack is not full, and then pops and prints the elements in reverse order, demonstrating the LIFO behavior of the stack.
