# Lab Report 4
## Step 4 - Log into ieng6
Keys clicked: ```ssh cs15lfa23ao@ieng6.ucsd.edu<enter>``` ssh command to remotely access ieng6 computer, enter to run command  
I could use ```<up><up><up><up>``` with a number of ups and then ```enter```, but since I have too many commands in terminal history, it is easier if I type it instead since the command is not hard to remember. 
<img width="592" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/e3ee7903-6e0c-4e8c-8249-57a749e037a6">

## Step 5 - Clone my fork of the repository
Keys clicked: ```git clone git@github.com:sssssrrt01/lab7.git<enter>``` git clone the fork of the repository that I made, enter to run command  
<img width="754" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/2c2184ac-5e3c-4d07-acdd-8433b4c7dd72">

## Step 6 - Run tests
Keys clicked:  
1. ```ls<enter>``` to check directory name
2.  ```cd lab7<enter>``` to enter lab7 directory
3.  ```ls<enter>``` to check name of test bash file
4.  ```sh test.sh<enter>``` to run test bash script
<img width="667" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/fb19e882-b037-455c-8544-bb93cda4c5fd">

## Step 7 - Edit the code s.t. test no longer fails 
Keys clicked:  
1. ```vim ListExamples.java<enter>``` open vim editor to edit ListExamples.java  
<img width="397" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/86008422-8960-4105-a487-0ab44823bcba">

2. ```:44<enter>lllllli<backspace>2<esc>``` :44 and enter to jump to line 44, move six to the right, enter insert mode, delete wrong character, press correct character, esc back to normal mode
<img width="443" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/598003ea-102b-4f7c-82c8-b8a833fb444a">

3. ```:wq<enter>``` :wq command to write and quit vim editor to return to terminal
<img width="396" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/fcfcf6bc-3d94-440a-8808-5f42fecfec38">

## Step 8 - Run tests and see that they pass now 
Keys clicked: ```sh test.sh<enter>``` run test bash script  
<img width="375" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/ab1b69e3-258d-41ca-a4b1-4311df862241">

## Step 9 - Commit and push changes to GitHub
Keys clicked:  
1. ```git add .<enter>``` adds all changed files to be committed
2. ```git commit -m "fix bug"<enter>``` commit files
3. ```git push``` push commit to origin (forked repository)  
<img width="588" alt="image" src="https://github.com/sssssrrt01/cse15l-lab-reports/assets/103394770/2d06cfd9-737f-4d6d-ba35-c75baf90a8f4">








