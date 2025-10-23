# File Paths in Bash
- Paths tell the system where files and directories are located

## Absolute vs Relative Paths
- Absolute path: Starts from the root directory `/` and points to a specific location in the file system.
- Relative path: Starts from your current working directory

- Relative Path Directory Example:
`cd Projects`
`ls Arena/*.txt`

- Absolute Path Directory:
- `cd /home/yasir/Projects`
- `ls /home/abdi/Arena/*.txt`

## Checking Paths Exist

path="Arena/game.sh"
```
if [ -e "$path" ]; then
  echo "Path exists: $path"
else
  echo "Path not found."
fi
```
