#  Command-Line Arguments in Bash
- Command-line arguments allow you to pass data into a script when it runs.
- This makes scripts dynamic and reusable for different inputs.

## Argument Symbols
| Symbol | Meaning |
| ------- | -------- |
| `$0` | Script name |
| `$1`, `$2` | First and second arguments |
| `$#` | Number of arguments passed |
| `$@` | All arguments (treated separately) |
| `$*` | All arguments (treated as one string) |

## Example Script: script.sh
- `echo "Script name: $0"`
- `echo "First argument: $1"`
- `echo "Second argument: $2"`
- `echo "Total number of arguments: $#"`
- Then run:
- `bash script.sh hello world`
- Result:
- `Script name: script.sh`
- `First argument: hello`
- `Second argument: world`
- `Total number of arguments: 2`

## Looping Arguments
- $@ allows you to loop through all arguments

```
for arg in "$@"
do
  echo "Argument: $arg"
done
```
