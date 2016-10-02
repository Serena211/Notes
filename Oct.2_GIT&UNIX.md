[**Git**]()

	git pull --rebase origin master

—-rebase:

	git reset --hard HEAD

[**UNIX**](https://www.tjhsst.edu/~dhyatt/superap/unixcmd.html)

	ps aux | grep foo | grep -v grep | awk '{print $2}' | xargs kill

1. pipe: You can connect two commands together so that the output from one program becomes the input of the next program. Two or more commands connected in this way form a pipe.
2. ps aux: list all running process by #ID
	a = show processes for all users
	u = display the process's user/owner
	x = also show processes not attached to a terminal

3. grep "xx": search files for 'xx'

4. grep **-v**: **invert match**

5. grep -v grep: not list grep's process ID

4. awk '{print $2}’: print out second column

5. xargs kill: kill all PID’s running process

[e.g. from stackoverflow](http://stackoverflow.com/questions/3510673/find-and-kill-a-process-in-one-line-using-bash-and-regex)

	kill $(ps aux | grep '[p]ython csp_build.py' | awk '{print $2}')

Notes:
1. [awk](http://blog.csdn.net/andyxm/article/details/5964071)

	Syntax:

		awk '/search pattern1/ {Actions}    
     		/search pattern2/ {Actions}' file

	$0 print line; $1,$2,$3... print column;
