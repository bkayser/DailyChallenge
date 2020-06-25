# Elliot's Daily Challenges

So far we have learned about several commands:

* `ls` for looking at a list of files
* `pwd` for showing what directory you are in
* `cd` for changing the current directory
* `yes` for silly stuff


### Thursday, June 25

1. On your Chromebook (laptop), open a terminal window.
2. Type `ls`.  This shows all files in your current directory.
3. Type `find .`  What does this command do?  If you aren't sure, use `man find` and look at the first line to find out.  You can ignore the rest of the stuff on the man page--there's a lot!
4. Type `find . -type d`.  What does this show?  How is it different than step 3?
5. (Bonus question, optional) Type `find . -type f`.  How is this different than steps 3 or 4?

Email me your answers.

### Friday June 26

1. On your Chromebook, open a terminal window.
2. Type `cat raven.txt`.  What is it?
3. Type `grep nevermore raven.txt`.  What does the `grep` command do?  If you aren't sure, use `man grep` to get a hint.
4. The grep command has many command line options.  These are extra "parameters" that you add to the command to get it to do certain things.  Most unix commands have options.  For instance the grep command supports a `-i` option.
5. Type `grep -i nevermore raven.txt`.  What do you think the `-i` option does?
6. Do `man grep` and see if you can find the info on the `-i` option.  Was your guess about what it did correct?

Email me the answers.

### Saturday, June 27

Today you will learn about the `|` operator.

1. On the Chromebook open a terminal window.
2. Type `find .`
3. Now type `find . | grep log`.  How is the output different?
4. Type `find . | grep fun`.

The `|` character is a "pipe operator"  It takes the output from one command and feeds it into another command.
