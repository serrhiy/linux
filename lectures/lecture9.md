File system hierarchy standard:
  /bin - basic executable files(for system apps, /usr/bin/ for apss installed after system installation);
  /dev - basic devices;
  /etc - configuration;
  /lib - libs for apps from /bin and /sbin;
  /sbin - system executable files(for admins);
  /root - home directory for root user;
  /usr(unix system resources) - has a copy of a root file system. If exists apps that are not critical for a system, they should be installed here(/usr/bin);
  /var - variable files, log files;
  /home - has other users home directory; 
  /media - mounting points for portable media;
  /mnt - temporarily mounted files;
  /opt - optianal packets for apps;
  /srv - data for public server services;
  /tmp - temp files;
  /proc - virtual file system kernel and process status;
  /boot - system bootloader files;
1. ```type``` - check whether the command is system or built-in a bash;
2. ```which``` - shows the full path of (shell) commands.
3. ```whereis``` - locate the binary, source, and manual page files for a command;
4. ```locate``` - find files by name, quickly;
5. ```tar``` - an archiving utility:
  a. ```sudo tar -cvf etc.tar /etc``` - c - create, f - file, v - verbose;
  b. ```sudo tar -cvzf etc.tar.gz /etc``` - use gnu zip(better);
  c. ```tar --wildcards -tf etc.tar "*conf"``` - find files in tar;
6. ```gzip``` - compress files:
  a. ```gzip <filename>```;
7.  ```gunzip``` - expand files;
8. ```bzip2``` - a block-sorting file compressor:
  a. ```bzip2 <filename>```;
9. ```bunzip2``` - unzip bzip2;
10. ```xz``` -  compress .xz and .lzma files:
  ```xz <filename>```;
11. ```unxz``` - decompress .xz and .lzma filesl;
12. ```dd``` - convert and copy a file(disk dump):
  a. ```sudo dd if=/dev/sda of=mbr.bin bs=512 count=1``` if/of - input/output file, bs - block size, count - count of blocls;