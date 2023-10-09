# Lab Report 1 - Remote Access and FileSystem (Week 1)

Using `cd`, `ls`, and `cat` with varying arguments to observe behavior.

## Using `cd`
![Image](https://sssssrrt01.github.io/cse15l-lab-reports/cd.png)
Using cd without any argument returns me to the home directory. The current directory is `/home/lecture1/` when this is called.

Using cd with a path as an argument will enter that directory. The current directory is `/home/`, and we enter the lecture1 directory when `cd lecture1` is called.

Using cd on a file will bounce an error. This is an error because a file is not a directory, and therefore does not follow the logic of `cd`. The current directory when this is called is `/home/lecture1/`.


## Using `ls`
![Image](https://sssssrrt01.github.io/cse15l-lab-reports/ls.png)
Using ls without arguments shows the path of the current working directory. The current working directory is `/home/`, and calling `ls` shows that this is the current directory.

Using ls with a directory will show the paths of that directory. The current working directory is `/home/`, and calling `ls lecture1` shows the paths/files within the lecture1 folder.

Using ls with a file argument will bounce an error. The current working directory is `/home/lecture1/`, and this makes sense because a file does not have filepaths, and therefore does not follow the correct logic of `ls`.

## Using `cat`
![Image](https://sssssrrt01.github.io/cse15l-lab-reports/cat.png)
Using cat without arguments will take in keyboard inputs, and duplicate them. The current working directory is `/home/`.

Using cat with directories will show a message that both arguments are directories and will not do anything. The current working directory is `/home/`, and the `cat` call tries to concatenate two working directories. The logic is unclear, as the meaning behind concatenating directories is ambiguous.

Using cat with files will concatenate the contents of the files. The files do not have any ambiguity, being text files, so the `cat` command knows to concatenate the text within.
