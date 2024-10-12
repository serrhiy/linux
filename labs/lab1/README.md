# Lab 1

1. Install any gnu/linux;
2. How to run  terminal: ```Ctrl + Alt + t```.
3. How to detect:
    - kernel version: Use system util uname(```man uname```). ```uname -r``` or  ```uname -a```;
    - architecture: ```uname -i```;
    - distributives version: Use system util lsb_release(```man lsb_release```). ```lsb_release -a```;
4. Using CLI:
    -  display help for using A: ```man A```;
    - change the current user to the administrator: ```sudo -i```;
    - go to the B directory using the auto-complete features: ```cd B``` (press ```Tab``` while typing B);
    - go to the current user's home directory: ```cd ~```;
    - print all environment variables: ```printenv``` or ```env```;
    - print the environment variable С: ```printenv C``` or ```echo "$C"```;
    - Set the environment variable D with the value E: ```D=E```;
    - print the environment variable D: ```printenv D``` or ```echo "$D"```;
    - print all environment variables: ```printenv```;
    - delete the environment variable D: ```unset D```;
    - print the list of the last executed commands: ```history [n]``` (n is optional number);
    - set the variable D using a command from the list of recent commands: just use arrows;
    - print the variable D: ```printenv D``` or ```echo "$D"```;
    - return to normal user: ```logout```;
    - print the variable D: ```printenv D``` or ```echo "$D"```;

