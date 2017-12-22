yii2-qiniu
=================================

--------------------------------
 `composer.json`:

```json
{
  "require": {
    "80h4ck/yii2-qiniu": "~1.0.0"
  }
}
```

Usage
-----

```php
<?php

use 80h4ck\qiniu\Qiniu;
$config = [
'accessKey'=>'xxx',
'secretKey'=>'xxx',
'domain'=>'http://demo.domain.com/',
'bucket'=>'demo',
'area'=>Qiniu::AREA_HUABEI
];



$qiniu = new Qiniu($config);
$key = time();
$qiniu->uploadFile($_FILES['tmp_name'],$key);
$url = $qiniu->getLink($key);
```
