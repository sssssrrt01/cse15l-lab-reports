# Lab Report 5 - Part 1

## Step 1 
Student post: I'm not sure why my code is not working, it says that <9> is not equal to <9>. I can't figure it out. The pictures of the code and error are attached below. Thank you.
<img width="798" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/e9efb15b-2856-4380-ae2f-fedce360484a">
<img width="458" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/b3d2818b-82b6-414b-9c6e-eee7864c847c">

## Step 2
TA response: Hi, the testing file for this code is just a trivial test of adding two numbers. I can confirm that you are adding the numbers properly, but I would advise you to check your return value of your add method.  

## Step 3 
Student response: I see! I realize now that I am returning the wrong value. I have fixed it as such.  
<img width="379" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/d775d9d1-20cd-4509-9d16-b5c18fd2c3dc">
<img width="442" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/ef00c44f-27e3-4f08-a6ad-3ea7ff0d6ff7">


## Step 4
File setup:
The Addition.java, AdditionTest.java, and test2.sh files are in a directory called lab7 on the ieng6 computer.  

Pre-bug fix file:  
<img width="453" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/4001a46d-796d-4c08-9813-6d478406b87c">

Post-bug fix file:  
<img width="431" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/66b7834d-8454-4c49-af34-0276382742aa">

Testing file:  
<img width="475" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/823c075a-b71b-4922-ac52-9856df64eda6">

Bash script to run JUnit test file:  
<img width="824" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/da285f91-6a95-463d-bcf2-738174894432">

Command line used to run test: ```sh test2.sh``` 
Command line used to fix bug: ```vim Addition.java```, which opens the vim editor to edit the file, which is saved and closed with ```:wq```  

What to edit: The bug is a result of the wrong return value. Instead of returning the sum of the two numbers, the method just returns one of the input numbers! Instead of returning ```numberOne```, the file should return ```sum```. 







