# Bash example tasks

## Lab 1

<details>
<summary>Expand!</summary>

1. Change your own password. Then go back to the default password.
	
	<details>
	<summary>Answer</summary>
	
	```
	passwd
	```
	
	</details>

2. Check your own ID and the groups you belong to.
	
	<details>
	<summary>Answer</summary>
		
	```
	id
	```
		
	</details>

3. Check who is currently logged into the system.
	
	<details>
	<summary>Answer</summary>
		
	```
	whoami
	```
		
	</details>
4. See the description of the directory structure.
	
	<details>
	<summary>Answer</summary>

	```
	man 7 hier
	```
		
	</details>
	
5. View the contents of your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	ls ~
	```
		
	</details>
	
6. List the contents of the primary directories on your system (e.g. /dev, /etc, /home, /usr).
	
	<details>
	<summary>Answer</summary>
		
	```
	ls /etc /dev /etc /home /usr
	```
		
	</details>	

7. Create directory cat1 in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	mkdir ~/cat1
	```
		
	</details>
		
8. In directory cat1, create a directory structure with one command: cat2/cat3/cat4.
	
	<details>
	<summary>Answer</summary>
		
	```
	mkdir -p ~/cat1/cat2/cat3/cat4
	```
		
	</details>
	
9. Delete the entire directory structure of cat3/cat4 in one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm -r ~/cat1/cat2/cat3
	```
		
	</details>
	
10. Create files with any names with extensions .txt and .c in your home directory (2-3 files with each extension)
	
	<details>
	<summary>Answer</summary>
		
	```
	touch ~/xD.txt ~/xDD.txt ~/xDDD.txt ~/y.c ~/y.cc
	```
		
	</details>
	
11. Copy all the files from the home directory with the extension .txt to the directory cat1 with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp ./*.txt ~/cat1
	```
		
	</details>

