# Loops in Bash
- Loops allow you to repeat commands or processes automatically.
- This is essential for automation, iteration, and handling multiple files or inputs.

## `for` Loop
- This is used to iterate through a sequence of items:
```
for i in {1..5}; do
  echo "Count: $i"
done
```
- Result:
```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

## Looping over files
- This allows you to loop through and output files in a directory:
```
for file in *.txt; do
  echo "Processing $file"
done
```

## `While` loop
- This will repeat as long as the condition is true.
```
count=1

while [ $count -le 5 ]; do
  echo "Count: $count"
  ((count++))
done
```

## Control Statements using `break` and `continue`
- This allows you to exit the loop immediately.
```
for i in {1..10}; do
  if [ $i -eq 5 ]; then
    break
  fi
  echo "Number: $i"
done
```
- Result:
```
Number: 1
Number: 2
Number: 3
Number: 4
```

```
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo "Number: $i"
done
```
- Result:
```
Number: 1
Number: 2
Number: 4
Number: 5
```
