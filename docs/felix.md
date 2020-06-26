# Welcome to Felix’s Daily Challenge

Last week you learned some basic unix commands including `man`, `ls`, `wc` and `cat`.

Remember, google is your friend!  You can find out how to do all of these things using google as well as the `man` command.

### Thursday, June 25

1. Click on [this link](https://raw.githubusercontent.com/forumone/The-Raven/master/raven.txt).  Look familiar?  
2. Using the `ssh` command open a remote shell on your server under the user "pi" (not "minecraft").  You can do this from your laptop or Elliott's laptop.  By "your server" I mean the Raspberry PI server named `beetgang`.
3. Change directory to the "Documents" directory.
4. Type the command: `curl https://raw.githubusercontent.com/forumone/The-Raven/master/raven.txt`
5. What did that do?  Look at the output of the command, and look at the files in the directory.
6. Use the `cat` command to print the contents of the file `raven.txt`.
7. Use the `grep` command to print the contents of the file `raven.txt` that contain the word "nevermore".  Use the man page or google to figure out how to do this.
8. Use the same command in 7 but add a command line option (begins with the `-` character) so it prints lines that contain nevermore "case-insensitive".  This means it will print lines matching "nevermore" regardless of whether "nevermore" is capitalized or not.  Again, use google or the man page to figure out which option to use.

Now show me the results or email them to me.

### Friday, June 26

1. Open a remote shell to pi@192.
2. Complete yesterday's challenge.  Send me the results.

For today, you're going to customize ssh to make it simpler to use.

1. On you laptop find the `.ssh` directory.  This is where we created the public key a few days ago.  It should be in your home directory.
2. If there is not already a file in that directory called `config` we're going to create one.
3. Use nano to edit or create the `config` file.
4. Add the following lines to the config file:
'''
Host 192.168.0.2
 User pi
Host beetgang
 User minecraft
```
5. Now open up a COMMAND prompt and type `ssh beetgang`.
   * Did it prompt you for a password?
   * What account are you logged in as?
6. Now type `exit` to logout of beetgang.  Log back in again by typing `ssh 192.168.0.1`
   * Did it prompt you for a password?
   * What account are you logged in as?

Be sure and send me the output from yesterdays challenge, then come tell me what happened in the last two steps above.

### Saturday, June 27

Today you're going to learn about the linux "apt" package manager.  A package manager is a system for installing software on a particular platform.  On the mac you've got the App Store but you've also got something called "brew" for installing linux utilities.  Different versions of linux have different package managers.  RPM is another package manager.  On Debian, you use "apt".

1. Open a remote shell to pi@beetgang.
2. Type `apt --help`.  This will list the commands.
3. Using google as well as the apt search command, find a "roguelike" game you can install with apt.  There are a bunch of different ones.  Pick one and install it.
4. Type `apt info MYNEWPACKAGE` where `MYNEWPACKAGE` is the apt package you just installed.  Email me the output.
4. Run your new rogue like game from the command line.  What do you think?  Give me a demo.

