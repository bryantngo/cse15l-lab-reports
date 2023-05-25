# Lab Report 3
## The grep command 
The grep command is used to search and filter text based on a given patten or expression. 

## -A num 
This command allows us to display the number of lines of text after the corresponding match. This can be useful in finding context while searching for a specific keyword.

```

$ grep -A 2 prescreening technical/911report/chapter-1.txt

    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirmed that he had boarded the aircraft. This did not hinder Atta's plans.

    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
    
```
This searches for the word "prescreening" finding one instance in chapter 1 of the 911 report, thus reporting the line including the key word and the line immedietely following. If instead I wrote "-A 3", this would report the line including the key word and the two lines immedietely following.

I found this command asking ChatGPT for interesting grep command line options.

## -C num
This command allows us to display the number of lines of text before and after the corresponding match.

```
$ grep -C 2 prescreening technical/911report/chapter-1.txt

    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.

    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirmed that he had boarded the aircraft. This did not hinder Atta's plans.

    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.

```
This reports the line including the key word and the line immedietely preceding and succeeding.

I found this command asking ChatGPT for interesting grep command line options.

## -v 
We can also reverse the search to include lines not including the key word. This may be useful in narrowing down specific lines that may include useful information you are certain is not relevant to the key word.

```
$ grep -v "the" technical/911report/preface.txt

    
        
            PREFACE
                Democrats chosen by elected leaders from our nation's capital at a time of great
                avoid such tragedy again?
                27, 2002).
            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
                current and previous administrations who had responsibility for topics covered in
                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
                public testimony from 160 witnesses.
                learned.
            We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The
                political grievances, but its hostility toward us and our values is limitless. Its
                and equal rights for women. It makes no distinction between military and civilian
                targets. Collateral damage is not in its lexicon.
                and national security did not understand how grave this threat could be, and did not
                fault lines within our government-between foreign and domestic intelligence, and
                sharing information across a large and unwieldy government that had been built in a
                different era to confront different dangers.
                positive-an America that is safer, stronger, and wiser. That September day, we came
                accountability.
            As we complete our final report, we want to begin by thanking our fellow
                Commissioners, whose dedication to this task has been profound. We have reasoned
                built. They have given good advice, and faithfully carried out our guidance. They
                have searched records and produced a multitude of documents for us. We thank
                This final report is only a summary of what we have done, citing only a fraction of
                issues and organizations, we are conscious of our limits. We have not interviewed
                every knowledgeable person or found every relevant piece of paper. New information
                inevitably will come to light. We present this report as a foundation for a better
            We have listened to scores of overwhelming personal tragedies and astounding acts of
                preparing to respond if it becomes necessary. We emerge from this investigation with
                this process with strong opinions about what would work. All of us have had to
                citizens to study, reflect-and act.
            Thomas H. Kean, chair
            Lee H. Hamilton, vice chair
            
```
This reports all the lines that do not include the key word "the". Note that "The" is still included. This may be useful in exluding lines that you already know are not relevent. 

```
grep -v "a" technical/government/Env_Prot_Agen/ro_clear_skies_book.txt




EXECUTIVE SUMMARY - THE CLEAR SKIES INITIATIVE
businesses.

� Cut sulfur dioxide (SO2) emissions by 73 percent, from current
� Cut emissions of nitrogen oxides (NOx) by 67 percent, from
� Cutting mercury emissions by 69 percent, -the first-ever
tons in 2018.


contributes to ground-level ozone or smog.
electricity for consumers.
reductions.


country:
reductions."
August, 2001.



BACKGROUND � THE SUCCESS OF THE CLEAN AIR ACT


POLLUTION HAS DECLINED BY 29 PERCENT WHILE OUR ECONOMY HAS GROWN
NEARLY 160 PERCENT
of the courtroom.


THE CLEAR SKIES INITIATIVE � BUILDING ON THE CLEAN AIR ACT
will reduce the risk of toxic effects from mercury exposure to
supply.


HOW THE CLEAR SKIES INITIATIVE WORKS


THE CAP AND TRADE SYSTEM IN THE CLEAR SKIES INITIATIVE

HOW DOES IT WORK?
to reduce their emissions


WHY DOES IT WORK?


WHAT ARE THE RESULTS?
Integrity 


10 9 8 7 6 5 4 3 2 1 0

1980 1985 1990 1995 1996 1997 1998 1999

WHAT THE EXPERTS SAY ABOUT THE ACID RAIN CAP AND TRADE
PROGRAM
them."
p. 2.
Resources for the Future, July 1998, Revised April 2000.
exist."
non-intrusive."



```
I found this command from [this](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/) link.



        
    















