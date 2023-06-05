# CSE15L Lab Report 5

## Task
Design a debugging scenario in the spirit and style of the ones above. Write your report as a conversation on EdStem.

### Environment
I am using visual studio code and its terminal on the remote ieng6 account.

### Symptom
<img width="512" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/551e2264-dc9a-4eaf-9966-6adb83b057e9">
I see that there is an NoClassFoundDefError, which should cause at least one test to fail. Yet I still see the program printing:
```
All tests passed
4/4
```
### Failure-inducing input and content
I am at my project directory named list-examples-grader, running `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3` 

### Response from TA
Did you check your junit-output.txt? What will `FAILURES` at your line 29 in the grade.sh file be? And according to `FAILURES`, what would the ouput of your if-else statement starting line 31 in your grade.sh be? Also, what could be causing the ClassNoDefError? Could it be caused by the incorrect path and/or directory?

### Reply by student
I checked my junit-output.txt file, seeing that it is basically empty likely because of the crash which temrinated the program.
<img width="703" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/df3e091d-5840-4904-985a-2b29d4c643e6">
This caused the my if-else to always output "All tests passed 4/4" because junit-output.txt will not include the string "FAILURES!!!" if the program is terminated. 

### Setups
1. file and directory needed
  1. grade.sh
  2. grading-area
    1. junit-output.txt
2. Contents before fixiing (can be found by cloning https://github.com/ucsd-cse15l-f22/list-examples-grader/blob/main/grade.sh)
  1. grade.sh 
<img width="701" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/9aa371bb-12af-465c-b16c-8e4253886422">
<img width="701" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/27ebe69d-5252-4afb-b6ab-c737aa7f219e">
  2. junit-output.txt
  <img width="701" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/c7f5b473-42b0-49ae-b24a-1033754022a9">
  
3. Command line to trigger the bug 
  * bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3

4. How to fix the bug 

The error to my junit test is fixed by creating a new directory, store the junit-output.txt file in the directory, and changing the CPATH in grade.sh due to the directory change. 
<img width="1024" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/2f193719-cd76-458a-a16f-2a9a61cec2e3">

## Reflection
In the second half of the quarter, I learned about the inportance of asking the TA during lab sessions. As the lab is getting harder and harder, asking TA does help a lot when my partner and I were stuck on a problem. I also learned about the importance of setting up a good junit test because it does help finding bugs and debugging the program. 
