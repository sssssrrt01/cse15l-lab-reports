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
Find command:  
<img width="904" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/4d1540a2-09f5-4cea-ba6a-3a292312fd99">
<img width="485" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/118885a7-849e-4052-ba11-62ff1bf628a3">
<img width="465" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/524a2b3a-7dd9-49f6-9026-a4933bd68661">




## Works Cited


