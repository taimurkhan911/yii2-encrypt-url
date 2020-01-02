# yii2-encrypt-url


config/web.php
```
'urlManager' => [
    'enablePrettyUrl' => true,
    'showScriptName' => false,
    'rules' => [
        [
            'class' => 'defyma\helper\EncryptUrl',
            'pattern' => '',
            'route' => 'site/index',
            'skey' => '<change to your key>'
        ],
    ],
],
```

contoh php:
```
\yii\helper\Url::to(['create', 'id' => 123]); //http://.../create?ODA3Ly8_OTUxMzE3Mjc4P2JkYTg3MTNkZTZmZjRiNjE_NTQ5OTI1MzA3MT82ZTg3NjllNTNiNTQ1ODkzNTZmYWFjYTRmODRlODQxMz83NDU5OTUyMjMxPz09UXdsd3FaVjdmT0hLblZiRnVRTHFaSj81MzAzMzIyNTQxPyEhXTk1MTMxNzI3OCw1NDk5MjUzMDcxLDc0NTk5NTIyMzEsNTMwMzMyMjU0MVs
```

contoh js:
```
<script>


//versi 1
var url_v1 = urlEncode('http://contoh.com/create?id=123');
console.log(url_v1); //http://.../create?ODA3Ly8_OTUxMzE3Mjc4P2JkYTg3MTNkZTZmZjRiNjE_NTQ5OTI1MzA3MT82ZTg3NjllNTNiNTQ1ODkzNTZmYWFjYTRmODRlODQxMz83NDU5OTUyMjMxPz09UXdsd3FaVjdmT0hLblZiRnVRTHFaSj81MzAzMzIyNTQxPyEhXTk1MTMxNzI3OCw1NDk5MjUzMDcxLDc0NTk5NTIyMzEsNTMwMzMyMjU0MVs

//versi 2
var url_v2 = urlEncodeObj('http://contoh.com/create', {'id':'123'});
console.log(url_v2); //http://.../create?ODA3Ly8_OTUxMzE3Mjc4P2JkYTg3MTNkZTZmZjRiNjE_NTQ5OTI1MzA3MT82ZTg3NjllNTNiNTQ1ODkzNTZmYWFjYTRmODRlODQxMz83NDU5OTUyMjMxPz09UXdsd3FaVjdmT0hLblZiRnVRTHFaSj81MzAzMzIyNTQxPyEhXTk1MTMxNzI3OCw1NDk5MjUzMDcxLDc0NTk5NTIyMzEsNTMwMzMyMjU0MVs


</script>
```
        
        
     
