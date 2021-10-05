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
- foo_dir := '/path/to/directory/'
- bar_path := '/path/to/file'
- baz_file := 'file.ext' (with extension)
- foo_name := 'file' (without extension)
- _variable := single heading underscores means protected variable.
  - also called as semi-private variale.
  - this can be seen from API user, but should not be used directly.
- __variable := double heading underscores means private variable. 
  - This is used for private variable, private functions, or classes' private attributes(properties, methods).
  - this cannot be seen and accesible from API user.
  - if there is no special reason, they are start with double consecutive under scores '__'.
  - to access to instance properties/functions, it's gonna be referenced via methods decorated with @property(setter and getter).
    - or if it's needed, you can access like `instance._ClassName__attribute_name` 
  - exeption: `dataclass` properties are defined as normal form `<var>` because they should be accessed directory by default.


## when to use `Class / Data Class / function`.
### Data Class
- focus on the properties themselvs
- Data Class is similar to NamedTuple

### Class 
- it's needed to store some datas, but the logic or algorithms are more emphersized than datas.
- doing inheritance or realize polymorphism
- it's needed to split clearly preprocess and main logic because preorcess is enough to be run once but main process may be run repeatedly.
- implementing complicated algorithm.
- a class is composed of multiple logics and interfaces(public methods).
- if it contains only one public method and have no properties, consider to use function instead of class.
#### example  
- a class has its configuration as Config dataclass


### function
- it's not needed to store any data but only logics.
- implementing simple algorithm.
- it cannot be decomposed anymore.