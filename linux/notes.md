Linux Commands

echo
Purpose: Outputs any text that we provide.

Example:
echo "Hello"

------------------------------------------------

whoami
Purpose: Finds out which user we're currently logged in as.

Example:
whoami

------------------------------------------------

ls
Purpose: Lists files and directories in the current directory.

Examples:
ls
ls -l
ls -la

------------------------------------------------

cd
Purpose: Changes the current working directory.

Examples:
cd Documents
cd ..
cd ~

------------------------------------------------

cat
Purpose: Displays the contents of a file in the terminal.

Example:
cat notes.txt

------------------------------------------------

pwd
Purpose: Prints the full path of the current working directory.

Example:
pwd

------------------------------------------------

find -name "*.txt"
Purpose: Finds every .txt file.

Example:
find . -name "*.txt"

------------------------------------------------

grep
Purpose: Searches the contents of a file for specific values.

Example:
grep "error" log.txt

------------------------------------------------

wc -l access.log
Purpose: Counts the number of entries (lines) in "access.log".

Example:
wc -l access.log

------------------------------------------------

grep "81.143.211.90" access.log
Purpose: Finds all entries containing the IP address "81.143.211.90" in "access.log".

Example:
grep "81.143.211.90" access.log

------------------------------------------------

grep -R
Purpose: Searches recursively through all files and subdirectories.

Example:
grep -R "PRETTY_NAME" /etc/

This command:
- Searches every file in the specified directory.
- Searches all subdirectories.
- Shows where "PRETTY_NAME" appears.

------------------------------------------------

du
Purpose: Displays the disk usage of files and directories.

Example:
du

------------------------------------------------

du -a
Purpose: Lists the disk usage of both files and directories.

Example:
du -a

------------------------------------------------

du -h
Purpose: Displays file and directory sizes in a human-readable format (B, KB, MB, GB).

Example:
du -h

------------------------------------------------

du -c
Purpose: Prints the total disk usage at the end of the output.

Example:
du -c

------------------------------------------------

du -d <number>
Purpose: Displays the disk usage up to the specified directory depth.

Example:
du -d 2

grep

Purpose:
Searches for a specific word or pattern inside a file.

Example:
grep "user" file.txt

------------------------------------------------

grep -R

Purpose:
Searches recursively through all files and subdirectories.

Example:
grep -R "PRETTY_NAME" /etc/

------------------------------------------------

grep -h

Purpose:
Hides the filename from the output when searching recursively.

Example:
grep -Rh "pattern" folder/

------------------------------------------------

grep -c

Purpose:
Displays only the number of times a pattern appears in a file.

Example:
grep -c "error" log.txt

------------------------------------------------

grep -i

Purpose:
Searches for a pattern while ignoring uppercase and lowercase letters.

Example:
grep -i "password" file.txt

------------------------------------------------

grep -l

Purpose:
Displays only the names of files that contain the specified pattern.

Example:
grep -l "password" *.txt

------------------------------------------------

grep -n

Purpose:
Displays the matching line along with its line number.

Example:
grep -n "password" file.txt

------------------------------------------------

grep -v

Purpose:
Displays all lines that do NOT contain the specified pattern.

Example:
grep -v "error" log.txt

------------------------------------------------

grep -E

Purpose:
Treats the search pattern as an Extended Regular Expression (ERE).

Example:
grep -E "user|admin" file.txt

Notes:
Useful for searching using regular expressions.

------------------------------------------------

grep -e

Purpose:
Searches for multiple patterns in a single command.

Example:
grep -e "user" -e "admin" file.txt

Notes:
Multiple `-e` flags can be used to search for multiple patterns.
Unlike `-E`, `-e` can be used multiple times in the same command.

------------------------------------------------

Lab Activity

Objective:
Practice using the `grep` command and its important flags.

Task:
Downloaded the practice file provided in the TryHackMe Linux Modules room and used `grep` to search for information.

Commands Used:
grep user grep.txt
grep password grep.txt
grep comment grep.txt

Findings:
User: bobthebuilder
Password: LinuxIsGawd
Comment: fs0ciety

Learning Outcome:
Learned how to use `grep` to search for specific patterns in files and understood how different flags make searching more efficient.

------------------------------------------------

du --time
Purpose: Displays the last modification timestamp along with the disk usage.

Example:
du --time
