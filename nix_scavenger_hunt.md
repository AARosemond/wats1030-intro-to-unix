# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* /c/Users/binan/projects/wats1030-intro-to-unix*
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* challenge_files  LICENSE  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  README.md  super_scavengers.md
* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* More detailed info is available. file size, time downloaded, file lables, etc.: drwxr-xr-x 1 binan 197613    0 Jan 20 19:17 ..
drwxr-xr-x 1 binan 197613    0 Jan 20 19:17 .git
drwxr-xr-x 1 binan 197613    0 Jan 20 19:17 challenge_files
-rw-r--r-- 1 binan 197613 1.1K Jan 20 19:17 LICENSE
-rw-r--r-- 1 binan 197613 5.7K Jan 20 19:24 nix_scavenger_hunt.md
-rw-r--r-- 1 binan 197613  325 Jan 20 19:17 nix_scavenger_hunt_stretch.md
-rw-r--r-- 1 binan 197613 2.8K Jan 20 19:17 README.md
-rw-r--r-- 1 binan 197613  268 Jan 20 19:17 super_scavengers.md
* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the 
`a`(-a intro: Display,  in  succession,  all  of the available intro manual pages contained within the manual.  It is possible to quit  between  suc     cessive displays or skip any of them.), 
`l` (-l -Tdvi ./foo.1x.gz > ./foo.1x.dvi           This  command  will  decompress  and format the nroff source manual page ./foo.1x.gz into a device independent (dvi) file.), and `h`() options mean when used with the `ls`(ls Display the manual page for the item (program) ls.) command. *Write down what those options do?*
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*($ ls /
bin  dev  git-bash.exe  LICENSE.txt  proc               tmp           unins000.exe  usr
cmd  etc  git-cmd.exe   mingw64      ReleaseNotes.html  unins000.dat  unins000.msg)
* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:* ("/" is the only output I got).  
* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:(/c/Users/binan)*
* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* (1)
* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now? (~/projects/wats1030-intro-to-unix/)*
* Press the up arrow on your keyboard. *What just happened? (
my last command just got pasted in the command line)*
* Press the up arrow a few more times. *What do you see? (It pastes and overlays my commands from earlier)*
* Run the `history` command. *What do you see? ( history
    1  git --version
    2  ls -al ~/.ssh
    3  ssh-keygen -t rsa -b 4096 -C "rosemond@seattleu.edu"
    4  eval $(ssh-agent -s)
    5  ssh-add ~/.ssh/id_rsa
    6  clip < ~/.ssh/id_rsa.pub
    7  cat ~/.ssh/id_rsa.pub
    8  git config --global user.name "AARosemond"
    9  git config --global user.email "rosemond@seattleu.edu"
   10  git config --global user.name
   11  code --help
   12  code --help
   13  code --help
   14  code --help
   15  git config  --global core.editor "code --wait"
   16  git config --global -e
   17  git config --global -e
   18  aar
   19  git status
   20  ls
   21  cd projects
   22  ls
   23  cd wats3010-skills-2/
   24  ls
   25  git status
   26  git add .
   27  git commit -m"added fontawesome"
   28  git push
   29  node --version
   30  ls
   31  cd projects
   32  ls
   33  node --version
   34  cd ~/challenge_files
   35  cd challenge_files
   36  ls .demo
   37  ls
   38  cd ~/projects/wats1030-intro-to-unix/
   39  cd ~/projects/wats1030-intro-to-unix/
   40  history)*

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?(binan)*
* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:(none)*
* How long has your system been running? Use `uptime` to see, and *paste the result here:(bash: uptime: command not found)(uptime -h bash: uptime: command not found)*
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here? (I've been working since 7:58pm in bash and since 8:12pm in ps.
ps aux
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     1981       1    1981      13260  cons0     197613 19:58:06 /usr/bin/bash
     2037    1981    2037      14740  cons0     197613 20:12:29 /usr/bin/ps) *
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here? (top -hv
bash: top: command not found)(The  top  program  provides  a dynamic real-time view of a running system.  It can display system summary information as  well  as  a list  of processes or threads currently being managed by the Linux kernel.  The types of system summary  information  shown  and  the types,  order  and size of information displayed for processes are all user configurable and that configuration can be  made  persistent across restarts)*

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find? (2)*
* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed? (01-15-2015)*

grep = (Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241)

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.(grep -r "Waldo"
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt.
Explicabo vel esse blanditiis dolorem culpa non quia.)*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file? (01
2015_special_stuff.demo
Afton-Jast.user
Aimee-Maggio.user
Alfonso-Gottlieb.user
Allen-Kemmer.user
Almina-Cormier.user
Alta-Lemke.user
Amina-McGlynn.user
Anabel-Hammes.user)q*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.(nothing, when I use "more". but when I use "less" I get detailed, paginated info on each file with names starting with digits and A)*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:(ps aux|grep <binan>
bash: syntax error near unexpected token `newline')*
