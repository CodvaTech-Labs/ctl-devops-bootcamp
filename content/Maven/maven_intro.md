+++
title = "Linux Basic Commands"
weight = 15
chapter = false
pre = "<b> 1.5 </b>"
+++

| Command             | Description                                       | Example(s)                                       |
|---------------------|---------------------------------------------------|--------------------------------------------------|
| ls                  | List directory contents                          | ls                                               |
| cd                  | Change directory                                  | cd /var/log                                      |
| pwd                 | Print working directory                           | pwd                                              |
| mkdir               | Create a directory                                | mkdir mydir                                      |
| rm                  | Remove files or directories                       | rm myfile.txt                                    |
| cp                  | Copy files and directories                        | cp file1.txt file2.txt                           |
| mv                  | Move or rename files and directories              | mv oldname.txt newname.txt                       |
| touch               | Create an empty file                              | touch myfile.txt                                 |
| cat                 | Concatenate and display file content              | cat myfile.txt                                   |
| grep                | Search for patterns in files                      | grep "pattern" myfile.txt                        |
| find                | Search for files and directories                  | find /home -name "file.txt"                      |
| chmod               | Change file permissions                           | chmod 644 myfile.txt                             |
| chown               | Change file owner and group                       | chown user:group myfile.txt                      |
| tar                 | Archive files into a tarball                      | tar -cvf archive.tar file1.txt file2.txt          |
| gzip                | Compress files using gzip                         | gzip myfile.txt                                  |
| unzip               | Extract files from a zip archive                  | unzip archive.zip                                |
| ssh                 | Securely connect to a remote server via SSH        | ssh username@remotehost                          |
| scp                 | Securely copy files between local and remote hosts | scp myfile.txt username@remotehost:/path/to/dest |
| systemctl           | Control system services                           | systemctl start apache                           |
| top                 | Display system resource usage                     | top                                              |
| ps                  | Display running processes                         | ps aux                                           |
| kill                | Terminate a process                               | kill PID                                         |
| df                  | Display disk space usage                          | df -h                                            |
| du                  | Estimate file and directory space usage            | du -sh mydir                                     |
| ifconfig (or ip)     | View and configure network interfaces             | ifconfig                                        |
| ping                | Send ICMP echo requests to a host                 | ping google.com                                  |
| wget                | Download files from the internet                  | wget https://example.com/file.txt                 |
| history             | View command history                              | history                                          |
| man                 | Display the manual page for a command             | man ls                                           |

Please note that these examples provide a basic understanding of each command. Each command has various options and additional use cases, which can be explored by referring to the command's manual page (e.g., `man ls` for detailed information on the `ls` command and its options).