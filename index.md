# 一番大きい文字
## 二番目
### 三番目
#### 四番目
##### 五番目
###### 六番目

![Yaktocatってなんだ？](https://octodex.github.com/images/yaktocat.png)

```python
import datetime
import requests
import json
import re
from pathlib import Path

PRE_NOTIFY_DAY = 14
REMIND_DAY=7

NONE = 0
PRE_NOTIFY = 1
REMIND = 2

period = [30, 90, 180]
class CardItem:
    def __init__(self, id, name, duedate, desc):
        self.duedate = duedate
        self.name = name
        self.id = id
        self.pastDays = ( datetime.datetime.now() - datetime.datetime.strptime( self.duedate, "%Y-%m-%dT%H:%M:%SZ") ).days
        self.description = desc
        self.followUpCnt = self.getCntFollowUp()


```
