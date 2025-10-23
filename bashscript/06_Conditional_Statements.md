# Conditional Statements in Bash
- Conditional statements allow your script to make decisions and execute commands based on certain conditions.

## `if` Statement
- The most common structure is the `if` `then` `fi` block.
- Example:
```
num=10

if [ $num -gt 5 ]; then
  echo "The number is greater than 5."
fi
```
## `if` `else` Statement
- For two possible outcomes
```
if [ "$name" == "Yasir"]; then
echo "Welcome back!"
else
  echo "Access denied."
fi
```

## `if` `elif` `else` Statement
- For multiple conditions
```
if [ "$score" -ge 90 ]; then
  echo "Grade: A"
elif [ "$score" -ge 80 ]; then
  echo "Grade: B"
else
  echo "Grade: C or lower"
fi
```
## Common Test Expressions
| Type       | Test                | Meaning                   |
| ---------- | ------------------- | ------------------------- |
| **String** | `[ -z "$var" ]`     | True if variable is empty |
| **String** | `[ "$a" == "$b" ]`  | Strings are equal         |
| **Number** | `[ "$a" -eq "$b" ]` | Numbers are equal         |
| **Number** | `[ "$a" -gt "$b" ]` | a > b                     |
| **Number** | `[ "$a" -lt "$b" ]` | a < b                     |
| **File**   | `[ -f "$file" ]`    | File exists               |
| **File**   | `[ -d "$dir" ]`     | Directory exists          |
| **File**   | `[ -e "$path" ]`    | File or directory exists  |
