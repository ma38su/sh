# 38sh

38sh is a simple Shell. The shell supports only limited features.

The shell supports x86-64 Linux or macOS. It's tested on macOS Catalina.

## How to Build

Run make to build:

```
make
```

## How to run

```
./38sh
```

## Supported Features

### Built-in Command
- cd/chdir
- exit

### Environment variables is read only.

Environment variables is supported to read only.

```
$ echo $HOME
/home/ma38su
$ echo ${HOME}
/home/ma38su
```

### String Literal

```
$ echo "$HOME"
/home/ma38su
$ echo '$HOME'
$HOME
```

### Redirection and Pipe

```
$ command < File      # Input Redirection
$ command > File      # Output Redirection (Create & Truncate)
$ command >> File     # Output Redirection (Create & Append)
```

```
$ command1 | command2 # Pipe
```

Input/Output Redirection and Pipe can be used in combination.

```
$ command < File1 > File2
$ command1 < File1 | command2 > File2
```

### Multi Commands in one line

```
$ echo hello && world
hello
world
$ echo hello; echo world
hello
world
```

## Author
ma38su

## Reference
1. ふつうのLinuxプログラミング 第2版
