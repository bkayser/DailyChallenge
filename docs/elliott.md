# Elliott's Daily Challenges

Congratulations!  You've been doing daily challenges for a month!  You are becoming a Unix expert!

Last week we learned more about input, output, and pipes.  You learned how to create a "pipeline" of data using
the `|` operator.


### Monday, July 13

You don't need to email me today.  Just find me when you are done and show me what you learned.

You already know how to use the `cat` command to look at the contents of a file.  Today you're going to learn a new command for looking at files.  Rather than looking at a large file all at once, it's better to "page" through the file, looking at one page at a time.  Your new command will help you with that.

1. Open up a terminal and cd to the `fun` directory.
2. Type `cat quotes.txt`.
3. Type `less quotes.txt`.
   The `less` command is similar to `cat` but with one big difference: _it only shows one page at a time_.  To see the next page, hit the space bar.
4. Keep hitting the space bar until you've gone through all the quotes.
5. Type `q` to quit.

![less](images/less.png)

The `less` command not only lets you go through text page by page, but you can go forward and backward.
1. Type `sort quotes.txt | less`
2. You can type `f` instead of the space bar to go forward.  You can type `b` to go back a page.  Use `f` and `b` to page down to the bottom of the quotes and then go back up to the top of the quotes.
3. Now type `/you`.  The `/` character means "search".  After you type `/you` you should see the word "you" highlighted on the screen.
4. Go forward and backward to see all the "yous" in the quotes.txt file.

The less command does many other things.  To see all the things you can do with `less` type in the letter `h`.  

#### Less is More

Why is the program to page through text called "less"?  It's because it's based on an older command called "more".  The "more" command also paged through text but it could only go forward and not backward, and it didn't have all the fancy commands that "less" has.  Try it!  Type "more" instead of "less".

