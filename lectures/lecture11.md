/etc/passwd - contains a database of user accounts;
/etc/shadow - stores users passwords from /etc/passwd;
/etc/groups - stores data about groups;
/etc/gshadow - stores groups passwords;

group - a union of several accounts to set the same restrictions for participants of groups;

directory /etc/skel contains files that are added to the new user's home directory;

after uninstalling the corset, only the configuration files are changed, its home directory is not changed

1. ```sudo su -``` - change user to root;
2. ```useradd``` - add user:
  a. ```useradd <username> -g sudo -m -s /bin/sh``` -g add to group, -m - copy files from /etc/skel -s - default shell. But this user as not password yet;
3. ```passwd``` - change password:
  a. ```passwd <username>```;
4. ```userdel``` - delete user:
  ```userdel <username>```;
  ```userdel -r <username>``` - delete all data(including home directory);
5. ```usermod``` - modify a user account:
  a. ```usermod -L <username>``` - lock user;
  b. ```usermod -U <username>``` - unlock user;
  c. ```usermod -aD <groupname>``` - add user to group;
6. ```groupadd``` - add group:
  a. ```groupadd <groupname>```;
7. ```gpasswd``` - set password for group:
  a. ```gpasswd <groupname>```;
8. ```groupmod``` - modify a group:
  ```groupmod -g 10000 <groupname>``` - change groups id;
9. ```groupdel``` - delete group:
  a. ```groupdel <groupname>```;
10. ```chage``` - change user password expiry information:
  ```chage -l <username>``` - list data;
  ```chage -E 2024-11-25 <username>``` - block user after this day;
