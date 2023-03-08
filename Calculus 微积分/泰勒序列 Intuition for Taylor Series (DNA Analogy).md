##  Intuition for Taylor Series (DNA Analogy) //泰勒序列的直觉
### Pulling information from a point  //从一个点拉取信息
#### - <img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/223323099-1689e082-9c83-417e-8512-1d875bcc6daf.png"> 函数在点x的值
#### - <img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/223323326-d90f12b6-1780-4d05-9ca8-8a48fcf5f560.png"> 一阶导，函数的变化率（the velocity 速度）
#### - <img width="60" alt="image" src="https://user-images.githubusercontent.com/31954987/223628596-60b6f495-2dbf-40b7-8045-b76045ebf899.png"> 二阶导(the acceleration 加速度)
#### - <img width="60" alt="image" src="https://user-images.githubusercontent.com/31954987/223628425-2d4bce5b-9c38-4523-a7fe-fb1704697a2c.png"> 三阶导
(acceleration of the acceleration)


### Growing a Function from a point //从一个点生成函数
#### imagining any function, at its core, is a polynomial (with possible infinite terms): 想象任何函数的核心实际都是一个多项式(无限形式)
<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/223325186-9022b1fe-85d0-46bd-b0a1-f7f4d9acc976.png"> 
to rebuild our function, we start at a fixed point(c_0) 我们从函数值在x=0的时候插入函数
<img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/223326168-5ed96b7d-a59c-4f5f-b426-3a8237fa6cd6.png">

### Getting more DNA  //取得更多DNA
#### 现在我们有C_0, 我们如何把C_1 从等式中独立出来？
<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/223325186-9022b1fe-85d0-46bd-b0a1-f7f4d9acc976.png"> 
- 我们能否将 x = 1？那么就有<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/223334523-0b71e9fc-0fc5-489d-9046-06dc93d65845.png">
- 如果我们divide by x?
<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/223334911-e07c18f8-2543-48ce-a86d-45ddf6d84773.png">
我们能 set x = 0 让其他的terms 消失，然而我们不能 divide 0
那么办法就是using derivative!
we can take the derivative of the blueprint of <img width="50" alt="image" src="https://user-images.githubusercontent.com/31954987/223339293-5cbcfdd2-20b6-48b8-89be-9caf34d00c7b.png">
<img width="450" alt="image" src="https://user-images.githubusercontent.com/31954987/223340752-99e7a253-0b43-4c0d-9801-c0db501d7d8f.png">
<img width="450" alt="image" src="https://user-images.githubusercontent.com/31954987/223345820-dbdff1c7-201f-4837-a4e3-f71bf983cc52.png">

现在我们可以通过设定 x = 0 把c_1独立出来

这！泰勒序列的Magic 重复求导 设定x = 0 

- <img width="450" alt="image" src="https://user-images.githubusercontent.com/31954987/223629360-a0945834-fec5-4d6a-a970-af579c9771c3.png">
于是我们可以通过 设定x = 0 来独立 C_2
- <img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/223630056-7a453740-8cf9-486b-bec8-e54048808366.png">


####  The Taylor Series for a function around point x=0 is: //泰勒序列函数围绕点 x=0
### Example: Taylor Series of sin(x)  //sin(x)的泰勒序列
####  1) Sine has infinite terms  //Sine有无限♾️术语
####  2）Sine is missing every other term  //正弦每隔一个术语就没有
####  3) Different starting positions have different DNA  //不同的起点有不同的DNA
### Application: Function Approximations//函数的逼近
### Application: Comparing Functions//对比函数
### //
####  Relationship to Fourier Series  //傅立叶序列的关系
####  Does the Taylor Series always work? //泰勒序列一直有效么？
####  Turning geometric to algebraic definitions  //把几何定义转化为代数定义
