# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * **Show current working directory path:** `pwd` to print working directory
> > * **Creating a directory:** `mkdir moose` to make directory called moose
> > * **Deleting a directory:** `rm -r` to remove, where `-r` option means 'recursive' and will delete the directory *and* its child directories. Careful: this cannot be undone!!
> > * **Creating a file using** `touch` **command:** `touch filename.txt` Note: Can add filepath before it to create it someplace other than the working directory
> > * **Deleting a file:** `rm` to remove, e.g., `rm waterboy.txt` will delete that file. Careful: this cannot be undone!!
> > * **Renaming a file:** `mv` command (usually to move files) also renames them. To rename a file, use `mv` with the old file as the first argument and the new file as the second argument. By moving `batman.txt` into `spiderman.txt`, we rename the file as `spiderman.txt`
> > * **Listing hidden files:** `ls -a` will list all files, including hidden ones
> > * **Copying a file from one directory to another:** `cp origin/file1.txt origin/file2.txt destination_dir/` will create a copy of files 1 and 2 in the destination directory. Process: to copy file(s) into a directory, use `cp` with (a list of) source file(s) as the first argument(s) and the destination directory as the last argument.
> > * **Moving a file:** `mv` command works mostly like `cp` but actually moves the files to a new directory instead of making a copy there. Again, to move multiple files into a directory, use `mv` with a list of source files as the first arguments, and the destination directory as the last argument. See above for using `mv` to rename.
> > * **Wildcard:** Special characters to select groups of files. `*` selects all files in the working directory. `m*.txt` selects all files in the working directory starting with "m" and ending with ".txt"

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > Command | What It Does
> > ------- | ------------
> > `ls` | List contents
> > `ls -a` | List all contents, including hidden files and directories starting with '.'
> > `ls -l` | List contents in long format
> > `ls -lh`  | List contents in long format (`-l`) with readable file size (`-h`), e.g., K or B
> > `ls -lah` | List all (`-a`) contents in long format (`-l`) with readable file size (`-h`)
> > `ls -t`| List in order by the time they were last modified
> > `ls -Glp` | List contents in long format (`-l`) with directories marked with / (`-p`) and in color (`-G`)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > Command | What It Does
> > ------- | ------------
> > `ls -r` | Displays files in reverse order
> > `ls -1` | Displays each entry on a line
> > `ls -m` | Displays the names as a comma-separated list
> > `ls -g` | Displays the long format listing, but exclude the owner name
> > `ls -x` | Displays files as rows across the screen

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > REPLACE THIS TEXT WITH YOUR RESPONSE

 

