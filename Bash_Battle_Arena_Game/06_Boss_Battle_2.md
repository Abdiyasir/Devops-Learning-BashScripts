# Boss Battle 2 - Intermediate Scripting

1. Creates a directory called Arena_Boss.
2. Creates 5 text files inside the directory, named file1.txt to file5.txt.
3. Generates a random number of lines (between 10 and 20) in each file.
4. Sorts these files by their size and displays the list.
5. Checks if any of the files contain the word 'Victory', and if found, moves the file to a directory called Victory_Archive.
```
touch script.sh
chmod +x script.sh
mkdir -p Arena_Boss
cd Arena_Boss
```
```
touch file1.txt file2.txt file3.txt file4.txt file5.txt
```
```
if [ -z "$1" ]
then
echo "Please provide a directory"

elif [ ! -d "$1" ]
then
echo "Directory does not exist"


else



for file in "$1"/*.txt

do

random_num=$((RANDOM % 11 + 10))
seq "$random_num" | shuf >"$file"
echo "Generated $random_num random lines in $file"

done

fi
```
```
if [ -z "$1" ]
then
echo "Please provide a directory"

elif [ ! -d "$1" ]
then
echo "Directory does not exist"


else


echo "Files sorted by size : "

find  "$1" -type f -exec  ls -lh {} + | sort -h -k 5,5 | awk '{print $9, $5}'

fi
```
```
mkdir -p Victory_Archive

if [ -z "$1" ]
then
echo "Please provide a directory"

elif [ ! -d "$1" ]
then
echo "Directory does not exist"


else

find "$1" -type f -name "*.txt" -exec grep -l "Victory" {} \; -exec mv

echo "Move complete"

fi
```
