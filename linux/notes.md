
echo - Output any text that we provide
whoami - 
Find out what user we're currently logged in as
ls - Lists files and directories in the current directory
cd - Changes the current working directory
cat -Display the contents of a file in the terminal
pwd - prints the full path of the current working directory
find -name *.txt -able to find every .txt file 
grep - allows us to search the contents of file for specific values.
wc -l access.log -  to count the number of entries in "access.log"
 grep "81.143.211.90" access.log - to find any entries with the IP address of "81.143.211.90" in "access.log"
grep -R - can tell grep to search recursively through all files and subdirectories. eg: grep -R "PRETTY_NAME" /etc/
This will:
• Search every file in the current directory
• Search all subdirectories
• Show where the PRETTY_NAME appears