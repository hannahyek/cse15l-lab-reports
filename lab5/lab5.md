# Lab Report 5

My favorite lab report that I've completed for CSE 15L is the very first report. 

I completed the task of explaining how to log into a course-specific account on ieng6 by making my first ever repository and github pages site.
While I did not pass this report on the first try, the feedback and markdown skills I learned through making the report has helped me throughout the rest of the course.
Particularly, this task was my favorite as I got to explore all the different creative options to display the information (even adding a cute cat picture at the end of my report).
The actual tasking of logging into a course-specific account is used every week since I have written the lab report and I am glad I have learned this fundamental knowledge needed to pass this course.

Now, I am knowledgable on a faster method of logging into a course-specific account. Rather than typing the password to the account every time I need to access my account, I was able to create an SSH key to skip this step on my device.

## To do so:
1. In your local terminal, run `ssh-keygen`
2. Keep hitting `<Enter>` until the program shows some text it calles the “randomart image”
3. Log into your remote course specific account on ieng6
4. Run `mkdir .ssh` in the terminal
5. Logout of your remote account
6. Copy the public SSH key you created onto your remote account
> Scroll up and find the line where it says: `Your public key has been saved in: <path to your public SSH key>` and copy the path. The public key file should end in `.pub`.

7. From your local computer, run `scp <path to your public SSH key> cs15lwi23__@ieng6.ucsd.edu:~/.ssh/authorized_keys`
8. Enter your password
9. You're all set up! Try to log onto your remote account again, you shouldn’t be prompted for a password anymore.


Thanks!

![Image](catpng.png)	
