# LINUX

<a href="https://explainshell.com/explain" target="_blank">🔥 Learn About Commands 🔥</a>


## Cheatsheet of Linux
| **Command** | **Description** |
| --------------|-------------------|
| `man <tool>` | Opens man pages for the specified tool. | 
| `<tool> -h` | Prints the help page of the tool. | 
| `apropos <keyword>` | Searches through man pages' descriptions for instances of a given keyword. | 
| `cat` | Concatenate and print files. |
| `whoami` | Displays current username. | 
| `id` | Returns users identity. | 
| `hostname` | Sets or prints the name of the current host system. | 
| `uname` | Prints operating system name. | 
| `pwd` | Returns working directory name. | 
| `ifconfig` | The `ifconfig` utility is used to assign or view an address to a network interface and/or configure network interface parameters. | 
| `ip` | Ip is a utility to show or manipulate routing, network devices, interfaces, and tunnels. | 
| `netstat` | Shows network status. | 
| `ss` | Another utility to investigate sockets. | 
| `ps` | Shows process status. | 
| `who` | Displays who is logged in. | 
| `env` | Prints environment or sets and executes a command. | 
| `lsblk` | Lists block devices. | 
| `lsusb` | Lists USB devices. | 
| `lsof` | Lists opened files. | 
| `lspci` | Lists PCI devices. | 
| `sudo` | Execute command as a different user. | 
| `su` | The `su` utility requests appropriate user credentials via PAM and switches to that user ID (the default user is the superuser).  A shell is then executed. | 
| `useradd` | Creates a new user or update default new user information. | 
| `userdel` | Deletes a user account and related files. |
| `usermod` | Modifies a user account. | 
| `addgroup` | Adds a group to the system. | 
| `delgroup` | Removes a group from the system. | 
| `passwd` | Changes user password. |
| `dpkg` | Install, remove and configure Debian-based packages. | 
| `apt` | High-level package management command-line utility. | 
| `aptitude` | Alternative to `apt`. | 
| `snap` | Install, remove and configure snap packages. |
| `gem` | Standard package manager for Ruby. | 
| `pip` | Standard package manager for Python. | 
| `git` | Revision control system command-line utility. | 
| `systemctl` | Command-line based service and systemd control manager. |
| `ps` | Prints a snapshot of the current processes. | 
| `journalctl` | Query the systemd journal. | 
| `kill` | Sends a signal to a process. | 
| `bg` | Puts a process into background. |
| `jobs` | Lists all processes that are running in the background. | 
| `fg` | Puts a process into the foreground. | 
| `curl` | Command-line utility to transfer data from or to a server. | 
| `wget` | An alternative to `curl` that downloads files from FTP or HTTP(s) server. |
| `python3 -m http.server` | Starts a Python3 web server on TCP port 8000. | 
| `ls` | Lists directory contents. | 
| `cd` | Changes the directory. |
| `clear` | Clears the terminal. | 
| `touch` | Creates an empty file. |
| `mkdir` | Creates a directory. | 
| `tree` | Lists the contents of a directory recursively. |
| `mv` | Move or rename files or directories. | 
| `cp` | Copy files or directories. |
| `nano` | Terminal based text editor. | 
| `which` | Returns the path to a file or link. |
| `find` | Searches for files in a directory hierarchy. | 
| `updatedb` | Updates the locale database for existing contents on the system. |
| `locate` | Uses the locale database to find contents on the system. | 
| `more` | Pager that is used to read STDOUT or files. |
| `less` | An alternative to `more` with more features. | 
| `head` | Prints the first ten lines of STDOUT or a file. |
| `tail` | Prints the last ten lines of STDOUT or a file. | 
| `sort` | Sorts the contents of STDOUT or a file. |
| `grep` | Searches for specific results that contain given patterns. | 
| `cut` | Removes sections from each line of files. |
| `tr` | Replaces certain characters. | 
| `column` | Command-line based utility that formats its input into multiple columns. |
| `awk` | Pattern scanning and processing language. |
| `sed` | A stream editor for filtering and transforming text. | 
| `wc` | Prints newline, word, and byte counts for a given input. |
| `chmod` | Changes permission of a file or directory. |
| `chown` | Changes the owner and group of a file or directory. |


## Bash Shell Scripting

```bash
#! /usr/bin/bash

echo hello bash me is Ritesh 😎.

TEMP="some data"
echo "this is some : $TEMP"

get values from the user

read -p "enter something : " INP
echo "you entered $INP"

# #if else statements

if [ $INP -eq 100 ]
then
    echo "you are awesome"
elif [ "$INP" == "Rish" ]
then
    echo "you are awesome too"
else
    echo "get lost"
fi

-eq equal
-ne not equal
-gt greater than
-ge greater than or equal to
-lt less than
-le less than or equal to


lets make programme number 1 🎃

addition of two numbers

read -p "enter number 1: " NUM1
read -p "enter number 2: " NUM2
((SUM=$NUM1+$NUM2))
echo "the sum of the numbers is $SUM"

lets make programme number 2 👓

# highest of three numbers

read -p "enter number 1: " NUM1
read -p "enter number 2: " NUM2
read -p "enter number 3: " NUM3
if((NUM1>NUM2));then
    if((NUM1>NUM3));then
        echo "the greatest is $NUM1"
    else
        echo "the greatest is $NUM3"
    fi
elif((NUM2>NUM3));then
    echo "the gratest is $NUM2"
else
    echo "the greatest is $NUM3"
fi

lets make programme number 3 🥼

# swap two numbers

read -p "enter number 1: " NUM1
read -p "enter number 2: " NUM2
((NUM1=$NUM1+$NUM2))
((NUM2=$NUM1-$NUM2))
((NUM1=$NUM1-$NUM2))
echo "after swap $NUM1 and $NUM2"

For Loops
NAME="hello bash me is Ritesh 😎"
for var in $NAME
do
    echo $var
done

while 

N=10
while((N!=0))
do 
    echo $N
    ((N--))
done

lets make programme number 4 🎓

# prime number

read -p "enter a number to check: " N
I=2
P="prime"
while((I<N))
do
    if((N%I==0))
    then
        P="not prime"
        break
    fi
done
echo $P

programme number 5 🧐
# even odd

# Do it by yourself 😉
read var
if(($var%2==0));then
    echo "even"
else
    echo "odd"
fi


programme number 6 🎂
# sum of digits 

read -p "enter a number: " N
S=0
while((N!=0))
do
    ((T=$N%10))
    ((N=$N/10))
    ((S=$S+$T))
done
echo $S
```

```bash
#! /usr/bin/bash
for var in "$@"
do
    echo $var
done


echo $#

((n=$1+$2))
echo $$
echo $n

n=1
while((n!=6))
do
    mkdir dir-$n
    cd dir-$n
    touch file-$n
    cd ..
    ((n++))
done
```

```bash
#! /usr/bin/bash
x=3;y=5;z=10;
if [ ($x -eq 3 ) -a ( $y -eq 5 -o $z -eq 10 ) ]
then
    echo $x
else
    echo $y
fi
```

