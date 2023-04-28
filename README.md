# Linux commands Q&A for SCR in PP on AiR

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

7. Create directory kat1 in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	mkdir ~/kat1
	```
		
	</details>
		
8. In directory kat1, create a directory structure with one command: kat2/kat3/kat4.
	
	<details>
	<summary>Answer</summary>
		
	```
	mkdir -p ~/kat1/kat2/kat3/kat4
	```
		
	</details>
	
9. Delete the entire directory structure of kat3/kat4 in one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm -r ~/kat1/kat2/kat3
	```
		
	</details>
	
10. Create files with any names with extensions .txt and .c in your home directory (2-3 files with each extension)
	
	<details>
	<summary>Answer</summary>
		
	```
	touch ~/xD.txt ~/xDD.txt ~/xDDD.txt ~/y.c ~/y.cc
	```
		
	</details>
	
11. Copy all the files from the home directory with the extension .txt to the directory kat1 with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp ./*.txt ~/kat1
	```
		
	</details>

12. Copy all files from the home directory with the extension .c to the directory kat2 with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp ./*.c ~/kat1/kat2
	```
		
	</details>
	
13. Copy the entire directory structure of kat1 creating an analogous structure called kat1b.
	
	<details>
	<summary>Answer</summary>
		
	```
	cp -r ~/kat1 ~/kat1b
	```
		
	</details>
	
14. Delete all files in kat1/kat2.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm ~/kat1/kat2/*
	```
		
	</details>

15. Delete the entire directory structure of kat1b with one command.
	
	<details>
	<summary>Answer</summary>
		
	```
	rm -r ~/kat1b
	```
		
	</details>
	
16. Rename any file in directory kat1.
	
	<details>
	<summary>Answer</summary>
		
	```
	mv ~/kat1/x.txt ~/kat1/xx.txt
	```
		
	</details>	

17. Move the directory kat1/kat2 to your home directory, thus creating the directory kat2b.
	
	<details>
	<summary>Answer</summary>
		
	```
	mv ~/kat1 ~/kat2b
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

20. Copy all regular files between 10 and 100 bytes from /usr/bin to kat1/kat2 (use the find command with the -exec parameter).
	
	<details>
	<summary>Answer</summary>
	
	```
	find /usr/bin -size +10 -size -100 -exec cp {} ~/kat1/kat2 \;
	```
	
	</details>
	
21. In your home directory, create a file named plik.txt - check the access rights to it.
	
	<details>
	<summary>Answer</summary>
		
	```
	touch ~/plik.txt | ls -l ~
	```
		
	</details>
	
22. For plik.txt, add write access for other users.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod a+w ~/plik.txt
	```
		
	</details>
	
23. For plik.txt, subtract the owner's write permission.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod u-w ~/plik.txt
	```
	
	</details>
	
24. For plik.txt, add execute permission for all users.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod +x ~/plik.txt
	```

	</details>
	
25. For file plik.txt and all users, allow only file read.
	
	<details>
	<summary>Answer</summary>
		
	```
	chmod 444 ~/plik.txt
	```
		
	</details>

26. For file plik.txt, restore the original rights using numerical notation.
	
	<details>
	<summary>Answer</summary>
	
	```
	chmod 664 ~/plik.txt
	```
	
	</details>

27. Create a link to plik.txt named plik2.txt in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	ln ~/plik.txt ~/plik2.txt
	```
	
	</details>

28. Create a symbolic link to directory kat1/kat2 named abc in your home directory.
	
	<details>
	<summary>Answer</summary>
		
	```
	ln -s ~/kat1/kat2 ~/abc
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
	
## Lab 02
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
	``
	
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
	

<details>
<summary>TODO</summary>
	
-- LAB 03 --

1.Wyświetl plik /etc/passwd z podziałem na strony przyjmując, że strona ma 5 linii tekstu. Podpowiedź: sprawdź program more
	cat /etc/passwd | more -n 5

2.Stwórz pliki tekst1 oraz tekst2, wypełnij kilkoma linijkami tekstu. Korzystając z polecenia cat utwórz plik tekst3, który będzie składał się z zawartości plików tekst1 oraz tekst2.
	cat > ~/tekst1.txt
	Nie wiem
	Ctrl + D
	cat > ~/tekst2.txt
	niczego
	Ctrl + D
	cat ~/tekst1.txt ~/tekst2.txt > ~/tekst3.txt

3.Wyświetl po 5 pierwszych linii wszystkich plików w swoim katalogu domowym w taki sposób, aby nie były wyświetlane ich nazwy. Podpowiedź: pamiętaj, że z programami, które przyjmują jako argumenty nazwy plików możesz używać wzorców.
	cat * */* 2>/dev/null | head -n 5

