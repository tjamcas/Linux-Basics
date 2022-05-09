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
### Manipulating .tar and .zip files
1. `tar` archive creation        
    Syntax: `tar [OPTIONS] tar-file-name source-path`       
    Example: `tar -cvf myfiles.tar Exercise\ Files/`        
    `-c`: create an archive; `-v`: verbose; `-a`: determine appropriate compression; `-f`: output to a file     
    To create a compressed file, you must use the appropriate file extension.       
    g-zip: `tar -cvf myfiles.tar.gz Exercise\ Files/`       
    b-zip: `tar -cvf myfiles.tar.bz2 Exercise\ Files/`      
2. `tar` archive extraction     
    Syntax: `tar -xf tar-file-name -C destination-path`        
    Example 1: `tar -xf myfiles.tar.bz2` extracts the files in the current working directory (no destination path was specified).     
    `-x`: extract       
    Example 2: `tar -xf myfiles.tar.gz -C unpack2` extracts the archive into the `./unpack2` directory      
    `-C`: change into directory for extracting      
3. `zip` zip-file creation      
    Syntax: `zip -r zip-file-name source-path`       
    Example: `zip -r exfiles.zip Exercise\ Files/`       
    `-r` recursively zip directory content      
4. `unzip` zip-file extraction        
    Syntax: `unzip zip-file-name -d destination-path`       
    Example: `unzip exfiles.zip -d unpack4` unzips the zip file to `./unpack4` folder        
