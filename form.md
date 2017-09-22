## form表单有什么作用？有哪些常用的input 标签，分别有什么作用？
<form> 标签用于为用户输入创建 HTML 表单并向服务器传输数据。

单行文本框`<input type="text">`
密码框`<input type="password">`
单选组件`<input type="radio">`
多选组件`<input type="checkbox">`
隐藏组件`<input type="hidden" name=" " value=" ">`
按钮：
普通按钮`<input type="button">`  (但不会提交)
提交数据按钮`<input type="submit" >`
重置按钮`<input type="reset">`
## post 和 get 方式的区别？
- get:在向后台传输数据时，会用`&`把数据连接起来，然后链接在`?`后面，形成一个新的URL。而post不会形成新的URL，但数据依旧能传输给后台。
- get常用于向后台提取或查询数据，即输入一个提示词，后台根据提示词筛选数据，从而得到数据。而post常用于向后台传输数据，post的安全性较高。
- get方式可提交的数据量跟URL的长度有直接关系，因此并不能传输大量的数据。而post传输的数据量取决于服务器的处理程序的处理能力，但相比get方式，能够传输较大量的数据。
- 在form中，Method的默认方式是get。
## 在input里，name 有什么作用？
`name`属性规定`input`元素的名称，用于对提交到服务器后的表单数据进行标识，或者在客户端通过 JavaScript 引用表单数据。
## radio 如何 分组?
将需要设为同一分组的radio的name属性，设为相同值。
下面为同一组：
```
<input type="radio" name="a" value="1">

<input type="radio" name="a" value="2">

<input type="radio" name="a" value="3">
```
下面为不同组：
```
<input type="radio" name="a" value="1">

<input type="radio" name="b" value="1">
```
## placeholder 属性有什么作用?
placeholder 属性提供可描述输入字段预期值的提示信息（hint）。
该提示会在输入字段为空时显示，并会在字段获得焦点时消失。
## type=hidden隐藏域有什么作用? 举例说明
- 隐藏域在页面中对于用户是不可见的，在表单中插入隐藏域的目的在于收集或发送信息，以利于被处理表单的程序所使用。浏览者单击发送按钮发送表单的时候，隐藏域的信息也被一起发送到服务器。
- 能够防止csrf攻击，若被知晓服务器并向其传输数据，但由于<input type="hidden" name="" value="">中得到的name和value与服务器中存储的不相符，则不会更新服务器中的数据，从而抵挡csrf的攻击。
