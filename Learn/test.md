# Hello,world!
## *二级标题*
### ~~**三级标题**~~
#### 现在开始介绍语法
- #一级标题
- ##二级标题
- ###三级标题
每写完一个段落需要隔一行空行。
可以用下面这个操作
在文本框内显示为一道横线/分割线
---

**重点加粗**
*斜体*
~~删除线~~
==*mardown preview enhaned扩展功能*==
==高亮==
另外，选中文本后，按下`Ctrl+B`可以给选中文编加粗
同理，用`Ctrl+I`可以让选中文本变为斜体

列表
* 无序列表1
  * 嵌套无序列表1
  * 嵌套无序列表2
* 无序列表2

1. 有序列表1
    1. 嵌套有序列表1
    2. 嵌套有序列表2
2. 有序列表2
3. 有序列表3

==*扩展功能*==
- [ ] 未完成的事件1
- [x] 已完成的事件2
需要注意的是，在文本界面可以直接用鼠标勾选框框；并且要注意-后和[]后的空格都是不可忽略的。
   
---

引用文本：
>引用别人说的话
>就这样写
>By . LXP

---

这是`行内代码`语法
其中`是英文状态下，按1左边那个按键得到的

代码块语法
``` C++
#include<iostream>
using namespace std;
cout<<"hello world"<<endl;
```
==*扩展功能*==
代码行数的显示
```C++ {.line-numbers}
#include<iostream>
using namespace std;
int main()
{
    cout<<"hello world!"<<endl;
    system("pause");
    return 0;
}
```

---

[超链接名称](链接地址)
[markdown教程](https://zhuanlan.zhihu.com/p/366596107)

![图片提示语](图片地址)
![example](./picture/p1.png)

利用paste image插件可以实现剪贴板粘贴图片
前提是要做一些小调整
按下`Ctrl + ,`，打开设置窗口，输入`Paste Image Path`并搜索，将框内的文编改成`${currentFileDir}/images`。
设置后，就可以用剪贴板粘贴功能。
按下快捷键`Ctrl + Alt +V`就能把图片自动保存到当前目录下，并以正确的格式粘贴到当前的Markdown文件中。

---

表格

| 表头  | 表头  |
| ----- | ----- |
| 内容1 | 内容2 |
| 内容3 | 内容4 |

扩展用法：
| 表头 | 表头 |
| ---- | ---- |
| 内容 | 内容 |
| ^    | 内容 |
| ^    | 内容 |
| >    | 内容 |
利用`Shift + Alt + F`可以实现表格自动对齐
注意这边合并只有这两种方式，需要好好思考布局


---

注释：
<!--这是注释，可以多行-->
注意，注释在文本页面是看不见的。只有在代码界面才能看到。其中除了中文，其他都是必要的字符。
注释可以随时做点草稿，如果还想留着，但是不显示，就可以按下快捷键`Ctrl + /`将当前行进行注释/反注释
VS Code会在每次修改==代码==后重新渲染一遍，如果又很多公式，渲染将会很慢。这时有两个建议
- 分为多个文件
- 将暂时不需要的部分注释掉，加快渲染速度

---

段落和段落之间需要空一行。

就像这样。

---

数学公式支持
Markdown 的数学公式吸纳了大部分的 Latex 语法, 你可以以一种简单的方式在 VS Code 中书写数学公式。

行内公式：
单位圆  $x^2+y^2=1$
公式块
$$
\begin{cases}
x=\rho\cos\theta \\
y=\rho\sin\theta \\
\end{cases}
$$

注意，不要在公式内使用中文，除非是`\text{中文}`,但也不推荐。

1. 上标和下标
   - 上标： $x^2+y^{12}=1$
   - 下标： $x_2+y_{12}=1$
2. 分式
   - 较小的行内行分数 $\frac{1}{2}$
   - 展示型的分式 $\displaystyle\frac{x+1}{x-1}$
其中`\displaystyle`用于将行内展示转为块展示。
3. 根式
   - 开平方 $\sqrt{2}$
   - 开$n$次方 $\sqrt[n]{2}$
4. 空格
数学公式中的**空格和换行**都会在编译时**被忽略**，想要实现空格的功能，需要用特别的命令
   - 紧贴$a\!b$
   - 没有空格$ab$
   - 小空格$a\,b$
   - 中空格$a\;b$
   - 大空格$a\ b$
   - quad空格$a\quad b$
   - 两个quad空格$a\qquad b$
5. 累加、累乘和积分
   - 累加$\sum_{k=1}^n\frac{1}{k} \quad \displaystyle\sum_{k=1}^n\frac{1}{k}$
   - 累乘$\prod_{k=1}^n\frac{1}{k} \quad \displaystyle\prod_{k=1}^n\frac{1}{k}$
   - 积分$\displaystyle \int_0^1x{\rm d}x \quad \iint_{D_{xy}} \quad \iiint_{\Omega_{xyz}}$
6. 括号修饰
用`\left`和`\right`可以让括号适配内部大小
注意，例如`\left(`或者`\right)`是一个整体
   - 圆括号$\displaystyle \left(\sum_{k=1}^n\frac{1}{k} \right)^2$
   - 方括号$\displaystyle \left[\sum_{k=1}^n\frac{1}{k} \right]^2$
   - 花括号$\displaystyle \left\{\prod_{k=1}^n\frac{1}{k} \right\}^2$
尤其注意这边的left和right需要前后都有\，否则会出错
   - 尖括号$\displaystyle \left\langle\prod_{k=1}^n\frac{1}{k} \right\rangle^2$
注意这里，\langle是尖括号的一边
7. 多行算式对齐
   - 居中
$$
\begin{aligned}
y &=(x+5)^2-(x+1)^2 \\
&=(x^2+10x+25)-(x^2+2x+1) \\
&=8x+24 \\
\end{aligned}
$$
   - 左对齐
$
\begin{aligned}
y &=(x+5)^2-(x+1)^2\\
&=(x^2+10x+25)-(x^2+2x+1)\\
&=8x+24\\
\end{aligned}
$
8. 方程组
