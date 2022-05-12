# Linux Command Lie Interface

## Introductory Linux Shell Commands

### Finding Help on Bash commands
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
### Output redirection
1. Redirecting stdout to a file     
    Syntax: `command >1 filename` or `command > filename`       
    Example: `ls > filelist.txt`        
2. Redirecting stderr to a file     
    Syntax: `command >2 filename`       
    Example: `cat bogus-file >2 errormsg.txt`        
3. Redirecting and appending stdout to a file       
    Syntax: `command >> filename`       
    Example `echo "appended text" >> filelist.txt`        
### Environment variables
1. Display all of the shell variables        
    Syntax: `env`       
2. Display path     
    Syntax: echo $PATH
3. Determining folder location of a command     
    Syntax: `which command-name`        
    Example: `which ls`     
4. Edit the shell profile / Add a folder to the PATH        
    Go to home directory - determine whether the bash profile exists:  `cd ~` followed by `ls -a` and lok for filename `.bash_profile`
    Edit the `.bash_profile` file: `vi ~/.bash_profile`     
    Add line: `PATH="$PATH:/some/other/path:/another/new/path"      
### Determining version of Linux
1. Find release file: `ls -l /etc/*release`     
2. Display release file: `cat /etc/lsb-release`         
    or, if there are multiple release files, to display them all: `cat /etc/*release`       
3. To  display Linux kernel version: `uname -a`       
### Determining system resources
1. Display available memory: `free -h`      
2. Display cpu information: `cat /proc/cpuinfo` or `lscpu`     
3. Display disk information: `df-h`     
4. Display disk used by file and folders information: `sudo du -hd1 /`      
5. Display hardware: `sudo lshw | less`     
6. Display network interface information: `ip a`        
### Installing and updating software with the `apt` package manager:
1. Search for software package in Linux distro repository      
    Syntax: `apt search sw-name`        
    Example: `apt search tree`      
2. Display information about a software package in the repository     
    Syntax: `apt show sw-name`        
    Example: `apt show tree`        
    Save the file and restart your terminal shell
3. Install a software package      
    Get latest packages in repository: `sudo apt update`        
    Install package from repository: `sudo apt install sw-name`, for example, `sudo apt install tree`       
4. Upgrade software packages
    Get latest packages in repository: `sudo apt update`        
    Uograde software packages: `sudo apt upgrade`       
