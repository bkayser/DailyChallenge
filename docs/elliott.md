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

### Wednesday, July 8

Many unix commands operate on "input" and generate "output".  The "input" to a command can be from three places:
1. A file, like when you type `sort quotes.txt`
2. Typing: the command processes information you type in.
3. Another program, like when you use the `|` operator between two commands.  It takes the output of the first command and feeds it to the next command as input.

Today we're going to do some more work with type (2) above: typing input to commands.

The most important thing to know is how to tell the command "there is no more input".  You know that when you type `<Ctrl-C>` that it "interrupts" the command.  To tell the command "there is no more input" instead, __you type the Ctrl-D character__.  So for each of the commands you try below, make sure you type `<Ctrl-D>` when you are finished with the input.

1. Type `cat`.  This program just takes each line that you type and prints it out.  So after you enter a line, it will "echo" it back just as you typed it in.  Try it!  Type in your name.  It will print out a copy of your name.
2. When you finish typing in the input, type the `<Ctrl-D>` character.

Now let's try this for some other commands.  Make sure you type a few lines of text, then type `<Ctrl-D>`.  For some commands, like `cat` it will print the output right after you type a line.  For others, like `sort` and `wc`, it will wait until you type all of the input, then print out all of the output.

Type the following commands, then enter at least four lines of input, then hit `<Ctrl-D>`.  Copy and paste each one into an email message.

```bash
grep e
head -2
wc
sort
```

Now we're going to try two new unix commands: `rev` and `rotix`.  Let's see if you can guess what these programs do!  It shoud be easy to guess what the `rev` command does, but what does the `rotix` command do?  It looks like gibberish, but it's actually a special encoding!

```bash
rev
rotix
```

If you are still trying to figure out what `rotix` does, try using it to "decode" this hint. Enter the following text into the rotix command (type `rotix` and then enter this text, then type `<Ctrl-D>`):
```
Ryyvbgg xabjf gung ebgvk fuvsgf rnpu yrggre guvegrra cynprf.
```

Send me your answers or come find me for help!

### Thursday, July 9

Today I'm going to show you how to create a file using the output of multiple commands.

You are also going to learn a new unix command, `fortune`.  Aren't you fortunate?

![fortune](https://www.horoscope.com/images-US/games/game-fortune-cookie-1.png)

We'll use two new operators: `>` and `>>`.

The `>` operator is what you put after a unix command to tell it to "send the output to a file".

1. Open a terminal on your Chromebook
2. `cd` to the `fun` directory.
3. Type `fortune`.  What did it tell you?  Do it again, a couple of times.
4. Now type `fortune > fortunes.txt`.  It didn't print anything!  What did it do?
5. Type `cat fortunes.txt`.  This shows you the output from the `fortune` command you typed in step 4!
6. Repeat steps 4 and 5 a couple of times.  Notice that there is a new fortune each time.
7. Now let's see if we can make a file with several fortunes in it.  Type the following commands.  Note these are only different because they use the `>>` instead of the `>` operator.  After each one, look at the `fortunes.txt` file (using the `cat` command).
    ```bash
    fortune >> fortunes.txt
    fortune >> fortunes.txt
    fortune >> fortunes.txt
    ```
8. Now can you tell me the difference between `>>` and `>`?
9. Now try these commands for fun.
    ```bash
    date > diary.txt
    fortune >> diary.txt
    pwd >> diary.txt
    echo "I am Iron Elliott" >> diary.txt
    ```
10. Use cat to print out the contents of the `diary.txt` file and then email it to me.


### Friday, July 11

In unix, we call the different symbols `<`, `>`, `>>` and `|` "operators".

Today we're going to work more with the `|` operator.  This is called "the pipe operator".  The pipe operator takes output from one command and sends it directly into another command as input.  So data goes through the "pipe" that connects two commands, or programs.

![pipe](images/pipe.png)

You don't need to send me your answers for 1-7.  Just make sure you try each step.

1. Open a terminal window on your Chromebook.
2. There is a file `raven.txt` in your current (home) directory.  Move this into the `fun` directory by typing the command `mv raven.txt fun`.  That means _move the raven.txt file into the fun directory_.
3. `cd` to the `fun` directory then type `ls`.  You should see the raven.txt file and the quotes.txt file.
4. Type `tail -2 raven.txt`.  You should see the last two lines of the poem "The Raven."
5. Type `tail -2 raven.txt | rev`.  Notice what's different?
6. Type `cat quotes.txt | sort | tail -20 | head -1`
7. Type `cat raven.txt | grep Lenore`.

These two commands do the same thing.  Try it by typing them both in:
* `grep Lenore raven.txt`
* `cat raven.txt | grep Lenore`

Now that you know what the pipe operator does try the following challenges and send me the output in an email.  You can only use the `|` operator, not the `>` or `>>` operators.
1. Print out each line of raven.txt that has the word "Nevermore" and reverse the letters.
2. Print out a fortune encoded using the `radix` rot13 encoding.  Hint: you already learned the command that prints out a fortune.
3. Sort the file `quotes.txt`, select lines with the word "your", reverse them, then encode them with `radix`.
4. What percent of lines in "The Raven" have the word "Lenore" in them?  Show the commands you used.

Bonus Challenge: Use as many commands as you can in a single line using the `|` operator.  You are not allowed to use a command more than once, and you have to print something out.  Don't show me the command, just the output.  See if I can guess what commands you used!

### Saturday, July 12


The `echo` command is used to print out text.  You tell echo what to print and it prints it.  

1. Open a terminal window on your Chromebook.
2. `cd` to the `fun` directory.
3. Type `echo "My name is Elliott"`
4. Type `echo Today is Saturday`
5. Type these lines.  Notice that it doesn't print anything out until you type the last line.
```
echo "Today is Saturday.
The weather is warm.
I will play basketball."
```
6. Now type `echo "Today is Saturday" > diary.txt` Why didn't it print anything?
7. Type `echo "Today is Saturday > diary.txt"`  What happened?  Why is this different?
8. Type the following lines:
```
echo "I read 30 minutes." >> diary.txt
echo "I played basketball." >> diary.txt
echo "I watched Sponge Bob on TV." >> diary.txt
```
9. Type `cat diary.txt` and send me the output.