12. Copy all files from the home directory with the extension .c to the directory kat2 with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp ./*.c ~/cat1/cat2
	```
		
	</details>
	
13. Copy the entire directory structure of kat1 creating an analogous structure called cat1b.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp -r ~/cat1 ~/cat1b
	```
		
	</details>
	
14. Delete all files in cat1/cat2.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm ~/kat1/kat2/*
	```
		
	</details>

15. Delete the entire directory structure of cat1b with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm -r ~/cat1b
	```
		
	</details>
	
16. Rename any file in directory cat1.
	
	<details>
	<summary>Answer</summary>
		
	```
	mv ~/cat1/x.txt ~/cat1/xx.txt
	```
		
	</details>	

17. Move the directory cat1/cat2 to your home directory, thus creating the directory cat2b.
	
	<details>
	<summary>Answer</summary>
		
	```
	mv ~/cat1 ~/cat2b
	```
		
	</details>	

18. Using the find program, find all files that have the word mozilla in the name and are located in subdirectories of the /usr directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	find /usr -name mozilla
	```
	
	</details>	

19. Using the find program, find all the bin directories that are in the /usr directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	find /usr -type d -name bin
	```
	
	</details>	

20. Copy all regular files between 10 and 100 bytes from /usr/bin to cat1/cat2 (use the find command with the -exec parameter).
	
	<details>
	<summary>Answer</summary>
	
	```
	find /usr/bin -size +10 -size -100 -exec cp {} ~/cat1/cat2 \;
	```
	
	</details>
	
21. In your home directory, create a file named file.txt - check the access rights to it.
	
	<details>
	<summary>Answer</summary>
		
	```
	touch ~/file.txt | ls -l ~
	```
		
	</details>
	
22. For file.txt, add write access for other users.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod a+w ~/file.txt
	```
		
	</details>
	
23. For file.txt, subtract the owner's write permission.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod u-w ~/file.txt
	```
	
	</details>
	
24. For file.txt, add execute permission for all users.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod +x ~/file.txt
	```

	</details>
	
25. For file file.txt and all users, allow only file read.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod 444 ~/file.txt
	```
		
	</details>

26. For file file.txt, restore the original rights using numerical notation.
	
	<details>
	<summary>Answer</summary>
	
	```
	chmod 664 ~/file.txt
	```
	
	</details>

27. Create a link to file.txt named file2.txt in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	ln ~/file.txt ~/file2.txt
	```
	
	</details>

28. Create a symbolic link to directory file1/file2 named abc in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	ln -s ~/file1/file2 ~/abc
	```
	
	</details>

29. View the system help for all the commands presented in the class.
	
	<details>
	<summary>Answer</summary>

	```
	your_command --help
	```
		
	</details>
	
</details>
	
## Lab 2

<details>
<summary>Expand!</summary>

1. List your own processes with the ps command. Compare the results with the results of the ps x and ps ax commands.
	
	<details>
	<summary>Answer</summary>
		
	a - This option prints the running processes from all users. <br>
	x - This option prints the processes those have not been executed from the terminal.
		
	</details>

2. Log in to the system several times through virtual consoles or by opening a new window in the graphical environment. Always check the name of the terminal you are working on with the tty command.
	
	<details>
	<summary>Answer</summary>
		
	```
	tty
	/dev/pts/{console_number}
	```
		
	</details>

3. Display the process hierarchy with the pstree command.
	
	<details>
	<summary>Answer</summary>
		
	```
	pstree
	```
		
	</details>

4. View the list of processes with the top command, sorting it by CPU usage and memory usage (check the -o switch)
	
	<details>
	<summary>Answer</summary>
		
	```
	top
	top -o %MEM
	```
		
	</details>

5. Follow these steps in order:
	- Change the priority of the bash shell you are currently in to 10.
		
		<details>
		<summary>Answer</summary>
			
		```
		sudo chvt 10
		```
		or <br>
		<kbd> <br> CTRL <br> </kbd> + <kbd> <br> ALT <br> </kbd> + <kbd> <br> F10 <br> </kbd>
			
		</details>
	
	- Run the sleep command for 30 seconds. Pause them immediately with Ctrl-Z.
		
		<details>
		<summary>Answer</summary>
			
		```
		sleep 30s
		```
			
		</details>
	
	- Run another sleep command in the background, this time for 3600 seconds.
		
		<details>
		<summary>Answer</summary>
			
		```
		sleep 3600s &
		```
			
		</details>
	
	- List the active jobs in the current session with the jobs command.
		
		<details>
		<summary>Answer</summary>
			
		```
		jobs
		```
			
		</details>
	
	- Check the priority and status (running/paused) of programs running in the current session with the appropriate ps command.
	
		<details>
		<summary>Answer</summary>
			
		```
		ps a
		```
			
		</details>

	- Restore suspended sleep in the background.
	
		<details>
		<summary>Answer</summary>
			
		```
		kill -CONT {id_procesu}
		```
			
		</details>

	- Check for active jobs with the jobs command until sleep 30 ends.
	
		<details>
		<summary>Answer</summary>
			
		```
		jobs
		```
			
		</details>
	
	- End sleep 3600 by bringing it back to the foreground and closing it with Ctrl-C.
	
		<details>
		<summary>Answer</summary>
	
		```
		fg {id_from_jobs}
		```
		
		</details>

6. Run the sleep 1000 sequence in the background; touch sleep_finished. Check if sleep_finished file exists. End the sleep process with the TERM signal. Check again for existence of sleep_finished.
	
	<details>
	<summary>Answer</summary>
		
	```	
	sleep 1000 &
	touch ~/sleep_finished
	ls ~/sleep_finished
	```
		
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> C <br> </kbd>
		
	```
	ls ~/sleep_finished
	```
		
	it exist
		
	</details>

7. Launch an application with a GUI, such as the Mousepad text editor. Check its PID. Send a STOP signal to its process, check if the application responds. Send a CONT signal.
	
	<details>
	<summary>Answer</summary>
		
	```
	kill -STOP {process_PID}
	kill -CONT {process_PID}
	```
		
	</details>

8. Create a folder in your home directory called readonly. Remove write access to it. Then execute the command that will try to create the file in it, and in case of failure it will display ERROR message (command echo ERROR).
	
	<details>
	<summary>Answer</summary>
		
	```	
	mkdir ~/readonly | chmod 444 ~/readonly
	touch ~/readonly/xd.txt || echo ERROR
	```
		
	</details>

9. Go to the /proc directory and read its contents with ls -l /proc.
	
	<details>
	<summary>Answer</summary>
		
	```
	cd /proc
	ls -l /proc
	```
		
	</details>
	
10. Compare the PIDs of the processes pointed to when ps is invoked with the names of the directories in the /proc folder. Then try to go to the directory named corresponding to the PID of the ps process - does the given directory still exist?
	
	<details>
	<summary>Answer</summary>
	
	```
	ps
	```
	
	no
	
	</details>

11. Go to the subdirectory in /proc named after the PID of the bash process (you can get it by typing ps). Browse its contents and view the contents of the status. Pay attention to the information stored (e.g. Name, State,PID).
	
	<details>
	<summary>Answer</summary>
		
	```
	ps
	cat status
	```
	
	</details>

12. Check the information on which processor you are currently working on. To do this, read the content of the cpuinfo file with the cat /proc/cpuinfo command
	
	<details>
	<summary>Answer</summary>
		
	```
	cat /proc/cpuinfo
	```
	
	</details>

13. Check the RAM usage information. To do this, read the contents of the meminfo file with the command cat /proc/meminfo.
	
	<details>
	<summary>Answer</summary>
		
	```
	cat /proc/meminfo
	```
	
	</details>

14. Using Nano, increase the size of the bash history stored (HISTSIZE value in the .bashrc file in your home directory)
	
	<details>
	<summary>Answer</summary>
	
	```
	nano .bashrc
	```
	
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> W <br> </kbd> ➤  <kbd> <br> HISTSIZE <br> </kbd> <br>
	
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> X <br> </kbd> ➤  <kbd> <br> Y <br> </kbd> <br>
	
	</details>

15. Using Vim, edit any text file.

	<details>
	<summary>Answer</summary>
	
	```
	vim xD.txt
	```
	write something <br>
	<kbd> <br> SHIFT <br> </kbd> + <kbd> <br> ; <br> </kbd> <br> + 
		<kbd> <br> x <br> </kbd> + <kbd> <br> ENTER <br> </kbd>
	
	</details>

16. Run in a single console, three nano editors in the background, for three different files. Check the background processes in the current terminal with the jobs command. Learn to bring the selected process back to the foreground.
	
	<details>
	<summary>Answer</summary>
	
	```
	sudo chmod 777 /etc/nanorc
	nano /etc/nanorc
	```
		
	unocomment allow nano to suspend
		
	```
	nano x.txt
	```
		
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> Z <br> </kbd>
	
	```
	nano xD.txt
	```
		
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> Z <br> </kbd>
		
	```
	nano xDD.txt
	```
		
	<kbd> <br> CTRL <br> </kbd> + <kbd> <br> Z <br> </kbd>
	
	```
	jobs
	bg 1
	```
	
	</details>

</details>
	
## Lab 3

<details>
<summary>Expand!</summary>

1. Paginate the /etc/passwd file, assuming the page has 5 lines of text. Hint: check out more

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | more -n 5
	```
	
	</details>
	

2. Create text1 and text2 files, fill them with a few lines of text. Using the cat command, create a text3 file, which will consist of the contents of the text1 and text2 files.
	
	<details>
	<summary>Answer</summary>
	
	```
	xD > ~/xD.txt | D > ~/xDD.txt | cat ~/xD.txt ~/xDD.txt > xDDD.txt
	```
	
	</details>

3. Display the first 5 lines of all files in your home directory so that their names are not displayed. Hint: remember that you can use patterns with programs that take filenames as arguments.

	<details>
	<summary>Answer</summary>

	```
	cat * */* 2>/dev/null | head -n 5
	```
	
	</details>

4. List lines 3, 4, and 5 of the /etc/passwd file

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | sed -n '3,5p'
	```
	
	</details>

