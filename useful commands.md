<b>File & Directory Manipulation</b>

`ls`                            :     Lists directory contents

`cd [directory]`                :     Changes the current working directory

`pwd`                           :     Prints the current working directory path

`mkdir [directory_name]`        :     Creates a new directory
`mkdir -p`                      :     Creating nested directories for multi-stage simulations (mkdir -p project/run1/dos)
`touch [filename]`              :     Creates an empty file or updates a file's timestamp
`cp [source] [destination]`     :     Copies files or directories
`mv [source] [destination]`     :     Moves or renames files and directories
`rm [file/directory]`           :     Deletes files or directories (use with caution, especially with -r for directories)
`cat [filename]`                :     Concatenates and displays the contents of a file
`man [command name]`            :     Displays the manual page for a command
`ln -s`                         :     Linking large pseudopotential files to current directories, avoiding duplication


Searching and Analyzing Output Files

`rep [pattern] [filename]`      :     Essential for extracting data from huge output files   (grep "total energy" scf.out or grep -A 5 "TOTAL-FORCE" vasp.out [shows 5 lines after match])
`echo [text]`                   :     Displays a line of text to the terminal
`tail -f`                       :     Monitoring simulation progress in real-time (tail -f slurm.out or tail -f output.log)
`head / tail`                   :     Viewing the beginning or end of files (can be used to check the final optimized structure)
`less`                          :     Viewing large output files without loading them completely
`diff`                          :     Comparing two input or output files to find differences in parameters
`wc -l`                         :     Counting lines (can be used to check if an MD trajectory has the expected number of steps). 

Data Extraction & Text Processing

`awk`        :   Extracting specific columns, such as energy values or atomic coordinates  (awk '{print $1, $5}' fort.10)
sed        :   Searching and replacing strings (e.g., altering atomic positions, changing k-points, or swapping pseudopotentials without opening an editor, BE CAREFUL!) 
sort       :   Sorting files, useful for energy convergence checks
paste      :   Merging data from two files, such as joining energy and volume data

File Transfers & Archiving

rsync/scp  :   Securely transferring files between your local machine and a cluster (scp input.in user@hpc:~/job/)
tar -czvf/tar -xzvf: Compressing/decompressing folders, often used for transferring results




pwd                   :    Print Working Directory.
passwd                :    Changing password
chmod +x script.sh    :    Permissions change (to make an executable)
