## Linux Commands

| ID  | Description                                                                                                                                     | Command                                                                                                                                                                                                                        |
|:---:|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  1  | To open a directory                                                                                                                             | ```cd "Directory name"```                                                                                                                                                                                                      |
|  2  | How to list files inside a directory                                                                                                            | ```ls -ltr``` (After CD to a directory, using this cmd we list all files inside a dir)                                                                                                                                         |
|  3  | How to check which directory we are inside                                                                                                      | ```pwd``` (By running this cmd, it will print which dir we are currently on)                                                                                                                                                   |
|  4  | Search for a specific directory                                                                                                                 | ```find "path" -name "File name"```                                                                                                                                                                                            |
|  5  | To change directory/file permissions R(Read)-4, W(Write)-2, X(Execute)-1                                                                        | ```chmod 777(Change the number according to the permissions) "File name"```                                                                                                                                                    |
|  6  | How to change user password                                                                                                                     | ```passwd or passwd "userid"```                                                                                                                                                                                                |
|  7  | How to copy directory/files from one dir to another                                                                                             | ```cp "Source file path including file name" "destination file path where we are copying to including filename"```                                                                                                             |
|  8  | How to move directory/files from one dir to another                                                                                             | ```mv "Source file path including file name" "destination file path where we are copying to including filename"```                                                                                                             |
|  9  | How to create a file                                                                                                                            | ```touch "filename"```                                                                                                                                                                                                         |
| 10  | How to create a directory                                                                                                                       | ```mkdir "Directory name"```                                                                                                                                                                                                   |
| 11  | How to create a file and open in a editor                                                                                                       | ```vi "filename"```                                                                                                                                                                                                            |
| 12  | How to use wild cards like ```*,?,{},[]```                                                                                                      | Eg: ```ls tex*``` (To list all files which starts with tex), ```ls te?t``` (To list all files which starts with tex) ```mkdir/touch text{1..10}``` to create multiple files at once ```ls *[ex]*``` list all files contains ex |
| 13  | Soft link will lost linkage of the file gets deleted and Hard link will stii be intact                                                          | ```ln```(Hard Link),```ln -s```(Soft Link)                                                                                                                                                                                     |
| 14  | How to change a file or directory ownership for Owner/Group                                                                                     | ```chown "name of the user we want to change" "file name"```,```chgrp "name of the group we want to change" "file name"``` ```chown "username":"groupname" filename``` (To change the user and group name at the same time)    |
| 15  | Help Commands                                                                                                                                   | ```whatis cd,man cd,ls --help```                                                                                                                                                                                               |
| 16  | To know who is the user                                                                                                                         | ```whoami```                                                                                                                                                                                                                   |
| 17  | To know the name of the host                                                                                                                    | ```hostname```                                                                                                                                                                                                                 |
| 18  | How to delete directory and files                                                                                                               | ```rmdir```(To delete dir) ```rm``` (To delete files)                                                                                                                                                                          |
| 19  | How to display the date and time                                                                                                                | ```date```                                                                                                                                                                                                                     |
| 20  | Clear the terminal screen (When your entered too many commands and want to keep it clean)                                                       | ```clear```                                                                                                                                                                                                                    |
| 21  | How to write into a file(we have 3 ways)                                                                                                        | ```1) VI "filename" Editor``` ```2) use >> to output into a file``` ```3) echo > or >>``` Eg: echo "Hi! this is Ganesh" >> "filename" and > (Single is used for the first time only)                                           |
| 22  | Input and Output Redirects. There are 3 types of standards--> stdin File Descriptor # 0, stdout File Descriptor # 1, stderr File Descriptor # 2 | "N/A"                                                                                                                                                                                                                          |
| 23  | To check hidden files inside a directory                                                                                                        | ```ls -la```                                                                                                                                                                                                                   |
| 24  | Input data from another file                                                                                                                    | ```cat < "filename"```                                                                                                                                                                                                         |
| 25  | How to send error messages to a file                                                                                                            | ```ls -ltr /root 2> "Filename"``` (When we run this command in user account, it will throw error and that we want to send it to an error file)                                                                                 |
| 26  | stdout--> Command to store and view the output of something                                                                                     | ```echo "ganesh" "pipe" tee "filename"``` (to overwrite on the same line) and ```echo "ganesh" "pipe" tee -a "filename" ```(To enter in a new line)                                                                            |
| 27  | How to check how many words are there in a file                                                                                                 | ```wc -c "filename"```                                                                                                                                                                                                         |
| 28  | If a directory has 100 files ans want to see them one page at a time                                                                            | ```ls -ltr "pipe" less``` (Space bar to go step by step, b to go 1 page back, g to go to the first page, G to go to end page, and Q to quit)                                                                                   |
| 29  | To get last bottom few lines from a file                                                                                                        | ```tail -5 "filename"``` to display bottom last 5 lines in a file                                                                                                                                                              |
| 30  | To get first top few lines from a file                                                                                                          | ```head -5 "filename"``` to display top first 5 lines in a file                                                                                                                                                                |


### ACL:

* Access control list is an extra layer of permissions for files/dir systems.
* We can assign these roles to a specific user/group.
* Commands to assign ACL commands
```
* setfacl -m(modify) u:user(replace g:group for group):rwx "path of the file" (To set file permissions)
* setfacl -dm "entry" "path of the dir" (To allow all files or directories to inherit ACL entries form the directory it is within)
* setfacl -x u:user "path" (To remove a specific entry)
* setfacl -b "path of the file" (To remove all users)
NOTE: 
1) As we assign the ACL permissions to a file/directories it adds + sign at the end of the permission when we run ls -ltr.
2) Setting W Permission with ACL does not allow to remove a file. 
* getfacl (To get existing file permissions)
```
### Text Processors Commands <u>(Powerful Commands)</u>:

* <u>[cut](cat_command.md)</u>
* <u>[awk](awk_command.md)</u>
* <u>[grep/egrep](grep_egrep_command.md)
* sort/uniq
* wc
* Compare files diff/cmp
* compress and uncompress (tar,gzip,gunzip)
* Truncate file size (truncate)
* Combining and splitting files