## How to Understand Derivatives: The Product, Power and Chain Rules  //如何理解导数：乘积、幂和🔗链规则
My take on derivatives:
- function f: We have a system to analyze //函数f: 我们有一个系统需要进行分析
- f'(aka df/dx): moment-by-moment behavior //f'函数f的导数：是函数f的瞬时⌚️行为
- (h = f + g): f is just part of a bigger system //(h = f + g)中函数f只是大系统中的一个子系统
- Using the behavior of the parts, to predict the behavior of the whole //目的在于使用函数局部的行为，来预测整体的行为

每一部分都有 "point of view" about how much change it added. Combine every point of view to get the overall behavior  //将每一部分变化量相加得到整体函数的行为

|Concept 概念|Intuition 直觉|
|-------|---------|
|Function f(x) 函数f(x)| Turns input(x) into output(y)  把输入(x)转化为输出(y)|
|Derivative of f(x) f(x)的导数| Wiggle x, how much does y change? x摆动, y会随之变化?<img width="610" alt="Screen Shot 2022-10-18 at 00 55 05" src="https://user-images.githubusercontent.com/31954987/196237711-e0922a55-e10b-4663-9774-7a0ebd4cd19a.png">|
|Derivative of system 导数|Combined perspective of each part 结合每部分的角度|
|Addition Rule[f+g]' ➕  导数的加法法则|Add contributions from f and g  f, g的贡献相加|
|Product Rule[f*g]' ✖️  导数的乘法法则|Add contributions:a slice from f,a slice from g|
|Power Rule[x^n] 导数的幂乘方|Combine N different perspectives  |
|Chain Rule 链式规则|Zoom into a perspective's root cause|


