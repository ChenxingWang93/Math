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

