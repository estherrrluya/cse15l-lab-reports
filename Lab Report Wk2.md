# Lab Report Week 3

In this lab report, I will go through what we've learned through week 2 and week 3.

## Part 1

Part 1 will include a web server called StringServer that keeps track of a single string being added to by incoming requests, which is showed below.

![image](Screen Shot 2023-01-30 at 10.17.37 PM.png)

The method called are *getPath()*, *equals*, *getQuery()*, and *split()*. First, *getPath()* is called on the incoming *url* that returns the Path name of the given url. Then, *equals()* is called with the */add-message* as a input. If the Path name is */add-message*, then we will perform a split of query parameters from the input URL with the value *=*. In the next *if* statement, the first index, which is the value before *=*, of the parameter is compared with *s*. And then we will update the output to the string after *s=* with a new line by concatination the string with *\n*. 

No value got changed for any relevant fields of the class because the user can change directly on the localhost url to achieve their different requests. For example, I have changed the stirng after *s=* several times that generate different outputs in the following image.

![image](Screen Shot 2023-01-30 at 10.17.37 PM.png)

## Part 2

In part 2, I will go through the debugging process from lab 3. 

### Bug - Array ReverseInPlace Method

Below shows a failure-inducing input {1, 2, 3}. I expect the output to be a the reversed array which is {3, 2, 1} 

```
 @Test 
 public void testReverseInPlace1() {
    int[] input1 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3, 2, 1}, input1);
 }
```
But the actual output—the symptom—is below, that the element differs at index 2. The expected value is <1>, but it was actually <3>.

![Image](Screen Shot 2023-01-30 at 9.13.48 PM.png)

The bug in this code is that arr is continually updated, thus as you traverse the code, the array has already been modified when you arrive to the beginning of the array. 

But, for some input the failure is not induced like the one below.

```
  @Test 
  public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
  }

```

This is because the element only gets to be changed once.

Before finding the failure-inducing input, the code snippet is below. 

```
  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

After detecting the bug, the code is changed to below.

```
  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    int[] currArr = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      currArr[i] = arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = currArr[arr.length - i - 1];
    }
  } 
```

In this code snippet, the original array is first stored in a new *currArr* the same length as the input array, and then the input array is reversed according to the element from the opposite index in this *currArr*. This way, the original array won't be changed at the first few index.

## Part 3

I learned a lot during week 2 and 3, especially on how to handle different requests using url specific methods. I also learned how to use local github to commit code changes and push the new changes.  

