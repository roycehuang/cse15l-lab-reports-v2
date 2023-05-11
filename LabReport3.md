# Lab Report 3 - Researching Commands (Week 3)
due Wednesday, May 10 by 10pm

### 1. Command less
1. more : it is the same as the command less, but doesn't allow the user to go back up through the file, only scroll down.
2. cat : prints the entire file contents as strings, but doesn't allow the user to traverse through the file.
3. head : shows the first n amount of lines, defaulted to the first 10.
4. tail : shows the last n amount of lines, defaulted to the last 10.

### Resources
Relied mostly on ChatGPT and some googling to find information on alternative methods.
prompt: what are four alternate ways of doing the command less in terminal
response: Here are four alternate ways to use the less command in a terminal:

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


Along with each option/mode you show, cite your source for how you found out about it as a URL or a description of where you found it.

To find information about the commands, a simple Web search like “find command-line options” will probably give decent results. 
There is also a built-in command on many systems called man (short for “manual”) that displays information about commands; you can use man grep, 
for example, to see a long listing of information about how grep works. Also consider asking ChatGPT!
