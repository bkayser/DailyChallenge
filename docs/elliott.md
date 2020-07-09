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
