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

String Manipulation (String Operations)

Purpose:
String manipulation is the process of modifying, extracting, filtering, replacing, formatting, or processing text in Linux.

Used By:
- SOC Analysts
- Penetration Testers
- System Administrators
- CTF Players
- Bash Scripting

Notes:
These commands are commonly used to process and analyze large log files efficiently.

------------------------------------------------

tr

Purpose:
Translates or deletes characters from the input.

Example:
echo "cyberforge" | tr 'a-z' 'A-Z'

Output:
CYBERFORGE

------------------------------------------------

tr

Purpose:
Replaces spaces with hyphens.

Example:
echo "Cyber Forge" | tr ' ' '-'

Output:
Cyber-Forge

------------------------------------------------

tr -d

Purpose:
Deletes specified characters from the input.

Example:
echo "abc123xyz" | tr -d '0-9'

Output:
abcxyz

------------------------------------------------

awk

Purpose:
Processes and extracts data from text based on fields (columns).

Example:
echo "Anjali SOC 20" | awk '{print $1}'

Output:
Anjali

------------------------------------------------

awk

Purpose:
Prints the second field.

Example:
echo "Anjali SOC 20" | awk '{print $2}'

Output:
SOC

------------------------------------------------

awk

Purpose:
Prints multiple fields.

Example:
echo "Anjali SOC Analyst" | awk '{print $1,$3}'

Output:
Anjali Analyst

------------------------------------------------

awk '{print}' file.txt

Purpose:
Prints the contents of a file.

Example:
awk '{print}' file.txt

------------------------------------------------

awk '/ctf/' file.txt

Purpose:
Prints only the lines containing a specific pattern.

Example:
awk '/ctf/' file.txt

------------------------------------------------

awk '{print NR,$0}' file.txt

Purpose:
Prints each line along with its line number.

Example:
awk '{print NR,$0}' file.txt

------------------------------------------------

AWK Variables

$1
Meaning:
First field.

------------------------------------------------

$2
Meaning:
Second field.

------------------------------------------------

$3
Meaning:
Third field.

------------------------------------------------

$0
Meaning:
Represents the entire line.

------------------------------------------------

NR

Meaning:
Represents the current line number.

------------------------------------------------

sort

Purpose:
Sorts lines of text alphabetically or numerically.

Example:
sort file.txt

------------------------------------------------

uniq

Purpose:
Removes or displays duplicate lines from sorted data.

Example:
uniq file.txt
------------------------------------------------

sed (Stream Editor)

Purpose:
sed is a command-line tool used to process and edit text streams without opening a text editor.

Common Uses:
- Find and replace text
- Search for patterns
- Delete lines
- Insert or modify text
- Filter output
- Perform batch text editing

------------------------------------------------

sed 's/Linux/Kali/' file.txt

Purpose:
Replaces the first occurrence of "Linux" with "Kali" on each line.

Example:
sed 's/Linux/Kali/' file.txt

------------------------------------------------

sed 's/cat/dog/g' file.txt

Purpose:
Replaces every occurrence of "cat" with "dog" on each line.

Example:
sed 's/cat/dog/g' file.txt

------------------------------------------------

sed 's/linux/Kali/gi' file.txt

Purpose:
Replaces all occurrences while ignoring uppercase and lowercase differences.

Example:
sed 's/linux/Kali/gi' file.txt

------------------------------------------------

sed -n '/error/p' logfile.txt

Purpose:
Displays only the lines containing the pattern.

Example:
sed -n '/error/p' logfile.txt

------------------------------------------------

sed '/error/d' logfile.txt

Purpose:
Deletes all lines containing the pattern.

Example:
sed '/error/d' logfile.txt

------------------------------------------------

sed '2d' file.txt

Purpose:
Deletes line 2.

Example:
sed '2d' file.txt

------------------------------------------------

sed '3,6d' file.txt

Purpose:
Deletes lines 3 through 6.

Example:
sed '3,6d' file.txt

------------------------------------------------

sed -n '5,10p' file.txt

Purpose:
Prints lines 5 to 10 only.

Example:
sed -n '5,10p' file.txt

------------------------------------------------

sed '1,3 s/john/JOHN/g' file.txt

Purpose:
Replaces every occurrence of "john" with "JOHN" only in lines 1 to 3.

Example:
sed '1,3 s/john/JOHN/g' file.txt

------------------------------------------------

sed 's/apple/orange/2' file.txt

Purpose:
Replaces the second occurrence of "apple" on each line.

Example:
sed 's/apple/orange/2' file.txt

------------------------------------------------

sed 's/apple/orange/2g' file.txt

Purpose:
Replaces from the second occurrence onward.

Example:
sed 's/apple/orange/2g' file.txt

------------------------------------------------

