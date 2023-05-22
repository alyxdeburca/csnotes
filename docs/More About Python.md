---
share: true  
---

## Recursion

```python
def factorial(numIn):
	if numIn > 1:
		return numIn * factorial(numIn - 1)
	else:
		return 1
ans = factorial(6)
print(ans)
```
- What is recursion?
  - Breaking down a problem into subsets of itself
  - Repeating these steps until the problem is solved
- In computing a Recursive Function calls itself
  - In each Recursive call, it passes a subset of the function as an argument
  - Problem continuously broken down into subsets of itself until it reaches a stopping point also called a **Base Case**
  
  **Testing for Palindromes using Recursion**
```python
def is_palindrome(l,r,S):
	if l>=r:
		return True
	if S[l] != S[r]:
		return False
	return is_palindrome(l+1,r-1,S)
my_string = input("Enter a string: ")
l = 0
r = len(my_string) - 1
check = is_palindrome(l,r,my_string.upper())
if check:
	print(f"{my_string} is a palindrome")
else:
	print(f"{my_string} is not a palindrome")
```
**Factorial calculation using recursion**
```python
def main():
	# n = eval(input("Enter a non-negative integer: "))
	for n in range(1,10):
		print("Factorial of " + str(n) + " is " + str(factorial(n)))
def factorial(n):
	if n == 0:
		return 1
	else:
		return (n * factorial(n-1))
main()
```
- So, should we use Recursion all the time?
  - Can be useful in solving mathematical problems
  - Can be efficient but that's not always the case
  - Sometimes, iteration is much simpler and faster
  - Recursion can be 'elegant' ... but also confusing
  - Many programmers avoid recursion
  - However, it can be useful ....
  - Often used in Factorial, Fibonacci Series, etc.
  - Also useful in searching and sorting algorithms
**Fibonacci Sequencer using Recursion**
```python
def fib(n):
	if n in {0, 1}:
		return n
	return fib(n-1) + fib(n-2)
x = int(input("How many elements? "))
print("Fibonacci Sequence", x, "elements")
for i in range(0,x):
	print(fib(i))
```

**Fibonacci Sequencer without Recursion**
```python
from fibonacci import fibonacci
x = input("How many elements? ")
print("Fibonacci Sequence", x, "elements")
for i in fibonacci(length=int(x)):
	print(i)
```

## Searching And Sorting
- Algorithms used to Sort and Search through Lists
- **Lists:**
  - Also called an array in other languages
  - Used to store an ordered collection of items
  - Typical examples of Lists could include
    - Weekdays = \['Mon', "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"\]
  - List functions and Operators can be used to manipulate lists
  - Lists are Zero-Based
  - Watch this when looping through a list
  - Beware the Off-By-One-Error - OBOE!
  - Item n in a list Mylist can be accessed using MyList\[n\]
  - A string is a basic type of list
  - `MyString = "Python"` can be converted to a list using .list()

- **List Functions:**
  - List.pop(n) removes item n
```python
myList = [85, 96, 63, 96, 17, 31, 96, 50]
key = 96
keyCtr = 0
for index in range(len(myList)):
	if myList[index] == key:
		location = index
		keyCtr = keyCtr + 1
print(f"Linear Search: \n")
print(f"Find {key} in {myList}\n")

if keyCtr == 0:
	print("Key not found.")
else:
	if keyCtr == 1:
		print(f"Key found at: {location}")
	else:
		print(f"{keyCtr} keys found. Final location: {location}\n")

```
```python
myList = [85, 96, 63, 96, 17, 31, 96, 50]
key = 96
locations = []
while True:
	try:
		for index in range(len(myList)):
			if myList[index] == key:
				myList.pop(index)
				locations.append(index)
	except:
		break
print(f"Found {len(locations)} keys at locations {locations}")

```

```python
myList = [17, 24, 31, 45, 50, 63, 85, 96]
def binarySearchLoop(listIn, key):
	first = 0
	last = len(listIn) -1
	while (last - first) >=0:
		middle = first + ((last - first) // 2)
		if listIn[middle] == key:
			return middle
		elif key < listIn[middle]:
			last = middle - 1
		else:
			first = middle +1
	return False
key = 64
search = binarySearchLoop(myList, key)
if search == False:
	print("Key not found.")
else:
	print(f"Key found at index: {search}.")
```

