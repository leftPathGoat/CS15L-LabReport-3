# CSE15LabReport2

Find
=====
**Basic useage of find** 
Format: `find <path> <expression>`
This command find the file and print the path to the terminal. This could be used to search particuar file in a large folder.
Examples:
````
$ find chapter-1.txt
chapter-1.txt
````
````
$ find biomed/1468-6708-3-1.txt
biomed/1468-6708-3-1.txt
````

**Searching a file by name** 
Format: `find <path> -name <pattern>`
This command-line option allow users to search files that follow a certain name pattern.
In the following examples, the files that have the same name pattern in the given directory is printed in terminal.
Examples:
````
$ find technical/911report/ -name "*1.txt"
technical/911report/chapter-1.txt
technical/911report/chapter-11.txt
technical/911report/chapter-13.1.txt
````
````
$ find technical/911report/ -name "*2.txt"
technical/911report/chapter-12.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-2.txt
````

**Searching a file by type** 
Format: `find <path> -type <type>>`
This command-line option allow users to search files of a certain type.
In the following examples, the particular type of files is printed in terminal.
Examples:
````
$ find technical/ -type d
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
````
````
$ find technical/ -type l
````
The above command type l returns the symbolic link in the directory. The command has no return because there is no symbolic link in the directory.
**Searching and executing command on a file by name** 
Format: `find <path> -name <pattern> -exec <command> {} \;`
This command-line option allow users to search files and execute a command on the returned files.
In the following examples, the file is returned to the terminal and command executed.
Examples:
````
$ find technical/biomed/ -name "*12.txt" -exec echo {} \;
technical/biomed/1471-2091-2-12.txt
technical/biomed/1471-2105-3-12.txt
technical/biomed/1471-2121-2-12.txt
technical/biomed/1471-2121-3-12.txt
technical/biomed/1471-213X-1-12.txt
technical/biomed/1471-2148-2-12.txt
technical/biomed/1471-2156-2-12.txt
technical/biomed/1471-2172-3-12.txt
technical/biomed/1471-2180-1-12.txt
technical/biomed/1471-2199-2-12.txt
technical/biomed/1471-2199-3-12.txt
technical/biomed/1471-2202-2-12.txt
technical/biomed/1471-2202-4-12.txt
technical/biomed/1471-2334-3-12.txt
technical/biomed/1471-2350-2-12.txt
technical/biomed/1471-2350-3-12.txt
technical/biomed/1471-2407-2-12.txt
technical/biomed/1471-2431-2-12.txt
technical/biomed/1472-6750-1-12.txt
technical/biomed/1472-6793-1-12.txt
technical/biomed/1472-6882-1-12.txt
technical/biomed/1472-6963-3-12.txt
technical/biomed/1475-2867-3-12.txt
technical/biomed/1475-925X-2-12.txt
technical/biomed/1477-7525-1-12.txt
technical/biomed/ar612.txt
technical/biomed/gb-2001-2-4-research0012.txt
technical/biomed/gb-2002-3-3-research0012.txt
````
````
$ find technical/ -type d -exec echo {} \;
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
````
