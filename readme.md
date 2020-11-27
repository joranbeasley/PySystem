# pySystem

a simple utility to assist with interfacing with the OS

it only consists of a single class `System`

you can call any program very pythonically

```python
from pySystem import System

git = System(kwdSep="=",shortSep=" ").git
print(git.log(pretty="format:%ad %s"))

print(System().ls("-la"))
```

if you want to have no space for short args like in `getopts`

you can use `shortSep=""`

```
result = System(shortSep="").myProgram(c=5,s="Hello")
# calls `./myProgram -c5 -sHello
```
