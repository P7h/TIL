## Current week number with Python

Following code snippet prints current year, week number and day of the week.

```python
import datetime

year, week_number, day_of_the_week = datetime.datetime.now().isocalendar()
print year, week_number, day_of_the_week
```
