#### Seeing imaginary numbers as rotations //把虚数看作是旋转
![image](https://user-images.githubusercontent.com/31954987/198835936-c7eb8875-1942-444d-9aee-0a0879eff276.png)
#### i, the square root of -1, is a number in a different dimension! Once that clicks, we can use multiplication to "combine" rotations of two complex numbers: 
![image](https://user-images.githubusercontent.com/31954987/198836165-b3cbc4d2-9ca9-4087-94b5-f097d5471ad0.png)
#### // 复数的乘法：没有使用sine或者cosine来添加角度

### The Boring Explanation: How?
#### write the complex numbers as polar coordinates(radius & angle) //将复数做极坐标(半径& 角度)
![image](https://user-images.githubusercontent.com/31954987/198837607-e15e3e22-4bc8-454a-8573-67ce45024df9.png)
#### next, take the product, group by real/imaginary parts:
![image](https://user-images.githubusercontent.com/31954987/198837683-877a5c8f-f286-404e-804b-43160365d0cd.png)
![image](https://user-images.githubusercontent.com/31954987/198837707-32b8260e-6b05-4929-ad6c-c743cc8d8263.png)

#### how ⬆️ matches the sine and cosine angle addition formulas:
![image](https://user-images.githubusercontent.com/31954987/198837845-2220847d-0299-4f6f-8a9e-8fd92c058886.png)



### The Fun Explanation: Why!
#### see why we can multiply two complex numbers and add the angles. //两个复数相乘 &角度相加
![image](https://user-images.githubusercontent.com/31954987/198837949-fedad40e-68a7-42f9-b296-a4627979a06d.png)

- **Regular multiplication** ("times 2") scales up a number (makes it larger or smaller) //缩放
- Imaginary multiplication ("times i") rotates you by 90 degrees //虚数乘法

#### Multiplying by (2 + i): "double number -- add in a perpendicular rotation"

### Visualizing Complex Multiplication //视觉化复数乘法✖️
#### That was easy -- a real number (4) times a complex (3+i). What about two complex numbers ("triangles"), like <math xmlns="http://www.w3.org/1998/Math/MathML">
  <mo stretchy="false">(</mo>
  <mn>3</mn>
  <mo>+</mo>
  <mn>4</mn>
  <mi>i</mi>
  <mo stretchy="false">)</mo>
  <mo>&#x22C5;</mo>
  <mo stretchy="false">(</mo>
  <mn>2</mn>
  <mo>+</mo>
  <mn>3</mn>
  <mi>i</mi>
  <mo stretchy="false">)</mo>
</math>

#### ![image](https://user-images.githubusercontent.com/31954987/198838230-bdd7d0d5-b688-442a-80bf-6a67efcd52d5.png)


#### alternate explanation! 
![image](https://user-images.githubusercontent.com/31954987/198838329-3b39f2f4-8f98-4f5e-9c53-bf65a930a091.png)
#### Instead of grouping the multiplication by triangle, we analyze each part of the FOIL (first, outside, inside, last). Adding each component takes us along a path and ends in the same spot!


### But What About the Angles? //角度如何？
![image](https://user-images.githubusercontent.com/31954987/198838488-c12ed1cb-c5d8-46b2-8cec-f138312995a9.png)

### Side Effects May Include Scaling //等级
#### Notice how we're making larger copies of our original triangle and adding them together. What's the change in size compared to our starting blue triangle?

#### Well, let's call our original length "x". Whatever it is, we end up getting a new triangle layered on top, with a size of 2x + 3x (a + bi in general). And from Pythagoras (I love that gentleman) the "real" distance is

![image](https://user-images.githubusercontent.com/31954987/198838688-8099fa80-3569-49fc-8c8b-79534bec445b.png)

#### That is, we take our original distance (x) and scale it by the size of the new triangle (size of a + bi). //取原始距离，缩放新的三角的大小
#### If the new triangle is size 1 <math xmlns="http://www.w3.org/1998/Math/MathML">
  <msup>
    <mi>a</mi>
    <mn>2</mn>
  </msup>
  <mo>+</mo>
  <msup>
    <mi>b</mi>
    <mn>2</mn>
  </msup>
  <mo>=</mo>
  <mn>1</mn>
</math>
then the distance won't change!

### A Few Thoughts
#### Real satisfying insight comes from playing with analogies and examples
#### Polya 乔治波利亚 said it well:"when you have satisfied yourself that the theorem is true, you start proving it"
