# Welcome to Felix’s Daily Challenge

This week you are going to learn some of the most used and most basic unix commands including `man`, `ls`, `wc` and `cat`.

Remember, google is your friend!  You can find out how to do all of these things using google as well as the `man` command which you'll learn about Friday.

### Thursday June 18

1. Using the `ssh` command open a remote shell on your server.  
2. Using the ls and cd commands, list the files and directories in the linux root directory.  
3. Copy and paste them to an email and send it to me.

### Friday June 19

1. Open a remote shell on your server.  
2. Using the `man` command, open the unix manual page for the `ls` command.  Find the option to list files, one file per line.  
3. Use that command to list all the files in your current directory, one per line.  
4. Copy the contents of the window, including the ls command, and email it to me.

### Saturday June 20

1. Open a remote shell.
2. Go to the `paper/plugins` directory.
3. Use the `ls` command to list all the jar files along with their sizes in that directory.
   * Hint: use the man page to discover the option that will print the size of the file next to the file.  There may be several that will work.
   * Hint: add the `-h` option to the command to make the output easier to read.
4. Email me the name and size of the largest file.

### Sunday June 21

1. Open a remote shell.
2. Use the `cat` command to print out the contents of the file `paper/run`.
3. Copy and paste the command and it’s output into an email and send it to me.

### Monday June 22

1. Open a remote shell.
2. Use the cat command to create a new file called `fun` in your home directory that has one line with the words “Hello World”.
3. Tell me when you finished so I can go look at the file.

*Hint*: This is easy to do.  The trick is to figure out how.  Google will tell you exactly how to do it if you pick the right search terms.  Remember that this is the linux operating system, but generally people refer to these as “unix” commands because they are universal to all unix systems and it’s derivatives, including linux.

### Tuesday June 23

1. Open a remote shell.
2. cd to the `paper` directory.
3. Use the command `ls *.log` to show a list of files that end with `.log`.  The `*` character is referred to as a wildcard and will “match” anything in the file name.  Writing `*.log` tells the `ls` command to restrict it’s output to files that match `*.log`.
4. Open the unix man page for the command `wc`.  Figure out how to print out the number of lines in a file using the wc command.
5. Use the `wc` command along with the wildcard expression `*.log` to print the total number of lines in all log files in the `paper` directory.
