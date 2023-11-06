# Lab Report 3 - Bugs and Commands 

## Part 1 - Bugs 
In the `ArrayExamples` class, a bug was found within the `reversed` method. This method is supposed to return a new array with the elements reversed. However, due to a mistake in the loop's logic, it produces an error as a result. The error was revealed by our JUnit test suite. When the JUnit is run its output pinpoints the location of the bug and demonstrates its effect.

**Failure-Inducing Input**: 

The JUnit test method, `testReversed1()`, will show the defects within the `reversed` method in the `ArrayExamples`class:

```
@Test
public void testReversed1()
{
  int[] arr = {1, 2, 3};
  int[] expected = ArrayExamples.reversed(arr);
  assertArrayEquals(new int[]{3, 2, 1}, expected);
}
```
This test should pass if the `reversed` method functions correctly, but it fails with the current implementation. 

**Non-Failure-Inducing Input**: 

The test method `testReversed()` demonstrates where the `reversed` method does not cause a failure dealing with an empty array:
```
@Test
public void testReversed()
{
  int[] input1 = {};
  assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1));
}

```
This test passes because reversing an empty array does not change it.

**Symptom:** 

![Image](output.png)

