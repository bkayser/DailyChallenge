# Elliot's Daily Challenges


### Thursday, June 18

1. On your computer, open a terminal window and type `ls`.
2. Send me the results.

What does ls show you?

### Friday, June 18

1. Open a terminal window.
2. Type `ls`.
3. Type `ls -l`.
4. Notice how those commands show different things.  Can you tell what the difference is?
5. Type `ls -lh`.
6. Copy the output of `ls -lh` and paste it into an email message to me.
7. Based on the output of `ls -lh` find the biggest file in your directory and tell me how big it is.  You can tell me in units of `kb` or `mb` or even `gb` if you see that.  Type your answer into the email.

### Saturday, June 19

1. Open a terminal window.  Type `ls` to see the files in the current working directory.
2. Type `pwd`.  This is a command that means "Print the working directory"
3. Type `cd Documents`.  The `cd` command means "Change the working directory".
4. Type `ls` to look at the files in the current working directory.  What do you see?
4. Now type `pwd`.  How is this different than what `pwd` printed before?
5. Now type `cd ..` and then type `pwd`.  What is the current working directory now?
6. Again, type `cd ..` and then type `pwd`.  What is the current working directory now?
7. One more time, type `cd ..` and then type `pwd`

Now create a new email message to bill@kayser.org and answer the following two questions:

1. What is a directory?
2. What happens when you type `cd ..`?

### Sunday, June 20, Father's Day

1. Open a terminal window.
2. Type `no`.  What happens?  There is no unix command called `no`.  That would be silly.  So the shell prints out an error.
3. Type `yes`.  What happens?  Uh-oh!
4. Type `<ctrl-c>`.  That means, hold down the "control" key and press the letter "C".  What did that do?

'<ctrl-c>' is a command that almost always "interrupts" a running command or program that you started in the terminal window.

Now, create a new email message to bill@kayser.org saying "Happy Fathers Day".  For a bonus, copy and paste a funny image into the email.  Get Felix to help if he's in the mood.

### Monday, June 21

Review `ls` and `pwd` commands.

### Tuesday, June 22

1. Open a terminal window.
2. Using the command `mkdir` create a new directory in your current working directory.  Call this directory "fun".
3. Go into the new "fun" directory.  Hint: Use the command that you have been using to "change directory".
4. Type the following command: `ls > foo`.  Normally the `ls` command lists all the files in the directory but this time it printed nothing out!  
5. Type `ls`.  There should be a new file in the fun directory called `foo`.
6. What do you think is in the `foo` file?  Let's find out by printing the contents of `foo`.  Type the command `cat foo`.  What do you see?
7. What do you think the command `ls > foo` does?  Write your answer in an email and send it to me.

If you have any problems or don't have an answer for (7) come find me and I'll help you.

### Wednesday, June 23

Today we're going to create a file with some text in it.

Remember, when using any command like `ls`, `mkdir` or `cat` you can quickly remind yourself how these commands work and what the options are in several ways:

* Google the command with a phrase, like "how to create a directory with mkdir"
* Look at the manual for the command by typing `man` plus the name of the command, like `man mkdir`.
* Many commands have a quick "help" option you can show by adding `-h` or `--help` at the end of the command.

1. Open a terminal window.
2. "Change directory" to the `fun` directory.  If there is no `fun` directory, create one using step 2 from Tuesday. 
3. Type `nano elliott.txt`.
   * `nano` is a program called a "text editor."  It allows you to edit a document like you do in google docs, but there is no formatting.
   * You can google "nano" to find out more about how to use it and what commands there are.
4. In your new document, type "Hello World.  My name is Elliott."
5. Can you find the command to exit nano?  Make sure it saves what you typed in.
6. Use the `cat` command to print the contents of the `elliott.txt` file.
7. Copy and paste the contents of your screen into an email message and send it to me.
