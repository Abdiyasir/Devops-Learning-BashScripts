# Level 3: Conditional Statements
- Write a script that checks if a file named hero.txt exists in the Arena_Boss directory. If it does, print Hero found!; otherwise, print Hero missing!.
```
- if [ -z "$1" ]
then
echo "Please provide a directory"

elif [ ! -d "$1" ]
then
echo "Directory does not exist"


else


if [ -f "Arena_Boss/hero.txt" ]
then

echo "Hero Found!"

else

echo "Hero Missing"

fi

fi
```





