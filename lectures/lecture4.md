1. ```cat``` - concatenate files;
2. ```| more``` - simple page: ```cat /etc/passwd /etc/group | more```;
3. ```| less``` - improved pager (or just ```less <filepath>```);
4. ```cut``` - get fields from file: ```cut -d: -f1,2 /etc/passwd```;
5. ```expand``` - replace tabs with spaces: ```expand -t4 <filename>```;
6. ```unexpand``` - opposite to ```expand```: ```unexpand -t4 <filepath>```;
7. ```fmt``` - format file: ```fmt -w30 <filename>``` - every line no longer 30 chars;
8. ```head -10 <filepath>``` - print first 10 lines in file;
9. ```tail -10 <filepath>``` - print last 10 lines in file;
10. ```tail -f <filename>``` - see file in live mode;
11. ```od``` - print file in octal;
12. ```join``` - makes a unification based on key elements;
13. ```paste``` - line-by-line file merging;
14. ```pr``` - prepare text content for printing;
15. ```nl``` - numerate lines;
16. ```sed``` - string editor: 
  a. ```sed -e 's/u/U/g'``` (e - expression, s - substitude, g - global);
  b. ```sed -e 's/u/U/g'``` (i - in place);
  c. ```sed -e 's/\t/  /g'```;
  d. ```sed -e '/ubuntu/d'``` - delete lines with 'ubuntu;
  e. ```sed -e '/ubuntu/d'``` - delete lines with 'ubuntu' word;
  f. ```sed 2d``` - delete second line.
17. ```wc``` - word count:
  a. ```wc -c``` - chars;
  b. ```wc -l``` - lines;
  c. ```wc -w``` - words;
18. ```sort``` - sort string:
  a. ```cut -d: -f1 /etc/passwd | sort```;
  b. ```sort -t: -k1 /etc/passwds``` - the same;
  c. ```sort -t: -k3 -n /etc/passwds``` - sort as numbers;
19. ```uniq``` - find unique lines:
  a. ```cut -d: -f7 /etc/passwd | sort | uniq```;
  b. ```cut -d: -f7 /etc/passwd | sort | uniq -c```;
20. ```tr``` - replace chars from stdin to stdout(only pipe):
  a. ```cat <filepath> | tr u U```;
  b. ```cat <filepath> | tr -d u```;
21. ```split```- split into files:
  a. ```aplit -l1 <filepath>``` - every file will have only 1 line;