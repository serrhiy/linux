1. ```ldd``` - print shared object dependencies:
  a. ```ldd <filename>```;
2. ```ldconfig``` - configure dynamic linker run-time bindings:
  a. ```ldconfig -p``` - print  the  lists of directories and candidate libraries stored in the current cache;
  b. ```ldconfig``` - update cache.

Managing packages in Debian

1. ```dpkg``` - debian package:
  a. ```dpkg -s <package>``` - get status;
  b. ```dpkg -l``` - get data about all packages
  c. ```dpkg -L <package>``` - get all files related to package;
  d. ```sudo dpck -r <package>``` - deleting;
  e. ```sudo dpck -P <package>``` - deleting with configuration;
  f. ```sudo dpck-reconfigure <package>```;  
2. installing: 
  a. ```apt-get download zsh``` - instaqll .deb file;
  b. ```sudo dpkg -i <zsh>.deb``` - will be an error because of dependency problem;
  c. ```apt-get download zsh-common``` - install dependency;
  d. ```sudo dpkg -i <zsh-common>.deb``` - install it;
  e. ```sudo dpkg -i <zsh>.deb``` - will be installed without error;
3. ```apt``` - install packages:
  a. ```apt update``` - update list of packages;
  b. ```apt upgrade``` - update packages;
  c. ```apt install <package>``` - install package;
  d. ```apt purge <package>``` - delete package whith configuration;
  c. ```apt autoremove``` - remove extra packages;
  d. ```apr depends <package>``` - see dependencies;
