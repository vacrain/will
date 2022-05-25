# typora中插入LaTeX数学公式

本文内容参考https://blog.csdn.net/baidu_38060633/article/details/79183905 在Typora上进行了实验。



## typora公式语法

数学公式有两种形式： inline 和 display

- **inline（行间公式）?*在正文插入数学公式，用`$...$` 将公式括起来
- **display(快间公式)** ：独立排列的公式，用 `$$...$$`将公式括起来，默认显示在行中间

equation是用户给当前公式自定义的名字（随便写）



## LaTeX 编辑数学公式基本语法元素

- **各类希腊字母表：**

  eg: `$\alpha$`:α\alpha*α*

  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20181104140244618.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhcHB5ZGF5X2Q=,size_16,color_FFFFFF,t_70)

### 常用语法

所有字符后面都可以跟个空格，避免与表达式中的字母符号混淆

| 特殊字符     | 说 明                                   | 实例                                    |
| ------------ | --------------------------------------- | --------------------------------------- |
| $            | 数学公式前后加$是行内公式               | 数学公式:$a=x+y$                        |
| $$           | 数学公式加$$就是读占一行的公式          | 独占一行:$$a=x+y$$                      |
| \            | 转义字符,特殊字符要显示原意,就在前面加\ | $\$$                                    |
| \\\          | 在数学公式中是换行                      | $a=x+y\\b=y$                            |
| _            | 后跟内容为下标                          | $a_i$                                   |
| ^            | 后跟内容为上标                          | $a^i$                                   |
| {}           | 被括号起来的公式是一组内容              | $x_{22} y^{(x)} x^{y^z}$                |
| \frac        | 分数                                    | $\frac{1}{a}$                           |
| \sqrt        | 根号                                | $\sqrt{xy}+\sqrt[a]{x}$                 |
| \ldots       | 跟文本底线对齐的省略号                  | $a_{i\ldots{n}}$                        |
| \cdots       | 跟文本中线对齐的省略号                  | $i\cdots n$                             |
| \sum         | 求和                                    | $\sum_{k=1}^nkx $                       |
| \int         | 积分                                    | $\int_a^b$                              |
| \limits      | 强制上下限在上下侧                      | $\sum\limits_{k=1}^nkx $                |
| \nolimits    | 强制上下限在右侧                        | $\sum\nolimits_{k=1}^nkx$               |
| \overline    | 上划线                                  | $\overline{a+b}$                        |
| \underline   | 下划线                                  | $\underline{a+b}$                       |
| \overbrace   | 上花括号                                |   $\overbrace{a+b+\dots+n}^{m个}$                        |
| \underbrace  | 下花括号                                | $\underbrace{a+b+\dots+n}_{m个}$ |
| \vec         | 向量                                    | $\vec{a}$                           |
| \lim | 极限 | $\lim_{x \to \infty}$ |
| \left \right | 用于自适应匹配分隔符如{,(, | 详情见**方程组** |
| \approx | 约等于 | $\approx$ |
| \cdot | 点乘 | $A\cdot B$ |
| \times | 叉乘 | $5\times7$ |
| \sim | 波浪号 | $\sim$ |

# [Latex的各种帽子](https://www.cnblogs.com/huangshiyu13/p/6936884.html)

\hat{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603120154086-1796504419.png)

 

\widehat{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115206883-1221744972.png)

 

\tilde{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603120217180-1447460397.png)

 

\widetilde{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115230914-856427055.png)

 

\overline{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115258914-2058523655.png)

 

\underline{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115337914-281021826.png)

 

\overbrace{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115357946-879399711.png)

 

\underbrace{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115418664-307206021.png)

 

\overset{a}{b}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115449805-1519805797.png)

 

\underset{a}{b}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115513586-1854738396.png)

 

\overleftarrow{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115537008-1609428112.png)

 

\overrightarrow{A}

