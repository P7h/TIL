## PID Stats

I/O Stats of any process

```bash
pidstat -d -p <PID> <Interval>
```

```
PID - The identification number of the task being monitored.
kB_rd/s - Number of kilobytes the task has caused to be read from disk per second.
kB_wr/s - Number of kilobytes the task has caused, or shall cause to be written to disk per second.
kB_ccwr/s - Number of kilobytes whose writing to disk has been cancelled by the task. This may occur when the task truncates some irty pagecache. In this case, some IO which another task has been accounted for will not be happening.
Command - The command name of the task.
```

Sample command:
```bash
pidstat -d -p 20191 10
```

Sample output:
```bash
01:01:32 PM       PID   kB_rd/s   kB_wr/s kB_ccwr/s  Command
01:01:42 PM     20191      0.00       0.00          0.00             java
```
