Download Link: https://assignmentchef.com/product/solved-csc3320-lab-5
<br>
<span class="kksr-muted">Rate this product</span>

Purpose: Learn how to write basic shell script.In Chapter 2 and 3, you have learned a list of utilities. However, each time we could only type a single command on command line in terminal. It is inconvenient sometimes when a task has to been accomplished by multiple commands. For example, if the task needs to be repeated, you may have to restart the execution of the list of commands by typing the command one by one. For this reason, the shell script file is used to store the commands interpreted by shell. It is more than a regular file containing only the command. You can even write for loop, if else and switch case statement in the shell script. The shell script file can be executed directly by providing the name of it on command line.

Write a report by answering the questions and upload the report (named as Lab5_P1_FirstNameLastName.pdf or Lab5_P1_FirstNameLastName.doc) to google classroom. Thislab assignment is related to the slides

#12 to #14 in chapter 4 Part 1:

Now it is your turn to create your first shell script file by following the steps below.

1

Step

Step

Step 1: Go to your home directory and create a new file named as simple.sh (vi simple.sh or nano simple.sh), then include following lines in your simple.sh.Question 1) : What did you see in the output of step 3?

Step 4: Execute this file by adding ./ before the its name. $ ./simple.sh

Question 2) : What did you see in the output of step 4? Step 5: Try following command to make simple.sh executable.

$chmod a+x simple.sh

Step 6: Execute this file again. $ ./simple.sh

Note: you must type ./ before the name. This is because current working directory is not in PATH. However, you can modify the value of PATH variable and add current working directory into it by referring to next part.

Question 3): Attach a screenshot of the output in step 6.Question 4): Describe the meaning of -n option in echo command.

Read the slides #13 in Chapter 4 and then answer the following two questions.

2:

Save

your

3

:

file

editor.

by

file

Execute

and exit

this

invoking

its

name.

2

Question 5): Is “Simple Script” a comment? If not, what is the meaning of it or why we use it?Question 6): Is “#!/bin/bash” a comment? If not, what is the meaning of it or why we use it in first line?

Part 2:

To discard the ./ before the script file name when executing it, we need to change the PATH variable’s value and add current working directory into it.

Step 7: Print out the value stored in PATH variable.Question 7) : How many directories you can find in the output? Note: the directories are separated by colon.

Step 8: Try command below to insert current working directory at the beginning of the string value stored in PATH variable. $PATH=.:$PATHStep 9: Execute simple.sh again by trying following command. $simple.sh

$ simple.sh

Question 8) : Can you find errors prompted in step 9 ? If not, please briefly describe why there is no need to put ./ before the file name.

Step 10: Log out the connection to the snowball server and reconnect to it. Or simply close your terminal and then reopen your terminal.

Step 11: Print out the value stored in PATH variable again.Question 9: Can you find the current working directory . in the PATH variable?

Step 11: Execute simple.sh again by trying following command. $simple.sh $ simple.sh

Question 10) : Can you find errors prompted in step 11 ? If yes, please explain why?

3

Part 3 – Optional:

This part is optional, but you will find more questions about this part in your next lab.

Step 1:Create a new file named as checkError.sh (vi checkError.sh or nano checkError.sh), then include following lines in your checkError.sh.

$#/bin/bash/* Check Error Script */ echo “Try to find out some errors!!!”

# Seach for the words which can be matched by regex [^a]*ce# And save the output to file “Result”echo “The regex [^a]*ce can match the string(s):” &gt; Result grep ‘^[^a]*ce$’ &lt;&lt; END &gt;&gt; Result lance ace brace decide piece -ENDHERE

# Check the existence of file “Result”# Send the content in “Result” to your emailbox# $1 is replaced by your campusID ls mail $1 &lt; Result

# $1 is replaced by your campusID echo “The result has been sent to ${1}@student.gsu.edu” echo “Congratulations! You have corrected all the errors!”

Or you can directly copy this file from my public directory to your current working directory by following command and then skip step 2.

$cp /home/bbello1/public/checkError.sh checkError.sh

Step 2: Save your file and exit editor.Step 3: Try following command to make checkError.sh executable. $chmod

a+x checkError.sh

Step 4: Execute this file by following command. $./checkError.sh campusIDNote: Replace campusID with your own campus ID.E.g. $./checkError.sh bbello1

4

Questions:

Can you find some errors when executing the command in step 4? If yes, please point out which lines contain errors. Think about the correction in your next lab. Before the correction, you could pre-view the slides #15 – #24 in Chapter 4.

Hints:

<ul>

 <li>Following is a sample of the output once all the errors are corrected$ ./checkError.sh bbello1 Try to find outsome errors!!! checkError.sh ResultThe result has been sent to <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="ccaeaea9a0a0a3fd8cbfb8b9a8a9a2b8e2abbfb9e2a9a8b9">[email protected]</a> Congratulations! You have corrected all the errors!</li>

 <li>You can use cat -n checkError.sh to check line numbers.</li>

 <li>You may need to use CTRL-C to terminate the execution of the command, especially for the script file with errors.</li>

</ul>