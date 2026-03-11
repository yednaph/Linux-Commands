<b> `awk` </b>

Some examples:

To sum integers from a file or stdin, one integer per line
`printf '1\n2\n3\n' | awk '{ sum += $1} END {print sum}'`

To use a specific character as a separator to sum integers from a file
`printf '1:2:3' | awk -F ":" '{print $1+$2+$3}'`

To specify an output separator character
`printf '1 2 3' | awk 'BEGIN {OFS=":"}; {print $1,$2,$3}'`
