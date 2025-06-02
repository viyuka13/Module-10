# # Stack-Stack Reversal Program 🔁

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

## 🎯 Aim

To write a Python program that reverses the values in a stack using standard stack operations.

## 📋 Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:
      stack = []
      n = int(input())
      
      for _ in range(n):
          element = int(input())
          stack.append(element)
      
      reverse = []
      
      while stack:
          reverse.append(stack.pop())
      
      print(reverse)

## 🧪 Sample Input and Output
![image](https://github.com/user-attachments/assets/a579fbb8-9cac-42ac-98bf-cd416a216762)

## Result
The program creates a stack, pushes 4 elements onto it, then pops all elements to create a reversed list. The reversed list is printed, showing that the elements come off the stack in last-in, first-out order.
