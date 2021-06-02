<h1 align="center"> Working with shell </h1>

### Viewing File Size 

* du -sk filename - size Kb
* du -sh filename - size Mb

### Archiving filename

#### tar (tape archive)

+ tar -cf compfile filename/s - archiving file
+ tar -tf compfile - check the content in compfile
+ tar -xf compfile - extracting the archive file
+ tar -zcf compfile filename/s - compress file with reducing size

Command for compress and extracting

|compressing|extracting|
|-----------|----------|
|bzip2 filename | bunzip2 compfile |
|gzip filename | gunzip compfile|
|xz filename| unxz compfile |

### Searching pattern

* locate filename - find the file with given filename
* find directory -name filename - find the file with given filename
* grep word filename - to find the line where given word is mentioned
* grep -i word filename - to find the line where given word is mentioned(no case sensitive)
* grep -r word directory - to search file which has given word in the content
* grep -v word filename - display all the line except given word is mentioned
* grep -w word filename - display the line where given word is mentioned (exam)
* grep -vw word filename - display all the line except given word is mentioned
* grep A"n" word filename - display the "n" no.of next lines starting from the line which has given word
* grep B"n" word filename - display the "n" no.of previous lines till the line which has given word

## IO Redirection

3 Data Streams
 
* Standard Input - commands
* Standard output - output of the commands
* Standard Error - error if command is wrong

### Redirection

* St.output > filename - moves the output value to filename
* St.output | tee  filename - moves the output value to filename
* St.output >> filename - append the output value to filename
* St.output 2> filename  - move the error output value
* St.output 2> /dev/null - doesn't want to display error message.


### vi Editor

* vi directory/filename - to create file

**Operation Modes**

* command Mode(esc)- enter "esc" to go to command mode
* Insert Mode(i)- enter "i" before insert/delete value
* Last line Mode(:) - enter ":" before save/discard file

+ yy - copy the line
+ p - paste copied line
+ dd - to delete line
+ d"n"d - to delete n no. of lines
+ u - undo
+ r -redo
+ /word - to find the word 
+ n - move next line
+ N - move previous line
+ :w - to save
+ :wq - to save and quit
+ :q! - quit without saving

### LABS

* Working with shell - 
	+ compress command - bzip2, tar
	+ redirection command - > and >> commands
	+ searching pattern - grep -i word filename , grep word filename
	
* vi editor - editing, copy , delet in vi editor