5. Display lines 7, 6 and 5 counting from the end of the /etc/passwd file (i.e. 7th, 6th, and 5th, respectively)

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | tail -n 7 | head -n 3
	```
	
	</details>

6. Display the contents of /etc/passwd on one line

	<details>
	<summary>Answer</summary>

	```
	cat /etc/passwd | tr '\n' ' '
	```
	
	</details>

7. Use the tr filter to modify the file by placing each word (separated by a space) on a separate line. Hint: to pass a space character as an argument, you must put it in quotes

	<details>
	<summary>Answer</summary>

	```
	cat < ~/xD.txt | tr ' ' '\n'
	```
	
	</details>

8. Count all the files in the /etc directory and its subdirectories

	<details>
	<summary>Answer</summary>
	
	```
	find /etc -not -type d 2>/dev/null | wc -l
	```
	
	</details>

9. Write a command that counts the sum of the first three lines of the /etc/passwd file

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | head -n 3 | wc* -c
	```
	
	</details>

10. List the files in the current directory, converting all lowercase letters to uppercase.

	<details>
	<summary>Answer</summary>
	
	```
	ls | tr a-z A-Z
	```
	
	</details>

11. List the access rights of files in the current directory, their size and name

	<details>
	<summary>Answer</summary>
	
	```
	ls -l | awk '{print $1 " " $5 " " $9}'
	```
	
	</details>

