# Examples of AI Debugging Assistant in Action

This document provides practical examples of how the AI debugging assistant prompt works in real scenarios with different types of student code and skill levels. It demonstrates how the AI guides students without directly giving answers, building problem-solving and debugging skills.

## Example 1: Beginner Student – List Index Error

### Student's Code:
```python
fruits = ["apple", "banana", "cherry"]
print(fruits[3])
```


### Student's Problem:

"I'm trying to print the last fruit, but Python gives an IndexError."

### AI Response:

Hi! You’re working with lists that’s great. Let’s troubleshoot:

- How many elements are in your fruits list
- What are the valid index positions for these elements
- Which element are you actually trying to access

Try printing len(fruits) and see what range of indices is allowed. What happens if you use a negative index for the last element

### Why this works:

- Encourages counting and index reasoning
- Introduces Python indexing rules
- Provides small, actionable hints


---



## Example 2: Intermediate Student – String Concatenation Issue

### Student's Code:
```python
name = input("Enter your name: ")
age = input("Enter your age: ")
print("Hello " + name + ", you are " + age + " years old!")
```



### Student's Problem:

"When I type my age as 21, everything works, but I want to do arithmetic with the age later and it fails."

### AI Response:

Nice work collecting user input! Let’s consider:

- What type is returned by input()?
- If you want to add numbers later, how can you convert age to an integer?
- How could you print the message while keeping age as an integer for calculations?

Try using a type conversion and see how it affects both printing and math operations.

### Why this works:

- Explains the data type issue without giving full conversion code
- Encourages understanding input handling
- Provides context for debugging future arithmetic errors

---

## Example 3: Advanced Student – Off-by-One in Loops
### Student's Code:
```python
for i in range(1, 11):
    if i % 2 == 0:
        print(i)
        
```

### Student's Problem:

"I want to print only even numbers from 2 to 10, but I’m not sure if my loop is robust for other ranges."

### AI Response:

Good job using range() and modulo! Let’s analyze:

- What values of i does range(1, 11) produce?
- Are all values you want being included?
- How might the loop behave if you changed the start or end values?

Consider experimenting with range()’s start, stop, and step parameters. What happens if you use a step of 2 instead of checking with modulo?

### Why this works:

- Highlights potential off-by-one issues
- Encourages reasoning about loop behavior
- Suggests optimization without directly rewriting code

---

## Example 4: Beginner Student – ZeroDivisionError
### Student's Code:
```python
x = int(input("Enter a number: "))
y = int(input("Enter another number: "))
print(x / y)

```


### Student's Problem:

"When I enter 0 for the second number, I get an error."

### AI Response:

Ah! Division by zero can’t happen in Python. Let’s think:

- What values of y cause this error?
- How could you check or prevent zero before dividing?
- What message could you show if y is zero?

Try adding a conditional check. What happens if y is not zero vs zero?

Why this works:

- Focuses on understanding the exception
- Encourages thinking about edge cases
- Suggests a hands-on fix without giving exact code

---

## Example 5: Intermediate Student – File Handling
### Student's Code:
```python
file = open("data.txt", "r")
data = file.read()
print(data)
file.close()

```

### Student's Problem:

"Sometimes I get a FileNotFoundError, but I thought the file exists."

### AI Response:

Great start with file handling! Let’s reason:

- Is data.txt in the same directory as your script?
- What happens if the file path is wrong or misspelled?
- How can you safely open a file to avoid the program crashing if the file doesn’t exist?

Think about using Python’s file existence checks or try/except blocks to handle missing files gracefully.

### Why this works:

- Highlights common file I/O pitfalls
- Encourages proactive error handling
- Guides without giving the full solution

---

## Key Patterns in New Examples

- Encouragement first – Recognize what’s done well
- Clarifying questions – Understand the student’s perspective
- Guided discovery – Lead to insight without giving solutions
- Hints & suggestions – Provide actionable next steps
- Learning focus – Build understanding of Python concepts

### Adaptation by level:

- Beginners → syntax, data types, small logic issues
- Intermediate → loops, arithmetic, file handling
- Advanced → recursion, performance, design patterns

These examples illustrate how the AI prompt encourages independent debugging while providing structured guidance appropriate to the student's skill level.