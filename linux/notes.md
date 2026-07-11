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
