# 常用语法
## 文字部分
**需要加粗的文字** 

*需要倾斜的文字* 

***需要加粗并倾斜的文字*** 

~~需要加删除线的文字~~

> &nbsp;&nbsp;需要引用的文字

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;需要缩进的文字
## 间隔符

----

## 图片引入
### 内联
	![图片名称|图片大小](图片链接)
	![figure 1|100](https://img2.baidu.com/it/u=2854509241,2177956875&fm=253&fmt=auto&app=120&f=JPEG?w=546&h=500 "23")
![figure 1](https://img2.baidu.com/it/u=2854509241,2177956875&fm=253&fmt=auto&app=120&f=JPEG?w=546&h=500 "23")

### 引用
![figure 1][0]
[0]: https://img2.baidu.com/it/u=2854509241,2177956875&fm=253&fmt=auto&app=120&f=JPEG?w=546&h=500 "23"

## 超链接
[百度](http://baidu.com)
### 内联链接
This is an [example link](http://example.com/).
### 引用链接

I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
[1]: http://google.com/       "Google" 
[2]: http://search.yahoo.com/  "Yahoo Search" 
[3]: http://search.msn.com/    "MSN Search"




## 列表
### 无序表
- 无序列表1 

- 无序列表2 

+ 无序列表3 

* 无序列表4
### 有序表
1. 列表内容1 
2. 
3. 列表内容2  

### 混合表
%%上一级与下一级之间敲三个空格%%

+ 一级无序列表1
   * 二级无序列表1
   * 二级无序列表2
- 一级无序列表2       
   1. 二级有序列表1
   2. 二级有序列表2
1. 一级有序列表1
    + 二级无序列表3
    + 二级无序列表4
2. 一级有序列表2
    1. 一级有序列表3
    2. 二级有序列表4

## 表格
`--`表示文字默认居左，
`:-:`表示文字居中
`--:`文字居右



| 姓名| 年龄 | 性别 |
| :- | :-: | :-: |
| xxx     | 25   | 男   |
| xxx | 26   | 中性 |
| xxx     | 24   | 男女男     |


## 代码
### 行内代码
`ctrl + A`
### 行间代码
```
def a(input):
	return input + 1
```
使用四个空格或者Tab也可以达到同样的效果

	23333
	45666

## 标签TAG
#+文字+空格
#标签 
# 常见公式
一般公式分为两种形式，==行内公式==和==行间公式==。行内公式是在公式代码块的前后均添加一个**`$`** ；行间公式则是在公式代码块的前后均添加两个**`$$`** 。
**行内公式**
$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.$  

**行间公式**
$$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.\tag{1}$$


**排列组合**
一般用**`\binom{a}{b}`**或者**`{a \choose b}`**实现
示例：
$$\binom{a}{b} \tag{2}$$
$${a \choose b \tag{3}}$$

## 1. 向量表示
**向量表示：** 使用`\mathbf{x}`来表示向量$\mathbf{x}$。

$$f(\mathbf{x})=\mathbf{w}^T\mathbf{x} \tag{4}$$


## 2.分段函数
定义函数的时候经常需要分情况给出表达式，使用 `{…`。其中：
（1）使用**`\`** 来==分隔分组==；
（2）使用**`&`** 来指示==需要对齐的位置==；
（3）使用**`\ + 空格`**来表示==**空格**==；
（4）如果要使分类之间的垂直间隔变大，可以使用**`\[2ex]`** 代替\ 来分隔不同的情况。(**`3ex`**,**`4ex`** 也可以用，**`1ex`** 相当于原始距离）。
**分段函数1**
$$
y=
\begin{cases}
-x,\quad x\leq 0\\
x, \quad x>0
\end{cases}
\tag{5}
$$

**增大分组的垂直间隔**
$$
y=
\begin{cases}
-x,\quad x\leq 0 \\[2ex]
x, \quad x>0
\end{cases}
\tag{11}
$$

**方程组**
$$ \left\{ \begin{array}{c} a_1x+b_1y+c_1z=d_1 \\ a_2x+b_2y+c_2z=d_2 \\ a_3x+b_3y+c_3z=d_3 \end{array} \right. $$

**分段函数2**
$$
u(x)=
\begin{cases}
exp x,\quad if \space x \leq 0\\
1, \quad if \space x >0 \tag{6}
\end{cases}
$$

**均方误差**
$$ J(\theta) = \frac{1}{2m}\sum_{i = 0} ^m(y^i - h_\theta (x^i))^2 \tag{7}$$

**批量梯度下降**
$$
\frac{\partial J(\theta)}{\partial\theta_j}=-\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j 
$$

**推导过程**
$$
\begin{aligned}
\frac{\partial J(\theta)}{\partial\theta_j}
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i)) \\
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_jx_j^i-y^i) \\
& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i))x^i_j
\end{aligned}
$$

**==case环境的使用==**
$$
a =
   \begin{cases}
     \int x\, \mathrm{d} x\\[3ex]
     b^2 \tag{8}
   \end{cases}
$$


**最大（最小）操作符**
$$
\begin{gathered}
\operatorname{arg\,max}_a f(a) 
 = \operatorname*{arg\,max}_b f(b) \\
 \operatorname{arg\,min}_c f(c) 
 = \operatorname*{arg\,min}_d f(d)
\end{gathered}
$$

**求极限**
$$
\begin{aligned}
  \lim_{a\to \infty} \tfrac{1}{a} 
\end{aligned} \tag{9}
$$
$$
\begin{aligned}
   \lim\nolimits_{a\to \infty} \tfrac{1}{a}
\end{aligned} \tag{10}
$$

**求积分**
$$
\begin{aligned}
   \int_a^b x^2  \mathrm{d} x
\end{aligned}
$$
$$
\begin{aligned}
   \int\limits_a^b x^2  \mathrm{d} x
\end{aligned}
$$

**矩阵**
$$
\begin{equation}
\left[
\begin{array}{cccc}
a_{1,1}& a_{1,2} &\cdots & a_{1,768}\\
a_{2,1}& a_{2,2} &\cdots& a_{2,768}\\
\vdots & \vdots & \ddots & \vdots \\
a_{n,1}& a_{n,2} &\cdots &a_{n,768}
\end{array}
\right ]
\end{equation}
$$

## 3. 多行表达式
有时候需要将一行公式分多行进行显示，其中**`\begin{aligned}`** 表示==开始方程==，**`\end{aligned}`** 表示==方程结束==；使用**`\\`**表示公式换行。**`\begin{gather}`**表示==环境设置==。，**`&`** 表示==对齐的位置==。

**备注：** 如果各个方程需要在某个字符处对齐（如等号对齐），只需在所有==要对齐的字符前==加上 **`&`** 符号。
$$
\begin{aligned}
J(\mathbf{w})&=\frac{1}{2m}\sum_{i=1}^m(f(\mathbf{x_i})-y_i)^2\\
&=\frac{1}{2m}\sum_{i=1}^m [f(\mathbf{x_i})]^2-2f(\mathbf{x_i)}y_i+y_i^2
\end{aligned}
$$


## 4. 符号大全
### 1. 常用数集符号
| 符号         | 代码         | 说明                                                               | 示例                                              |
|:------------ |:------------ |:------------------------------------------------------------------ |:------------------------------------------------- |
| $\mathbb{N}$ | `\mathbb{N}` | 自然数集，即{0,1,2,3,..}                                           | 无                                                |
| $\mathbb{Z}$ | `\mathbb{Z}` | 整数集合，{-3,-2,-1,0,1,2,...}                                     | $\mathbb{Z}^+,\mathbb{Z}^-$表示正整数集和负整数集 |
| $\mathbb{Q}$ | `\mathbb{Q}` | 有理数集，{$\frac{a}{b},\mid a,b \in\mathbb{Z}\ and\  b\neq0$}     | $\mathbb{Q}^+,\mathbb{Q}^-$                       |
| $\mathbb{R}$ | `\mathbb{Q}` | 实数集，{$x \mid x\in [-\infty,+\infty]$}                          | $\mathbb{R}^+,\mathbb{R}^-$                       |
| $\mathbb{A}$ | `\mathbb{A}` | 无理数集合，{$x \mid x \in \mathbb{R}\ and \ x \notin \mathbb{Q}$} | 无                                                |
| $\mathbb{C}$ | `\mathbb{C}` | 复数集，{$x+yi \mid x,y \in \mathbb{R}$}                           | 无                                                |


### 2. 字母加标表示
| 符号        | 示例        |
|:----------- |:----------- |
| `\bar{x}`   | $\bar{x}$   |
| `\acute{x}` | $\acute{x}$ |
| `\check{x}` | $\check{x}$ |
| `\grave{x}` | $\grave{x}$ |
| `\breve{x}` | $\breve{x}$ |
| `\ddot{x}`  | $\ddot{x}$  |
| `\dot{x}`   | $\dot{x}$   |
| `\hat{x}`   | $\dot{x}$   |
| `\tilde{x}` | $\tilde{x}$ |


### 3.希腊字母
| 表达式                    | 示例                        |
|:------------------------- |:--------------------------- |
| `\alpha A`                | $\alpha, A$                 |
| `\beta B`                 | $\beta, B$                  |
| `\gamma \Gamma`           | $\gamma, \Gamma$            |
| `\delta \ Delta`          | $\delta, \ Delta$           |
| `\epsilon \varepsilon E`  | $\epsilon ,\varepsilon, E$  |
| `\zeta Z`                 | $\zeta Z$                   |
| `\eta H`                  | $\eta, H$                   |
| `\theta \vartheta \Theta` | $\theta, \vartheta, \Theta$ |
| `\iota I`                 | $\iota, I$                  |
| `\kappa K`                | $\kappa, K$                 |
| `\lambda \Lambda`         | $\lambda, \Lambda$          |
| `\mu M`                   | $\mu, M$                    |
| `\xi \Xi`                 | $\xi, \Xi$                  |
| `o O`                     | $o O$                       |
| `\pi \Pi`                 | $\pi, \Pi$                  |
| `\rho \varrho P`          | $\rho, \varrho, P$          |
| `\sigma \Sigma`           | $\sigma, \Sigma$            |
| `\tau T`                  | $\tau, T$                   |
| `\upsilon \Upsilon`       | $\upsilon, \Upsilon$        |
| `\phi \varphi \Phi`       | $\phi, \varphi, \Phi$       |
| `\chi X`                  | $\chi, X$                   |
| `\psi \Psi`               | $\psi, \Psi$                |
| `\omega \Omega`           | $\omega, \Omega$            |  


### 4. 运算符号
| 符号                                      | 公式                                            | 说明               |
|:----------------------------------------- |:----------------------------------------------- |:------------------ |
| $+,-$                                     | `+`,`-`                                         | 加法、减法         |
| $\times,\cdot$                            | `\times`,`\cdot`                                | 乘法、点乘         |
| $\div,/,\frac{a}{b}$                      | `\div`,`/`,`\frac{a}{b}`                        | 除法、分数         |
| $\pm,\mp$                                 | `\pm`,`\mp`                                     | 正负号             |
| $(),[],\{\}$                              | `()`,`[]`,`\{\}`                                | 括号               |
| $\sum_{a}^{b},\prod,\coprod$              | `\sum_{a}^{b}`,`\prod`,`\coprod`                | 连续运行符         |
| $\int_{a}^{b},\oint_{c}^{d}$              | `\int_{}^{}`,`\oint_{}^{}`                      | 积分号             |
| $\oplus,\otimes,\odot,\uplus$             | `\oplus`,`\otimes`,`\odot`,`\uplus`             | 带圈符号           |
| $\bigoplus,\bigotimes,\bigodot,\biguplus$ | `\bigoplus`,`\bigotimes`,`\bigodot`,`\biguplus` | 大号带圈符号       |
| $=$                                       | `=`                                             | 等号               |
| $\neq$                                    | `\neq`                                          | 不等号             |
| $\equiv$                                  | `\equiv`                                        | 恒等号             |
| $\approx$                                 | `\approx`                                       | 约等于             |
| $\sim$                                    | `\sim`                                          | 等价于             |
| $\propto$                                 | `\propto`                                       | 正比于             |
| $\widehat{=}$                             | `\widehat{=}`                                   | 相关于             |
| $>,<$                                     | `>`,`<`                                         | 大于、小于         |
| $\geq, \leq$                              | `\geq` ,`\leq`                                  | 大于等于、小于等于 |
| $\geqq,\leqq$                             | `\geqq`,`\leqq`                                 | 大于等于、小于等于 |
| $\gg,\ll$                                 | `\gg`,`\ll`                                     | 远大于、远小于     |
| $\lfloor, \rfloor$                        | `\lfloor`,`\rfloor`                             | 下界               |
| $\lceil \rceil$                           | `\lceil`, `\rceil`                              | 上界               | 

### 5. 集合符号
| 符号                  | 公式                   | 说明       |
|:--------------------- |:---------------------- |:---------- |
| $\colon$              | `\colon`               | 冒号、比   |
| $\{，\}$              | `\{ \}`                | 左右花括号 |
| $\mid,\vert$          | `\mid`,`\vert`         | 竖线       |
| $\cup$                | `\cup`                 | 并集       |
| $\cap$                | `\cap`                 | 交集       |
| $\backslash$          | `\backslash`           | 差集       |
| $\triangle$           | `\triangle`            | 差集       |
| $\dot\cup$            | `\dot\cup`             | 并查集     |
| $\sqcup$              | `\sqcup`               | 并查集     |
| $^{\mathrm{C}}$       | `^{\mathrm{C}}`        | 补集       |
| $\mathcal{P}$         | `\mathcal{P}`          | 超集       |
| $\sqcup {P}$          | `\sqcup {P}`           | 方括号集   |
| $\vee{P}$             | `\vee{P}`              | 同上       |
| $\wedge {P}$          | `\wedge {P}`           | 同上       |
| $\subseteq$           | `\subseteq`            | 子集       |
| $\subset, \subsetneq$ | `\subset`,`\subsetneq` | 真子集     |
| $\supseteq$           | `\supseteq`            | 超集       |
| $\supset,\supsetneq$  | `\supset`,`\supsetneq` | 真超集     |
| $\in,\ni$             | `\in`,`\ni`            | 属于       |
| $\notin,\not\ni$      | `\notin`,`\not\ni`     | 不属于     | 


### 6.常用函数
| 符号                 | 示例                 |
|:-------------------- |:-------------------- |
| `\sqrt[a]{b}`        | $\sqrt[a]{b}$        |
| `\sin\theta`         | $\sin\theta$         |
| `\cos\theta`         | $\cos\theta$         |
| `\tan\theta`         | $\tan\theta$         |
| `\arcsin\frac{L}{r}` | $\arcsin\frac{L}{r}$ |
| `\max H`             | $\max H$             |
| `\log_ \alpha x`     | $\log_ \alpha x$     |
| `\gcd(T,U,V,W,X)`    | $\gcd(T,U,V,W,X)$    |
| `\lim_{a \to b}T`    | $\lim_{a\to b}T$     |
| `\arg x`             | $\arg x$             |
| `a \bmod b`          | $a \bmod b$          | 

### 7. 离散数学运算符
| 公式               | 示例               |
|:------------------ |:------------------ |
| `\land p`          | $\land p$          |
| `\wedge p`         | $\wedge p$         |
| `\bigwedge p`      | $\bigwedge p$      |
| `\to p`            | $\to p$            |
| `\lor p`           | $\lor p$           |
| `\vee p`           | $\vee p$           |
| `\bigvee p`        | $\bigvee p$        |
| `\lnot p`          | $\lnot p$          |
| `\neg p`           | $\neg p$           |
| `\setminus p`      | $\setminus p$      |
| `\smallsetminus p` | $\smallsetminus p$ | 


# Obsidian常用功能
## 双链功能
>链接到某一篇笔记：$[[ ]]$
>链接到某一篇笔记中的某个标题：$[[ # ]]$
>链接到某一篇笔记中的某个段落（块）：$[[ # ^ ]]$
>为链接创建定义（关键词）：$[[ | 关键词]]$
>链接到外部文件如印象笔记：$[关键词]（链接）$

## 快捷键大全
![](图片集合/Pasted%20image%2020220610022223.png)
