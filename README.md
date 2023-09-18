# What is Bash Scripting

- Bash is a widely used shell on Linux systems.
- While it is interactively used as an interactive shell, we can also use it to run bash scripts.
- Bash scripts are files that contain Bash code which can be run like a regular program.
- Bash scripts allow us to incorporate logic, text formatting and other helpful features into files that we can share with others or which we can use to save ourselves from typing out commands manually whenever we need to run them.
- Bash is a shell, a program that lets us interact with the computer, giving us access to installed programs, hardware resources and files stored in the system.
- An interactive command-line shell that also allows commands to be combined into script files, which can be run like programs.
- Combining commands into scripts saves time and reduces errors.
- Bash is best for writing small to medium-sized scripts that will run on Linux systems.
- If your workflow can be run as commands in a Bash terminal, consider making a script.

## How to Create a Bash Script

To create a bash script, you need a text editor. One of the most commonly used editors is `nano`.

To create a shell script, you can use the command:
```
$ nano myscript.sh
```

The `sh` extension indicates that it is a shell file.

You can now edit the shell file with any commands. For example, we can create a simple command that displays text: 'Hello World':

```
echo "Hello World"
echo "This is my first script"
```

Save the exit the shell file.

To execute the shell script, you can run the command:
```
$ bash myscript.sh
```
This asks bash to interpret the shell script, line by line.

However this method is rarely used. Instead, at the top of the shell script you can invoke a shebang:

```
#!/bin/sh
```

This is a special expression that shows who is the interpreter of this script which in this case is `sh (shell)`.

You can now execute the shell script in a much more simpler manner by running the command:

```
$ ./myscript.sh
```

However, running this command will output a permission error. To solve this you can inspect user permissions by running:

```
$ ls -l myscript.sh
```

To enable execute permissions, run the command:
```
sudo chmod u+x myscript.sh
```

You can now successfully execute the shell script by running the execute command:
```
$ ls -l myscript.sh
```

This successfully executes the shell script and displays the output as shown:
```
Hello World
This is my first script
```

Congratulations on running your first shell script :)