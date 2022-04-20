# Typora编写基于LaTex的数学公式常见示例

------

​                                                                                                                                   ==Author: GisonWin==


#### 使用Typora编写基于LaTex的数学公式

1. 如何在typora中插入数学公式

   在typora中输入$$+回车,即可看到多行公式编写,输入$ 行间公式$ .公式编辑支持LaTex语法.

2. 如何导出typora内容

   导出支持图片,PDF,Word等常见格式.

3. 上标 ^ 下标 _

   ```shell
   #-----------------------
   \begin{split}
   & a^2 
   & a^{2^{3}} 
   & a^{332} \\
   & a_1 
   & a_{1_{23}}
   & a_{1}^{32}
   \end{split}
   ```

   $$
   \begin{align}
   & a^2 
   & a^{2^{3}} 
   & a^{332} \\
   & a_1 
   & a_{1_{23}}
   & a_{1}^{32}
   \end{align}
   $$

   

4. 插入水平线

   ```shell
   语法为\overline ,\underline
   #-----------------------
   \overline{a+b+c}=\underline{c+b+a}
   ```

   $$
   \overline{a+b+c}=\underline{c+b+a}
   $$

5. 平方根

   ```shell
   \sqrt[n],n默认为2
   #-----------------------
   \sqrt[5]{a^3+5ab+b^3}
   ```

   $$
   \sqrt[5]{a^3+5ab+b^3}
   $$

6. 插入水平大括号

   ```shell
   语法 \overbrace \underbrace
   #--------------------
   \begin{split}
   & \overbrace{1,2,3,\dots,100}^{100} \\
   & \underbrace{1,2,3,5,\dots,128}_{40} \ (斐波纳契数列)\\
   \end{split}
   ```

   $$
   \begin{align}
   & \overbrace{1,2,3,\dots,100}^{100} \\
   & \underbrace{1,2,3,5,\dots,128}_{40} \ (斐波纳契数列)
   \end{align}
   $$

   

7. 分数和省略号

   ```shell
   语法 \frac{}{},第一个花括号为分子,第二个花括号为分母
   #--------------------------------
   \frac{1}{10} \\
   1/10 \\
   \cdots \\
   \dots \\
   ```

   $$
   \begin{align}
   \frac{1}{10} \\
   1/10 \\
   \cdots \\
   \dots \\
   \end{align}
   $$

8. 积分

   ```shell
   语法为\int
   #------------------------------
   \begin{split}
   & \int_{a}^{b} \\
   & \int{x}dx \\
   & \int_{1}^{2}{xdx} \\
   \end{split}
   ```

   $$
   \begin{align}
   & \int_{a}^{b} \\
   & \int{x}dx \\
   & \int_{1}^{2}{xdx} \\
   \end{align}
   $$

9. 极限

   ```shell
   语法 \lim
   #-----------------------------
   \begin{split}
   & \lim{a+b} \\
   & \lim_{n\rightarrow+\infty} \\
   \end{split}
   ```

   $$
   \begin{align}
   & \lim{a+b} \\
   & \lim_{n\rightarrow+\infty} \\
   \end{align}
   $$

   

10. 求和

    ```shell
    语法\sum\limits  \sum 两种写法都可以
    #-------------------------
    \begin{split}
    & \sum_{a}^{b} \\
    & \sum\limits_{a}^{b} \\
    \end{split}
    ```

    $$
    \begin{align}
    & \sum_{a}^{b} \\
    & \sum\limits_{a}^{b} \\
    \end{align}
    $$

    

11. 向量

    ```shell
    单符号 \vec  多符号用\overrightarrow  \overleftarrow
    #------------------------------
    \begin{align}
    & \vec a=\overrightarrow{AB}=\overleftarrow{BA} \\
    \end{align}
    ```

    $$
    \begin{align}
    & \vec a=\overrightarrow{AB}=\overleftarrow{BA} \\
    \end{align}
    $$

    

12. 空格,乘积

    ```shell
    空格语法为 \quad 两个空格 \qquad 
    #-----------------------------------------
    \begin{split}
    & a\quad b\\ #一个m的宽度
    & a\qquad b \\ #两个m的宽度
    & a\ b \\ # 1/3宽度      大空格
    & a\; b \\ # 2/7m宽度    中等空格
    & a\, b \\ #1/6m 宽度    小空格
    & ab \\ #没有空格
    & a\!b \\ #缩进1/6m宽度   紧贴
    \end{split}
    ```

    $$
    \begin{align}
    & a\quad b\\
    & a\qquad b \\
    & a\ b \\
    & a\; b \\
    & a\, b \\
    & ab \\
    & a\!b \\
    \end{align}
    $$

    ```shell
    乘积语法\prod
    #---------------------------------------------
    \begin{split}
    &  \prod{x} \\
    &  \prod_{n=1}^{99}{x_n} \\
    \end{split}
    ```

    $$
    \begin{align}
    &  \prod{x} \\
    &  \prod_{n=1}^{99}{x_n} \\
    \end{align}
    $$

