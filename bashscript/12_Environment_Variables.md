# Environment Variables
- Environment variables are values that affect the way processes and commands run on a Linux system.  
- They are used to store system-wide or session-specific information like user paths, home directories, and configuration details.
| Variable | Description |
|-----------|--------------|
| `$HOME` | User’s home directory |
| `$USER` | Current username |
| `$SHELL` | The shell being used |
| `$PATH` | Directories searched for executables |
| `$PWD` | Current working directory |

## Viewing Environment Variables
- You can view all active environment variables with: `printenv`
- You can display a specific one with: `echo $PATH`

## Creating Environment Variables
```
export MY_VAR="Hello World"
echo $MY_VAR
source ~/.bashrc  # Reloads and applies new changes instantly
```

## Examples

#!/bin/bash
```
echo "User: $USER"
echo "Home Directory: $HOME"
echo "Current Shell: $SHELL"
echo "Search Path: $PATH"
```


