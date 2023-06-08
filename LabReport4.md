# CSE15L Lab Report 4

## Task
`
For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.
`

## Log into ieng6

### Key pressed:

```
ssh cs15lsp23sg@ieng6.ucsd.edu <enter>
<My password><enter>
```
Log in to my ieng6 account using ssh

### Screenshot:

<img width="691" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/40bd4754-fecd-4fe7-8d5e-bbcdab33ee0b">

## Clone your fork of the repository from your Github account

### Key pressed:

```
git clone https://github.com/ucsd-cse15l-s23/lab7<enter>
```
This line of command clones the repo to the current directory 

### Screenshot:

<img width="691" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/feb0e2c2-94cc-4049-8d15-c14912d3b6dc">

## Run the tests, demonstrating that they fail

### Key pressed:

```
cd lab7<enter>
bash test.sh<enter>
```
First use the command `cd` to change directory to `lab7`, then we can run the test on `ListExamples.java` by using `bash` with `grade.sh`, which contains the command for testing.

### Screenshot:

<img width="681" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/c7cece05-b7b5-4fc8-b375-4de2f809dba7">

## Edit the code file ListExamples.java to fix the failing test

### Key pressed:

```
vim ListExamples.java<enter>
```
This command opens up the `vim` editor for the file `ListExamples.java`

### Screenshot:

Before pressing `<enter>`:

<img width="623" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/92b4e018-09a9-4dde-8172-9753f8af49a5">

After pressing `<enter>`:

<img width="696" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/7fa7eeb1-606c-47aa-8f03-26f98976e363">       

### Key pressed:

```
/index1
nnnnnnnn
```
The command `/index1` finds all the "index1" that appears in the file and the command `n` can traverse through all of them. I find the error after the eighth time pressing `n`.

### Screenshot(after pressing `n` eight times):

<img width="703" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/82714065-17fc-406e-8b9f-faee299bf2f9">

### Key pressed:

```
e
x
i
2
<esc>
```
The command `e` jump to the end of the word, the command `x` deletes the character, the command `i` enter the insert mode, `2` inserts the number 2 at the current position, and finally the command `<esc>` exits the insert mode.

### Screenshot:

After pressing `e`:
<img width="705" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/6c56fbca-c6aa-4fb7-927a-79c8069bffe5">

After pressing `x`:
<img width="695" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/bb22e94d-8fcb-4b76-8346-4f372e2ab978">
  
After pressing `i`:
<img width="699" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/87b1c7e5-67db-4f1f-82e7-99d05a3337be">

After pressing `2`:
<img width="702" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/743a823b-22c9-4fa4-8cc9-9c8cf5560969">

After pressing `<esc>`:
<img width="698" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/6df3ad59-7dfc-4d6d-8b81-b8b47e1dffe7">
  
### Key pressed:

```
:wq<enter>
```
The command `:wq` saves the modification and quit `vim`. 
  
### Screenshot:

Before pressing `<enter>`:
<img width="701" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/3292aec0-43aa-47d0-afc8-d693711a918b">

After pressing `<enter>` (There are 2 `vim ListExamples.java` because I forgot to take a screenshot before enter vim the first time so I exit and did that part again):
<img width="702" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/c642458b-50e1-4184-963d-848f24ec692c">

## Run the tests, demonstrating that they now succeed

### Key pressed:

```
<up><up><enter>
```
This line of command goes back to the command line after the previous one, which happens to be `bash test.sh`, which will run the `test.sh` and see if the modification worked. As the output shown in the terminal, both test are now passed.

### Screenshot:

After the first `<up>`:
<img width="699" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/1ca38241-78a7-43b0-af23-fedfedfb2d08">

After the second `<up>`:
<img width="703" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/a88bf454-c38a-4515-92b6-ff617822df56">

After pressing `<enter>`:
<img width="688" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/708eee02-acca-4e44-b2a0-d424fe17ddab">

## Commit and push the resulting change to your Github account

First creates a new repo named "CSE15L-lab-report4-result" in my github account:
<img width="1424" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/2364d3fb-11f8-4690-b69e-4af6568f7c8c">

And then copy the SSH key at the site it redirects automatically after creating the repo:
<img width="1412" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/d7d2cae8-5e06-4580-ba54-d39698b8a73d">

Finally go back to the terminal and push the result to github:

### Key pressed:

```
exit<enter>
ssh-keygen<enter><enter><enter><enter>
```

### Screenshot:

Exit remote:
<img width="699" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/0718a88e-da91-48b1-bfce-2764c7d58de3">

After `ssh-keygen` and pressing `<enter>`:
<img width="696" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/f615e355-9018-4d85-a4c1-d244f8ade20c">

However, after this, I somehow are not able to log into my ieng6 account anymore:
<img width="480" alt="image" src="https://github.com/nshy-ucsd/cse15l-lab-reports/assets/122579697/001d09d1-9bdc-4125-ab96-4ec845244b20">

