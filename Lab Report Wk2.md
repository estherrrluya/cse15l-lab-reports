# Lab Report Week 3

In this lab report, I will go through what we've learned through week 2 and week 3.

## Part 1

Part 1 will include a web server called StringServe that keeps track of a single string being added to by incoming requests.


## Part 2

In part 2, I will go through the debugging process from lab 3. 

### Bug 1 - Array Reverse Method

Below shows a failure-inducing input {1, 2, 3}. I expect the output to be a the reversed array which is {3, 2, 1} 

```
  @Test 
	public void testReverseInPlace1() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3, 2, 1}, input1);
	}
```
But the actual output is below. 

![Image](Screen Shot 2023-01-30 at 9.13.48 PM.png)





