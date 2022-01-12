
```
刚才写的忘了保存起来了，....
现在是2022/1/12日14：31分，目前为止搭建博客的任务算是完成了

没保存就没保存吧，就不写了没什么事。
通过vscode编写markdown推送到github
图片就上传到微博图床插入吧

markdown还有好多东西要学呢，我发现这真是个好东西。
```
<!-- 此为目录 -->
- [超链接标签](#HTML超链接标签)
- [表格标签](#HTML表格标签)
- [列表标签](#列表标签)
- [表单标签](#表单标签)





## <a id="HTML标签">HTML标签 Day0</a>
### 常用标签

1. 段落标签p
2. 换行标签br(单标签)

### 文本格式化标签

1. <b>加粗</b> strong或b
2. <em>斜体</em> em或者i
3. <del>删除线</del> del或者s
4. <ins>下划线</ins> ins或者u

### div和span
div和span都是无语义标签

1. div单独占一行
2. span不单独占行






## <a id="HTML超链接标签">HTML超链接标签 Day1</a>

 一般的语法格式为 &lt; a  href="跳转链接  target="跳转方式"&gt; &lt;/ a&gt; 跳转方式默认为_self 

### 一般分为

 1. 外部链接,即跳转到外部
 2. 内部链接,网页内部页面之间的相互链接
 3. 空链接,未指定的链接
 4. 下载链接
 5. 网页元素的链接:网页中各种元素文本图像等都可以添加超链接
 6. 锚点链接 :`<a id="top"></a>` `<a href="#id">回到顶部</a>`即可

### 常用的特殊字符
![Snipaste_2022-01-12_14-39-12.png](http://tva1.sinaimg.cn/large/006wklZvly1gyavusfetuj30uc0deafo.jpg)

## <a id="HTML表格标签">HTML表格标签 Day1</a>

- 不是为了布局，一般是展示一些小数据。table是最外层，tr表示行即table row ，td为列即table data
- 为了明了的展示，表格一般分为thead和tbody，用thead表示表格头部标签，头部的单元格用th表示，表头即第一行会加粗

```
<table>
    <thead>
        <tr>
            <th></th>
            <th></th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>
```

- 表格的属性，平时较少用到，一般表格都是搭配css
![Snipaste_2022-01-12_15-11-38.png](http://tva1.sinaimg.cn/large/006wklZvly1gyaxf5amawj30vs097dkg.jpg)
- 合并单元格
  - rowspan 跨行 colspan 跨列
  - 合并后再删除多余的单元格


```
<tr>
    <td rowspan="2"></td>
        <td></td>
        <td></td>
    </tr>
    <tr >
        <td colspan="2"></td>
        <td></td>
        <td></td>
</tr>
```




## <a id="列表标签">列表标签 Day1</a>
```
列表一般用来布局
```

### 无序列表*
```
<ul>里只能嵌套<li>
<li>相当于容器

<ul>
    <li>
        
    </li>
</ul>

```
### 有序列表
```
较少使用
<ol>
    <li></li>
</ol>
```

### 自定义列表
```
一般用于页尾
<dl>
    <dt>联系我们</dt>
    <dd>微信</dd>
    <dd>QQ</dd>
    <dd>微博</dd>
</dl>
```




## <a id="表单标签">表单标签 Day1</a>
```
表单一般由表单域、表单控件、提示信息构成
```
### 表单域
```
<form action="地址" method="提交方式" name="表单域名称"></form>
包含整个表单的区域
会把<form>范围内的信息提交
```
![Snipaste_2022-01-12_17-17-03.png](http://tva1.sinaimg.cn/large/006wklZvly1gyb0cp048oj30u605xq5l.jpg)

### 表单控件

#### input输入表单元素(单标签)
```
<input type="属性值">
```
![Snipaste_2022-01-12_16-39-08.png](http://tva1.sinaimg.cn/large/006wklZvly1gyb0jcq5x1j30wf0grqag.jpg)
  
- 在单选框radio中,要指定相同的name才能实现单选
```
男 <input type="radio" name="sex" value="man">
女 <input type="radio" name="sex" value="woman">
```
- 对于单选框和多选框一般都要指定name和value
- 在文本框中写入value值可展示预设文本
```
<input type="text" value="请输入用户名">
```
- 在单选框和复选框中checked 可使加载后input元素被选中
```
男 <input type="radio" name="sex" value="man" checked>
女 <input type="radio" name="sex" value="woman">
```
- maxlength 可指定文本框最大的字符长度
```
<input type="text" name="username" value="请输入用户名" maxlength="6">

```
#### select下拉表单元素






#### textarea文本域表单元素