### Functions: Anything, Anything But Graphs // 函数图像之外的理解
#### 不要一下子就想到"f(x) = x^n"的函数图像
#### derivative rules are about machinery.  //导数是有关于机械
#### the function as the process "input(x) => f => output(y)" //函数作为过程 把x作为输入 函数f 输出y
![image](https://user-images.githubusercontent.com/31954987/196243399-e98cd22e-6f31-4334-a2cf-52a96a4667be.png)

####
|||constant lead cam 恒定lead凸轮⬇|
|---|---|---|
|<img width="625" alt="Screen Shot 2022-10-18 at 01 28 36" src="https://user-images.githubusercontent.com/31954987/197349664-7f5fcb7c-c8f3-487b-a8be-e6f1882d4c91.png">   |<img width="625" alt="Screen Shot 2022-10-23 at 00 12 52" src="https://user-images.githubusercontent.com/31954987/197349739-2b63b97f-1715-4593-a548-e4c6a1b1fea4.png">|<img width="626" alt="Screen Shot 2022-10-23 at 00 16 13" src="https://user-images.githubusercontent.com/31954987/197350245-88420328-8750-4c6c-9271-54a20a65fbf6.png">|


|reciprocal cam 倒数凸轮⬇|||
|---|---|---|
|<img width="625" alt="Screen Shot 2022-10-23 at 00 27 20" src="https://user-images.githubusercontent.com/31954987/197350650-630fa9ff-d35c-4048-8bc8-2ccbaf321d23.png">   |<img width="625" alt="Screen Shot 2022-10-23 at 00 29 03" src="https://user-images.githubusercontent.com/31954987/197350776-8b697382-417b-40b7-abbe-e821ec1039a3.png">   |<img width="628" alt="Screen Shot 2022-10-23 at 01 20 49" src="https://user-images.githubusercontent.com/31954987/197353808-e78162bb-2c79-4ba7-9d1b-b490155e2243.png">   |


|square cam 平方凸轮⬇|tangent cam 正切⬇||
|---|---|---|
|<img width="627" alt="Screen Shot 2022-10-23 at 01 56 06" src="https://user-images.githubusercontent.com/31954987/197355639-3b5b8d26-459e-457c-9dd1-51d5b5ff3ed8.png">   |<img width="628" alt="Screen Shot 2022-10-23 at 01 59 22" src="https://user-images.githubusercontent.com/31954987/197355746-df36fae6-0e70-4f51-ab4d-082f0830015a.png">   |<img width="627" alt="Screen Shot 2022-10-23 at 02 04 33" src="https://user-images.githubusercontent.com/31954987/197355958-c5cb3ab4-d49b-4015-aa27-7c4703945b46.png">   |



#### the machine computes functions like addition and multiplication with gears -- you can _see the mechanics unfolding_  //计算机计算函数的➕与✖️ 就像齿轮⚙️ 
![image](https://user-images.githubusercontent.com/31954987/197349596-004c238e-0b56-469c-93c5-5271c5669b81.png)


### Wiggle Wiggle Wiggle // 摆动 摆动 摆动
### Addition and Subtraction // ➕ &➖
#### ![image](https://user-images.githubusercontent.com/31954987/197357542-57e35080-267d-4be3-96ea-cbe23f1e2f6a.png)
#### ![image](https://user-images.githubusercontent.com/31954987/197357557-b5f69a1d-f2f1-40d0-baee-36572ee376af.png)


### df vs df/dx //
#### sometimes we use _df_, other times _df/dx_ // 用_df_来衡量变化量
- _df_ is a general notion of "however much f changed"
- _df/dx_ is a specific notion of "however much f changed, in terms of how much x changed"
#### In calculus,sometimes we want to think about the actual change, not the ratio. Working at the "df" level gives us room to think about how the function wiggles overall. We can eventually scale it down in terms of a specific input.  //在微积分中, 实际变化, 而不是变化率, 在"df"层面
![image](https://user-images.githubusercontent.com/31954987/197356866-620a356b-80c3-45d9-801d-4b87cfdd67d2.png)


### Multiplication (Product Rule) // ✖️
![image](https://user-images.githubusercontent.com/31954987/197372039-c58e6c0f-0366-4086-9520-408d16443257.png)
#### see how each part contributes from its own point of view, and combine them:  //每一部分如何贡献自己最终结合在一起
- total change in h = f's contribution(from f's point of view) + g's contribution(from g's point of view)
![image](https://user-images.githubusercontent.com/31954987/197372555-b7337121-abeb-441c-b9b8-40d169942a85.png)
what's going on?  
- we have our system: f and g are multiplied, giving h(the area of rect)  
- Input "x" changes by dx off in the distance. f changes by some amount df. Similarly, g changes by its own amount dg. Because f and g changed, the area of the rectangle changes too.  //输入"x" dx矩形的范围改变.
- What's the area change from f's point of view? Well, f knows he changed by df, but has no idea what happened to g. From f's perspective, he's the only one who moved and will add a slice of area = df * g
- Similarly, g doesn't know how f changed, but knows he'll add as slice of area "dg * f" 
#### the overall change in the system(dh) is the two slices of area //总体的变化
![image](https://user-images.githubusercontent.com/31954987/197372845-14985733-d665-4ea8-9e3a-b21094621d08.png)

#### then "divide by dx" to write this in terms of how much x changed:  //
![image](https://user-images.githubusercontent.com/31954987/197372930-081edcbc-63b3-41fb-acc6-e98af7896e68.png)



### The Chain Rule // 链规则
#### g depends on f, which depends on x:
![image](https://user-images.githubusercontent.com/31954987/197373032-9dbf27bc-f2de-4164-967d-2e287e7f50a4.png)
![image](https://user-images.githubusercontent.com/31954987/197373033-2d597097-acd5-4d07-a49b-822dd5c6fd5b.png)

#### the chain rule let us "zoom into" a function and see how an initial change(x) can effect the final result down the line (g)  //链规则让我们"zoom into" 一个函数，看初始变化如何影响最终的变化

#### Interpretation 1: Convert the rates //解读1: 转化rates
#### a common interpretation is to multiply the rates:
![image](https://user-images.githubusercontent.com/31954987/197391972-9a030a1d-040b-4a7f-9d14-45c709d22a00.png)

#### x wiggles f. This creates a rate of change of df/dx, which wiggles g by dg/df. The entire wiggle is then 
![image](https://user-images.githubusercontent.com/31954987/197392107-6424b270-4b41-4d58-b3a4-08274c9ef7fa.png)

#### Interpretation 2: Convert the wiggle //解读2: 转化wiggle
#### I prefer to see the chain rule on the "pre-wiggle" basis:
- x wiggles by dx, so
- y wiggles by dy, so
- g wiggles by dg

#### Cool, how are they actually related? (It's the output wiggle per input wiggle):
![image](https://user-images.githubusercontent.com/31954987/197395562-9f9419d1-fd74-444f-8384-25de3d871738.png)
#### the derivative of f(df/dx)is how much to scale the initial wiggle, and the same happens to g:
![image](https://user-images.githubusercontent.com/31954987/197395657-c94f5c14-1503-49ab-8ffa-963760e5bf0d.png)
#### It will scale whatever wiggle comes along its input lever (f) by dg/df.If we write the df wiggle in terms of dx:
![image](https://user-images.githubusercontent.com/31954987/197395721-c215dc41-fa9f-413e-adb4-b6337cdc16c3.png)
#### we have another version of the chain rule: dx starts the chain, which results in some final result dg. If we want the final wiggle in terms of dx, divide both sides by dx:
![image](https://user-images.githubusercontent.com/31954987/197395873-ee5cffb1-9c07-4c81-acfb-aa47537fb5e5.png)
#### The chain rule isn't just factor-label unit cancellation -- it's the propagation of wiggle,which gets adjusted at each step. The chain rule works for several variables (a depends on b depends on c), just propagate the wiggle as you go.

#### try to "zooming into" different variable's point of view. Starting from dx and looking up, you see the entire chain of transformations needed before the impulse reaches g //zoom into不同的变量视角，完整的变化链⛓️



### Chain Rule: Example Time // 链规则：例子
#### input(x) => f:x^2 => g:f^3 => output(y)
#### f:x^2 means f squares its input. g:f^3 means g cubes its input, the value of f. For example: 
#### input(2) => f(2) => g(4) => output:64
#### Start with 2, f squares it (2^2 = 4), and g cubes this (4^3 = 64). It's a 6th power machine:
![image](https://user-images.githubusercontent.com/31954987/197396983-86b320ff-ab3a-4725-905b-2b1798f533e7.png)

#### and what's the derivative? //导数是？
![image](https://user-images.githubusercontent.com/31954987/197376684-0af6d9c5-a24f-4f33-87e5-6c575c99695c.png)
- f changes its input wiggle by df/dx = 2x
- g changes its input wiggle by dg/df = 3f^2
#### the final change is: 
3f^2 * 2x = 3 (x^2)^2 * 2x = 3 * x^4 * 2 x = 6 x^5



### Chain Rule:  // 链规则
#### Functions treat their input like a blob  //函数把他们的输入作为blob
#### In many examples, the variable "x" is the "end of the line". //在很多例子中，变量"x"是 line的结束🔚
#### How come we multiply derivatives with the chain rule, but add them for the others?



### Power Rule: Oft Memorized, Seldom Understood //经常记住，鲜有理解
#### Normally: What's the derivative of x^4? 4x^3, brought down the exponent and subtracted one. Now explain why!
#### Hrm. There's a few approaches
#### x^4 is really x * x * x * x, it's the multiplication of 4 "independent" variables. Each x doesn't know about the others, it might as well be  //是四个独立的变量相乘
#### x * u * v * w
#### think about the first x's point of view:
- it changes from x to x + dx
- the change in the overall function is [(x + dx) - x][u * v * w] = dx[u * v * w]
- the change on a "per dx" basis is [u * v * w]

#### Similarly,
- From u's point of view, it changes by du, it contributes (du/dx) * [x * v * w] on a "per dx" basis
- v contributes (dv/dx) * [x * u * w]
- w contributes (dw/dx) * [x * u * v]

#### the curtain is unveiled: x, u, v, and w are the same! The "point of view" conversion factor is (dx/dx = du/dx = dv/dx = dw/dx = 1), and the total change is (x * x * x) + (x * x * x) + (x * x * x) + (x * x * x) = 4x^3

#### In a nutshell: the derivative of x^4 is 4^x3 because x^4 has four identical "point of view" which are being combined.  //有四个不同的视角, x^4 仅仅只是意味着这4个视角重合

