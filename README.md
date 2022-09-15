# Git
## Find the commit in which a given file was added
```
git log --diff-filter=A -- <file name>
```
* **Documentation:**
```
--diff-filter=[(A|C|D|M|R|T|U|X|B)…​[*]]
```
Select only files that are Added (A), Copied (C), Deleted (D), Modified (M), 
Renamed (R), have their type (i.e. regular file, symlink, submodule, …​) changed (T), 
are Unmerged (U), are Unknown (X), or have had their pairing Broken (B).

## List committed files
```
git show <commit_id> --name-only
```

## Delete the last commit
```
git reset --hard HEAD^
```

## Check one commit is an ancestor of another commit
```
git merge-base A B
```

# Linux programming

## Static library

* source code (.c) -> Compiler (machine language - object code) -> Linker + library functions -> Executable code

* Linker makes a copy of all library function to executable file

* Static library have extension .a in Linux and .lib in windows
* Command to create static library:
```
ar rcs <.a> <.o> <.o> ...

// Linker
gcc -o main main.o -L. <.a>
```
## Dynamic library

* Also called shared library
* Linked at run time
* Every program can access this library at run time and can avoid creation of multiple copies for every program

## Compare Static and Dynamic library
|                       Static                     |                            Dynamic                     |
|--------------------------------------------------|--------------------------------------------------------|
|1) Code to run the file is in one executable file |1) Only the address of the library is provided in the   |
|and gets copied into target application which     |target program so every program can access them without |
|create standalone executable                      |creating copies                                         |
|                                                  |                                                        |
|2) It is locked into the program at compile time  |2) It act as separate file out of executable so can be  |
|so cannot be modified without recompilation       |modified at any time without recompilation              |


