# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
      SIZE = 5
      queue = [None] * SIZE
      front = -1
      rear = -1
      removed_values = []
      
      def enqueue(value):
          global front, rear
          if (rear + 1) % SIZE == front:
              print("Queue is full")
              return
          if front == -1:
              front = 0
          rear = (rear + 1) % SIZE
          queue[rear] = value
      
      def dequeue():
          global front, rear
          if front == -1:
              print("Queue is empty")
              return None
          value = queue[front]
          if front == rear:
              front = -1
              rear = -1
          else:
              front = (front + 1) % SIZE
          return value
      
      def display():
          if front == -1:
              print("Queue is empty")
              return
          i = front
          elements = []
          while True:
              elements.append(queue[i])
              if i == rear:
                  break
              i = (i + 1) % SIZE
          print("Queue contents:", elements)
      
      # Enqueue 3 values from user
      for _ in range(3):
          val = int(input("Enter value to enqueue: "))
          enqueue(val)
      
      display()
      
      # Dequeue 3 values and store them
      for _ in range(3):
          removed = dequeue()
          if removed is not None:
              removed_values.append(removed)
      
      print("Removed values:", removed_values)

### Output:
![image](https://github.com/user-attachments/assets/1aefd3f4-fb75-4039-a498-278752b17525)

## Result:
The program initializes a circular queue with a fixed size of 5. It enqueues 3 user inputs, displays the queue contents, then dequeues 3 values, printing them. The circular queue maintains the order correctly and the removed values are displayed as expected.
