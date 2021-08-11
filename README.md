# coding-style
my coding styles 



# Entire

- max letters per row
  - soft limit := (1 << 5) - 1
  - hard limit := (1 << 6) - 1 
- max rows limit per function
  - soft limit := (1 << 4) - 1
  - hard limit := (1 << 5) - 1
  - if exceeds, it's time to refactor.
- max rows limit per class/struct
  - soft limit := (1 << 6) - 1  
  - hard limit := (1 << 7) - 1
  - if exceeds, such a class/struct should be split the functionality into other classes/structs 
- max rows limit per file 
  - soft limit := (1 << 7) - 1  
  - hard limit := (1 << 8) - 1
  - needless to say, to write a large amount of rows in a file is nonsense and it is hard to read.    
  - 
 
 
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
