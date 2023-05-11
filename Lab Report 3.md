# Researching Commands
*By: Madeleine Jimenez*

In this lab report I will be researching four different command-line options for grep which includes:
`grep -i`, `grep -n`, `grep -b`, and `grep -v`
With these different command-line options I will also provide two examples for each while explaining their output and function. 

Thank you for taking the time to read my lab report!

## 1st interesting command-line option

*The first interesting command-line option that I chose was `grep -i`. 
In the following examples I will show and explain what `grep -i` does when used on a file.*

**1st Example**

Command: 
```
grep -i golden technical/911report/*.txt
```

Output:
```
technical/911report/chapter-2.txt:  Prophet Mohammed as a golden age. Its memory is strongest among the Arabs. What
technical/911report/chapter-2.txt:  The extreme Islamist version of history blames the decline from Islam's golden age on
technical/911report/chapter-2.txt:  financial support network that came to be known as the "Golden Chain," put together
technical/911report/chapter-2.txt:  Saudi and other financiers associated with the Golden Chain. Through his
```
* In this example I used `grep -i` to find the word `golden` in all the text files within the 911reports. 
* When doing this command I am able to check for the word regardless if it starts with a lower case or upper case letter.
* As you can see in the output of the example the first two outputs contain `golden` with a lower case `g` and the 
last two outputs contain `Golden` with a upper case `G`.

Note: I will use this example for other command-line options to show how only with `grep -i` it shows both lower and upper case! :)

**2nd Example**

Command:
```
grep -i CHEESE technical/*/*.txt
```

Output:
```
technical/biomed/1471-2180-3-15.txt:  cheeses prepared from unpasteurized milk. Children in these
technical/biomed/1471-2210-1-10.txt:  food (powdered milk, cheese, egg products) during storage [
technical/plos/journal.pbio.0020146.txt:   procedures, such as those for producing cheeses and wines, all of which produced foodstuffs
technical/plos/journal.pbio.0020306.txt:   division. ‘The shell is rather like a Camembert cheese box or a petri dish’, explains
```
* In this example I used `grep -i` to find the word `CHEESE` in all uppercase within all text files within technical.
* When using this command it did not matter that I input cheese in all upper case, it was still able to find cheese in the text files.
* This command is very useful as you do not have to only input an upper or lower case word when inputing your desired word as it will find both. 
* If I did not use `-i` then I would have not recieved any output as none of the text files have an the word `CHEESE` in all upper case.

## 2nd interesting command-line option

*The second interesting command-line option that I chose was `grep -n`. 
In the following examples I will show and explain what `grep -n` does when used on a file.*

**1st Example**

Command:
```
grep -n golden technical/911report/*.txt
```

Output:
```
technical/911report/chapter-2.txt:97:  Prophet Mohammed as a golden age. Its memory is strongest among the Arabs. What
technical/911report/chapter-2.txt:122:  The extreme Islamist version of history blames the decline from Islam's golden age on
```
* In this example I used `grep -n` to find the word `golden` within all the text files in the 911reports.
* This command provides the line number where the sentence with the word can be found.
* This command is useful if you are trying to find a word and the line where it is.
Note: As mentioned previously I reused `golden` you can see in this example that the other two output 
lines with a upper case `G` did not appear as I did not use `-i`.

**2nd Example**

Command:
```
grep -n cheese technical/*/*.txt
```

Output:
```
technical/biomed/1471-2180-3-15.txt:17:  cheeses prepared from unpasteurized milk. Children in these
technical/biomed/1471-2210-1-10.txt:312:  food (powdered milk, cheese, egg products) during storage [
technical/plos/journal.pbio.0020146.txt:140:  procedures, such as those for producing cheeses and wines, all of which produced foodstuffs
technical/plos/journal.pbio.0020306.txt:30:  division. ‘The shell is rather like a Camembert cheese box or a petri dish’, explains
```
* In this example I used `grep -n` to find the word `cheese` within all the text files in technical.
* As explained previously this command provides the line number where the sentence with the word can be found
* You can see from the output that cheese can be found on lines 17, 312, 140, and 30.

## 3rd interesting command-line option

*The third interesting command-line option that I chose was `grep -b`. 
In the following examples I will show and explain what `grep -b` does when used on a file.*

**1st Example**

Command:
```
grep -b golden technical/911report/*.txt
```

Output:
```
technical/911report/chapter-2.txt:8362:  Prophet Mohammed as a golden age. Its memory is strongest among the Arabs. What
technical/911report/chapter-2.txt:10331:  The extreme Islamist version of history blames the decline from Islam's golden age on
```
* In this example I used `grep -b` to find the word `golden` within all the text files in the 911reports.
* This command includes the byte offset of each matching line in its output, showing the position within the file where the sentence with the word starts.
* This is command is similar to `grep -n` as it provides a way to find the position of a pattern or word in a file.

**2nd Example**

Command:
```
grep -b cheese technical/*/*.txt
```

Output:
```
technical/biomed/1471-2180-3-15.txt:679:  cheeses prepared from unpasteurized milk. Children in these
technical/biomed/1471-2210-1-10.txt:17548:  food (powdered milk, cheese, egg products) during storage [
technical/plos/journal.pbio.0020146.txt:10818:  procedures, such as those for producing cheeses and wines, all of which produced foodstuffs
technical/plos/journal.pbio.0020306.txt:1880:  division. ‘The shell is rather like a Camembert cheese box or a petri dish’, explains
```
* In this example I used `grep -b` to find the word `cheese` within all the text files in technical.
* As explained in the prior example `grep -b` includes the byte offset of each matching line in its output,
thus it is helpful in finding the exact position or location of a pattern/word in a file.

## 4th interesting command-line option

*The fourth interesting command-line option that I chose was `grep -v`. 
In the following examples I will show and explain what `grep -v` does when used on a file.*

**1st Example**

Command:
```
grep -v o technical/government/Media/A_Perk_of_Age.txt
```

Output:
```
By Kelly Greene
issues.
assistance.
```
* In this example I used `grep -v` to find lines that did not contain the letter `o` within the text file A_Perk_of_Age.
* This command is an invert match where it instead finds the lines within a file that do **not** contain the word/letter you input. 
* This is useful for when you may be looking for a specific file that does not contain a certain word.
* In this example these were the only lines that did not have a word conatining the letter `o`

**2nd Example**

Command:
```
grep -v i technical/government/Media/A_Perk_of_Age.txt
```

Output:
```
By Kelly Greene
reach all 50 by the end of March. You have to pay the group's dues
```
* In this example I used `grep -v` to find lines that did not contain the letter `i` within the text file A_Perk_of_Age.
* As explained above, this command is an invert match where it instead finds the lines within a file that do **not** contain the word/letter you input. 
* This is useful for when you may be looking for a specific file that does not contain a certain word.
* In this example these were the only lines that did not have a word conatining the letter `i`

## Citations
* [Wikibooks](https://en.wikibooks.org/wiki/Grep)
* I also used `man grep` to see all the command-line options and explanations.

## All Done

Thank you again for reading my lab report! I hope you have a good rest of your day! :)
