1. create the abc directory in the user's home directory, and in it the same subdirectory structure as in /usr/lib: ```find /usr/local/ -type d -printf "%P\n" | xargs -IX mkdir -p ~/abc/X```;
2. skip;
3. find directories of level 3 or more relative to abc and create a file1.txt in each of the found directories and write the full name of the directory (from the root /) to it :```find ~/abc/ -mindepth 3 -type d | xargs -IX sh -c "echo X > X/1.txt"```;
4. Select from the /etc/passwd file the home directories of all users who have /bin/bash. Copy the .bash_history files from them to the /root/test directory, replacing the file name with the username: ```fgrep /bin/bash /etc/passwd | cut -d: -f6,1 --output-delimiter=' ' | xargs -n2 sh -c 'cp "$1/.bash_history" "/home/serhii/test/$0"'```;