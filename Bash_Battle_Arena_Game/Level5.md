# Level 5: The Boss Battle - Combining Basics
1. Creates a directory names 'Battlefield'
2. Inside Battlefield, create files named knight.txt, sorcerer.txt, and rogue.txt.
3. Check if knight.txt exists; if it does, move it to a new directory called Archive.
4. List the contents of both Battlefield and Archive.
```
mkdir -p Battlefield
```
```
touch Battlefield/knight.txt Battlefield/sorcerer.txt Battlefield/rogue.txt
```
```
if [ -z "$1" ]
then
echo "Please provide a directory"

elif [ ! -d "$1" ]
then
echo "Directory does not exist"


else

mkdir -p Archive

if [ -f "Battlefield/knight.txt" ]
then
mv Battlefield/knight.txt Archive/
echo "Knight.txt has been moved to Archive/"

else

echo "Knight.txt does not exist"

fi

fi
```
```
echo "Battlefield Contents"
ls Battlefield

echo "Archive Contents"
ls Archive
```



