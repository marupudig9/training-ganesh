<h5>Awk is a utility/language designed for data extraction. Most of the time it is used to extract fields from a file or from a output.</h5>

Commands:

1) awk '{print $1}' "file_name" - Prints the first column from the file
2) ls -ltra | awk '{print $1 $3}' - to print the first and third columns from the output of ls.
3) ls -ltra | awk '{print $NF}' - to print the last column from the output of ls, when we dont know how many columns we have in a file.
4) awk '/ganesh/ {print}' "file_name" - To search for specific pattern in a file.
5) awk -F: '{print $1}' "file_name" - It will print only first field of the file from each column.
6) echo "hello ganesh" | awk '{$2="harika"; print $0}' - To replace ganesh with harika and prints the output
7) awk 'length($0) >15' "file_name" - This command prints the lines which has more characters.
8) ls -ltr | awk '{if($9 == "ganesh") print $0;}' - To print that specific directory.
9) ls -ltra | awk '{print NF}' - To print how many rows have for each cloumn.