![img](https://images2015.cnblogs.com/blog/798706/201706/798706-20170603115558133-701562040.png)

### 其他常见例子

注意使用\begin{equation}...\end{equation},equation对应每种表达式，但是单行的情况下可以不用

- **基本预算符：**$\pm$  $\div$

- **矩阵与行列式**

```latex
$$
	\begin{matrix}
	1 & x & x^2\\
	1 & y & y^2\\
	1 & z & z^2\\
	\end{matrix1}
$$

```

$$
\begin{matrix}
	1 & x & x^2\\
	1 & y & y^2\\
	1 & z & z^2\\
	\end{matrix}
$$


 行列式：

```latex
$$
X=\left|
	\begin{matrix}
		x_{11} & x_{12} & \cdots & x_{1d}\\
		x_{21} & x_{22} & \cdots & x_{2d}\\
		\vdots & \vdots & \ddots & \vdots \\
		x_{11} & x_{12} & \cdots & x_{1d}\\
	\end{matrix}
\right|
$$
```


$$
X=\left|
	\begin{matrix}
		x_{11} & x_{12} & \cdots & x_{1d}\\
		x_{21} & x_{22} & \cdots & x_{2d}\\
		\vdots & \vdots & \ddots & \vdots \\
		x_{11} & x_{12} & \cdots & x_{1d}\\
	\end{matrix}
\right|
$$

- **分隔符**

各种括号用 () [] { } \langle\rangle 等命令表示,注意花括号通常用来输入命令和环境的参数,所以在数学公式中它们前面要加 \。可以在上述分隔符前面加 \big \Big \bigg \Bigg 等命令来调整大小。

- **箭头**

```latex
$\leftarrow$
```

$$
\leftarrow
$$

![在这里插入图片描述](https://img-blog.csdnimg.cn/20181104140310286.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhcHB5ZGF5X2Q=,size_16,color_FFFFFF,t_70)

- **方程式**

  ```latex
  E=mc^2
  ```

  $$
  E=mc^2
  $$

  

- **分段函数**

  ```latex
  $$
  f(n)=
  	\begin{cases}
  		n/2, & \text{if $n$ is even}\\
  		3n+1,& \text{if $n$ is odd}
  	\end{cases}
  $$
  
  ```

  $$
  f(n)=
  	\begin{cases}
  		n/2, & \text{if $n$ is even}\\
  		3n+1,& \text{if $n$ is odd}
  	\end{cases}
  $$

- **方程组**

  ```latex
  $$
  \left\{
  	\begin{array}{c}
  		a_1x+b_1y+c_1z=d_1\\
  		a_2x+b_2y+c_2z=d_2\\
  		a_3x+b_3y+c_3z=d_3
  	\end{array}
  \right.
  $$
  
  ```

  $$
  \left\{
  	\begin{array}{c}
  		a_1x+b_1y+c_1z=d_1\\
  		a_2x+b_2y+c_2z=d_2\\
  		a_3x+b_3y+c_3z=d_3
  	\end{array}
  \right.
  $$

### 常用公式

- **线性模型**

  ```latex
  $$
  	h(\theta) = \sum_{j=0} ^n \theta_j x_j
  $$
  ```

$$
h(\theta) = \sum_{j=0} ^n \theta_j x_j
$$

- **均方误差**

  ```latex
  $$
  	J(\theta) = \frac{1}{2m}\sum_{i=0}^m(y^i - h_\theta(x^i))^2
  $$
  ```

  $$
  	J(\theta) = \frac{1}{2m}\sum_{i=0}^m(y^i - h_\theta(x^i))^2
  $$

  **求积公式**

  ```latex
  $$
  	H_c=\sum_{l_1+\dots +l_p}\prod^p_{i=1} \binom{n_i}{l_i}
  $$
  ```

$$
H_c=\sum_{l_1+\dots +l_p}\prod^p_{i=1} \binom{n_i}{l_i}
$$

- **批量梯度下降**

  ```latex
  $$
  	\frac{\partial J(\theta)}{\partial\theta_j} = -\frac1m\sum_{i=0}^m(y^i - 	h_\theta(x^i))x^i_j
  $$
  ```

  $$
  \frac{\partial J(\theta)}{\partial\theta_j} = -\frac1m\sum_{i=0}^m(y^i - 	h_\theta(x^i))x^i_j
  $$

- **推导过程**

  ```latex
  $$
  \begin{align}
  	\frac{\partial J(\theta)}{\partial\theta_j}
  	& = -\frac1m\sum_{i=0}^m(y^i - h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i))\\
  	& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_j x^i_j-y^i)\\
  	&=-\frac1m\sum_{i=0}^m(y^i -h_\theta(x^i)) x^i_j
  \end{align}
  $$
  
  ```

  $$
  \begin{align}
  	\frac{\partial J(\theta)}{\partial\theta_j}
  	& = -\frac1m\sum_{i=0}^m(y^i - h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i))\\
  	& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_j x^i_j-y^i)\\
  	&=-\frac1m\sum_{i=0}^m(y^i -h_\theta(x^i)) x^i_j
  \end{align}
  $$

- 字符下标

  ```latex
  $$
  \max \limits_{a<x<b}\{f(x)\}	
  $$
  ```

$$
\max \limits_{a<x<b}\{f(x)\}
$$

### 参考

1. https://blog.csdn.net/baidu_38060633/article/details/79183905
2. https://www.latex-project.org/help/

注：如有问题，请指正，谢谢

