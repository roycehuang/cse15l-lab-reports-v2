# Lab Report 3 - Researching Commands (Week 3)
due Wednesday, May 10 by 10pm

4 command-line options or alternate ways to the command ```less```:

### 1. ```less -N``` 
_example 1:_

input:
```
less -N ./technical/911report/chapter-1.txt
```
output:
```   
      1 
      2         
      3                 
      4 "WE HAVE SOME PLANES"
      5 
      6     Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied them   
      6 selves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Other   
      6 s went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end     
      6 of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early mo   
      6 rning run.
      7 
      8     For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers wer   
      8 e Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.
      9 
     10 INSIDE THE FOUR FLIGHTS
     11 
     12 Boarding the Flights
     13 
     14     Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
     15 
     16     When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted     
     16 Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in     
     16 place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirm   
     16 ed that he had boarded the aircraft. This did not hinder Atta's plans.
 ```

_example 2:_

input:
```
less -N ./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
```

output:
```
      1 
      2 
      3 
      4 
      5 Discussion of
      6 Draft Recommendations
      7 
      8 Daniel Hungerford opened the final session of the conference by
      9 outlining the group's ultimate task-to create research
     10 recommendations from conference deliberations. Before the
     11 conference, he and Daniel Pollock drafted recommendations for the
     12 steering committee to consider. During the conference, the steering
     13 committee modified those recommendations, and they were distributed
     14 to attendees for general discussion.
     15 Hungerford stated that the goal of the conference was not to
     16 achieve unanimity regarding the recommendations, but to have
     17 significant and general agreement. He indicated the process would
     18 be to discuss the recommendations one by one, identifying any gaps
     19 or omissions and offering general comments. He emphasized that the
     20 sequence of the recommendations did not imply a priority order.
     21 Because the published recommendations will include supporting text,
     22 he encouraged the group to consider any points of clarification
     23 that would be instructive. Hungerford then opened the floor for
     24 discussion.
     25 Recommendation #1 Research on screening and intervention should
     26 address the full spectrum of alcohol problems among ED
```
The -N command line option displays the line numbers at the beginning of each line. This command is useful in when viewing code, so that when edits need to be made, the user knows exactly where the change is needed. 

### 2. ```less -f```
_example 1:_

input:
```
less -f ./technical/government/Alcohol_Problems/
```
output:
```
read error  (press RETURN)
```

_example 2:_

input: 
```
less -f ./technical/911report/chapter-1.txt
```

output:
```
        
                
"WE HAVE SOME PLANES"

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.

    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.

INSIDE THE FOUR FLIGHTS

Boarding the Flights

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.

    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirmed that he had boarded the aircraft. This did not hinder Atta's plans.

    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
./technical/911report/chapter-1.txt

```

The -f command forces less to open non-regular files such as directories. This could be useful for when using a less command on everything in a main directory, it wouldn't return an error and end the code.

### 3. ```less -S```
_example 1:_

input:
```
less -S ./technical/911report/chapter-1.txt
```
output:
```
        
                
"WE HAVE SOME PLANES"

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves >

    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Moham>

INSIDE THE FOUR FLIGHTS

Boarding the Flights

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.

    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passeng>

    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was>

    It would be their final conversation.

    Between 6:45 and 7:40, Atta and Omari, along with Satam al Suqami, Wail al Shehri, and Waleed al Shehri, checked in and boarded American Airli>

    In another Logan terminal, Shehhi, joined by Fayez Banihammad, Mohand al Shehri, Ahmed al Ghamdi, and Hamza al Ghamdi, checked in for United A>

    Their flight was scheduled to depart at 8:00.
```
_example 2:_
input:

output:

### 4. tail : shows the last n amount of lines, defaulted to the last 10.

<img width="699" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/a298da1b-6baf-4641-afa7-8f6d611a9635">

<img width="728" alt="image" src="https://github.com/roycehuang/cse15l-lab-reports-v2/assets/130111798/76268b90-9bf6-405c-9f45-8cb38d30c905">

### Resources
Relied mostly on ChatGPT and some googling to find information on alternative methods.
https://phoenixnap.com/kb/less-command-in-linux 
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