4.Wyświetl linie o numerach 3, 4 i 5 z pliku /etc/passwd
	cat /etc/passwd | sed -n '3,5p'

5.Wyświetl linie o numerach 7, 6 i 5 licząc od końca pliku /etc/passwd (czyli kolejno 7. od końca, 6. od końca i 5. od końca)
	cat /etc/passwd | tail -n 7 | head -n 3

6.Wyświetl zawartość /etc/passwd w jednej linii
	cat /etc/passwd | tr '\n' ' '

7.Za pomocą filtru tr wykonaj modyfikację pliku, polegającą na umieszczeniu każdego słowa (oddzielonych spacją) w osobnej linii. Podpowiedź: aby przekazać znak spacji jako argument, musisz umieścić go w cudzysłowie
	cat < ~/xD.txt | tr ' ' '\n'

8.Zlicz wszystkie pliki znajdujące się w katalogu /etc i jego podkatalogach
	find /etc -not -type d 2>/dev/null | wc -l

9.Napisz polecenie zliczające sumę znaków z pierwszych trzech linii pliku /etc/passwd
	cat /etc/passwd | head -n 3 | wc* -c

10.Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.
	ls | tr a-z A-Z

11.Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę
	ls -l | awk '{print $1 " " $5 " " $9}'

12.Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliki 
	ls -1sp | grep -v / | sort -n -r | grep -oE '[^ ]+$'

13.Wyświetl zawartość pliku /etc/passwd posortowaną wg numerów UID w kolejności od największego do najmniejszego
	cat /etc/passwd | sort -t ':' -n -k 3 -r

14.Wyświetl zawartość pliku /etc/passwd posortowaną najpierw wg numerów GID w kolejności od największego do najmniejszego, a następnie UID
	cat /etc/passwd | sort -t ':' -n -k 4 -r -k 3

15.Podaj nazwy trzech najmniejszych plików w katalogu posortowane wg nazwy
	ls -1sp | grep -v / | sort -n -r | grep -oE '[^ ]+$' | sort | head -3

16.W pliku /etc/services przechowywana jest lista popularnych usług sieciowych, wraz z numerami portów i protokołem. Wylistuj (tylko) nazwy usług, które korzystają z protokołu UDP.
	cat /etc/services | grep 'udp' | awk '{print $1}'


17.Wyświetl, ile wirtualnych terminali (dev/tty) o numerach z zakresu 50-69 znajduje się w systemie.
	ls /dev/tty* -1 | grep '[5-6][0-9]' | ls /dev/tty* -1 | grep '[5-6][0-9]' | wc -l

18.Zbuduj potok, który wyświetli w terminalu PID procesu cupsd.
	ps -ax | grep -e 'pts' | grep -e 'cupsd' | awk '{print $1}'

-- LAB 04 --

1.Zdefiniuj zmienną IMIE i przypisz jej swoje imię. Wyświetl zawartość tej zmiennej. Wyeksportuj tą zmienną i sprawdź, czy jest dostępna w nowym (potomnym) interpreterze.
	IMIE=Adam
	echo $IMIE
	en~a
	Nie jest dostępna w innnym interpreterze
2.Wyświetl listę zmiennych eksportowanych.
	env

3.Zmień własny znak zachęty, modyfikując zmienną PS1.
	PS1="xd: "

4.Napisz skrypt, który dla każdego elementu (pliku, folderu) w bieżącym katalogu wyświetli jego nazwę wraz z informacją czy jest to plik czy katalog.
                                                        
