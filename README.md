# coding-style
my coding styles 



# Entire

- max letters per row := (1 << 5) - 1
- max rows per function := (1 << 5) - 1
  - if exceeds, it's time to refactor.
- max rows per class/struct := (1 << 7) - 1
  - if excedds, such a class/struct should be split functionality to other classes/structs 
- max rows per file := (1 << 8) - 1


# Python

## variable names
- <foo>_dir := /path/to/<directory>/
- <var>_path := /path/to/<file>
- <var>_file := <file> (with extension)
- <var>_name := <file> (without extension)
  

