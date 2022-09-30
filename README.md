# 201934612_-_lectue_note_5.md
summarize about shell command 2


## Shell commands
### languages  
#### I/O redirection
* **>**: using after a command to create and save the ouput in a file.
* **cat**: displays the content of a text file. 
* **>>**: If file exitsts, appending output to an extising file
          : If file doesn't exist, creating and writing to a new file.
* **<**: redirect input from a file. (can mix with ">".)

#### Pipelines "|"
 - It feeds output of previous command to input of next command.
 - It shows in another screen.
 - If you want to exit the screen, press "q" key.

#### Expansion
**using**: special characters expand its meaning when give to shell commands.
**example**
1. echo (text): print out the (text)
2. echo *: expanded to contain information about files in the current directory
3. echo ~: expanded current user's home directory

#### Backslash '\\'  
: Ignoring line change in command, to enter a long command in multiple lines.

#### Permissions
: Files and directories have a permission assigned differently to owner/group/others.
* **necessity**: Because Linux is a multi-user system (to protect directory)
* **rwx**
  : read, write, execute (print 'rwx rwx rwx')
  : "chmod" changes permissions
  : formation example) chmod 600 flename (6: rw- for owner, 0: --- for group, 0: --- for others)
      - 777 (=111 111 111)(rwxrwxrwx): no restrictions on permissions.  
      - 755 (=111 101 101)(rwxr-xr-x): the file's owner may read, write, and execute the file. All others may read and execute the file(no write).  
      - 700 (=111 000 000)(rwx------): the file's owner may read, write, and execute the file. Nobody else has any rights.  
                                     : this setting is useful for programs that only the owner may use and must be kept private from others.  
      - 666 (=110 110 110)(rw-rw-rw-): all users may read and write the file. (no execute)  
      - 644 (=110 100 100)(rw-r--r--): the owner may read and write a file, while all others may only read the file.  
      - 600 (=110 000 000)(rw-------): the owner may read and write a file. All others have no rights.  

#### Superuser
 - A superuser has all system administation authority.
 - Some commands need superuser's privilleges.
 - Put "sudo" before the command if you are a superuser. (but not recommending)
 - If you get out of a superuser sessions, type "exit"

#### Text Editors
: in Linus, you can choose CLI-based or GUI-based text editors.
 1. CLI-based
  - vi, vim
    : vi is infamous for its obuse user interface. (vi; powerful, lightweight, fast)
    : vim is a remarkable editor.
  - Emacs: It contains every feature ever conceived of for a text editor.
  - nano
    : It tis a free clone of the text editor supplied with the pine email program.
    : It is very easy to use, but is very short on features compared to vim and emacs
    : It is recommended for first-time users who need a command line editor.
 2. GUI-based
  - gedit
    : It is the editor supplied with the GNOME desktop environment. 
    : It is easy to use and contains enough features to begginers)
  - kwrite
    : It is the "advanced editor" supplied with KDE.
    : It has syntax highlighting, a helpful feature for programmers and script wrtiers.
  
  #### Shell script
  **script**: It automatically executes the pre-written ones sequentially.
  **way** 
   1. Open the text editor of the GUI you are using and write the script.
   2. ex. nano myscript.sh
      - Write the file name after the CLI, nano.
      - If file name exists, you can revise the contents of the file.
      - If file name doesn't exist, you can enter the contents of the file.
                            
 #### History
 - Type "history" to see previous command history or command history that save it to a text file.
 
