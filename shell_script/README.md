<h1 align="center"> Shell Scripts for Beginners </h1>

These notes have prepared based on [Shell Scripts for Beginners](https://beta.kodekloud.com/lessons/course-introduction-2/).<br /> 

### Why Shell Scripts ?
* Automate Daily Backups
* Automate Installation and Patching of software on multiple servers
* Monitor system periodically
* Raise alarms and send notifications
* Troubleshooting and Audits

### Ojectives
* Variables
* Control Logic
* Loops
* Executing shell scripts
* Shebang

# Intoduction

* Shell scripts are set of commands stored in a file 
* It will executed each line one after the other until all lines are get completed.
* If any of the commands taking long time execute, it will wait it's finished before proceeding next line of commands.

#### Variables

* Variables should be Alphanumeric or Underscore.
* Variables are Case Sensitive

### Command Line Argument

* Argument should be passed while executing shell script, 
	Eg: ``` bash print-name.sh Python ```
* Can the access the argument in script as **$position** inside the script.
	Eg: ``` echo $1 ```

### Reading Input

* The script will prompt the input from user while executing 
	Eg: ``` bash print-name.sh
			Enter Name : Python ```
* The prompting message is to be adjusted inside the script before specifying the variablle name 
	Eg: ```read -p "Enter Name:" name
			echo $name ```
			
### Arithmetic Operations

* The arithmetic operation can be done using expr commands and should use \* while multiplication
	Eg: ``` $ expr 6 + 3
			$ expr 6 - 3
			$ expr 6 / 3
			$ expr 6 \* 3 ``` 

* Also can be done double paranthesis without using expr command
	Eg: ```	A=6
			B=3
			$ (( A+B ))
			$ (( A-B ))
			$ (( A/B ))
			$ (( A*3 )) ``` 

### Conditional Logic

#### If condition

+ **If then Statement**
syntax : 
		```
		if [condition]
		then 
		statement
		fi
		```

+ **If then else statement**

Syntax : 
		```
		if [condition]
		then 
		statement 1
		else
		statement 2
		fi
		```

+ **If then elif else**

Syntax : 
		```
		if [condition 1]
		then 
		statement 1
		elif [condition2]
		then 
		statement 2
		else
		statement 3
		fi
		```

#### For Loops

#### Uses of for loop

* Execute a command or a set of commands many times
* Iterate through files
* Iterate through lines within a file
* Iterate through the output of a command

+ **for loops with values**

Syntax:
		```
		for value in value 1 value2 value3 ......valuen
		do
			statement
		done
		```
		
+ **for loops with values and values exporting from the file**

Syntax: 
		```
		for value in $( cat filename )
		do
			statement
		done
		```
		
+ **for loops with conditions**

Syntax:
		```
		for (( value intialization ; condition ; increment or decrement ))
		do
			statement
		done
		```
		
#### While Loops

#### Uses of While Loop

* Execute a command or a set of commands multiple times but you are not sure how many times.
* Execute a command or a set of commands until a specific condition occurs
* Create infinite loops


Syntax:		
		```
		While [ condition ] # If the condition is true
		do
			statement
		done
		```

### SHEBANG

If a script designed for perticular shell, the we need to mention shell type on the top of the 
script this method is known as SHEBANG

Synatx: #!/bin/shell type

### Function

#### Uses of While Loop

* Break up large script that performs many different tasks:
	+ Installing packages
	+ Adding users
	+ Configuring firewalls
	+ Perform Mathematical calculations

Syntax :
		``` function function_name() {
				statement 1
				statement 2
				statement 3
				.
				.
				.
				statement n
			}
		
		function_name() # calling function
		```

### Labs

1. variables - assigning values to varibles, using variablle in various tasks
2. Command Line Argument - passing the values through command line and that related operations
3. Read Argument - taking input as argument before executing the script and related excercises.
4. Conditional logic - if elif else syntax correction and that related task.
5. for loop - usage of various types of for loop and that related excercises
6. while loop - correction of syntax errors in while loop and related excercises.
7. function - creation, calling the functions and correction of syntax error etc.