13. 矩阵与行列式

    ```shell
    矩阵:\begin{matrix}... \end{matrix},使用&分隔同行元素,\\换行
    #--------------------------------------
    \begin{matrix}
    1 & x & x^2 \\
    1 & y & y^2\\
    1 & z & z^3 \\
    \end{matrix}
    ```

    $$
    \begin{align}
    \begin{matrix}
    1 & x & x^2 \\
    1 & y & y^2\\
    1 & z & z^3 \\
    \end{matrix}
    \end{align}
    $$

    ```shell
    行列式:\left| \begin{matrix} ... \end{matrix} \right|
    #------------------------------------------
    X=\left|
    \begin{matrix}
    x_{11} & x_{12} & \cdots & x_{1d} \\
    x_{21} & x_{22} & \cdots & x_{2d} \\
    \vdots & \vdots & \ddots & \vdots \\
    x_{11} & x_{12} & \cdots & x_{1d} \\
    \end{matrix}
    \right|
    ```

    $$
    X=\left|
    \begin{matrix}
    x_{11} & x_{12} & \cdots & x_{1d} \\
    x_{21} & x_{22} & \cdots & x_{2d} \\
    \vdots & \vdots & \ddots & \vdots \\
    x_{11} & x_{12} & \cdots & x_{1d} \\
    \end{matrix}
    \right|
    $$

    

14. 分段函数/花括号

    ```shell
    语法:\begin{cases}...\end{cases}
    #--------------------------------------------------------
    f(n)=
    \begin{cases}
    	n/2, & \text{if $n$ is even}\\
    	3n+1,&\text{if $n$ is odd} \\
    \end{cases}
    ```

    $$
    f(n)=
    \begin{cases}
    	n/2, & \text{if $n$ is even}\\
    	3n+1,&\text{if $n$ is odd} \\
    \end{cases}
    $$

    

