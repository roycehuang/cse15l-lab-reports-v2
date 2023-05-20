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

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United>

    For those heading to an airport, weather conditions could not have been better for a saf>

INSIDE THE FOUR FLIGHTS

Boarding the Flights

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portl>

    When he checked in for his flight to Boston, Atta was selected by a computerized prescre>

    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a ca>

    It would be their final conversation.

    Between 6:45 and 7:40, Atta and Omari, along with Satam al Suqami, Wail al Shehri, and W>

    In another Logan terminal, Shehhi, joined by Fayez Banihammad, Mohand al Shehri, Ahmed a>

    Their flight was scheduled to depart at 8:00.
./technical/911report/chapter-1.txt
```
_example 2:_

input:
```
less -S ./technical/911report/chapter-2.txt
```
output:
```

    
        
            THE FOUNDATION OF THE NEW TERRORISM
            A DECLARATION OF WAR
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egy>
                physician, Ayman al Zawahiri, arranged from their Afghan headquarters for an>
                newspaper in London to publish what they termed a fatwa issued in the name o>
                "World Islamic Front." A fatwa is normally an interpretation of Islamic law >
                respected Islamic authority, but neither Bin Ladin, Zawahiri, nor the three >
                who signed this statement were scholars of Islamic law. Claiming that Americ>
                declared war against God and his messenger, they called for the murder of any
                American, anywhere on earth, as the "individual duty for every Muslim who ca>
                in any country in which it is possible to do it."
            
            Three months later, when interviewed in Afghanistan by ABC-TV, Bin Ladin enlarge>
                these themes.
            
            He claimed it was more important for Muslims to kill Americans than to kill other
                infidels." It is far better for anyone to kill a single American soldier tha>
                squander his efforts on other activities," he said. Asked whether he approve>
                terrorism and of attacks on civilians, he replied:"We believe that the worst>
                in the world today and the worst terrorists are the Americans. Nothing could>
                you except perhaps retaliation in kind. We do not have to differentiate betw>
                military or civilian. As far as we are concerned, they are all targets." Not>
                Islamic names often do not follow the Western practice of the consistent use>
```
The -S command line option truncates the lines to the edge of the terminal viewer. This is useful in cases when the user doesn't need to know the entire line and can recognize it based on the beginning of it. This function makes viewing larger files with long lines of text easier.

### 4. ```less -q```
_example 1:_

input:
```
less -q ./technical/911report/
```
output:
```
./technical/911report/ is a directory
```

_example 2:_

input:
```
less -q ./technical/911report/chapter-1.txt
```
output:
```

        
                
"WE HAVE SOME PLANES"

    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.

    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.

INSIDE THE FOUR FLIGHTS

Boarding the Flights

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.

    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to iden
./technical/911report/chapter-1.txt
```
The command line option -q quiets the error messages, such as when the user attempts to open a directory. This could be useful so that the user knows they attempted to open a directory specifically without throwing an error message.
### Resources
Relied mostly on ChatGPT and some googling to find information on alternative methods.

https://phoenixnap.com/kb/less-command-in-linux 

**prompt:** command line options for less

**response:** 

The less command is a pager utility in Unix and Linux systems that allows you to view text files interactively. Here are some common command line options for less:

-F: Automatically exit less if the entire file can be displayed on one screen.

-N: Display line numbers on the left side of the screen.

-S: Truncate long lines instead of wrapping them.

-i: Ignore case when searching.

-r: Display raw control characters. Useful for viewing files with escape sequences.

-X: Do not clear the screen before displaying file contents.

-M: Show more detailed prompt information, including percentage and line numbers.

-P <string>: Specify a custom prompt string to be displayed at the bottom of the screen.

-e: Quit less immediately if the input file is empty.

-h: Display a short help message with command line options.

-q: Run less in quiet mode, suppressing error messages.

These are just a few examples of the command line options available for less. You can combine multiple options together as needed. For more detailed information on less and its command line options, you can refer to the less manual or help documentation:

Copy code
man less
This will display the manual page for less and provide comprehensive documentation on its usage, options, and navigation commands.

**How I changed the output:**
After reading the information over, I typed out what I learned from my own understanding rather than using the same exact terminology.
