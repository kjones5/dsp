# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

#### Metis' List of 8

> > * **Show current working directory path:** `pwd` to print working directory
> > * **Creating a directory:** `mkdir moose` to make directory called moose
> > * **Deleting a directory:** `rm -r` to remove, where `-r` option means 'recursive' and will delete the directory *and* its child directories. Careful: this cannot be undone!!
> > * **Creating a file using** `touch` **command:** `touch filename.txt` Note: Can add filepath before it to create it someplace other than the working directory
> > * **Deleting a file:** `rm` to remove, e.g., `rm waterboy.txt` will delete that file. Careful: this cannot be undone!!
> > * **Renaming a file:** `mv` command (usually to move files) also renames them. To rename a file, use `mv` with the old file as the first argument and the new file as the second argument. By moving `batman.txt` into `spiderman.txt`, we rename the file as `spiderman.txt`
> > * **Listing hidden files:** `ls -a` will list all files, including hidden ones
> > * **Copying a file from one directory to another:** `cp origin/file1.txt origin/file2.txt destination_dir/` will create a copy of files 1 and 2 in the destination directory. Process: to copy file(s) into a directory, use `cp` with (a list of) source file(s) as the first argument(s) and the destination directory as the last argument.

#### My Chosen Commands

> > * **Moving a file:** `mv` command works mostly like `cp` but actually moves the files to a new directory instead of making a copy there. Again, to move multiple files into a directory, use `mv` with a list of source files as the first arguments, and the destination directory as the last argument. See above for using `mv` to rename.
> > * **Wildcard:** Special characters to select groups of files. `*` selects all files in the working directory. `m*.txt` selects all files in the working directory starting with "m" and ending with ".txt"
> > * **Viewing a file:** The `cat` command outputs the contents of a file to the terminal
> > * **Redirection:** Use `>` to redirect the standard output to a file, e.g., `echo "Hello" > hello.txt` to write text to new file or `cat oceans.txt > continents.txt` to read text of oceans.txt into the file continents.txt, which will overwrite the original contents of continents.txt. Related: `<` takes the standard input from the file on the right and inputs it into the program on the left.
> > * **Appending a file:** `>>` takes the standard output of the command on the left and appends it to the file on the right, e.g., `cat glaciers.txt >> rivers.txt`
> > * **Chaining commands:** Use a pipe `|` to take the standard output of the command on the left and pipe it as standard input to the command on the right, like "command to command" redirection. Ex: for `cat volcanoes.txt | wc | cat > islands.txt`, the standard output of `cat volcanoes.txt` is "piped" to the `wc` command. The standard output of `wc` is then "piped" to `cat`. Finally, the standard output of `cat` is redirected to `islands.txt`. 
> > * **Sorting:** `sort` takes the standard input and orders it alphabetically for the standard output
> > * **Duplicate Lines:** `uniq` stands for "unique" and filters out adjacent, duplicate lines in a file, so it misses non-adjacent duplicates. A more effective way to call `uniq` is to call `sort` to alphabetize a file (thus making all duplicates adjacent) and "pipe" the standard output to `uniq`, e.g., `sort deserts.txt | uniq`
> > * **Searching within files:** `grep` (aka "global regular expression print") does case-sensitive search of files for lines that match a pattern and returns the results. Use `-i` to make search case insensitive. Ex: `grep -i Mount mountains.txt` 
> > * **Searching within workspace:** `grep -R` searches all files in a directory and outputs filenames and lines containing matched results. `-R` stands for "recursive". `-l` stands for "files with matches." Ex: `grep -R Arctic /home/ccuser/workspace/geography` searches the geography directory for the string "Arctic" and outputs filenames and lines with matched results.
> > * **Find and replace:** `sed` stands for "stream editor." It searches for a text pattern, modifies it, and outputs it.

---

### Q2.  List Files in Unix   

What do the following commands do:   

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

> > We need `xargs` because some tools like `echo`, `rm`, `mkdir`, and `find` are not set up to accept standard input as arguments. Using `xargs` lets us pipe standard input to these commands, which will then run once for each argument (separated by a space).
> >  
> > *Example:* Use the `find`command to search for files/directories and then use `xargs` to operate on the results, e.g., by removing files, changing ownership, or moving files. Example modified from [this website](https://shapeshed.com/unix-xargs/).  
> >  `find "*.txt" | xargs -p rm` will find all .txt files and remove them after prompting me (hence `-p`)

 

