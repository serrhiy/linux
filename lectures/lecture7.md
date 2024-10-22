types of file:
  - ```-``` - simple file;
  - ```d``` - directory;
  - ```l``` - symbol link;
  - ```b``` - block device(read data by blocks);
  - ```c``` - symbol device(read data by chars);
  - ```p``` - named chanel;
  - ```s``` - socket;

Difference between hard and soft links:
All hard links refer to the same metadata as the file, when the file is deleted, hard links still refer to the metadata and have access to the file content. That is, a file in Linux exists as long as there is at least one hard link to it. Symlink is juast a link to file. If rename main file, it will by necessary to change all symlinks the refers to file;

An inode number(file index) is an index into the inode table for the file system.

A file descriptor is just an index into the array of open files for the current process.

1. ```ls``` - list files:
  a. ```ls -l``` - long format;
  b. ```ls -il``` - print index number;
2. ```/dev/urandom``` - pseudo-device for generating random chars:
  a. ```head -c1 /dev/urandom | od -An -tu1```;
  b. ```head -c4 /dev/urandom | od -An -tu4```;
3. ```find``` - find file:
  a. ```find / -type p 2> /dev/null```;
  b. ```find /etc -name '*.conf'```;
  c. ```find . -size 0 -exec ls -l {} \;```;
  d. ```find . -size +1c -size -6c -print```;
  e. ```find . -size +1c -size -6c -printf "%i %s %f\n"```;
  f. ```find /var -mtime -2 -type f -exec ls -l {} \; 2> /dev/null```;
  g. ```find /var -mmin -60 -type f -exec ls -l {} \; 2> /dev/null```;
  h. ```find . maxdepth 1 -type f -printf "%i %f\n"```;
4. ```touch``` - touch file:
  a. ```touch <filename>``` - create file;
5. ```stat``` - get statistics about file;
6. ```ln``` - create link to file:
  a. ```ln <exists-file> <new-file>``` - create hard link;
  b. ```ls -s <exists-file> <new-file>``` - create soft link;
7. ```cp <exists-file> <new-file>``` - copy file;
8. ```mv <exists-file> <new-file>``` - move file;
9. ```rm <file>``` - remove file:
  ```rm -rf <file>``` - remove directory and its content;
10. ```mkdir``` - make directory;
11. ```rmdir``` - remove directory;
