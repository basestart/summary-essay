#### _set and _get

- 要写的_get 和 _set到底是想实现什么功能

在实际工作中， 经常遇到数据请求并渲染的场景， 特别是在使用框架中的模板渲染数据时， 如果遇到数据的嵌套层级过深时， 为了避免报错， 经常要写很多&&规避错误， 代码非常的丑陋：

场景如下：

```
// a 中的数据从别处获取；
state = {
	a: {
		b: [
			{c: 'val'}
		]
	}
}

//为了保证浏览器不报错， 模板通常这样写
let {a} = this.state;
<tpl>{a.b && a.b.length && a.b[0].c}</tpl>

// 现在要达到的效果是这样的的
<tpl>{ _get (a, 'b[0].c', defaultVal) }</tpl>

```

_get 的代码如下

```

function _get (obj, path, defaultVal) {
	path = path.replace(/\[(\d+)\]/g, '.$1').split('.');
	let tmp = obj;
	for(let i = 0; i < path.length; ++i) {
		tmp = tmp[path[i]];
		if(!tmp) {
			return defaultVal || 0;
		}
	};
	return tmp;
}

//测试
let obj = {a:12};
let name = _get(obj, 'a', 2);
let name2 = _get(obj, 'a.b', 2)
console.log(name, '--name') // 12 "--name"
console.log(name2, '--name2') //2 "--name2"
```

_set 与 _get的使用场景相反， 需要为一个空对象深度赋值， 代码如下

```

function _set(obj, path, defaultVal) {
	path = path.replace(/\[(\d+)\]/g, '.$1').split('.');
	let tmp = obj
	for (let i = 0; i < path.length; ++i) {
		if(!tmp[path[i]]) {
			if(path[i + 1]) {
				if (/\d+/.test(path[i + i])) {
					tmp[path[i]] = new Array();
				} else {
					tmp[path[i]] = {}
				}
			} else {
				tmp[path[i]] = defaultVal
			}
		};
		tmp = tmp[path[i]];
	} 
	return obj;
}

//test
let obj = {};
let res = _set(obj, 'a.b[1].c', 12);
console.log(res, '--res')

{
	a: {
		b: [
			empty,
			{
				c: 12
			}
		]
	}
}

let res2 = _set(obj, 'a.b[1][2].c', 12);
console.log(res2, '--res')

{
	a: {
		b: [
			empty,
			[
				empty,
				empty,
				{
					c: 12
				}
			]
		]
	}
}

```

##### 当然这两个方法， lodash是已经实现了的， 参考路径如下

- [_get](https://www.lodashjs.com/docs/4.17.5.html#get)


- [_set](https://www.lodashjs.com/docs/4.17.5.html#set)