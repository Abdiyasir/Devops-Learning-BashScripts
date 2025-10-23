#  Running Bash Scripts
- There are two main ways to run a Bash script.

## Direct Execution
- You can run a script directly after making it executable:
- `chmod +x script.sh`
- `./script.sh`
- The first command (chmod +x) gives the file execute permission, and ./ tells the shell to run the script located in the current directory.

## Using the Bash Interpreter
- Alternatively, you can run the script using the Bash interpreter directly once the script has been made:
`bash script.sh`
- This method doesn’t require the file to have execute permissions — it simply runs the script through Bash.
- 