15. 方程组

    ```shell
    ##语法:\left \{ \begin{array}{c} ... \end{array} \right.
    ##注意 right.后面的点,因为方程组只有向右的括号.所以点作为结束.
    #----------------------------------------------
    \left \{
    \begin{array}{c}
    a_1x+b_1y+c_1z=d_1\\
    a_2x+b_2y+c_2z=d_2\\
    a_3x+b_2y+c_3z=d_3\\
    \end{array}
    \right.
    ```

    $$
    \left \{
    \begin{array}{c}
    a_1x+b_1y+c_1z=d_1\\
    a_2x+b_2y+c_2z=d_2\\
    a_3x+b_2y+c_3z=d_3\\
    \end{array}
    \right.
    $$

    

16. 箭头 

    ```shell
    \leftarrow 左箭头 \longrightarrow 长右箭头 \Leftarrow 左双箭头 \Rightarrow 右双箭头
    \longleftarrow 长左箭头 \leftrightarrow 左右箭头 \Leftrightarrow 左右双箭头
    \Longleftarrow 长双左箭头 \Longrightarrow 长双右箭头  \Longleftrightarrow 长左右双箭头
    #-----------------------------
    \begin{align}
    \begin{matrix}
    \leftarrow  & \rightarrow & \leftrightarrow \\
    \longleftarrow & \longrightarrow & \longleftrightarrow \\
    \Leftarrow & \Rightarrow & \Leftrightarrow \\
    \Longleftarrow & \Longrightarrow & \Longleftrightarrow \\
    \uparrow & \downarrow &\updownarrow \\
    \Uparrow & \Downarrow &\Updownarrow \\
    \nearrow & \searrow & \swarrow & \nwarrow \\
    \mapsto & \longmapsto & \leadsto \\
    \end{matrix}
    \end{align}
    ```

    $$
    \begin{align}
    \begin{matrix}
    \leftarrow  & \rightarrow & \leftrightarrow \\
    \longleftarrow & \longrightarrow & \longleftrightarrow \\
    \Leftarrow & \Rightarrow & \Leftrightarrow \\
    \Longleftarrow & \Longrightarrow & \Longleftrightarrow \\
    \uparrow & \downarrow &\updownarrow \\
    \Uparrow & \Downarrow &\Updownarrow \\
    \nearrow & \searrow & \swarrow & \nwarrow \\
    \mapsto & \longmapsto & \leadsto \\
    \end{matrix}
    \end{align}
    $$

    

17. 小写希腊字母

    ```shell
    \alpha \theta o \upsilon \beta \vartheta \pi \phi \gamma \iota \varpi  \varphi
    \delta \kappa \rho \chi \epsilon \lambda \varrho \psi \varepsilon \mu \sigma \omega 
    \zeta \nu \varsigma \eta \xi \tau
    #---------------------------------------------------------
    \begin{split}
    \begin{matrix}
    \alpha & \theta & o  & \upsilon & \beta & \vartheta & \pi & \phi & \gamma & \iota  & \varpi   & \varphi \\
    \delta & \kappa  & \rho  & \chi & \epsilon & \lambda & \varrho & \psi & \varepsilon & \mu & \sigma &  \omega \\
     \zeta & \nu & \varsigma & \eta & \xi & \tau \\
    \end{matrix}
    \end{split}
    ```

    $$
    \begin{align}
    \begin{matrix}
    \alpha & \theta & o  & \upsilon & \beta & \vartheta & \pi & \phi & \gamma & \iota  & \varpi   & \varphi \\
    \delta & \kappa  & \rho  & \chi & \epsilon & \lambda & \varrho & \psi & \varepsilon & \mu & \sigma & \omega \\
     \zeta & \nu & \varsigma & \eta & \xi & \tau \\
    \end{matrix}
    \end{align}
    $$

18. 大写希腊字母

    ```shell
    \Gamma \Lambda \Sigma \Psi \Delta \Xi  \Upsilon \Omega \Theta \Pi \Phi
    #------------------------------------
    \begin{split}
    \begin{matrix}
    \Gamma & \Lambda & \Sigma & \Psi & \Delta & \Xi & \Upsilon & \Omega & \Theta & \Pi & \Phi \\
    \end{matrix}
    \end{split}
    ```

    $$
    \begin{align}
    \begin{matrix}
    \Gamma & \Lambda & \Sigma & \Psi & \Delta & \Xi & \Upsilon & \Omega & \Theta & \Pi & \Phi \\
    \end{matrix}
    \end{align}
    $$

    

19. 三角函数

    ```shell
    #------------------------
    \sin \\
    \cos \\
    ```

    $$
    \sin \\
    \cos \\
    $$

    

20. 对数函数

    ```shell
    #-------------------------------
    \ln2 \\ \log_28 \\ \log_{2}8 \\ \log_23^{3^{3^{300}}} \\ \lg 10
    ```

    $$
    \begin{align}
    \ln2 \\ \log_28 \\ \log_{2}8 \\ \log_23^{3^{3^{300}}} \\ \lg 10 \\
    \end{align}
    $$

21. 关系运算符

    ```shell
    \pm \times \cdot \cdots \div \neq \equiv \leq \geq
    ```

    $$
    \begin{align}
    \begin{matrix}
     \pm & \times & \div &\cdot &\cdots & \neq & \equiv & \leq & \geq \\
     \end{matrix}
    \end{align}
    $$

    

22. 居中对齐和根据"="符号对齐

    ```shell
    居中对齐,当公式比较长或一个公式中有多个"="号时,使用居中对齐方式.
    #-------------------------
    \begin{gather}
    sum1 = a+b+c+d \\
    sum2= e+f \\
    sum3=g+h+i+j+k+l \\
    \end{gather}
    #----------------------------------
    根据=对齐多列 .=号前加&
    #---------------------
    \begin{align}
    sum1 &= a+b+c+d \\
    sum2&= e+f \\
    sum3&=g+h+i+j+k+l \\
    \end{align}
    #-------------------------
    如果不加&,则以上三公式默认是右对齐
    #-----------------------------
    \begin{align}
    sum1 = a+b+c+d \\
    sum2= e+f \\
    sum3=g+h+i+j+k+l \\
    \end{align}
    ```

    $$
    \begin{gather}
    sum1 = a+b+c+d \\
    sum2= e+f \\
    sum3=g+h+i+j+k+l \\
    \end{gather}
    $$

    ---------------

    
    $$
    \begin{align}
    sum1 &= a+b+c+d \\
    sum2&= e+f \\
    sum3&=g+h+i+j+k+l \\
    \end{align}
    $$

    ----

    $$
    \begin{align}
    sum1 = a+b+c+d \\
    sum2= e+f \\
    sum3=g+h+i+j+k+l \\
    \end{align}
    $$

    

23. 公式编号

    ```shell
    前后加上\begin{equation} \end{equation},公式会自动编号
    公式后要空一行再接下一段,否则下一段开头不会自动缩进
    #--------------------------------
    \begin{equation}
    X(k)=\sum_{n=0}^{N-1} x(n)e^{-j \frac{2 \pi}{N} k n}=\sum_{n=0}^{N-1} x(n) W_N^{kn},\quad k=0,1,...,N-1
    \end{equation}
    ```
    
    $$
    \begin{equation}
    X(k)=\sum_{n=0}^{N-1} x(n)e^{-j \frac{2 \pi}{N} k n}=\sum_{n=0}^{N-1} x(n) W_N^{kn},\quad k=0,1,...,N-1 
    \end{equation}
    $$





















