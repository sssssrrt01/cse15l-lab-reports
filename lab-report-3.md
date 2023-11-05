# Lab Report 3

## Part 1

Bugged section of code from Week 4 Lab:  

```
public class ArrayExamples {
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```

JUnit Test:  
```
import static org.junit.Assert.*;


import org.junit.*;

public class ArrayTests {
  @Test
   public void lab4TestFailing() {
    int[] input1 = {1, 2, 3, 4};
    assertArrayEquals(new int[]{4, 3, 2, 1}, ArrayExamples.reversed(input1));
  }

  @Test
   public void lab4TestPassing() {
    int[] input1 = {0};
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input1));
  }
}
```
lab4TestFailing will result in a failing Junit test.  
lab4TestPassing will result in a passing Junit test.  
<img width="1059" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/44783a74-689b-43c7-b8ad-d3c489e3007a">

The symptom of the failing test is that the expected value is 0, instead of being 4. However, this passes in the test where the input array is 0. That means something is making it so that the values are all being mapped to 0.

Before:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
```

After:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```

Fixes: We are assigning values to the wrong array because we are taking the values of newArray (all 0's) and putting them into arr.
I also changed the return to be newArray.


## Part 2
**Using -type:**  
<img width="623" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/7e200dec-bc5d-4525-a367-437f66d9a89a">

Command 1 output: Find all files and puts it into stuff.txt  
<img width="613" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/8d256c61-645a-421e-891d-ae08cf78ba60">
  

Command 2 output: Find all directories and puts it into stuff2.txt  
<img width="387" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/3430624d-cafa-4b57-bcb0-bd37fc2ed1ee">




## Works Cited


