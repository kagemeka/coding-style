# coding-style
my coding styles 



# Entire

- max letters per row := (1 << 5) - 1
- max rows limit per function := (1 << 5) - 1
  - if exceeds, it's time to refactor.
  - recommended max row count := (1 << 4) - 1
- max rows limit per class/struct := (1 << 7) - 1
  - if exceeds, such a class/struct should be split the functionality into other classes/structs 
  - recommended max row count := (1 << 6) - 1
- max rows limit per file := (1 << 8) - 1
  - needless to say, to write a large amount of rows in a file is nonsense and it is hard to read.    
  - recommended max row count := (1 << 7) - 1
 
 
 
# Python

## variable names
- <foo>_dir := /path/to/<directory>/
- <var>_path := /path/to/<file>
- <var>_file := <file> (with extension)
- <var>_name := <file> (without extension)
- __<var> := class's peoperties and functions for the instances. 
  - if there is no special reason, they are start with double consecutive under scores '__'.
  - to access to instance properties/functions, it's gonna be referenced via methods decorated with @property(setter and getter). 
  - exeption: `dataclass` properties are defined as normal form `<var>`
