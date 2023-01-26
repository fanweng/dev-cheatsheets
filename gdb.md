# GDB

### Check dependencies

```sh
(gdb) info sharedlibrary
```

### Set path for shared libraries

```sh
(gdb) set solib-search-path /path/to/symbol/folder
```

### Check thread information

```sh
(gdb) info threads
(gdb) thread 1
(gdb) thread 2
```

### Check `/proc` information

```sh
(gdb) info proc all
(gdb) info proc status
(gdb) info proc stat
(gdb) info proc mappings
```

### Check files

```sh
(gdb) info files
```

### Check frame information

```sh
(gdb) info frame
```

### Check backtrace information

```sh
(gdb) bt
(gdb) bt full
```

### Check stack overflow

In a running system, print the mappings of a process:

```sh
# cat /proc/<pid>/pmap
```

Examine the stack usage in a core dump:

```sh
(gdb) info threads
(gdb) thread <crashed_thread_id>
(gdb) info stack
# select the frame on top
(gdb) frame 0
(gdb) set $topsp=$sp
# select the frame on bottom
(gdb) frame <earliest_frame_id>
(gdb) print (char *)$sp - (char *)$topsp
# the value is an approximation of the stack usage
```