12. Display a list of files in the current directory, sorted by file size

	<details>
	<summary>Answer</summary>
	
	```
	ls -1sp | grep -v / | sort -n -r | grep -oE '[^ ]+$'
	```
	
	</details>

13. Display the contents of the /etc/passwd file sorted by UID numbers in order from largest to smallest
	
	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | sort -t ':' -n -k 3 -r
	```
	
	</details>

14. Display the contents of the /etc/passwd file sorted first by GID numbers in order from largest to smallest, then UID

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/passwd | sort -t ':' -n -k 4 -r -k 3
	```
	
	</details>

15. Enter the names of the three smallest files in the directory sorted by name

	<details>
	<summary>Answer</summary>
	
	```
	ls -1sp | grep -v / | sort -n -r | grep -oE '[^ ]+$' | sort | head -3
	```
	
	</details>

16. The /etc/services file stores a list of popular network services, along with port numbers and protocol. List (only) the names of services that use UDP.

	<details>
	<summary>Answer</summary>
	
	```
	cat /etc/services | grep 'udp' | awk '{print $1}'
	```
	
	</details>


17. View how many virtual terminals (dev/tty) numbered 50-69 are in the system.

	<details>
	<summary>Answer</summary>
	
	```
	ls /dev/tty* -1 | grep '[5-6][0-9]' | ls /dev/tty* -1 | grep '[5-6][0-9]' | wc -l
	```
	
	</details>

18. Build a pipeline that displays the cupsd process's PID in the terminal.

	<details>
	<summary>Answer</summary>
	
	```
	ps -ax | grep -e 'pts' | grep -e 'cupsd' | awk '{print $1}'
	```
	
	</details>
	
</details>

## Lab 4

<details>
<summary>Expand!</summary>

1. Define the NAME variable and assign your name to it. Display the contents of this variable. Export this variable and check if it is available in the new (child) interpreter.

	<details>
	<summary>Answer</summary>
	
	```
	NAME=John
	echo $NAME
	export $NAME
	```
	It is not available in any other interpreter
	
	</details>
	
2. Display the list of exported variables.
	
	<details>
	<summary>Answer</summary>
	
	```
	env
	```
	
	</details>

3. Change your own prompt by modifying the PS1 variable.

	<details>
	<summary>Answer</summary>
	
	```
	PS1="xd: "
	```
	
	</details>

4. Write a script that for each element (file, folder) in the current directory will display its name along with information whether it is a file or a directory.
 
	<details>
	<summary>Answer</summary>
	
	```	
	#!/bin/bash
	for FILE in ~/*
	do
	 name=$(basename $FILE)
	 if [ -f $FILE ]
	 then
	  echo "$(basename $FILE) -> file"
	 else
	  echo "$(basename $FILE) -> folder"
	 fi
	done
	```
	
	</details>

5. Write a script that for each of the files given as arguments to the call will display the name of the file, and then its contents sorted alphabetically.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	for FILE in $*
	do
	 echo  $( cat $FILE | sort )
	done
	```
	
	</details>

6. Write a script that will copy the file given as the first argument to all directories given as the subsequent arguments of the call.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	for ctl in ${@:2}
	do
	 cp $1 $ctl
	done
	```
	
	</details>

7. Write a script that will back up the files given as arguments to the backup directory and append the current date to their names:

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	if [ ! -d ~/backup ]
	then
	 mkdir ~/backup
	fi
	for file in $*
	do
	 cp $file ~/backup/$(basename $file)_$(date '+%Y-%m-%d')
	done
	```
	
	</details>

8. Write a script that will wait for the appearance of the file with the name indicated in the argument. The script should periodically (every 5 seconds) check the existence of the file. If the file exists, the script should display its contents and exit. Run the script and create a monitored file from the second terminal.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	while ! [ -f $1 ]
	do
	 sleep 5
	done
	cat $1
	```
	
	</details>

9. Create a script and place in it a function that implements the sum of two arguments (numbers) given to the script.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	function sum {
	 echo $(($1+$2))
	}
	sum $1 $2
	```
	
	</details>

</details>

## Repetition

<details>
<summary>Expand!</summary>

1. Write a script that will find in the directory given as an argument to the script all files with the sh extension, modified not more than 7 days ago and will grant them the right to execute.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	find $* -type f -mtime -7 -name "*.sh" -print0 | xargs -0 chmod +x
	```
	
	</details>
	
