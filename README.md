# Dropdown
Dropdown是面向PC端的基于jQuery开发的轻量级下拉框插件，支持key/value搜索，有token和select两种模式。

## Version
- 1.0.0

## Support
- Internet Explorer 8+
- Chrome for PC
- Safari for PC
- Firefox for  PC

## Based
- jQuery 1.4+

## Feature
1. 支持 `select` 和 `token` 两种模式
2. 支持 `optgroup` 分组
3. 保留原生 `select` 的键盘操作
4. 数据源可以直接通过接口 `data` 注入，也可以直接渲染 `select>option` ，由插件自动转换。
5. 插件同步 `select` 和 `ul>li` 标签，便于表单字段提交及前端校验，

## Principle
**程序设计原理如下图所示：**
![](http://images.vrm.cn/2017/03/21/WX20170321-174303.png)


## Options
| 名称 | 描述 | 类型|默认|
| ----|-----|-----|----|
| readOnly|是否只读|Boolean|`false`|
|limitCount|选择上限|Number|`Infinity`|
| input|搜索框模板|HTML|`<input type="text" maxLength="20" placeholder="搜索关键词或ID">`|
| data|数据源|Array|`[]`|
| searchable|是否可开启搜索|Boolean|`true`|
| searchNoData|无数据模板|HTML|`<li style="color:#ddd">查无数据，换个词儿试试 /(ㄒoㄒ)/~~</li>`|
| choice|选择后回调函数|Function| `function(){}`|


## Usage
引入

```html
<script src="http://cdn.bootcss.com/jquery/1.8.1/jquery.js"></script>
<link rel="stylesheet" type="text/css" href="./jquery.dropdown.css">
<script src="./jquery.dropdown.js"></script>
```

HTML 部分

```html
<div class="dropdown-mul-1">
   <!-- PS: select标签需手动设置隐藏 -->
	<select style="display:none"  name="" id="" multiple placeholder="请选择">
	    <option value="1">1</option>
	    <option value="2">2</option>
	    <option value="3">3</option>
	    <option value="4">4</option>
	    <option value="5">5</option>
	    <option value="6">6</option>
	    <option value="7">7</option>
	    <option value="8">8</option>
	    <option value="9">9</option>
	    <option value="10">10</option>
	    <option value="11">11</option>
	    <option value="12">12</option>
	</select>
</div>
```
JavaScript 部分

```js
$('.dropdown-mul-1').dropdown({
  limitCount: 40,
  multipleMode: 'label',
  choice: function () {
    console.log(arguments,this);
  }
});
```


## Example

[https://janking.github.io/dropdown/](https://janking.github.io/dropdown/)