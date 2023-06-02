# Lab Report 4 (Week 7)
due Monday, May 22 by 10pm
### Step 4: Logging into ieng6 account
<img width="791" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/d42f2ed9-4690-40fd-ab58-cfc6be489b20">

keys pressed: ```ssh cs15lsp23mf@ieng6.ucsd.edu <enter>``` 
in order to ssh into the account
I didn't have to enter a password because I followed the steps from the Week 7 lab to use an SSH key for my ieng6 account.
https://ucsd-cse15l-s23.github.io/week/week7/

### Step 5: Clone your fork of the repository from your Github account
<img width="722" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/762282a2-be07-4224-ba24-d988c76c0031">

keys pressed: ```git clone git@github.com:roycehuang/lab7.git <enter>```
in order to clone the fork of the lab7 repository

### Step 6: Run the tests, demonstrating that they fail
<img width="631" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/496fbb18-6f0e-4563-8e0d-1052cb74b058">

keys pressed: ```bash test.sh <enter>```
in order to run the tests

### Step 7: Edit the code file to fix the failing test
<img width="682" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/16d6f90d-de82-41b7-9527-1f18b27d8a90">

keys pressed: ```vim ListExamples.java <enter>``` in order to make edits to the file to fix the failing test ```/index1 += <enter> <n> <n> <rightarrow> <rightarrow> <rightarrow> <rightarrow> <rightarrow> <rightarrow> <i> <backspace> <2> <escape> :wq!``` edited the file and made the change, then saved and quit vim editor. 

by using ```/index1 += ``` the / command under the normal mode searches for the string following it. In this case it searched for instances of "index1 += ", and by pressing the key "n" vim goes to the next instance of the string. Then, using right arrows to get to the location of where to edit, we enter the insert mode using "i" and delete once to delete the 1 after index and replace it with 2. Then click escape to return to the normal mode and press ```:wq!``` in order to save and quit vim editor.
### Step 8: Run the tests, demonstrating that they now succeed
<img width="337" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/f67387a3-d8cf-496a-9409-0eea986f2b50">

keys pressed: ```<up><up><enter>``` The ```bash test.sh``` command was 2 up in the search history, so I used the up arrow to access it and run it again now that changes were made to ListExamples.java

### Step 9: Commit and push the resulting change to your Github account 
<img width="770" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/721f1011-3ad3-4272-9e8d-21c0a05acbc6">

keys pressed: ```git add ListExamples.java <enter> git commit -m "edited ListExamples.java" <enter> git push origin main <enter>```
by using these commands I was able to add, commit, and push the changes to the fork I have on github.
