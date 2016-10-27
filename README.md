#freeCodeTheme
##这里记录的是freeCodeCamp前端题目集和解题时自己重点标出的内容

1.      当 JavaScript 中的变量被声明的时候，程序内部会给它一个初始值 undefined。
当你对一个值为 undefined 的变量进行运算操作的时候，算出来的结果将会是 NaN，NaN 的意思是 "Not a Number"。
当你用一个没有 定义 的变量来做字符串连接操作的时候，它会如实的输出"undefined"。

2.      += 等于 = .. + ..

3.	字符串的不可变性（错误：myStr[0] = "J";）;改变 myStr 中的唯一方法是重新给它赋一个值

4.	相等运算符 == 数据类型转换后比较，全等运算符（===）数据类型不转换，只比较值

5. 	if (a) {}不管a是大于0还是小于0都会执行里面的语句，只有a是undefined才不会被执行

6.	当你知道对象的属性名称时用点来访问属性，当你想访问的属性的名称有一个空格或属性是一个变量，
这时你只能使用中括号操作符([])，属性名称中如果有空格，必须把属性名称用单引号或双引号包裹起来。

7.	删除对象属性delete ourDog.bark;声明对象时，对象的属性名称可以用引号也可以不用引号。

8.	JSON=对象数组 [{},{},{}] {{},{},{}}

9.	\s 空白字符 space

10.	不带return 返回undefined,返回空用return null;

11.	$($('.slot')[1]) $('.slot')所有slot jquery对象,$('.slot')[1] 第二个slot JS对象，$($('.slot')[1])转成jquery对象

12.	除了上一种方法外，我们还可以使用构造函数来创建对象。
构造函数 通常使用大写字母开头，以便把自己和其他普通函数区别开。  
 
	`var Car = function() {
  this.wheels = 4;
  this.engines = 1;
  this.seats = 1;
}; `

	在前面的课程（构造函数）中，我们使用了 this 指向当前（将要被创建的）对象中的 公有属性 。
我们也可以创建 私有属性 和 私有方法 ，它们两个在对象外部是不可访问的,使用我们熟悉的 var 关键字去创建。 
13. array.map(function(currentValue,index,arr)，thisValue) map 方法会迭代数组中的每一个元素，并根据回调函数来处理每一个元素，
最后返回一个新数组。注意，这个方法不会改变原始数组。thisValue待验证

14.	var singleVal = array.reduce(function(previousVal, currentVal) {
  return previousVal - currentVal;//******返回一个值
}, 0);
使用 reduce 方法时，你要传入一个回调函数，这个回调函数的参数是一个 累加器 （比如例子中的 previousVal) 和当前值 (currentVal）。
reduce 方法有一个可选的第二参数，它可以被用来设置累加器的初始值。
如果没有在这定义初始值，那么初始值将变成数组中的第一项，而 currentVal 将从数组的第二项开始。

15.	var oldArray = [1,2,3,4,5,6,7,8,9,10];
var newArray = oldArray.filter(function(val){
  return val<6;
});回调函数返回 true 的项会保留在数组中，返回 false 的项会被过滤出数组。

16.	sort 方法将改变原数组，返回被排序后的数组.
sort 可以把比较函数作为参数传入。a-b从小到大
如果没有传入比较函数，它将把值全部转成字符串，并按照字母顺序进行排序。

17.	var str = string.replace(子字符串或正则，替换成什么（可以是函数的返回值）)  **不会改变原来的字符串，生成一个新的字符串。

18.	字符串首字母大写:截取字符串的第一个加上后面的substring(0,1)+substring(1)

19.	条件表达式不能连写a<b<c,只能b>a&&b<c

20.	arr.splice(index,howmany)会改变原数组，newArr = arr.slice(start,end)不会改变原数组

21.	return与break:return跳出函数执行（return在循环里也同时跳出循环）,break跳出循环，可以执行下面的语句。

22.	JavaScript中有6个值为“假”，这六个值是false,null,undefined,0,''(空字符串),NaN,
在条件判断语句中会将其他5个假值转成布尔值。
虽然这六个值都是假，但它们之间并非都相等。

	对于“==”，以上得出下列结论
<br>false ，0，'' 两两比较结果为true
<br>null只和undefined比较时为true， 反过来undefined也仅和null比较为true，没有第二个。

23.	str.charCodeAt(index)返回ASCII，String.fromCharCode(ASCII,ASCII2,...) 返回字符串。

24.	`var json = [{"a":1,"b":2},{"c":1,"d":2}];`
	<br/>`json.forEach(function(val){`
	<br/>`var keys = Object.keys(val);console.log(keys);});`
	<br>`//["a","b"]`

25. obj.hasOwnProperty(prop) 使用 hasOwnProperty 方法判断某对象是否含有特定的自身属性

26.	a-z：97-122; A-Z：65-90; 0-9：48-57

27.	数组转成字符串arr.join()结果将用逗号连接，arr.join('')将不使用连接符。

28.	str.charCodeAt(index)返回的是ascii字符串，ascii码判断用parseInt(before.charCodeAt(0))>64

29.	数组push数组：result.push(['A','T'])

30.	正则多个条件用或|，/(&|<|>|'|")/gi

31.	进制转换
<br>parseInt("11", 2); // 3 2进制转10进制 
<br>parseInt("77", 8); // 63 8进制转10进制
<br>parseInt("af", 16); //175 16进制转10进制
<br>
<br>(152).toString(2) // "10011000" ; 先用括号将152转换“包”成一个对象， 或者如下写法;
<br>152..toString(2) // 这里第一个点将152转换成float类型的小数，第二个点是引出对象方法;
<br>152..toString(16) // "98" : 十进制转16进制
<br>152..toString(32) // "4o" ：十提制转32进制

32. Array.isArray(arr)判断是不是数组，返回true,false;
arr.every()测试数组的所有元素是否都通过了指定函数的测试.返回true,false;

33.	正则表达式没有^$开始结束，如果一部份满足就会返回true;用小括号括起两选一()(\s|\-)?
;美国电话号码正则：var reg = /^(1\s?)?(\(\d{3}\)|\d{3})(\s|\-)?\d{3}(\s|\-)?\d{4}$/gi;

34. Number.toFixed(num) 四舍五入 num表示保留的小数,变成string对象;  Math.round(): 四舍五入; Math.pow(2,3) 2的3次方 Math.abs绝对值;
Math.sqrt平方根

35. 反向引用。\n第n个捕获组(正则里带括号的)的反向引用 <br>源字符串：abcdebbcde
<br>正则表达式：([ab])\1 表示连续两个相同的字母a或b

36.	**.json只能用双引号括起属性
