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
```
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
3. Using google as well as the apt search command, find a "roguelike" game you can install with apt.  There are a bunch of different ones.  Pick one and install it.  Remember to put `sudo` in front of the apt install command so it will execute with the correct permissions.
4. Type `apt info MYNEWPACKAGE` where `MYNEWPACKAGE` is the apt package you just installed.  Email me the output.
5. Run your new rogue like game from the command line.  What do you think?  Give me a demo.

### Sunday, June 28

Just like every house has an address, every computer on the internet also has an address.  We call this an "IP Address."  In order for your computer to talk to another computer on the internet, you have to know its IP address.  Rather than make you memorize IP addresses the internet allows you to refer to an IP address by name.  So instead of typing `http://172.217.3.174` into a web browser, you can just type `http://google.com`.  This is because of something called DNS.

Today you're going to learn a bit about DNS.  DNS stands for Domain Name System.  It's the system that allows you to reach other computers and servers on the internet using a name instead of an IP address.  It's what allows you to tell people to connect to furrynightmare.com.

1. Login to beetgang as the user pi.
2. The server doesn't have DNS utilitites on it so we need to install that using the apt get command, so type `sudo apt install dnsutils`.
3. This installs two new commands, `nslookuop` and `dig`.  Type `nslookup furrynightmare.com`.
   * This sends a request to a DNS server asking it what the IP address of `furrynightmare.com` is.
   * In the output, you should see a line that starts with `Server:`.  This is the address of the DNS server you are using.
   * Below that it might say "Non-authoritative answer" and then list a name and address.  That is the IP address that furrynightmare.com maps to.
4. What is the IP address of furrynightmare.com?
5. Let's say you learned that it is `192.56.100.22`.  Now let's do a "reverse lookup" on that IP address.  Type the command `nslookup 192.56.100.22`.  That's going to tell us the name of the computer that has that IP address.  You'd expect it to just tell you "furrynightmare.com" but it doesn't.  Instead it tells you the name of the server on Amazon that I created that is running the reverse proxy.

So what can you do with all this?  Well for one thing, if you see a user's IP address in a log file, you should be able to look up their server.  Maybe you can find out where they are, or at least what country they are from!

Email me the output from #5.