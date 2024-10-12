1. ```grep``` - find line by regular expression:
  a. ```grep [[:digit:]] /etc/passwd```;
  b. ```grep [[:lower:]] /etc/passwd```;
  c. ```grep [[:upper:]] /etc/passwd```;
  d. ```grep [[:alpha:]] /etc/passwd```;
  e. ```grep [[:alnum:]] /etc/passwd```;
  f. ```grep [[:punct:]] /etc/passwd```;
  g. ```grep [[:blank:]] /etc/passwd```;
2. ```grep -F bash /etc/passwd | cut -d: -f1 | sort | xargs -p -IX grep -F X /var/log/auth.log```;
3. ```seq 2 8 | xargs -IX sh -c 'echo fileX > fileX'```;
4. ```grep -F bash /etc/passwd | cut -d: -f1 | sort | xargs -t -IX grep X /etc/group```;