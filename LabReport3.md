# Lab Report 3 - Researching Commands (Week 3)
due Wednesday, May 10 by 10pm

4 command-line options or alternate ways to the command less:

### 1. more : it is the same as the command less, but doesn't allow the user to go back up through the file, only scroll down. In the same way as less, can exit by typing "q".

<img width="1083" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/f7faa078-4dae-41e1-94df-b15d4a1c7800">

<img width="714" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/3c4009f1-aeab-4052-a900-b21d21f54a05">

### 2. cat : prints the entire file contents as strings, but doesn't allow the user to traverse through the file.

<img width="748" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/ed589dc1-5398-4016-b2b9-917124c4f898">

<img width="693" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/ab05154d-53a6-4332-bd99-e9be2d541bc3">

### 3. head : shows the first n amount of lines, defaulted to the first 10.

<img width="728" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/ce2a042b-6cdf-4e63-b406-f244d3677ff5">

<img width="699" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/573ac7bb-2891-4c93-9eee-1913ca4ea630">


### 4. tail : shows the last n amount of lines, defaulted to the last 10.

<img width="699" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/a298da1b-6baf-4641-afa7-8f6d611a9635">

<img width="728" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/76268b90-9bf6-405c-9f45-8cb38d30c905">

### Resources
Relied mostly on ChatGPT and some googling to find information on alternative methods.
**prompt:** what are four alternate ways of doing the command less in terminal
**response:** 
Here are four alternate ways to use the less command in a terminal:

more: This command is similar to less but has fewer features. It allows you to scroll through a file one page at a time by pressing the spacebar. However, unlike less, you cannot scroll back up through the file.

cat: This command simply prints the contents of a file to the terminal. Unlike less, you cannot scroll through the file, and the entire file is printed at once.

head: This command allows you to view the first few lines of a file. By default, it will show you the first 10 lines, but you can specify a different number with the -n option.

tail: This command allows you to view the last few lines of a file. By default, it will show you the last 10 lines, but you can specify a different number with the -n option.

Note that while more, cat, head, and tail are similar to less, they have different features and use cases. less is more versatile than these commands as it allows you to scroll forwards and backwards through a file, search for text, and more.

Consider the commands less, find, and grep. Choose one of them. 
Online, find 4 interesting command-line options or alternate ways to use the command you chose. 
For example, we saw the -name option for find in class. For each of those options, give 2 examples of using it 
on files and directories from ./technical. Show each example as a code block that shows the command and its output, 
and write a sentence or two about what it’s doing and why it’s useful.

**How I changed the output:**
After reading the information over, I typed out what I learned in my own wording rather than using the same terminology, and added information that I found out during lab, such as how q ends the commands more or less that allow the user to scroll through sections of text at a time.
