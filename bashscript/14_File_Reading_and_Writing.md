# Reading and Writing Files in Bash
- Bash provides multiple ways to read from and write to files.
- This is useful for processing data, logs, or configuration files automatically.

 ## Reading Files
 - You can read a file line by line using a `while` loop.
```
#!/bin/bash

while read line; do
  echo "Line: $line"
done < myfile.txt
```
## Combining Reading and Writing
```
while read line; do
  echo "Processed: $line" >> newfile.txt
done < oldfile.txt
```
