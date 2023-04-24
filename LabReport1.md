# Lab Report 1 - Remote Access and FileSystem (Week 1)
due Monday, April 10 by 10pm

### 1. Finding the CSE15L Course Account
Using the website https://sdacs.ucsd.edu/~icc/index.php
- search for course username by putting in your username and student ID (beginning with A or U)
  ![image](https://user-images.githubusercontent.com/130111798/230518410-3819df3c-0706-4815-88f7-83216afda1d4.png)

Then click the Additional Account beginning with cs15lsp23 to where the screen will change to: 

<img width="690" alt="image" src="https://user-images.githubusercontent.com/130111798/230988953-8aa2dd7d-42c8-4bfe-8f63-f47314fe01bb.png">

and then click the Global Password Change Tool to change the password

### 2. Verify that VSCode is Installed
Use this website https://code.visualstudio.com/ if not installed
The interface should appear as:
  <img width="989" alt="image" src="https://user-images.githubusercontent.com/130111798/230989607-5aeb903c-7c29-4c4c-9169-d179b364974b.png">
  I already had the application installed so I skipped this step

### 3. Remotely Connect Using Your Course Account
If using a Windows computer, ensure that Git for Windows is installed, if not use the link https://gitforwindows.org/ to install. Mac computers can skip this step.

Then following steps from the link: https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994
- Open the terminal ```(Ctrl + Shift + ` )```
- Open the command palette ```(Ctrl + Shift + P)```
- Type "Select Default Profile"
- Select "Git Bash" from the options

 <img width="1057" alt="image" src="https://user-images.githubusercontent.com/130111798/230990499-050ad4a5-3879-407b-ad6e-c560b11ae80e.png">
- Click the + icon in the terminal window, the new terminal will now load to a Git Bash terminal

Next remotely connect with the course account we found in step 1:
- ```ssh cs15lsp23zz@ieng6.ucsd.edu ```
     - don't include the $, convention for command in terminal
     - replace the zz with your account
- If you see a message asking to verify yes/no if you want to connecting, say yes it's the first time, but if it's a system you often frequent, it could be someone else trying to control your access 
     - type "yes" and enter
- Then your screen should look similar to this:
  <img width="545" alt="image" src="https://user-images.githubusercontent.com/130111798/230992462-de641f41-8c12-4a26-a0ba-22b05a8dc928.png">

### 4. Run Commands
- ```cd ~ ``` goes into the root directory
- ```ls -a ``` lists all of the things inside the directory
- ![image](https://user-images.githubusercontent.com/130111798/233200598-5a4cb75d-ee2c-4849-9729-06c460ec38c0.png)
- ```ls -tal ``` (shown below) 
     - lists all of the files in long format sorted by the time they were edited
    <img width="485" alt="image" src="https://user-images.githubusercontent.com/130111798/230994408-c69d3c8e-875a-4a52-9a2d-1e51f11221b8.png">

- https://www.inmotionhosting.com/support/server/linux/ls-command/
     - helpful link in seeing different commands and what they mean, sourced to find what -tal does
