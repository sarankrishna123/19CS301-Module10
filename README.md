# 19CS301-Module10
###EX: 10.a  STACK
### Aim: To Write a python program to get the integer values from the user and push only the odd number into the stack and later pop the last 2 elements
### Algorithm:
STEP 1: Start.

STEP 2: Create a list and a variable n.

STEP 3: Get the value of n from user.

STEP 4: Using loop append only odd elements in the stack.

STEP 5 : Using another loop using built-in pop operation pop the last two elements.

STEP 6: Print the result.

STEP 7 : Stop.
### Program:
```
reg no:212223070023
name:saran krishna P S
stack = []
n = int(input("Enter the number of elements: "))

for _ in range(n):
    val = int(input())
    if val % 2 != 0:
        stack.append(val)

print("Stack after pushing odd numbers:", stack)

if len(stack) >= 2:
    stack.pop()
    stack.pop()
elif len(stack) == 1:
    stack.pop()

print("Stack after popping last 2 elements:", stack)

```
### Output:
![image](https://github.com/user-attachments/assets/dd8866bf-2d68-4da9-b7b6-c4d2f1b0730c)


### Result: Thus, the given program is implemented and executed successfully .
 


### EX: 10.2 IMPLEMENTATION OF STACK
### Aim: To Write a python program to implement the stack using deque method for rotating the stack.
### Algorithm:

STEP 1: Start.

STEP 2: Import collections and import deque.

STEP 3: Create a list and get the input from user.

STEP 4: Create a variable n and get number of inputs from user.

STEP 5 : Using a loop get the inputs from user and append in deque.

STEP 6: Using rotate function rotate the stack.

STEP 7 : Print the result. 

STEP 8 : Stop.
### Program: 

```
reg no:212223070023
name:saran krishna P S
from collections import deque

stack = deque()

n = int(input("Enter number of elements to push into the stack: "))
for _ in range(n):
    val = input("Enter value: ")
    stack.append(val)

print("Original Stack:", list(stack))

k = int(input("Enter rotation value (positive = right, negative = left): "))
stack.rotate(k)

print("Stack after rotation:", list(stack))

```
### Output:

![image](https://github.com/user-attachments/assets/e6fcaef4-4b5c-45b5-a015-b6bcdb9aeb99)

### Result: Thus, the given program is implemented and executed successfully .
 


EX: 10.3 QUEUE
### Aim: To Write a python program to implement the stack using deque method for rotating the stack.
### Algorithm:

STEP 1: Start.

STEP 2: Import collections and import deque.

STEP 3: Create a stack and a variable n.

STEP 4: Get the number of inputs from user.

STEP 5: Using a loop get the inputs from user.

STEP 6: Append the even and unique elements in the stack.

STEP 7: Print the result.
### Program:
```
reg no:212223070023
name:saran krishna P S
from collections import deque

class Stack:
    def __init__(self):
        self.stack = deque()

    def push(self, value):
        self.stack.append(value)

    def pop(self):
        if self.is_empty():
            return None
        return self.stack.pop()

    def rotate(self, k):
        self.stack.rotate(k)

    def display(self):
        print("Stack (top on right):", list(self.stack))

    def is_empty(self):
        return len(self.stack) == 0

# Example usage
s = Stack()
n = int(input("Enter number of elements to push into the stack: "))
for _ in range(n):
    val = input("Enter value: ")
    s.push(val)

s.display()

k = int(input("Enter rotation value (positive = right, negative = left): "))
s.rotate(k)

print("After rotation:")
s.display()

```
### Output:
![image](https://github.com/user-attachments/assets/f36727ec-a380-4373-885f-9aee0e398f09)

 
### Result: Thus, the given program is implemented and executed successfully .


### EX: 10.4 IMPLEMENTATION OF QUEUE
### Aim: To Develop a python program to get the 4 integer values from user and display the values using multiprocessing library
### Algorithm:

STEP 1: Start.

STEP 2: From Multiprocessing Import Queue.

STEP 3: Create a list and get the input from user.

STEP 4 : Append the elements in the list.

STEP 5: Using 'get' built-in function print the list.

STEP 6 : Print the result.

STEP 7 : Stop.
### Program:
```
reg no:212223070023
name:saran krishna P S
from multiprocessing import Process

def display_value(val):
    print(f"Value: {val}")

if __name__ == "__main__":
    values = []
    print("Enter 4 integer values:")
    for i in range(4):
        num = int(input(f"Value {i+1}: "))
        values.append(num)

    processes = []
    for val in values:
        p = Process(target=display_value, args=(val,))
        processes.append(p)
        p.start()

    for p in processes:
        p.join()

```
### Output:
 ![image](https://github.com/user-attachments/assets/f698ccce-41a4-4d3b-bb21-59ac020aae89)


### Result: Thus, the given program is implemented and executed successfully .
 
### EX: 10.4  check whether the stack is full and then display the stack values in reverse order
### Aim: Write a Python program to create a stack of maximum size 5 using LifoQueue, accept elements from the user, check whether the stack is full, and then display the elements in reverse order (from top to bottom).

### Algorithm:
Start
Import LifoQueue from the queue module.
Create a stack with a maximum size of 5.
Read the number of elements 𝑛
n to be inserted (up to 5).
For each element (up to 𝑛n):
Read the input number.
Push (put) the element onto the stack.
Check if the stack is full using stack.full().
Print True if full, else False.
Create an empty list to store popped elements.
While the stack is not empty:
Pop (get) an element from the stack and append it to the list.
Print the elements of the list (which represent the stack in reverse order).
End
### Program:
```
reg no:212223070023
name:saran krishna P S
from queue import LifoQueue
stack = LifoQueue(maxsize=5)
n= int(input())
for i in range(n):
    stack.put(input())
print(stack.full())
for i in range(n):
    print(stack.get())

```
### Output:
![image](https://github.com/user-attachments/assets/51f4d171-f949-4d94-8945-f2f7dd08b203)

### Result: Thus, the given program is implemented and executed successfully .
 


