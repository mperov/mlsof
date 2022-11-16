## mlsof
### It's wrapper Linux utility - lsof

mlsof allows to get more accurate list open files.  
Also this tool helps to find files with specified size.

### Main goal

There are situations when file is deleted but process opened file and didn't close this.  
So results of `du -sh /dir` and `df -h /dir` are different.  
mlsof can help to find such file.

### Usage

```
$ ./mlsof -h
usage: mlsof [-h] [-n] [-d] [-s byte b) or kilobyte (Kb) or megabyte (Mb) or gigabyte (Gb] [-p /path/to/dir]

optional arguments:
  -h, --help            show this help message and exit
  -n, -N, --nfs         add -N option for lsof
  -d, --deleted         show only deleted files
  -s byte (b) or kilobyte (Kb) or megabyte (Mb) or gigabyte (Gb)
                        show files, which size is more than specified size
  -p /path/to/dir       specify path to directory
```

### Requirements

+ Python3
