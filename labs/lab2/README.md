
1. Print the files test.txt, city.txt and pass.txt: ```cat test.txt city.txt pass.txt```;
2. Print the number of words in the files test.txt, city.txt and pass.txt: ```wc -w test.txt city.txt pass.txt```;
3. Print for each line of the file pass.txt allfileds except 1. The fields in the lines are separated by colon: ```cut -d: -f2- pass.txt```;
4. Print first 11 lines from the file pass.txt: ```head 11 pass.txt```;
5. Print city.txt with alphabetical sorting of lines in the forward direction: ```sort city.txt```;
6. Print city.txt replacing 'a' with 'X', 'b' with 'Y', 'c' with '/': ```sed -e 's/a/X/g' -e 's/b/Y/g' -e 's/c/\//g' city.txt```;
7. Print from city.txt all strings containing 'austria', case insensitive: ```grep austria -i city.txt```;
7. Split city.txt into several files, 3 lines in each: ```split -l3 city.txt```;