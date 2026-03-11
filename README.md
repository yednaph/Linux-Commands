<b>File & Directory Manipulation</b>

`ls`                            :     Lists directory contents

`cd [directory]`                :     Changes the current working directory

`pwd`                           :     Prints the current working directory path

`mkdir [directory_name]`        :     Creates a new directory

`mkdir -p`                      :     Creating nested directories for multi-stage simulations (`mkdir -p folder/folder/band`)

`touch [filename]`              :     Creates an empty file or updates a file's timestamp

`cp [source] [destination]`     :     Copies files or directories

`mv [source] [destination]`     :     Moves or renames files and directories

`rm [file/directory]`           :     Deletes files or directories (<b>use with caution, especially with -r for directories</b>)

`cat [filename]`                :     Concatenates and displays the contents of a file

`man [command name]`            :     Displays the manual page for a command

`ln -s`                         :     Linking large pseudopotential files to current directories, avoiding duplication

<b>Searching and Analyzing Output Files</b>

`rep [pattern] [filename]` :     Essential for extracting data from huge output files   (`grep "total energy" file.out` or `grep -A 5 "TOTAL-FORCE" file.out` [shows 5 lines after match])

`echo [text]`    :     Displays a line of text to the terminal

`tail -f`        :     Monitoring simulation progress in real-time (`tail -f file.out` or `tail -f output.log`)

`head / tail`    :     Viewing the beginning or end of files (can be used to check the final optimized structure)

`less`           :     Viewing large output files without loading them completely

`diff`           :     Comparing two input or output files to find differences in parameters

`wc -l`          :     Counting lines (can be used to check if an MD trajectory has the expected number of steps)

<b>Data Extraction & Text Processing</b>

`awk`      :   Extracting specific columns, such as energy values or atomic coordinates  (awk '{print $1, $5}' filename)

`sed`      :   Searching and replacing strings (e.g., altering atomic positions, changing k-points, or swapping pseudopotentials without opening an editor, <b>BE CAREFUL!</b>) 

`sort`     :   Sorting files, useful for energy convergence checks

`paste`    :   Merging data from two files, such as joining energy and volume data

<b>File Transfers & Archiving</b>

`rsync`/`scp`  :   Securely transferring files between your local machine and a cluster (`scp input.in user@machineaddress:~/job/`)

`tar -czvf`/`tar -xzvf`: Compressing/decompressing folders, often used for transferring results


<b>some other im[ortant commands </b>

`pwd`     :  Print Working Directory

`passwd`  :  Changing password

`chmod +x filename` :  Permissions change (to make an executable)
