# Bash Depth knowledge

## A Linux process has three basic streams
* stdin  (file descriptor 0) default is keyboard
* stdout (file descriptor 1) default screen
* sederr (file descriptor 2) default screen

## redirecting standered streams
* " < file " connect file to stdin
* " > file " redirect stdout to file
* " 2> file " redirect stderr to file
* " $> file " redirect stdout and stderr to file
* " 2>&1> " redirect stderr to stdout

```
#<(cmd) return the output of cmd as file descriptor
diff <(cmd1) <(cmd2)

#$(cmd) return output text of cmd
vim $(ls -la) # this will open vim with the result in the buffer

* cmd stands for any command like "ls -la"
```

## get exit code of any the previous command
```
echo $?
```

## use xargs command for parallel processing
