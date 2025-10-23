# Functions in Bash
- Functions let you put code into a small section that you can reuse whenever you need it in your script.

## Defining a Function
- A function can be defined in the following two ways:
```
function greet() {
  echo "Hello, $1!"
}
```
```
greet() {
  echo "Hello, $1!"
}
```
This function can be called by writing a name:
`greet "Yasir"`
- Results:
- `Hello, Yasir!`

## Function Parameters
```
add_numbers() {
  echo "Sum: $(( $1 + $2 ))"
}

add_numbers 5 10
```
- Result:
- `Sum: 15`

## Handling bad input
- This allows you to stop the function and send a non-zero status (error) back to the main script.
```
print_name() {
  if [ -z "$1" ]; then
    echo "Error: No name provided!"
    return 1
  fi
  echo "Name: $1"
}
```
