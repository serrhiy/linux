File access rights:
  - user-owner(u);
  - group-owner(g);
  - other users(o);

Three types of access rights:
  - read(r);
  - write(w);
  - execution(x);
You can change access rights with cxommand ```chmod```;

By default, the w flag is not set for a directory, and the w and x flags are set for files.

Super user (sudo) can write and read despite any flags(folders).

Sticky bit - remove possibility delete other users files;

1. ```whoami``` - get current user name;
2. ```groups``` - get a list of groups in which the current user is a member;
3. ```id``` - print real and effective user and group IDs;
4. ```umaask``` - set or view file mode creation mask;
5. ```chmod``` - change file mod:
  a. ```chmod u+x <filename>``` - set executable flag for user-owner;
  b. ```chmod g-w,o=wx <filename>``` - remove write flag for group and set write and execute flags for othert users;
  c. ```chmod ugo=r <filename>``` - set only read flag for all;
  d. ```chmod a=r <filename>``` - set only read flag for all;
  e. ```chmod +r <filename>``` - set only read flag for all;
  f. ```chmod 764 <filename>``` - set all flags for user, read and write for group and read for other users;
  g. ```chmod u+s <filename>``` - set flag ```SUID - sert user id```(the same is for group);
6. ```stat``` - display file or file system status;
7. ```lasattr``` - list file attributes on a Linux second extended file system;
