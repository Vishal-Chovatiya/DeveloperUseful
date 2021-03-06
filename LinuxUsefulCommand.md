> **Change file permission of whole folder**
- `find 3.0/ -type f -exec chmod 666 {} \;`

> **Redirect Error/Output to file**

- `command >out 2>&1` in `bash`.
- `>&` in `csh`.

> **Default bash prompt setting**

export PS1='[\u@\h \W]\$ '

> **Watch output of any command every X seconds(Default is 2 sec)**

`watch ls -l`

> **Replace a string in multiple files**

`sed -i 's/from/to/g' <PATH_TO_DIRECTORY>/*`

> **Print Directory Tree Structure**

`ls -alR`

NOTE: Or just `ls -R` if you don't want all the details.

OR

`ls -R | grep ":$" | sed -e 's/:$//' -e 's/[^-][^\/]*\//--/g' -e 's/^/   /' -e 's/-/|/'`

> **Print Tail Of File**

```tail -f [FILE]```

Note: use "10" or any number in place of f, for particular tail line output


> **Print Executable Files**

```find [DIRECTORY] -executable -type f ```

Note: use "-delete" option in last to delete those files


> **Print Directory Structre**

```find [DIRECTORY] -type d -print```

> **Find Files With Particular Extensions**

```find ./ -type f -name "*.rej"```

> **Gcc Compiler Options**

[All Compiler Options -c, -o, -E, -Wall, --Werror & 15 more](http://www.thegeekstuff.com/2012/10/gcc-compiler-options/)

> **File Compatibility**

```awk 'sub("$", "\r")' unixFile.txt > windowsFile.txt```

```awk '{ sub("\r$", ""); print }' windowsFile.txt > unixFile.txt```

> **Process**

```ps -au | grep [USERNAME]```

> **Create Soft & Hard Links**

```ln -sf [target] [source]```

*Soft Links(-s Parameter)* : point to the file name

*Hard Links(By Default)*   : point to the file contents(share the same inode)

> **Symbol Table Information**

```nm -n [ELF_file]```
*Note:-n option sort symbols by address*

*Example*

[VirtualAddress]        [SymbolType]      [SymbolName]

0000000000601038        B                 __bss_start

SymbolType : Lower case = local & Upper case = external

> **List of Object include in static lib**

```ar -t [libname.a]```

> **List of shared Object used**

```ldd [libname.so]  OR ldd [Executable]```

> **File Transfer between PCs**

```scp [file_name] [user]@[IP]:[location]```

i.e.```scp image.jpg vishal@192.168.0.1:/home/vishal```

> **tar file(compress)**

```tar -cvf [file_name].tar [file_name]```

> **Untar file(de-compress)**

```tar -xvf [file_name].tar```

> **Count No of Occurence in file**

```grep -rw [WORD] [FILENAME] | wc -l```

> **Redirecting output of program in file**

```./[PROGRAM] > [OUTPUT_FILENAME] 2>&1 &```

> **Custome Setting Script**

```
cd ~
alias ls="ls -lrt --color=auto"
export PS1='[\u@\h \W]$ '
```
- Run this as `$ . <Script_Name>`
