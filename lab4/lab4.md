# Lab Report 4: Challenge Tasks

---
## Log into ieng6
![Image](Screenshot(85).png)
Keys pressed:
```
ssh cs15lwi23awv@ieng6.ucsd.edu
<enter>
```
> Here, I am logging into the ieng6 server using the ssh command and my unique ID.

---
## Clone your fork of the repository from your Github account
![Image](Screenshot(86).png)
Keys pressed:
```
git clone 
<ctrl-v>
<enter>
```
> To clone the fork, I first copy the local ssh url from my github account. Then, I am able to use the git clone command and the ssh url to clone the repository.


## Run the tests, demonstrating that they fail
![Image](Screenshot(87).png)
Keys pressed:
```
ls
<enter>
cd lab7
<enter>
<ctrl-v>
<enter>
<ctrl-v>
L
<tab>
T
<tab>
<enter>
```
> In order to run the test file, we must first be in the correct directory. I check the contents of our current directory using the ls command, then change the current directory to lab7 using the cd command. From here, I am able to compile and run the JUnit tests using lines of code I copy pasted from the course webpage into the command line, making sure to specify the ListExamplesTests file when executing the code. I am able to autofill this file name using the tab key after the letter L to produce ListExamples, then hitting the T key and tab key to autofill the rest of the desired file name.


## Edit the code file to fix the failing test
![Image](Screenshot(88).png)
![Image](Screenshot(90).png)
![Image](Screenshot(91).png)
Keys pressed:
```
nano L
<tab>
.java
<enter>
<down> x 42
<right arrow> x 12
<backspace>
2
<ctrl-x>
y
<enter>
```
> To edit the code file, I access the command line text editor with the nano command and the name of the file. Again, I autofill the name of the code file using the tab key to autofill ListExamples from L. Once I am in the command line text editor, I use my down key to reach line 42 by pressing it that amount of times. I then go across this line using my right arrow key to edit the 12th character to a 2 instead of a 1. This will fix the failing test as it now updates the correct variable in the while loop and will not cause a runtime error. Finally, to save these changes I press my ctrl and x key to exit the file and y to confirm the changes. Hitting enter brings us out of the editor.


## Run the tests, demonstrating that they now succeed
![Image](Screenshot(92).png)
Keys pressed:
```
<up> x 4
<enter>
<up> x 4
<enter>
```
> To run the tests again, we can access our previous commands inputted in the terminal with the arrow keys. We previously compiled and ran the tests 4 commands ago, so I am able to press my up arrow key 4 times and hit enter to compile and repeat the process to run the tests as well.


## Commit and push the resulting change to your Github account
![Image](Screenshot(93).png)
Keys pressed:
```
git add L
<tab>
.java
<enter>
git commit L
<tab>
.java -m "Updated"
<enter>
git push
<enter>
```
> In our last step of the Challenge, I first use the git add command on the file that we edited to prepare the for the commit. After autofilling the file name and running the command, I use the git commit command and make the commit message to be "Updated" by using -m and specifying the message in quotes after. The last step to push the resulting change to my github account is to run the git push command. We're all done!
