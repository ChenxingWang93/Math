linear algebra 线性代数
矩阵，行列式，特征 matrices, determinants, eign
- Name the course _Linear Algebra_ 关注矩阵与向量 matrices & vectors 
- 用助记法mnemonics 教授概念诸如行列式顺序 Row/Column order

#### 线性代数数学等式的*math equations* 小型电子表格 *mini- spreadsheets* 

#### 从何得名 what's in a name?

![image](https://user-images.githubusercontent.com/31954987/224459595-2dfa8748-fd09-4f43-9c7c-6b07fc85a58f.png)

"algebra" = "relationships"
探索未知数之间的关系，在不知x &y 的情况下仍能求解
- <img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/224457860-577e59f5-0062-4686-ac90-b457c13a5594.png">

"Linear Algebra" = "line-like relationships" 线性代数 = 线性关系

#### 线性操作 Linear Operations
一种运算是基于输入的计算 an operation is a calculation based on some inputs 
- <img width="200" alt="image" src="https://user-images.githubusercontent.com/31954987/224459167-3eb85528-a33a-4deb-a911-5cc14b0d2a66.png"> 常规的 + 不是可预测的线性增长
- <img width="150" alt="image" src="https://user-images.githubusercontent.com/31954987/224459326-a69a2430-3f9d-4209-886d-10d6744234fa.png"> 指数的增长也不是，我们2倍输入得到的却是4倍的输出 doubled the input but quadruped the output

那什么类型的函数是线性的呢？缩放一个常量的比例
- <img width="150" alt="image" src="https://user-images.githubusercontent.com/31954987/224459656-5e3341b3-d035-4c17-9d2e-e49ef7ccecdc.png">

还能继续结合多个线性方程
- 组合多个线性方程组 <img width="450" alt="image" src="https://user-images.githubusercontent.com/31954987/224459754-40029feb-0442-46fe-abcf-202a0a3036de.png"> 为一个G:
- <img width="600" alt="image" src="https://user-images.githubusercontent.com/31954987/224459893-1171a060-2fe0-460d-9736-69e48c7aea85.png">

G 仍然是线性的，因为double 输入，double的是输出 
- <img width="900" alt="image" src="https://user-images.githubusercontent.com/31954987/224460521-eecc07d4-641f-4b84-8d4f-3538e96173b5.png">

我们可以把输入分开 split inputs apart, 独立分析每一部分 analyze them individually, 把结果结合在一起combine the result
- <img width="600" alt="image" src="https://user-images.githubusercontent.com/31954987/224460800-a9cad67b-b0d2-439c-bc84-81e3b22416c6.png">

如果我们允许非线性的操作 类似<img width="30" alt="image" src="https://user-images.githubusercontent.com/31954987/224460883-8993725f-9731-44dc-bcb9-333ee8c290b4.png">，我们不能split work 然后把结果结合在一起combine the results, 因为 <img width="200" alt="image" src="https://user-images.githubusercontent.com/31954987/224460984-30c811cb-0206-4b11-9fbf-5861bd67c168.png">

#### 组织输入与运算 organizing inputs and operations
- 追踪一系列输入 track a bunch of inputs
- 需要执行的可预测的线性操作 predictable, linear operations to perform
- 生成结果，再次变换 generate a result, transforming it again

我们如何追踪一系列输入 track a bunch of inputs?
> ```
> x
> y
> z
> ```

我们还可以这样写 <img width="80" alt="image" src="https://user-images.githubusercontent.com/31954987/224461998-644df07b-9e9c-4fd5-84bd-5e98840c78bd.png">
接着是迷你运算 mini arithmetic: 与一个实数相乘✖️ multiplication by a constant, 然后相加 with a final addition
<img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/224462143-110cbfaa-bc29-413d-9717-a163acd3ab42.png">

可把整个方程缩写为 abbreviate the entire function as <img width="50" alt="image" src="https://user-images.githubusercontent.com/31954987/224462388-ff3a0c91-c65e-43e4-a9f0-81a36f51e7c8.png">
只需要第一个输入input
- <img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/224462577-4e6bb40e-f8dc-405a-840d-b4f0580d1126.png">

如何处理多个输入集 multiple sets of inputs 在 (a,b,c) &(x, y, z) 运行 F 我们可以尝试
- <img width="200" alt="image" src="https://user-images.githubusercontent.com/31954987/224462700-8d51f8c5-8c6d-41dc-8f8f-3b09de713b00.png">
这样的方式显然是不行的，因为 F 只期待 3个输入, 而并非 6 个 

> ```
> 1st Input 2nd Input
> --------------------
> a         x
> b         y
> c         z
> ```

那么我们该如何通过 several operations 运行相同的输入 run the same input, 每个操作都有一个行 
> ```
> F: 3 4 5
> G: 3 0 0
> ```

输入：纵向 vertical columns; 运算：横向 horizontal rows; 


### 可视化矩阵 visualizing the matrix 

> ```
> --   --       --       --      
> |     |       |Operation|      --    --
> |D   D|       |Operation|      ｜D   D|
> |a   a|  /-|  |Operation|      ｜a   a|
> |t   t|  \-|  |Operation|      ｜t   t|
> |a   a|       |Operation|      ｜a   a|
> |     |       |Operation|      --    -- 
> --   --       --       --
> 输出数据         待执行运算        输入数据
> ```

> ```
>                               --    --
>                      ---      ｜D   D|
>                    /          ｜a   a| 
>                 D a t a       ｜t   t|
>               |---------|     ｜a   a|
>                    |          --    -- 
> --   --       --   |   --      输入数据 
> |     |       |Operation|      
> |D   D|       |Operation|      
> |a   a|  /-|  |Operation|      
> |t   t|  \-|  |Operation|    
> |a   a|       |Operation|
> |     |       |Operation|
> --   --       --       --
> 输出数据         待执行运算       
> ```

![image](https://user-images.githubusercontent.com/31954987/224517173-592220de-b098-4881-aff2-edcc307b30de.png)


把 一个 **输入input** 传递到 一个 **操作operation**
- **输入input(a, b, c)** -> **F** -> **输出output 3a + 4b + 5c** -> **G** -> **输出output 3a + 0 + 0**

> ```
>                                 -      -
>                                 | a  x |
> Inputs = A = [Input1 Input2] =  | b  y |
>                                 | c  z |
>                                 -      -
> 
>                   -          -    -     -
> Operations = M =  |operation1| =  |3 4 5|
>                   |operation2|    |3 0 0|
>                   -          -    -     -
> ```

一个矩阵是 用一个单变量代表 **输入** or **运算** 的电子表格 a single variable representing a spreadsheet of inputs or operations

### 技巧一：阅读顺序 The reading order

> ```
> 输入input => 矩阵matrix => 输出流output flow
> y = f(x) or f(x) = y
> 用大写字母capital letter 表示矩阵（M）
> 列中的单一输入 小写表示lowercase（x, y, z）组成输入inputs（A）& 输出outputs（B）
> 
> MA = B
>          --  --     
> --   --  |a  x|     --                         --
> |3 4 5|  |b  y|     |3a + 4b + 5c   3x + 4y + 5z|
> |3 0 0|  |c  z|  =  |     3a             3x     |
> --   --  --  --     --                         --
> 
>   运算M    输入A                  输出B
>   
> ```

### 技巧二：数字编码 The numbering 
> ```
> 矩阵大小由 **R*C** 度量，R:row count; C:column count
> 矩阵中的物件 item 也是被相同的方式引用：a_ij ith 行，jth 列
> 运算矩阵 operation matrix 2 * 3
> 输入矩阵 input matrix 3 * 2
> > [Operation Matrix] [Input Matrix]
> > [operation count x operation size] [input size x input count]
> > [m x n] [p x q] = [m x q]
> > [2 x 3] [3 x 2] = [2 x 2]
> ```

"size of operation" "size of input" (n = p) 只有当 n = p 时才能矩阵相乘 only matrices multiply 
输出矩阵 output matrix 有m operation rows for each input，and q inputs 得到一个 “m * q” 矩阵