2. Napisz skrypt który policzy liczbę linii zawierających słowo “color” w pliku ~/.bashrc

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	cat ~/.bashrc | grep color | wc -l
	```
	
	</details>

3. The linux system logs messages in the text file /var/log/kern.log. List the last 3 USB device events from this file.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	cat /var/log/kern.log | grep usb | tail -n 3
	```
	
	</details>

4. Write a script that will print the number of bytes downloaded by the network interface that has downloaded the most data

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	ifconfig | grep 'RX packets' | awk '{printf $5 "\n"}' | sort -nr | head -n 1
	```

	</details>

4. Write a script that lists the MAC addresses of all network interfaces

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	ifconfig | grep -o ..:..:..:..:..:..
	```
	
	</details>

5. Write a script that will create a report.txt file containing the name of the file in each line and its checksum calculated with the md5 algorithm for each *.txt file in the current directory. filename and checksum should be separated by a space. Use md5sum.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	find -maxdepth 1 -type f -exec md5sum {} \; | awk '{$2 = substr($2, 3); printf $1 " " $2 "\n"}' > raport.txt
	```
	
	</details>

6. Write a program to verify the integrity of files in a directory. For each *.txt file in the current directory, compare its checksum calculated with program/*u md5 with the checksum written in the report.txt file from the previous task, and display a warning message in case of discrepancies.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	var=$(find -maxdepth 1 -mindepth 1 -type f -exec md5sum {} \; | awk '{$2 = substr($2, 3); printf $1 " " $2 "\n"}'  | grep -v -e raport.txt -e $0)
	var2=$(cat raport.txt | grep -v -e raport.txt -e $0)
	if [ "$var" != "$var2" ]
	then
	 echo "Error"
	fi
	```
	
	</details>

7. Write a script that, based on the input file indicated by the first argument, will display the names of the three planets with the most moons, in alphabetical order.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	cat $1 | sort -n -r -k 4 | head -3 | sort
	```
	
	</details>

8. The trees.txt file contains information about several trees growing in the garden in the csv format (along with the header in the first line, informing about the content of the file's columns). Write a script that will write to the output.txt file 3 the heights of the two tallest birch trees with the “protected” status. (NOTE error in trees.txt file)

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	cat trees.txt | tail -n +2 | grep chronione | grep brzoza | awk -F',' '{printf $3 "\n"}' | sort -n -r | head -2 > output.txt
	```
	
	</details>

9. Write a script that will concatenate the contents of all files passed as arguments and output to the console

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	for file in $*
	do
	cat $file|  awk -v vname=$(basename $file) '{ printf vname ": " $1 "\n" }'
	done
	```
	
	</details>
	

10. Write a script that will count and print the sum of characters in all files given as call arguments.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	cat $* | tr -d '\n' | wc -c
	```
	
	</details>

