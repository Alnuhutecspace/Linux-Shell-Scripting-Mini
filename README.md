# Linux-Shell-Scripting-Mini 

# Linux-Shell-Scripting-Mini 

Shell scripting involves writing sequences of commands in a text file that a Unix-like operating system's shell can execute. These scripts automate tasks, manage system configurations, and perform various operations that would otherwise require manual input at the command line. 

## Key aspects of shell scripting:

- Shells: Different shells exist, such as Bash (Bourne Again SHell), sh (Bourne Shell), zsh, and ksh (Korn Shell). Bash is the most common default on Linux systems.

- Shebang: The first line of a shell script, known as the "shebang" (e.g., #!/bin/bash), specifies the interpreter to be used for executing the script. 

- Commands: Scripts consist of standard shell commands (e.g., ls, cd, echo), along with control flow structures like if/else statements, loops (for, while), and variables, similar to other programming languages.

- File Extension: Shell scripts are typically saved with a .sh extension, though it is not strictly required.

- Execution: To run a script, it first needs execute permissions (e.g., chmod +x scriptname.sh), and then it can be executed by typing ./scriptname.sh in the terminal.

- Applications: Shell scripting is widely used in system administration, software installations, file manipulation, automation of repetitive tasks, and creating custom utilities. 

## What is Shell Scripting 

Imagine you are tasked with setting up new workstations and user accounts regularly at your job. Instead of manually creating each folder and user account, a simple shell script serves as your efficient digital helper. 
By automating the creation of multiple directories and user accounts with just a few lines of code. 

Shell scripting is the processing of writing and executing a series of commands in a shell to automate tasks. A shell script is essentially a scripts or program written in a shell language, such  **bash,** **sh,** **zsh,** **or** ** PowerShell**? 

A basic shell script that will create multiple linux users at once would look like this. 

## Task for Me 

1. Create a folder on an ubuntu server and name it shell-scripting. 

![Create Directory](./img/01.%20Create%20Directory.png) 

2. Using the **vim** editor create a file called **my_first_shell_script.sh**.

![File Creation](./img/02.%20File%20Creation.png) 

3. Put the shell script code into the new file. 

![Shell Script Code](./img/03.%20Shell%20Script%20Code.png)

4. Save the file. 

![Save File](./img/04.%20Save%20File.png)

5. Use **cd** command to change into the  **shell_scripting** directory. 

![Change into the Directory](./img/05.%20Change%20into%20the%20Directory.png)

6. Use 'ls -al' command to confirm that the file is indeed created. 

![Confirming the Script Created](./img/06.%20Confirm%20the%20File%20Creation.png)

The thing notice about the permissions of the newly created file is this **-rw-rw-r--** in my work which means: 

1. The owner of the file has read **(r)** and write **(w)** permissions. 

2. The members of the file's has read **(r)** and write **(w)** permissions in my server.

3. Others of the file's has read **(r)** permission.

However, no one has execute permission, hence the script can not be executed. 

To execute the script you type the command. 

![Executing Command](./img/07.%20Executing%20Command.png)

- ./ This prefix to the file indicates that the command should look like for the current directory. 

    - The **(.)** represents the current directory. 

    -and the **(/)** is the directory seperator. 

When you hit Enter, you should get a response like 

![Bash Response](./img/08.%20Bash%20Response.png) 

Notice that we now have **permission denied** error which can easily be resolved by giving the file necessary permission it requires. We also notice the mention of bash at the beginning of the error message? This indicates the message is coming from the **Bash shell** itself. **Bash is the command interpreter or shell that is been used by the terminal to execute commands. 

## Task 2 for Me 

1. Add the execute permission for the 'owner' to be able to execute the shell script. The modification shown below gives only write permission to groups and others.

![Permission for Owner](./img/09.%20Permission%20for%20Owner.png) 

2. Run the shell script. 

![Script Run](./img/10.%20Script%20Run.png)

3. Evaluate and Ensure that the 3 folders are created.

![Evaluate for Folder Creation](./img/11.%20Evaluate%20for%20Folder%20Creation.png) 

4. Evaluate and ensure that 3 users are created on the linux server. 

![Evaluate for Users Creation](./img/12.%20Evaluate%20for%20Users%20Creation.png) 

## What is a Shebang (#!/bin/bash)? 

Notice that at the beginning of the shell script, we have '#!/bin/bash' written. This is what is called **Shebang**. It's a special notation used in Unix-like operating systems like Linux, to specify the interpreter that should be used to execute the script. 

Explore the /bin folder and see the different programs in there **bash** is one them which is used as the interpreter in that script. Using another shell like **sh** the shebang would be updated to **#!/bin/sh** 

Without shebang line, the system may not know how to interpret and execute the script, there is a need to explicitly specify the interpreter when running the script. 

## Variable Declaration and Initialization: 

In programming generally, not just shell scripting, **variable** are essential for creating dynamic and flexible programs. 

Variables can store data of various types such as numbers, strings, and arrays. You can assign values to variables using **=** operator, and access their values using the variable name preceded by a **$** sign, 

![Assign Variable](./img/13.%20Assign%20Value.png) 

Now that variable is assigned, how can I used it. 

## Retrieving Value from a Variable 

One of the most straightforward methods to use or retrieve the value stored in a variable is by echoing it back to console. This is done by **echo** command in shell scripting. 

![echo Command](./img/14.%20echo%20Command.png) 

This command instructs the shell to print the value of name to your screen, which in my case, would output **Jane**

![echo Print Out](./img/15.%20Echo%20Print%20Out.png) 

echo is a command used to print a text, variables, or values.
