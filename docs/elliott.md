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

### Tuesday, July 7

Today we'll play around with the head and tail commands some more.

**Read the instructions carefully!**

You only need to send me the answer to the last question, if you can figure it out.

1. Open a terminal on the Chromebook
2. Change directory to the `fun` directory where the `quotes.txt` file is.
3. Type the following commands:
    ```
    head -50 quotes.txt
    head -5 quotes.txt
    head -1 quotes.txt
    tail -5 quotes.txt
    tail -1 quotes.txt
    ```
    Are you able to figure out what the `-n` command line option does for the `head` and `tail` commands?
4. Type `head -10 quotes.txt > quotes.top10.txt`.  Use `cat` to see what's in the `quotes.top10.txt`.
5. Type `tail -1 quotes.top10.txt`.  This is the 10th line in the quotes.txt file.

The 5th to the last line in quotes.txt is "Wisdom begins in wonder."  You can see that if you use the `tail` command.
Can you figure out how to combine the tail and head commands like you did in steps 4 and 5 so that you print out only the line "Wisdom begins in wonder"?

Email me the two commands you used, or find me for help.
