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
<img width="687" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/ffd010ec-e818-490d-9c6b-8f3fb8616f97">  

Command 1 output: Find all files of under 1 MB and puts it into stuff.txt  
<img width="640" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/c9ef8afd-5761-4d6c-947a-c4f08a75cb01">
  

Command 2 output: Find all directories of under 1 MB and puts it into stuff2.txt  
<img width="390" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/38730f14-bd56-4f54-bac6-b6324b9fcaa9">




## Works Cited


