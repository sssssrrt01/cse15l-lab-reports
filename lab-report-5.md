# Lab Report 5 - Part 1

## Step 1 
Student post: I'm not sure why my code is not working, it says that <9> is not equal to <9>. I can't figure it out. The pictures of the code and error are attached below. Thank you.  
<img width="419" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/60655ffa-8d75-4572-8460-8696b0556ac5">  
<img width="798" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/e9efb15b-2856-4380-ae2f-fedce360484a">  
<img width="458" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/b3d2818b-82b6-414b-9c6e-eee7864c847c">  
## Step 2
TA response: Hi, the testing file for this code is just a trivial test of adding two numbers. I can confirm that you are adding the numbers properly, but I would advise you to check your return value of your add method.  

## Step 3 
Student response: I see! I realize now that I am using the wrong assert command in JUnit. Although the values are the same, the assert statement is checking whether both of the objects are the same, which it is not.  
<img width="379" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/d775d9d1-20cd-4509-9d16-b5c18fd2c3dc">
<img width="485" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/4152b708-acf7-4203-b0da-fdd211120028">


## Step 4
File setup:
The Addition.java, AdditionTest.java, and test2.sh files are in a directory called lab7 on the ieng6 computer. The student is responsible for fixing the files so that we achieve the proper functionality as well as fix the testing file.  

Pre-bug fix file:  
<img width="458" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/b3d2818b-82b6-414b-9c6e-eee7864c847c">

Post-bug fix file:  
<img width="485" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/a683a4db-9f43-4f80-b44f-d33e961947bf">

Testing file:  
<img width="475" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/823c075a-b71b-4922-ac52-9856df64eda6">

Bash script to run JUnit test file:  
<img width="824" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/da285f91-6a95-463d-bcf2-738174894432">

Command line used to run test: ```sh test2.sh``` 
Command line used to fix bug: ```vim AdditionTest.java```, which opens the vim editor to edit the file, which is saved and closed with ```:wq```    

What to edit: The bug is a result of the wrong object. Despite the values of the objects being the same, the Integer object with a value of 9 is not the same object as the int 9, so that will lead to an assert error, despite the values being the same.  

# Lab Report 5 - Part 2
Something I found really cool about this second half of the class was learning to manipulate files on a remote server. My computer broke and I had to get it repaired, so I actually did this assignment with the ieng6 remote computer instead of downloading the correct version of JUnit, Java, command line tools, etc (which was difficult without admin access on public computer). I realized after the fact of writing the code that I didn't have JUnit properly set up, so I used ```scp``` to move these files from my local machine to a directory in my ieng6 account. From there, I used the vim editor to continue editing the files, as well as using the bash scripts to run the tests. I was able to find a practical use of the remote computer just from my own experience of completing the assignments. 