11. Write a script that will create a pictures_backup folder in your home directory and copy all .jpg files in the current directory to it, and then make the new files read-only.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	mkdir ~/pictures_backup
	ls -a | grep "\.jpg"$ | xargs -I{} cp -u {} ~/pictures_backup
	chmod 444 ~/pictures_backup/*
	```

	</details>

12. Write a script that assigns the appropriate access rights to files based on the file - access rights argument pairs in numeric notation.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	while [ $1 ]
	do 
	 chmod $2 $1
	 shift
	 shift
	done
	```
	
	</details>

13. Write a script that appends the text specified as the first argument to the end of all files with the extension defined as the second argument and located in the current directory.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	for line in *.$2
	do
	 echo $1 >> $line0
	done
	```

	</details>

14. Write a script that sums up the size of files in the current directory for each extension given as an argument.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	for var in $*
	do
	 ls -l | grep "."$var | awk '{printf $5 "\n"}' | awk -v text=$var '{s+=$1} END {print text ": " s}'
	done
	```
	
	</details>

15. Write a script that will display the first line from the end of the file given as the first argument, the second line from the end of the file given as the second argument, etc. if the file is too short, display an appropriate message.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	cat $1 | tail -1
	var=$(wc -l $2 | awk '{printf $1}')
	if [ $var -gt 1 ]
	 then
	 cat $2 | tail -2 | head -1
	 else
	 echo "The second file has few lines"
	fi
	```
	
	</details>

16. Write a script that takes two arguments - two filenames, which will compare the contents of these two text files. If the content of both files is the same, the script should print the message: files are the same If the files are different, the script should print which of them has more lines, e.g.: file1.txt has more lines than file2.txt. You can use the diff file1.txt file2.txt command to compare the contents of the files

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	t1=$(cat $1)
	t2=$(cat $2)
	if [ "$t1" == "$t2" ]
	then
	 echo "identical files"
	else
	 l1=$(cat $1 | wc -l)
	 l2=$(cat $2 | wc -l)
	 if [ "$l1" -gt "$l2" ]
	 then
	  echo "file $1 has more lines than $2"
	 elif [ "$l1" -lt "$l2" ]
	 then
	  echo "file $2 has more lines than $1"
	 else
	  echo "the files have the same lines but they are different"
	 fi
	fi
	```
	
	</details>

17. Create 3 files in the empty directory: file1.txt, file2.txt and file3.txt. Put a few words in each. Write a script that converts the names of all files in this directory to the number of characters in the file.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	for file in $*
	do
	 count=$(cat $file | wc -w) 
	 path=$(dirname $file)"/"$count
	 mv $file $path
	done
	```
	
	</details>

18. Write a script that reads the process number (PID) and signal number from the keyboard in a loop and then sends the indicated signal to a specific process. Entering the word EXIT ends the script.

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	while true
	do
	 read -p "Enter PID: " pid
	 if [ "$pid" == "EXIT" ]
	 then
	  break
	 elif [ "$pid" ]
	 then
	  kill -STOP $pid 
	 fi
	done
	```
	
	</details>

19. Write a script that recursively renames each directory (except files!) to uppercase.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	var1=$(find $1 -type d | sort -n -r)
	for dir in $var1
	do 
	 var2=$(basename $dir | tr a-z A-Z)
	 var3=$(dirname $dir)
	 var5=$(echo $var3"/"$var2)
	 mv $dir $var5 
	done
	```
	
	</details>

20. UUID (universally unique identifier) or GUID is a globally unique identifier - the identifier of objects, among others, in Windows or wherever a unique identifier is needed

	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	for i in {1..10}
	do
	 uuidgen
	done | sort > id.txt
	```
	
	</details>

21. Write a script that asks the user for the number (index) of a word from the Fibonacci sequence and saves this value to a variable. In the script, add a function that uses recursion to calculate the given string term. Display the calculated value in the terminal.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	function fib(){
	 if (( $1 <= 0 ))
	  then
	   echo 1
	  else 
	   echo $(( $(fib $(($1-1)) ) + $(fib $(($1-2)) ) ))
	 fi
	}
	read -p "Enter number: " val2
	val=$(fib $val2)
	echo $val
	```
	
	</details>

</details>

## Example test

<details>
<summary>Expand!</summary>

1. Write a script that will create a photos folder in the current directory, and then move all files with .jpg and .png extensions in the current directory to it. Set the permissions of the transferred files to read-only. (for your own tests, create a few jpg and png files yourself)

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	var="photos"
	mkdir $var
	ls -a | grep -e "\.jpg"$ -e "\.png"$| xargs -I{} mv -u {} $var
	chmod 444 $var/*
	```
	
	</details>

2. The cars.txt file contains car data in the format year;model;speed. Display car names in one line sorted by speed, separated by commas. Pass the cars.txt file as an argument to the script.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	cat $1 | sort -k 3 -r | awk -F ';' 'a++{printf ","}{printf $2} END {print ""}'
	```
	
	</details>

3. Write a script that will count files and directories that are in the given directory (script argument), without counting in subdirectories. If the argument is not given, the count is to refer to the current directory.


	<details>
	<summary>Answer</summary>
	
	```
	#!/bin/bash
	find $1 -maxdepth 1 -mindepth 1 -type d | wc -l | awk -v text=$1 '{printf "Number of directories in directory " text " = " $1 "\n"}'
	find $1 -maxdepth 1 -mindepth 1 -not -type d | wc -l | awk -v text=$1 '{printf "Number of files in directory " text " = " $1 "\n"}'
	find $1 -maxdepth 1 -mindepth 1 | wc -l | awk '{printf "Sum = " $1 "\n"}
	```
	
	</details>

</details>

## Test script

<details>
<summary>Expand!</summary>

1. Write a script that will return the number of occurrences of a given word in a given file. Both the word and the file location are passed as arguments to the script. A word can follow or precede any other sequence of characters and can occur more than once on a single line, e.g.

	<details>
	<summary>Answer</summary>

	```
	#!/bin/bash
	cat $2 | grep -o $1 | wc -w
	```
	
	</details>

</details>
