### 数值的静态属性：

1. MAX_SAFE_INTEGER  最大安全整数
   MIN_SAFE_INTEGER 最低安全整数
2. isFinite 判断是否是有限数
   	Math.PI 在js中精度只达到小数15位
3. isInteger 判断是否为整数
4. isNaN es6新增，这个要和全局的isNaN区分开发
   这里的isNaN就是判断它是不是NaN，是就返回true，不是就返回false，es6新增这个方法就是为了识别NaN不等于NaN	

### 数值的实例方法

1. toExponential将数值转换为科学计数法表达

2. toString转换为字符串	

3. toFixed转换为指定位数的小数，支持四舍五入，注意会转换为string

4. toPrecision将一个数转为指定位数的有效数字	

5. toLocaleString转换为本地字符串数字，千分位的实现

6. 自定义方法
    1. 定义数值静态方法

    2. 定义数值实例方法我们也叫定义数值原型方法

       



### 字符串的静态方法

  1. String.fromCharCode返回指定unicode码点的字符，参数支持无、1个、或者n个

     

### 字符串实例的属性

​	1. length 长度，字符串是长度是只读的，长度改变

### 字符串实例的方法

	1. charAt方法返回指定位置的字符，参数是从0开始编号的位置。	
	
	2. charCodeAt返回字符串指定位置的 Unicode 码点，返回一个数字
	和fromCharCode是一对互转函数
	
	3. concat链接字符串函数，返回新字符串，不会改变原始字符串
			注意：不会改变原始字符串
	
	4. trim取出首尾的空格，注意中间的空格无法去掉
	
		1. trimStart，清除首空格
		2. trimEnd清除尾空格
	
	5. toLowerCase将大写字母转换为小写字母
	
	6. toUpperCase将小写字母转换为大写字母
	
	7. indexOf查找指定字符串出现的位置，返回-1表示没有，0表示找到字符，是在第一个位置，返回大于等0的字符表示包含此字符
	        查找空字符串永远返回0
			注意空字符串返回是0
	第2个参数，表示字符串搜索起始位置，默认是从0开始
	
	8. lastIndexOf，lastIndexOf 功能和indexOf类似，区别就是indexOf是从左向右查找，而lastIndexOf是从右向左查找
	
	9. slice用于根据起始索引值和结束索引值抽取字符串的部分字符，返回新字符串，不破坏原始字符串
	
		1. 支持负数，负数表示倒着数，-1，倒数第一个
		2. 如果省略第2个参数，表示结束索引值是最大的字符串长度		
	
	10. substring和slice函数非常相似，第1个表示起始索引值，第2个参数表示结束索引值，和
	
	 	1. slice主要区别是substring第2参数不支持负数，如果是负数，默认会转换为0始终将最小的值作为起始索引值，最大的值作为结束索引值
	
	 	2. substring和slice的区别？
	
	     1. 置换start和end的位置
	        slice 不会置换，substring会置换
	
	     2. start和end参数支持负数
	     slice 都支持负数，substring都不支持
	
	11. substr，用于从原字符串取出子字符串并返回，不改变原字符串
	
	 		1. 第1个参数是字符串起始索引值，支持负数			
	 		2. 第2个参数是字符串长度


	12. match用于确定原字符串是否匹配某个子字符串，返回数组，数组包含被匹配的字符和它的索引值，没有找到返回null
	
	13. search用法基本等同于 match，但是返回值为匹配的第一个位置，没有找到返回-1
	
	14. replace用于替换匹配的子字符串，一般情况下只替换第一个匹配


	15. split，按照给定规则分割字符串，返回数组，第2个参数limit，表示要取数组的个数
	
	16. localeCompare，a 最小  z
			最大升序排序   就是  a-z         0-9
			降序排序  就是   z-a         9-0
			中文就是取拼音
				升序        就是      阿不吃德
				倒序        就是      德吃不阿
	冒泡中文排序
		得到最后1个字符有多少办法？
			

	trimStart
		去除首空格，别名trimLeft
	trimEnd
		去除尾空格，别名trimRight
	padStart
		语法：模板字符.padStart(位数, 补全字符)
			开头字符补全
		padEnd
			结尾字符补全
		startsWith
			判断某字符是否以指定的字符开头
		endsWith
			判断某字符是否以指定的字符结尾
		link
			

	includes
		查找某字符是否包含指定的字符，返回布尔值