sed -e 's/Linux/Kali/' -e 's/SOC/Blue Team/' file.txt

Purpose:
Executes multiple sed commands in a single command.

Example:
sed -e 's/Linux/Kali/' -e 's/SOC/Blue Team/' file.txt

------------------------------------------------

sed -f script.sed file.txt

Purpose:
Reads and executes sed commands from a script file.

Example:
sed -f script.sed file.txt

------------------------------------------------

sed -E 's/[0-9]+/NUMBER/g' file.txt

Purpose:
Enables extended regular expressions.

Example:
sed -E 's/[0-9]+/NUMBER/g' file.txt

Output:
Replaces all numbers with the word NUMBER.

------------------------------------------------

echo "abc" | sed 'y/abc/xyz/'

Purpose:
Translates characters one by one.

Example:
echo "abc" | sed 'y/abc/xyz/'

Output:
xyz

------------------------------------------------

Important Flags

-e

Purpose:
Executes one or more sed commands.

Example:
sed -e 's/a/b/' file.txt

------------------------------------------------

-f

Purpose:
Reads commands from a script file.

Example:
sed -f script.sed file.txt

------------------------------------------------

-E

Purpose:
Enables extended regular expressions.

Example:
sed -E 's/[0-9]+/NUM/g'

------------------------------------------------

-n

Purpose:
Suppresses automatic output.

Notes:
Usually used together with the p command.

Example:
sed -n '/root/p' passwd.txt

------------------------------------------------

Common Cybersecurity Examples

Replace localhost with an IP address

Purpose:
Replace "localhost" with "127.0.0.1".

Example:
sed 's/localhost/127.0.0.1/g' config.txt

------------------------------------------------

Delete blank lines

Purpose:
Remove empty lines from a file.

Example:
sed '/^$/d' file.txt

------------------------------------------------

Show failed login attempts

Purpose:
Display only lines containing "Failed".

Example:
sed -n '/Failed/p' auth.log

------------------------------------------------

Remove comment lines

Purpose:
Delete lines starting with #.

Example:
sed '/^#/d' config.conf

------------------------------------------------

Show only IP addresses

Purpose:
Display only lines containing IPv4 addresses using regular expressions.

Example:
sed -n -E '/([0-9]{1,3}\.){3}[0-9]{1,3}/p' access.log

------------------------------------------------

Replace tabs with spaces

Purpose:
Replace every tab character with a space.

Example:
sed 's/\t/ /g' file.txt

sort

Purpose:
The sort command arranges lines of text in alphabetical or numerical order.

Syntax:
sort filename

Notes:
sort is commonly used before uniq because uniq only removes adjacent duplicate lines.

------------------------------------------------

sort -r

Purpose:
Sorts lines in reverse order.

Example:
sort -r file.txt

------------------------------------------------

sort -c

Purpose:
Checks whether a file is already sorted.

Example:
sort -c file.txt

------------------------------------------------

sort -u

Purpose:
Sorts the file and removes duplicate lines.

Example:
sort -u file.txt

------------------------------------------------

sort -o

Purpose:
Saves the sorted output to another file.

Example:
sort -o output.txt file.txt

------------------------------------------------

uniq

Purpose:
Removes or filters duplicate adjacent lines from a file or command output.

Syntax:
uniq filename

Notes:
uniq only removes adjacent duplicate lines. It is commonly used together with sort.

------------------------------------------------

sort file.txt | uniq

Purpose:
Sorts the file first, then removes duplicate lines.

Example:
sort file.txt | uniq

------------------------------------------------

uniq -c

Purpose:
Counts how many times each line appears.

Example:
sort hello.txt | uniq -c

Output:
2 hello future soc analyst..
1 you are doing great..you are stepping closer to your dream.

------------------------------------------------

uniq -d

Purpose:
Displays only duplicate lines.

Example:
sort hello.txt | uniq -d

Output:
hello future soc analyst..

------------------------------------------------

uniq -u

Purpose:
Displays only unique (non-duplicate) lines.

Example:
sort hello.txt | uniq -u

Output:
you are doing great..you are stepping closer to your dream.

------------------------------------------------

uniq -i

Purpose:
Ignores uppercase and lowercase differences while comparing lines.

Example:
sort hello.txt | uniq -i

Notes:
Lines such as "Hello" and "hello" are treated as the same.

------------------------------------------------

Lab Activity

Platform:
TryHackMe - Linux Modules

Objective:
Learn how to sort text and remove duplicate lines using the sort and uniq commands.

Commands Practiced:
sort
sort -r
sort -c
sort -u
sort -o
uniq
uniq -c
uniq -d
uniq -u
uniq -i

Learning Outcome:
Learned how to organize text files, identify duplicate entries, count repeated lines, display unique or duplicate lines, and combine sort with uniq to efficiently process log files.
