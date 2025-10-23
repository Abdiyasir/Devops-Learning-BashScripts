# PATH Variable and Running Scripts from Anywhere
- By default, you can only run scripts from the directory they’re located in.
- To make a script accessible system-wide, you need to add it to a directory included in the `$PATH`.

## What Is `$PATH`?
- `$PATH` is an environment variable that stores a list of directories.
- When you type a command, the shell searches through these directories to find it.
- Current PATH can be viewed by: `echo $PATH`
- An example would be `/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/usr/sbin`

## Running a Script from Anywhere
- You can move a script to a directory already in your PATH:
- `sudo mv script.sh /usr/local/bin/`
- `sudo chmod +x /usr/local/bin/script.sh`
- This can now be run by typing `script.sh`

## Adding Custom Paths
- You can also add your own directory, for example `~/scripts`
- mkdir -p ~/scripts
- 
