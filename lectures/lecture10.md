SIGHUP(1) - hang up;
SIGINT(2) - interrupt(Ctrl-C);
SIGKILL(9) - kill;
SIGTERM(15, default) - terminate;
SIGCONT(18) - continue;
SIGTSTP(20) - TTY Stop(Ctrl-Z).

1. ```sleep``` - delay for a specified amount of time:
  a. ```sleep 10``` - sleep 10 seconds;
2. ```<command> &``` - run in the background;
3. ```jobs``` - display processes runned in background;
4. ```bg``` - resume each suspended job jobspec in the background, as if it had  been  started with  &:
  a. ```sleep 2222``` -> ```Ctrl+Z``` -> ```jobs``` -> ```bg <id>```;
5. ```fg``` - resume jobspec in the foreground, and make it the current job:
  a. ```sleep 1111 &``` -> ```sleep 2222 &``` -> ```sleep 3333 &```-> ```fg``` -> ```Ctrl+z``` -> ```jobs``` -> ```bg <id>``` -> ```jobs```;
6. ```ps```report a snapshot of the current processes:
  a. ```ps --forest```
  b. ```ps -f``` - -f - father;
  c. ```ps aux``` - all processes in system;
  d. ```ps -C <command> -o user,pid,comm``` - find processes;
  e. ```ps -u <username>``` - list all proccess runned by user;
7. ```pstree``` - display a tree of processes:
  ```pstree -a``` - -a - all;
  ```pstree -ap``` - -p - process id;
8. ```kill``` - terminate a process:
  a. ```kill -l```;
  ```sleep 1111 &``` -> ```sleep 2222 &``` -> ```sleep 3333 &```;
  b. ```kill -s SIGTSTP <id>``` - is the same as ```Ctrl-z```;
  c. ```kill -18 <id>``` - is the same as ```bg <id>```;
  d. ```kill <id>``` - send SIGTERM;
9. ```killall``` - kill processes by name:
  a. ```killall <command>```;
  b. ```killall -18 <command>```;
10. ```pgrep``` - look up for processes based on name and other attributes:
  a. ```pgrep -l <part of command>```;
  b. ```pgrep -l -u ubuntu```;
11. ```pkill``` - kill processes based on name and other attributes:
  a. ```pkill <part of command>```;
12. ```top``` - display Linux processes;
13. ```uptime``` -  tell how long the system has been running;
14. ```free``` - display amount of free and used memory in the system;
15. ```nice``` - run a program with modified scheduling priority:
  a. ```nice -n 12 sleep 1000 &``` - run command ```sleep``` with priority 12;
16. ```renice``` - alter priority of running processes:
  ```renice -n 12 <id>```;
