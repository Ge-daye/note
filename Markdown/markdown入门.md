

# 一级标题 

## 二级标题

### 三级标题

#### 四级标题

###### 六级标题

`可以用ctrl+数字1~6来直接生成对应的标题`

# 本文档说明：

==每个模块使用markdown代码块作为解释==

==然后在它下面展示效果==



# 样式

## 删除

~~~mark
~~删除线~~ (用一对~~将想要添加删除键的文字包含起来)
~~~

~~删除线~~ (用一对~~将想要添加删除键的文字包含起来)



## 斜体加粗

~~~markdown
*斜体* 用一边一个个星号包含     快捷键ctrl+I
**加粗**用一边两个星号包含      快捷键ctrl+B
***斜体加粗***用一边三个星号包含  
~~~

*斜体* 用一边一个星号包含
**加粗**用一边两个星号包含

***斜体加粗***  用一边三个星号包含



## 下划线

~~~markdown
<u>下划线</u>   快捷键ctrl+U
~~~

<u>下划线</u>

 <u>快捷键</u>   快捷键ctrl+U



## 高亮

```markdown
==高亮==  用一边两个等号包含
```

==高亮显示==



## 上标

~~~mark
Y=X^2^
面积：m^2^
~~~

**二次函数**：Y=X^2^

**面积**：m^2^



## 下标

~~~mark
水：H~2~O
双氧水：H~2~O~2~
~~~

**水**：H~2~O

**双氧水**：H~2~O~2~



## 表情：

~~~mark
:computer_mouse: :email: :cry::smile:  :aerial_tramway: :cry: :email: :grapes:    :100: 
自带的表情符号
~~~

:smile:  :aerial_tramway:  :cry: :joy: :email: :grapes: :computer_mouse:

:100:   :eggplant:

## 表格

使用  ` |`  分割单元格， 使用  `-`  区别表头和内容（默认内容都是左对齐）

~~~mark
name | age
---- | ----                      <!-- 几个横杠无所谓，主要为了美观-->
张三 | 21
李四 | 20
小红 | 18

~~~

为了排版美观，`|`  两端要各留一空格

| name | age  |
| ---- | ---- |
| 张三 | 21   |
| 李四 | 20   |
| 小红 | 18   |

在表头分隔符----加上冒号：就可以指定对齐方式

~~~mark
name | age
---- | :----:
张三 | 21
李四 | 20
小红 | 18
~~~

| name | age  |
| :--- | :--: |
| 张三 |  21  |
| 李四 |  20  |
| 小红 |  18  |

### **更快捷的做法：**



1. **ctrl+T**   快速生成指定行列的表格
2. 直接粘贴网站里的表格

| 8K 视频拍摄    | 30fps    |
| -------------- | -------- |
| 4K 视频拍摄    | 30/60fps |
| 1080p 视频拍摄 | 30/60fps |
| 720p 视频拍摄  | 30fps    |

**另外：**鼠标右击表格对表格进行编辑



## 引用

~~~mark
>引用
> > 二级引用
~~~

> 引用
>
> > 二级引用
> >
>
> （两次回车可以跳过当前的引用）



## 无序列表

~~~markdow
* 列表内容    （* 后跟空格）
或者
+ 列表内容    （+ 后跟空格）
~~~

* 列表内容1

+ 列表内容2

### 



## 有序列表

~~~mark
1. 列表1  (点后面要留一个空格)
2. 列表2
………………
二级列表：
     先设置好以及列表的所有内容
     在想要添加二级列表的子列用tab键
~~~



1. 列表1
   1. 列表1.1
   2. 列表1.2
2. 列表2

##代码 

### 代码块

```mark
~~~语言名称
或者
​```语言
例： ```java
```

`java`

```java
public static void main(String []arg){
    System.out.ptintl();
}
```

### 行内代码

```mark
`行内代码`   用两个`包含
```

`行内代码`

## 分割线

```mark
***直接回车
---直接回车
```

***

---



## 链接

#### 外部链接(网址或者本地文件)

语法：`[text](url)`

```mark
[百度一下](http://www.baidu.com)
```

[百度一下](http://www.baidu.com)

==说明：网站必须带”http://“==



#### 内部链接（锚点链接）

语法：`[text](目的地标题)`

```mark
[返回最顶端](#一级标题)
```

[返回最顶端](#一级标题)



#### 

#### 自动链接

语法 `<url>`

```mark
<http://www.baidu.com>
```

<http://www.baidu.com>



#### 图片（网站文件或本地文件）

语法：`![photo name](url)`

```mark
![小猪佩奇](http://www.17qq.com/img_biaoqing/76514118.jpeg)
```

<img src="http://www.17qq.com/img_biaoqing/76514118.jpeg" alt="小猪佩奇" style="zoom: 50%;" />



![狮子](http://t8.baidu.com/it/u=1484500186,1503043093&fm=79&app=86&f=JPEG?w=1280&h=853)



## 待办事项

~~~
- [ ] 未完成的项目 <!--注意三个空格-->
- [x] 已完成的项目
~~~



- [x] 主项目
- [ ] 项目1
- [ ] 项目2
- [ ] 项目3
- [ ] haha



# 关于markdown中html标签的问题

在markdown文档中书写html标签会被直接解析，如果不想被解析，就在标签前加上反斜杠

如<a>链接</a>

\<a>链接\</a>

```html
如<a>链接</a>

\<a>链接\</a>
```

#  ceshi

[返回无序列表](##无序列表)