#!/bin/bash
for FILE in ~/*
do
 name=$(basename $FILE)
 if [ -f $FILE ]
 then
  echo "$(basename $FILE) -> plik"
 else
  echo "$(basename $FILE) -> katalog"
 fi
done

5.Napisz skrypt, który dla każdego z plików podanych jako argumenty wywołania wyświetli nazwę pliku, a następnie jego zawartość posortowaną alfabetycznie.
                                                           
#!/bin/bash
for FILE in $*
do
 echo  $( cat $FILE | sort )
done

6.Napisz skrypt, który będzie kopiował plik podany jako pierwszy argument do wszystkich katalogów podanych jako kolejne argumenty wywołania.
                                                            
#!/bin/bash
for ctl in ${@:2}
do
 cp $1 $ctl
done

7.Napisz skrypt, który wykona kopię zapasową plików podanych jako argumenty, do katalogu backup i dopisze do ich nazwy bieżącą datę:

#!/bin/bash
if [ ! -d ~/backup ]
then
 mkdir ~/backup
fi
for file in $*
do
 cp $file ~/backup/$(basename $file)_$(date '+%Y-%m-%d')
done

8.Napisz skrypt, który będzie oczekiwał na pojawienie się pliku o nazwie wskazanej w argumencie. Skrypt powinien cyklicznie (co 5 sekund) sprawdzać istnienie pliku. Jeśli plik istnieje, skrypt powinien wyświetlić jego zawartość i zakończyć się. Uruchom skrypt, a z poziomu drugiego terminala utwórz monitorowany plik.

#!/bin/bash
while ! [ -f $1 ]
do
 sleep 5
done
cat $1

9.Utwórz skrypt i umieść w nim funkcję realizującą sumę dwóch argumentów (liczb) podawanych do skryptu.

#!/bin/bash
function sum {
 echo $(($1+$2))
}
sum $1 $2

-- POWTÓRKA --

1.Napisz skrypt, który znajdzie w katalogu podanym jako argument do skryptu wszystkie pliki z rozszerzeniem sh, modyfikowane nie dawniej niż 7 dni temu i nada im prawo do wykonywania.

#!/bin/bash
find $* -type f -mtime -7 -name "*.sh" -print0 | xargs -0 chmod +x

2.Napisz skrypt który policzy liczbę linii zawierających słowo “color” w pliku ~/.bashrc

#!/bin/bash
cat ~/.bashrc | grep color | wc -l

3.System linux loguje wiadomości w pliku tekstowym /var/log/kern.log. Wypisz z tego pliku 3 ostatnie zdarzenia dotyczące urządzeń USB.

#!/bin/bash
cat /var/log/kern.log | grep usb | tail -n 3

4.1.Napisz skrypt, który wypisze ilość bajtów pobraną przez interfejs sieciowy, który pobrał tych danych najwięcej

#!/bin/bash
ifconfig | grep 'RX packets' | awk '{printf $5 "\n"}' | sort -nr | head -n 1

4.2.Napisz skrypt, który wypisze adresy MAC wszystkich interfejsów sieciowych

#!/bin/bash
ifconfig | grep -o ..:..:..:..:..:..

5.Napisz skrypt, który stworzy plik raport.txt, zawierający w każdym wierszu nazwę pliku oraz jego sumę kontrolną obliczoną algorytmem md5, dla każdego pliku *.txt w aktualnym katalogu. nazwa pliku i suma kontrolna powinny być oddzielone spacją. Wykorzystaj program md5sum.

#!/bin/bash
find -maxdepth 1 -type f -exec md5sum {} \; | awk '{$2 = substr($2, 3); printf $1 " " $2 "\n"}' > raport.txt

6.Napisz program weryfikujący integralność plików w katalogu. Dla każdego pliku *.txt w aktualnym katalogu, porównaj jego sumę kontrolną obliczoną za pomocą program/*u md5 z sumą kontrolną zapisaną w pliku raport.txt z zadania poprzedniego, oraz wyświetl ostrzegawczy komunikat w przypadku rozbieżności.

#!/bin/bash
var=$(find -maxdepth 1 -mindepth 1 -type f -exec md5sum {} \; | awk '{$2 = substr($2, 3); printf $1 " " $2 "\n"}'  | grep -v -e raport.txt -e $0)
var2=$(cat raport.txt | grep -v -e raport.txt -e $0)
if [ "$var" != "$var2" ]
then
 echo "Error"
fi

7.Napisz skrypt, który na podstawie pliku wejściowego wskazanego pierwszym argumentem wyświetli nazwy trzech planet o największej liczbie księżycy, w kolejności alfabetycznej.

#!/bin/bash
cat $1 | sort -n -r -k 4 | head -3 | sort

8.W pliku trees.txt zapisane są w formacie csv informacje o kilku drzewach rosnących w ogrodzie (wraz z nagłówkiem w pierwszej linii, informującym o zawartości kolumn pliku). Napisz skrypt, który zapisze do pliku output.txt 3 wysokości dwóch najwyższych brzóz o statusie “chronione”. (UWAGA błąd w pliku trees.txt)

#!/bin/bash
cat trees.txt | tail -n +2 | grep chronione | grep brzoza | awk -F',' '{printf $3 "\n"}' | sort -n -r | head -2 > output.txt

9.Napisz skrypt, który sklei zawartość wszystkich plików przekazanych jako argumenty i wypisze w konsoli

#!/bin/bash
for file in $*
do
cat $file|  awk -v vname=$(basename $file) '{ printf vname ": " $1 "\n" }'
done

10.Napisz skrypt, który zliczy i wypisze sumę znaków we wszystkich plikach podanych jako argumenty wywołania.

#!/bin/bash
cat $* | tr -d '\n' | wc -c

11.Napisz skrypt, który utworzy w katalogu domowym folder pictures_backup i skopiuje do niego wszystkie pliki z rozszerzeniem jpg znajdujące się w bieżącym katalogu, a następnie zmieni nowym plikom prawa dostępu na tylko do odczytu.

#!/bin/bash
mkdir ~/pictures_backup
ls -a | grep "\.jpg"$ | xargs -I{} cp -u {} ~/pictures_backup
chmod 444 ~/pictures_backup/*

12.Napisz skrypt, który przydzieli plikom odpowiednie prawa dostępu na podstawie par argumentów plik - prawa dostępu w notacji numerycznej.

#!/bin/bash
while [ $1 ]
do 
 chmod $2 $1
 shift
 shift
done

13.Napisz skrypt, który dopisze tekst określony jako pierwszy argument wywołania na końcu wszystkich plików z rozszerzeniem zdefiniowanym jako drugi argument i znajdujących się w bieżącym katalogu.

#!/bin/bash
for line in *.$2
do
 echo $1 >> $line0
done

14.Napisz skrypt, który zsumuje wielkości plików w bieżącym katalogu dla każdego rozszerzenia podanego jako argument.

#!/bin/bash
for var in $*
do
 ls -l | grep "."$var | awk '{printf $5 "\n"}' | awk -v text=$var '{s+=$1} END {print text ": " s}'
done

15.Napisz skrypt, który wyświetli pierwszą linię od końca z pliku podanego jako pierwszy argument, drugą linię od końca z pliku podanego jako drugi argument itd. eżeli dany plik jest zbyt krótki, wyświetl stosowny komunikat.

#!/bin/bash
cat $1 | tail -1
var=$(wc -l $2 | awk '{printf $1}')
if [ $var -gt 1 ]
 then
 cat $2 | tail -2 | head -1
 else
 echo "Plik drugi ma z mało linii
fi

16.Napisz skrypt przyjmujący dwa argumenty - dwie nazwy plikow, który porówna zawartość tych dwóch plików tekstowych. Jeżeli zawartość obu plików jest jednakowa skrypt powinien wypisać wiadomość: pliki jednakowe Jeżeli pliki są różne, skrypt powinien wypisać który z nich ma więcej linii, np.: plik1.txt ma więcej linii niż plik2.txt
Do porównania zawartości plików możesz wykorzystać komendę diff plik1.txt plik2.txt

#!/bin/bash
t1=$(cat $1)
t2=$(cat $2)
if [ "$t1" == "$t2" ]
then
 echo "pliki jednakowe"
else
 l1=$(cat $1 | wc -l)
 l2=$(cat $2 | wc -l)
 if [ "$l1" -gt "$l2" ]
 then
  echo "plik $1 ma wiecej linii niz $2"
 elif [ "$l1" -lt "$l2" ]
 then
  echo "plik $2 ma wiecej linii niz $1"
 else
  echo "pliki maja tyle samo linii ale sie roznia"
 fi
fi

17.Stwórz w pustym katalogu 3 pliki: plik1.txt, plik2.txt oraz plik3.txt. Umieść w każdym kilka słów. Napisz skrypt, który zamieni nazwy wszystkich plików w tym katalogu na liczbę znaków w danym pliku.

#!/bin/bash
for file in $*
do
 count=$(cat $file | wc -w) 
 path=$(dirname $file)"/"$count
 mv $file $path
done

18.Napisz skrypt, który w pętli wczytuje z klawiatury numer (PID) procesu, numer sygnału a następnie wysyła wskazany sygnał do określonego procesu. Wpisanie słowa EXIT kończy pracę skryptu.

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

19.Napisz skrypt zmieniający rekursywnie nazwę każdego katalogu (pomijając pliki!) na wielkie litery.

#!/bin/bash
var1=$(find $1 -type d | sort -n -r)
for dir in $var1
do 
 var2=$(basename $dir | tr a-z A-Z)
 var3=$(dirname $dir)
 var5=$(echo $var3"/"$var2)
 mv $dir $var5 
done

20.UUID (universally unique identifier) lub GUID jest to identyfikator globalnie unikatowy – identyfikator obiektów między innymi w systemie Windows lub wszędzie, gdzie potrzebny jest unikatowy identyfikator

#!/bin/bash
for i in {1..10}
do
 uuidgen
done | sort > id.txt

21.

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


-- TESTOWY TEST --

1.Napisz skrypt, który utworzy w bieżącym katalogu folder photos, a następnie przeniesie do niego wszystkie plik z rozszerzeniami jpg i png znajdujące się w bieżącym katalogu. Przeniesionym plikom ustaw prawa dostępu na tylko do odczytu. (na potrzby własnych testów utwórz samodzielnie kilka plików jpg i png) 

#!/bin/bash
var="photos"
mkdir $var
ls -a | grep -e "\.jpg"$ -e "\.png"$| xargs -I{} mv -u {} $var
chmod 444 $var/*

2.W pliku cars.txt zapisane są dane samochodów w formacie rok;model;prędkość. Wyświetl w jednej linii nazwy samochodów posortowane rosnąco wg prędkości, oddzielone przecinkami. Przekaż plik cars.txt jako argument do skryptu.

#!/bin/bash
cat $1 | sort -k 3 -r | awk -F ';' 'a++{printf ","}{printf $2} END {print ""}'

3.Napisz skrypt, który będzie zliczał plików i katalogów, które znajdują się w podanym katalogu (argument do skryptu), bez zliczania w podkatalogach. Jeśli argument nie został podany zliczanie ma dotyczyć katalogu bieżącego. Przykład:

#!/bin/bash
find $1 -maxdepth 1 -mindepth 1 -type d | wc -l | awk -v text=$1 '{printf "Liczba katalogow w katalogu " text " = " $1 "\n"}'
find $1 -maxdepth 1 -mindepth 1 -not -type d | wc -l | awk -v text=$1 '{printf "Liczba plikow w katalogu " text " = " $1 "\n"}'
find $1 -maxdepth 1 -mindepth 1 | wc -l | awk '{printf "Suma = " $1 "\n"}

-- TEST SKRYPTU --

1. Napisz skrypt, który zwróci liczbę wystąpień wybranego słowa w zadanym pliku. Zarówno słowo jak i lokalizacja pliku przekazywane są jako argumenty do skryptu. Słowo może następować lub poprzedzać dowolny inny ciąg znaków i może wystąpić więcej niż raz w jednej linii, np.

#!/bin/bash
cat $2 | grep -o $1 | wc -w
</details>
