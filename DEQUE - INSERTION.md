# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```
import collections 
n1=int(input())
n2=int(input())
n3=int(input())
de = collections.deque([n1,n2,n3])
de.append(14)
de.append(15)
print("The deque after appending at right is : ")
print(de)
```

### OUTPUT
<img width="936" height="287" alt="image" src="https://github.com/user-attachments/assets/e32387d8-2e11-4bb3-bc62-5e7f181d4599" />

### RESULT
Thus a Python program to insert elements at REAR END of deque using a collection built-in function has been executed successfully.
