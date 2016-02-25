## Find Platform, CPU, Memory of a Linux machine with Python

Based on snippets from [here](http://echorand.me/site/notes/articles/python_linux/article.html).

### Platform info and distribution of a Linux machine
```Python
import platform
print(platform.uname())
print(platform.linux_distribution())
```

### CPU Info of a Linux machine
```Python
from __future__ import print_function
from collections import OrderedDict
import pprint
 
def cpuinfo():
  cpuinfo = OrderedDict()
  procinfo = OrderedDict()
  nprocs = 0
  with open('/proc/cpuinfo') as f:
    for line in f:
      if not line.strip():
        cpuinfo['proc%s' % nprocs] = procinfo
        nprocs=nprocs+1
        procinfo=OrderedDict()
      else:
        if len(line.split(':')) == 2:
          procinfo[line.split(':')[0].strip()] = line.split(':')[1].strip()
        else:
          procinfo[line.split(':')[0].strip()] = ''
  return cpuinfo

cpuinfo = cpuinfo()
for processor in cpuinfo.keys():
  print(cpuinfo[processor]['model name'])
```

### Memory Info of a Linux machine
```Python
from __future__ import print_function
from collections import OrderedDict
def meminfo():
  meminfo=OrderedDict()
  with open('/proc/meminfo') as f:
    for line in f:
      meminfo[line.split(':')[0]] = line.split(':')[1].strip()
  return meminfo

meminfo = meminfo()
print('Total memory: {0}'.format(meminfo['MemTotal']))
print('Free memory: {0}'.format(meminfo['MemFree']))
```
