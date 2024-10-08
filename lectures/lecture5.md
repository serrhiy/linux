1. ```ls /var/ > <filepath>``` - redirect the result of execution from the stdout to a file (rewrite file or create if exists);
2. ```ls /var/ >> <filepath>``` - redirect the result of execution from the stdout to a file (append to the end or create if file doesnt exist);
3. ```ls /not_exists/ 2> <filepath>``` - redirect the stderr to a file;
4. ```ls /var/ /not_exists/ &> <filepath>``` - join stdout and stderr into file stream;
5. ```ls /var/ /not_exists/ 2> /dev/null``` - get only stdout stream and write erros into /dev/null (special consumer for ignoring streams);
6. ```ls /var/ /not_exists/ 2> <filepath> 1> <filepath>```
7. ```ls /var/ /not_exists/ > <filepath> 2>&1``` - stderr is reallocated to the stdout and written to the file;
8. ```cat < /etc/passwd``` - is the same for ```cat /etc/passwd```;
9. ```cat > <filepath>>``` - get data from stdin(keyboard) and put it into file stream;
10. ```cat << END``` - multiline capability(until ```END``` is entered);
11. ```cat << END > <filepath>``` - redirect stdout stream into file;
12. ```xargs``` - get args from stdout and redirect into stdin:
  a. ```cut -f6 -d: /etc/passwd | tail -3 | head -2 | xargs -t -n1 ls``` - ```-t``` - print command, ```-n1``` - each line is one arg;
13. ```tee``` - copy stdout streem into fiule stream:
  a. ````cut -f6 -d: /etc/passwd | tail -6 | tee <filepath>```;
14. ```sleep <number>``` - sleep for some time;
15. ```&``` - puts the command into background mode: ```sleep <number> &```;
16. ```echo $?``` - get last command result code(0 if success);
17. ```&&``` - execute command if previos conmmands result code is 0:
  a. ```ls /result/ && echo 'will not be printed'```;
  b. ```ls /var/ && echo 'will be printed'```;
18. ```true``` or ```false``` - can be used with ```&&```:
  a. ```echo first && true && echo second```;
  b. ```echo first && false && echo second```;

19. ```||``` - execute command if previos conmmands result code is not 0:
  a. ```ls /result/ || echo 'will be printed'```;
  b. ```ls /var/ || echo 'will not be printed'```;