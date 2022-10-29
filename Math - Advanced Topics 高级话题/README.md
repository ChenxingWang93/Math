### 1. A Visual, Intuitive Guide to Imaginary Numbers 虚数的直觉感受
### Math Mindset 数学心态
- What **relationship** does this model represent? **关系**
- What real-world items share this relationship? **现实世界中的关系**
- Does this relationship **make sense to me**? **现实世界中的这种关系能否帮助我们解决问题**

####  🌰 Imaginary Number 虚数
![image](https://user-images.githubusercontent.com/31954987/196034995-c03ee2fe-5391-4f15-9b52-9c03cbb3257d.png)
- **What's an imaginary number?**
##### a number pointing sideways(North⬆️/South⬇️) Gauss wanted them called "lateral" numbers 高斯称他们为“侧”向数
##### what does i means？i是什么意思？
##### i points North. 
##### i ⬆️逆时针旋转 90度
##### (i*i = -1) ⬆️⬅️逆时针旋转 180度
##### (i^4 = 1) ⬆️⬅️⬇️➡️旋转 360度
- **is i useful?** imaginary numbers makes 2d rotation problems simple.虚简化了二维旋转问题

####  A Visual, Intuitive Guide to Imaginary Number
- **Focusing on relationships, not mechanical formulas**. //关注**关系**
- **Seeing complex numbers as an upgrade to our number system**, just like 0，decimals and negatives //把复数看作**数系统的升级**
- **Using visual diagrams**, to understand the idea rather text /**/视觉化！**
##### Learning by analogy. imaginary numbers' ancestor, the negatives

|Fun Fact🤔事实 |Negative Numbers(-x) 负数   |Complex Numbers(a+bi) 复数  |
|--------------|---------------------------|----------------------------|
|Invented to answer|"what is 3-4?"|"What is sqrt(-1)"                   |
|Strange because.. |_How can you have less than nothing?_|_How can you take the square root of less than nothing?_|
|Intuitive meaning |"_Opposite_"|"_Rotation_"|
|considered absurd until|1700s|today😊       ｜
|Multiplication cycle[&general pattern]|1, -1, 1, -1... X, -X, X, -X...|1, i, -1, -i...X, Y, -X, -Y...|
|Measure size with|Absolute value <img width="60" alt="Screen Shot 2022-10-29 at 15 49 56" src="https://user-images.githubusercontent.com/31954987/198820377-bc754431-e386-49d3-8de0-694b0cf488d1.png">|pythagorean theorem勾股定理 <img width="68" alt="Screen Shot 2022-10-29 at 15 49 12" src="https://user-images.githubusercontent.com/31954987/198820342-18b28404-11db-442e-a772-953fa39ea472.png">｜
#### euler, who discovered e


### 3. Why Complex Multiplication Works? 复数的乘法
![image](https://user-images.githubusercontent.com/31954987/196349564-3290b837-1aa8-4160-ba0a-a9433524da16.png)
#### rotate twice in other direction(clockwise) to turn 1 into -1. This is "negative" rotation or a multiplication by -i:

![image](https://user-images.githubusercontent.com/31954987/198820724-f8b0bf54-d826-4897-9024-32dda8d5891d.png)
#### if we multiply by -i twice, the first multiplication would turn 1 into -i, and the second turn -i into -1. there two square roots of -1: i and -i
- i is a "new imaginary dimension" to measure a number
- i(or -i) is what numbers "become" when rotated


### 2. Intuitive Arithmetic with Complex Numbers
|Complex Operation 复数运算 |Intuitive Meaning|
|--------------|---------------------------|
|Magnitude:$ 大小|z|$|Distance from zero:$|z|=\sqrt{a^{2}+b^{2}}$ |
|Addition &Subtraction|Sliding numbers|
|Multiplication|Scale by magnitude, add angles|
|Division|Shrink by magnitude,subtract angles|
|Complex Conjugate:z*|"Imaginary Reflection": Same size, opposite angle if z = 3 + 4i, then z* = 3 - 4i|
|Conjugate Properties 共轭属性|(x + y)^* = x^* + y^*[add then reflect = reflect and add]  (xy)^* = x^* y^*[multiply then reflect = reflect and multiply]|

#### Complex Variables 复数 变量
with complex numbers, there's two dimensions to talk about, when writing 
_z = 3 + 4i_
![image](https://user-images.githubusercontent.com/31954987/196573678-d1ce1ec7-8e90-468e-8383-0833b0fb9b02.png)

#### Measuring Size 大小
complex numbers use two independent axes, size(magnitude) using Pythagoream Theorem 勾股定理:
![image](https://user-images.githubusercontent.com/31954987/196574430-31a579f9-5d7d-464d-a6ae-6738abb45e9c.png)
##### A number of _z = 3 + 4i_ would have a magnitude of 5(勾三股四弦五), 
##### The shorthand for "magnitude of z" is this |z|, 
##### Magnitude of a complex number: "distance from zero", Absolute value of negative: "distance from zero".

#### Complex Addition and Subtraction 复数的 加法与减法
![image](https://user-images.githubusercontent.com/31954987/196575412-eeffe598-e9b8-4b24-895b-1d9d64002c1c.png)
##### Adding (3 + 4i) to (-1 + i) equals to 2 + 5i.
##### a visual representation of how "independent components" are combined: we track the real and imaginary parts separately.

##### Subtraction is the reverse of addition - it is sliding in the opposite direction.
Subtracting (1 + i) is the same as adding -1*(1 + i), or adding (-1 - i)

#### Complex Multiplication ✖️
##### when we multiply two complex number(x and y) to get z:
- Add the angles: angle(z) = angle(x) + angle(y)
- Multiply the magnitudes: |z| = |x| * |y|

#### Complex Division 复数 ➗
##### Division is the opposite of multiplication, just like subtraction is the opposite of addition. when dividing complex numbers (x divided by y), we

- **Subtract angle:** angle(z) = angle(x) - angle(y)
- **Divide by magnitude:** |z| = |x| / |y|

#### Introducing Complex Conjugates 复数 的共轭性质
![image](https://user-images.githubusercontent.com/31954987/196579520-df1d376e-3f42-4e2c-9886-083b94e894c1.png)

z = a + bi,
z* = a - bi called the "complex conjugate", it has the same real part, but the "mirror image" in the imaginary dimension. the conjugate of "imaginary reflection" has the same magnitude, but the opposite angle!

![image](https://user-images.githubusercontent.com/31954987/196958516-56c75a1b-3800-4b0b-b73d-3583e0440c9d.png)


##### Learning by analogy. imaginary numbers' ancestor, the negatives
