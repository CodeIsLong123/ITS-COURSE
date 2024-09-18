
# Task 1 

## Thoughts 
- how do we set and unset environment variables?


## What to do 
- use printenv or env command to print out the environments variables
- printenv PWD
- env | grep PWD


### What is the difference? 

printenv PWD:
This directly prints the value of the PWD (Present Working Directory) environment variable.
Example: printenv PWD might return something like /home/user.

env | grep PWD:
This first lists all environment variables using env and then pipes the output to grep to search for the variable PWD.
This will show the entire line containing PWD, typically in the format PWD=/home/user.
Example: The output might be PWD=/home/user.-

### Set and unset environment variables 
- Use Export ot set and use unset to unset the variables 

When you use the export command to set environment variables, they are typically set in the current shell session and only affect that session and any child processes (like scripts or programs) launched from it. These variables are not persistent across different terminal sessions or after you close the current shell unless explicitly saved in configuration files.

# Task 2 


- how does a child process get its environment variables from its parent 
- When forking a proccess in UNIX it duplicates the calling process.
- The child is a dublicate of the parent, but it does not inherit all environment variables.

 
## What to do?
- Test if the a child and a parent process return the same values
- use the diff command to see if the two compiled versions are the same or not the same 'diff run run2'

**Results:**
The two binary files run and run2 differ

# Task 3
- In this task we study, how environment variables are affected when the program is run via execve()
- The function calls a system call to load a new coimmand and execute it.
- No new process is started, but overwritten by the new program loaded
- runs a new program in the inside the calling process. 
- it never returns
- What about the environment variables?? <- I think they are lost, because the environment variables only account for locally run things, so when a new program is started it has new environment variables.

 



