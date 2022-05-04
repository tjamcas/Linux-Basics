### Finding Help on Linux Bash commands
1. `man`    
    Syntax: `man command-name`   
    Example: `man ls`
2. `help` as an option to a command   
    Syntax: `command-name --help`   
    Example: `ls --help`    
    Note: the help option may not be available on all commands
3. `help` as a standalone command   
    Syntax: `help`    
    Note: this provides a list of shell commands - for example `ls` will not be included
4. `apropos`    
    Syntax: `apropos "search string"`   
    Example: `apropos "list directory contents"` will return several commands including `ls` and `dir`
    Note: `apropos` searches command descriptions for text that matches the search string and returns the command name(s)
### Navigating files and directories
1. `mkdir`    
    Syntax: `mkdir directory-name`    
    Note: Makes directory
2. `rmdir`    
    Syntax: `rmdir directory-name`    
    Note: Removes directory
3. `cp`, `mv`, `rm`   
    Syntax: `cp [OPTION] SOURCE DEST`   
    Syntax: `mv [OPTION] SOURCE DEST`   
    Syntax: `rm [OPTION] FILE`   
    Note: SOURCE and DEST can indicate a file or directory name
4. `find`
    Syntax: `find path-name [option]`   
    Example: `find ./markdown -name "*.md`
### Super-user or Root access
1. `sudo`   
    Syntax: `sudo command-string`   
    Example: `sudo ls /root`
### Changing file permissions
1. `chmod`   
    Syntax: `chmod octal-notation filename`   
    Example:  `chmod 744 myfile.md`   
    Syntax: `chmod symbolic-notation filename`   
    Example:  `chmod u-wx myfile.md`   
### Viewing and editing text files
1. View text files with: `cat`, `head`, `tail`, and `less`
2. Search for text in files with: `grep`
3. Manipulate text with `awk`, `sed`, and `sort`
4. Text editors: `vi`, `nano`
