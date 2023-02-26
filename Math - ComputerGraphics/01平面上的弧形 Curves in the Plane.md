Chaikin’s Curves algorithms 柴金曲线算法

- George Chaikin, University of Utah, 
- John Warnock, CEO of Adobe,
- James Clark, inventor of Postscript & PDF,

no continual things in computer 计算机中没有连续
discrete things in computer 离散的事物

point + vector an affine combination 点+向量 就是一组仿射

Barycentric Points 重心坐标

the sum of each coefficient of a polynomial combination is zero 多项式每个系数的和是0⃣️
- 即: <img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/221407748-95a8b817-c4c0-45d0-bce5-797054b8d6e4.png">



|name 名称|graph 图像|formula 公式|algorithm 算法|C++ code|note 注释|
|-------------------------------------------|-------|-------|---------|--------|-|
|Affine combination 仿射组合       |2个点     |       |
|Parabola 抛物线                   |3个点     |       |<img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/221404156-2a00d285-42c2-4bc5-b9a8-6a3f3dbe520b.png">||<img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/221404848-e1a28a57-c7ee-4320-9d81-f6f7316b9fea.png">为三个控制点Control Point, 也是拐点Inflection Point, 贝塞尔点Bezier Point|
|Subdivision Curve 细分曲线|4个点<img width="402" alt="Screen Shot 2023-02-26 at 22 52 10" src="https://user-images.githubusercontent.com/31954987/221417989-ca738cc2-477a-4b35-be7a-c0b7fe7b7f2c.png">     |       |Bernstein Polynomial 伯恩斯坦多项式 <img width="700" alt="image" src="https://user-images.githubusercontent.com/31954987/221403753-8d47260b-07e1-42fd-b8ce-a97e4af018a6.png">|||

