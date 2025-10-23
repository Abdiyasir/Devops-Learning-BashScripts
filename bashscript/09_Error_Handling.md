# Error Handling and Exit Codes in Bash
- Error handling is important for creating reliable scripts. In bash every command returns an exit code that tells whether it succeeded or failed.

## Exit Codes
- Exit code 0 means the command ran successfully.
- A non 0 exit code mean an error has occured.
- You can check the exit code of the last executed command using `$?`.
```
cp file.txt backup.txt
echo "Exit code: $?"
```
- If the script runs successfully it will output: `Exit code: 0`

## Exit Codes in Scripts
- Exit codes can be used in `if` statements to detect errors:
```
cp file.txt backup.txt

if [ $? -ne 0 ]; then
  echo "Copy failed!"
  exit 1
else
  echo "Copy successful."
fi
```
## Exit Scripting Options
| Script       | Meaning           | 
| ---------- | ------------------- |  
| set -e | Exit immediately if a command fails | 
| set -u | Exit if using an undefined variable | 
| set -x | Print each command before executing it | 
| set -eux | Combine all for safe debugging | 






