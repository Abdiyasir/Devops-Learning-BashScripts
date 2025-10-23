#  Arithmetic in Bash
- Bash supports arithmetic operations for working with numbers.
- These can be used to perform calculations, counters, and data processing inside bash scripts.

##  Basic Arithmetic
- Arithmetic expansion in Bash is done using `$(( ))`.
```
a=10
b=5
sum=$((a + b))
echo "Sum: $sum"
