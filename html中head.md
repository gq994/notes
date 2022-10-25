# html中的head头部

### 1. title标签			

​	设置窗口标题

```
<title>Document</title>
```

### 2. meta网页编吗

	<meta charset="UTF-8">

### 3. meta视口

	<meta name="viewport" content="width=device-width, initial-scale=1.0">

### 4. meta关键词

```
 *<!-- 用户搜索该页面时用的关键字 -->*
<meta name="keywords" content="关键词1、关键词2、、、、、一般8-9个关键词">
```

### 5. meta描述

```
  <!-- 网页描述 -->
  <meta name="description" content="网页描述，一般0-50字">
```

### 6.link标签

#### 	1.导入css样式

```
  <link rel="stylesheet" href="./css/style.css">
```

#### 	2.dns预解析

```
  <link rel="dns-prefetch" href="">
```

>  ***dns预解析，href=“需要解析的地址” 域名变成ip地址，*** 
>
>   ***前端性能优化的一项，网页加载完就解析对应的域名，***
>
>   ***可以减少用户访问网址对应网址的等待时间***

#### 	3.地址栏显示小图标

```
<link rel="shortcut icon" href="images/favicon.png">
图片类型支持ico和png
```

特别注意：低端IE**浏览器本地模式预览显示不了小图标**

### 7.base 基础链接

```
<base href="http://www.baidu.com/" target="_blank">
```

配置所有具备href属性链接的基础地址，包含a的href属性和link的href属性，对src属性也有影响

### 8.script脚本

```
外链导入
<script src="js/main.js"></script>

内嵌导入
<script>
  var a = 10;
</script>
```

### 9.noscript脚本

```
    当浏览器禁用js代码时，会渲染noscript中的内容
  <noscript>
      当前已禁止使用JavaScript代码
  </noscript>
```

### 10.meta作者

```
<meta name="author" content="gq"></meta>
```

### 11.meta版权

```
<meta name="copyright" content="xxx公司" >
```

### 12.meta刷新

```
  <!-- 每隔三秒会自动刷新 -->
  <!-- <meta http-equiv="refresh" content="3"> -->
    
  <!-- 3秒后自动跳转到指定网页 -->
  <!-- <meta http-equiv="refresh" content="3; url=http://www.baidu.com"> -->
```

### 13.meta渲染器

  *当前浏览器如果有webkit内核，则指定webkit渲染*

  *可以用在双核浏览器，比如360安全浏览器*

```
  <meta name="renderer" content="webkit">
```

### 14.meta浏览器兼容性

```
<meta http-equiv="X-UA-Compatible" content="IE=edge, chrome=1">
```

>   *浏览器兼容*
>
>   *IE=edge，表示用IE最新的内核（edge浏览器内核）渲染*
>
>   *Chrome = 1 ，表示指定使用谷歌浏览器内核渲染*
>
> ​        				 *前提用户浏览器需要安装一个*
>
> ​        				 *GCF(google chrome frame)谷歌内嵌浏览器框架*

### 15.meta格式化内容

```
  <!-- 忽略数字自动识别为电话号码，主要在iOS系统上 -->
  <meta name="format-detection" ccontent="telephone=no">
  
    <!-- 忽略识别邮箱，主要在iOS系统上 -->
  <meta name="format-detection" ccontent="email=no">
```

### 16.meta过期时间

```
<meta http-equiv="expires" content="0" />
expires 用于设定网页的到期时间，一旦网页过期，必须到服务器上重新传输
```

### 17.meta禁止缓存

```
    禁止缓存
    no-cache: 不使用缓存，直接向服务器发送请求
    no-store: 所有内容不缓存到缓存或者临时文件夹中
    must-revalidate: 当资源一定是从服务器发送验证请求，
                      若请求失败返回504状态码。
   <meta http-equiv="Cache-Control"content="no-cache,no-store,must-revalidate">         
```

