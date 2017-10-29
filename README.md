## 4-examples-for-understanding-colsure

```javascript
function love(name) {
	var text = 'Hello ' + name;
	var me = function() {
		console.log(text);
	}
	return me;
}
var loveme = love('AutumnsWind');
loveme(); // 输出 Hello AutumnsWind
```
```javascript
function love1() {
	var num = 223;
	var me1 = function() {
		console.log(num);
	}
	num++;
	return me1;
}
var loveme1 = love1();
loveme1(); // 输出224
```
```javascript
function love2() {
	var me2 = function() {
		console.log(temp);
	}
	var temp = 'Hello AutumnsWind';
	return me2;
}
love2()(); // 输出 Hello AutumnsWind
```
```javascript
var get, add, set;

function setup() {
	var num = 223;
	get = function() {
		console.log(num);
	}
	add = function() {
		num++;
	}
	set = function(x) {
		num = x;
	}
}
setup();
add();
get(); // 224
set(5);
get(); // 5
var old = get;
setup();
get(); // 223
old() // 5
```

<sub>转载自:
[http://blog.csdn.net/qq_27080247/article/details/50735380](http://blog.csdn.net/qq_27080247/article/details/50735380)
</sub>