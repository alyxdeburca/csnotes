---
share: true  
---

- Testing ensures software meets design requirements (SPECification)
- Finds Bugs - Logic errors
- But what about Syntax errors?

- Unit - Smallest components of a program that can be tested
  - e.g. Loop, Function, etc.
- Usually automated - much faster so allows more testing
- Test Cases (Chapter 1)
- Unit test is just another piece of code!
  - Passes parameters (Arguments) to the Function
  - Unit Test calculates (or holds) the "Expected Value"
  - Function returns the "Actual Value"
- Unit test code must be written independently
- Otherwise it's a pointless exercise (Programmers' Bias)
### Simple Unit Test
```python
print("Unit testing")
print("============")

def volumeOfCylinder(radiusIN, heightIN):
	volume = 3.14 * (radiusIN ** 2) * heightIN
	return volume
def unitTest():
	testR = 2
	testH = 1
	expectedVal = 3.14 * (testR ** 2) * testH
	actualVal = volumeOfCylinder(testR, testH)
	passed = True
	if expectedVal != actualVal:
		passed = False
	return passed
print(f"Test passed {unitTest()}")
```

### Automated Unit Test with 25 cases
```python
print("Function TEST")
def addNums(x,y):
	return(x+y)

print("i    j    Expected    Actual")
testPass = True
for i in range(5):
	for j in range(5):
		expectedResult = i + j
		actualResult = addNums(i,j)
		print(i, " ", j, "    ", expectedResult, "     ", actualResult)
		if expectedResult != actualResult:
			testPass = False
print("Test passed? ", testPass)
```

### Automated Unit test with Array of cases
```python
print("UnitTest_ReturnValue1") 
print("Unit Test Demo")

#First let's define the volume() Function def volumeOfCylinder (radius IN, heightIN): volume = 3.14 * (radiusIN ** 2)* height IN return volume

#Now let's define the unitTest() Function 
def VolumeOfCylinder(radiusIN, heightIN):
	volume = 3.14 * (radiusIN ** 2) * heightIN
	return volume

def unitTest():
	testRs = [2, 4, 6, 10]
	testHs = [1, 2, 3, 5]
	success = 0
	successful = ""
	
	for i in range (len(testRs)): 
		testR = testRs[i] 
		testH = testHs[i] 
		expectedVal = 3.14 * (testR ** 2) * testH 
		actualVal = volumeOfCylinder (testR, testH) 
		if expectedVal == actualVal:
			success = success + 1 
	successful = str(success) + "/" + str(len(testRs))

	return successful
#Now we need to call the unitTest() Function

#This is the only code in the Program Body! 
print("Test passed: ", unitTest())
```


