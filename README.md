# se-questions

### Q: Where does memory usually store in?
Memory usually stores in heap and stack.

### Q: So what is a stack in terms of memory? Isn't it a data structure?
Yes, stack is a data structure. In order to understand stack in term of memory, we need to understand the stack data structure.

Stack data structure follows First-In, Last Out (FILO) structure, which means if you put something into the stack, you can only insert / put things onto the top so it stacks up - push. You can't take anything out from the bottom, you can't take anything out from the middle, the only thing you can do is to take the item on the top out 1 by 1, which we call the action - pop.

In applications, we have what we call - a call stack.

```python
def doAddition(self, a, b):
    total = a + b
    return total

def main():
    x = 5
    y = 3
    result = doAddition(x, y)
    print("Sum of the integers : ", result)
```
When the main() is called, the main() method will be added into an empty call stack. The doAddition(x, y) method will be added on top on the main() in call stack. A call stack keeps track of the methods and tell the application where should it continue after a method finished its execution. For example, after doAddition(x, y) finished its summation, it will be popped out from the call stack and the application will go back to the main() method to print out the sum of both integers.

In every method in call stack will have its own local variable for example variables x and y in main(), variable total in doAddition()

### Q: How does the heap differ from stack?
Variables in stack will disappeared after the specific method finished its execution, and here is where heap memory comes in if you need a variable to outlive stack memory. Heap memory is still accessible after all methods finished running.

Since heap is so powerful, why not we just use heap for every variables? Because its EXPENSIVE (causes overhead)

To go deeper into stack and heap memory, we need to first understand value type and reference type, how data is stored and manipulated in computer memory.

### Q: What is value type and reference type?
