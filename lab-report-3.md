# Lab Report 3

# Part 1

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


# Part 2
## **1) Using -type:**  
```
find ./technical -type f > "stuff.txt"
find ./technical -type d > "stuff2.txt"
```

Command 1 output: Find all files and puts it into stuff.txt  
<img width="613" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/8d256c61-645a-421e-891d-ae08cf78ba60">
  

Command 2 output: Find all directories and puts it into stuff2.txt  
<img width="387" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/3430624d-cafa-4b57-bcb0-bd37fc2ed1ee">

This command is useful because it allows us to discriminate between files and directories and search accordingly.  
  
---
  
## **2) Using -name:**  
```
find ./technical -name "Survey.txt" > "stuff3.txt"
find ./technical -name "Media" < "stuff4.txt"
```

Command 3 output: Find all files that are named Survey.txt  
<img width="389" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/163c770e-840d-4aea-87e5-8d1be2650ab0">


Command 4 output: Find all things that are named Media (Directories in this case):  
<img width="320" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/63e392f9-c0d9-4648-a0c6-ba90c3e0e538">
This command is useful because it allows us to search for a file or a directory by a specific name. For instance, we might know the name of a file but not where it is downloaded to.  
  
---  
  
## **3) Using -size:**  
```
find ./technicial -type f -size +10k > "stuff5.txt"
find ./technical -type d -size +10k > "stuff6.txt"
```
  
Command 5 output: Find all files that are greater than 10 kilobytes:  
<img width="625" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/b3a5a004-0750-46d7-8ab4-b39425cf84aa">  

  
Command 6 output: Find all directories that are greater than 10 kilobytes:  
<img width="333" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/d5a9034d-8290-449d-84c2-b562f4a06de4">  
This command is useful because we can search for directories and files that are of a certain size range, or greater/less than.  
  
  
---
## **4) Using -newer:**  
```
find ./technical -newer "./technical/biomed" > "stuff7.txt"
find ./technical -newer "./technical/911report/chapter-2.txt" > "stuff8.txt"
```

Command 7 output: Find all files that are newer than the biomed directory:  
<img width="619" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/6ba7c595-aa39-4b6d-9d24-541364dd24c4">  

Command 8 output: Find all files that are newer than the chapter-2.txt file in the 911report directory:  
<img width="643" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/ccbebdef-d2e3-471a-a839-0c585e18c3fc">  
This command is useful because we may want to find all files or all directories that are created before or after a certain date. ```-newer``` allows us to do that.


## Works Cited
https://linux.die.net/man/1/find
All of the information used in part 2 was found from the official Linux documentation.

