# Elliott's Daily Challenges

Last week we covered some basics of web sites and web pages.  This week we will circle back around to command line utilities.

Remember to read instructions carefully!  Come get me if you have problems.

### Monday, July 6

Email me your responses for question 7 only.

1. Open a terminal on your Chromebook.
2. Change directory to the `fun` directory.
3. Open the web page [https://raw.githubusercontent.com/OptimusCrime/motd/master/quotes.txt](https://raw.githubusercontent.com/OptimusCrime/motd/master/quotes.txt).
4. Now you are going to use a special command called `wget` to get a copy of that web page into a local file in the fun directory.  Type the following command:
```bash
wget https://raw.githubusercontent.com/OptimusCrime/motd/master/quotes.txt
```
5. This creates a file in your `fun` directory called quotes.txt.  What do you think is in that file?  Type `cat quotes.txt`
6. How many lines of text are in `quotes.txt`?  Use the `wc` (word count) commnd to find out.  Remember to use `man wc` if you need to learn how to use the `wc` command.
7. Type the following commands which process the quotes.txt file.  For each command, look at the output and then tell me what the command does.
    1. `cat quotes.txt`
    2. `sort quotes.txt`
    3. `head quotes.txt`
    4. `tail quotes.txt`




