[**Git**]()

	git pull --rebase origin master
1. —-rebase: avoid to use;
2. git pull --> git merge (handle conflict) --> git push
```
(my_branch) $ git add .
(my_branch) $ git commit -m "..."
(my_branch) $ git checkout devel
(devel) $ git pull origin devel
(devel) $ git merge my_branch
(devel) $ git push origin devel
```


	git reset --hard HEAD
1. HEAD: pointer to last commit snapshot
2. --hard: resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded.
3. [read](http://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit)

[**UNIX**](https://www.tjhsst.edu/~dhyatt/superap/unixcmd.html)

	ps aux | grep foo | grep -v grep | awk '{print $2}' | xargs kill

1. `|`pipe: You can connect two commands together so that the output from one program becomes the input of the next program. Two or more commands connected in this way form a pipe.
2. `ps aux`: list all running process by #ID
	a = show processes for all users
	u = display the process's user/owner
	x = also show processes not attached to a terminal

3. `grep "xx"`: search files for 'xx'

4. `grep -v`: **invert match**

5. `grep -v grep`: not list grep's process ID

4. `awk '{print $2}’`: print out second column

5. `xargs kill`: kill all PID’s running process

[e.g. from stackoverflow](http://stackoverflow.com/questions/3510673/find-and-kill-a-process-in-one-line-using-bash-and-regex)


	tail -f /var/log/syslog
1. `tail -f filename` = `tail -n 10 filename`: monitor file update and display information from the end of the file



	cat list.txt | sort | uniq | wc -l
1. `cat list.txt`: display file
2. `cat list.txt list1.txt > all.txt`: concatenate two files
3. **wc**: word count
	**-l lines; -w words; -m characters**



	./a.out 2> /dev/null
1. /dev/null: black hole
2. linux io redirection: **1> stdout; 2> stderr; &> stdout and stderr**

Notes:
1. [awk](http://blog.csdn.net/andyxm/article/details/5964071)

	Syntax:

		awk '/search pattern1/ {Actions}    
     		/search pattern2/ {Actions}' file

	$0 print line; $1,$2,$3... print column;
2. reference:

	- http://www.ee.surrey.ac.uk/Teaching/Unix/
	- http://www.cyberciti.biz/faq/redirecting-stderr-to-stdout/
