#### 矩阵的乘法 缩放/旋转/倾斜 一个几何平面 scales/rotates/skews a geometric plane
![image](https://user-images.githubusercontent.com/31954987/230701943-7295c984-409a-450f-a046-52aef55d178e.png)

#### 矩阵的乘法 组成线性运算 matrix multiplications composes linear operations
从技术正确的定义 the technically accurate definition: yes 新的矩阵由原有的函数构成 new matrix that composes the og function 然而被运算的矩阵并非线性运算 however the matrix being operated on is not a linear operation 而是一系列的向量或者点 but a set of vectors or data points 

#### 矩阵的乘法是有关信息流的 matrix multiplication is about information flow, converting data to code and back 

> ```
> 
>                               -    -
>                               |D  D|
>                               |a  a|
>                               |t  t|
>                               |a  a|
>                               -    -
>                             
> -    -      -         -     
> |    |      |Operation|
> |D  D|      |Operation|
> |a  a|      |Operation|
> |t  t|      |Operation|
> |a  a|      |Operation|
> |    |      |Operation|
> -    -      -         -
> 
> ```

把线性代数当作“数学电子表格” think of linear algebra as "math spreadsheets" 
- 我们存储信息在不同的电子表格中 store information in various spreadsheets("matrices")
- 一些数据被看作是函数来运用一些被当作数据点 some of the data are seens as functions to apply, others as data points to use
- 在理解为函数和理解为向量之间切换 swap between function & vector interpretation as needed
把数据作为几何向量，data as geometric vectors 矩阵作为构造函数 matrix as a composing functions 但本质上都是经过系统的信息流 information flowing thru a system.

#### 工程师的直觉：代码是数据是代码 Programmer‘s intuition: Code is Data is Code
words as data, text is prose 单字作为数据，文本作为散文
- 测量值转化为公制单位 measurements to metric units
- swap ingredient
- adjust for altitude or different equipment

![image](https://user-images.githubusercontent.com/31954987/230767981-6d894971-96be-4540-8041-863d9092e40f.png)

编译器把程序当作文字，编辑它，并最终输出“指令” compilers treat a program as text, modify it, and eventually output "instructions"
|方向orientation|表达式formula|数学含义mathematical definition|计算机科学computer science|
|--------------|-------------|------------------------------|------------------------|
|垂直vertical column   |[3; 4; 5] 意味着 x = (3, 4, 5)|x 是一个向量数据 ; 用来分开每一行|                        |
|水平horizontal row |[3 4 5]   意味着 f(a, b, c) = 3a + 4b + 5c|三个输入->函数->回传1个值|                        |

![image](https://user-images.githubusercontent.com/31954987/230776197-5f9b86d1-9f64-4c42-9ef5-8f284305baf9.png)

> ```
> [-Operation->]       -   -  -     -
> -             -      | D |  | -x->|
> |  x   y   z  |      | a |  |     |
> -             -      | t |  | -y->|
>                      | a |  |     |
>                      |   |  | -z->|
>                      -   -  -     -
> 1个函数3个参数          1个向量3个元素
> 1个水平函数包含3个数据点  3个函数1个参数
> ```


以不同顺序结合数据和代码
如果 `x` 是 column vector 3 个 entries (`[3; 4; 5]`), then `x'` is:
- a function taking 3 arguments (`[3 4 5]`)
- `x'` can still remain a data vector, but as three seperate entries, the transpose 转置 “split it up”
类似的，如果 `f = [3 4 5]` is row vector, then `f'` can mean:
- a single data vector, in a vertical column.
- `f'` is seperated into three functions (each taking a single input).

练习：
当我们看到 `x' * x` `x'`(as single function) is working on `x`(a single vector), 结果是一个点积**dot product**

![image](https://user-images.githubusercontent.com/31954987/230847680-54d4e0e5-2c81-49e0-83c5-efbe2fa17298.png)

> ```
> 多functions 多vectors //混合每个function and input
> -      -                 -            -
> | -x-> |    -      -     | xx  xy  xz |
> | -y-> |    | x y z|  =  | yx  yy  yz |
> | -z-> |    -      -     | zx  zy  zz |
> -      -                 -            -
> ```

把 `xx` 看作 `x(x)` 函数x "function x" working on "vector x" 计算

#### 矩阵的移调 The Matrix Transpose

#### 矩阵的乘法与信息流相关 转换数据为代码而后转回 
