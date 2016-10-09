# Terminate all detached screens

	Note: Careful. This will kill **all** the screens started and are detached.

```bash
screen -ls | grep Detached | cut -d. -f1 | awk '{print $1}' | xargs kill
```