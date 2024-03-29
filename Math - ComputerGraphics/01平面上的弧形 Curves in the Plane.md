https://pomax.github.io/bezierinfo/


- Chaikin’s Curves algorithms 柴金曲线算法
- Chaikin's points only piece together parabolas 柴金曲线把抛物线拼凑在一起

- George Chaikin, University of Utah, 
- John Warnock, CEO of Adobe,
- James Clark, inventor of Postscript & PDF,

no continual things in computer 计算机中没有连续
discrete things in computer 离散的事物

point + vector an affine combination 点+向量 就是一组仿射

Barycentric Points 重心坐标

the sum of each coefficient of a polynomial combination is zero 多项式每个系数的和是0⃣️ affine combination of the p_1, p_2, p_3, p_4
- 即: <img width="400" alt="image" src="https://user-images.githubusercontent.com/31954987/221407748-95a8b817-c4c0-45d0-bce5-797054b8d6e4.png">



|name 名称|graph 图像|formula 公式|algorithm 算法|C++ code|note 注释|
|-------------------------------------------|-------|-------|---------|--------|-|
|Affine combination 仿射组合       |2个点     |       |
|Parabola 抛物线                   |3个点     |       |<img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/221404156-2a00d285-42c2-4bc5-b9a8-6a3f3dbe520b.png">||<img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/221404848-e1a28a57-c7ee-4320-9d81-f6f7316b9fea.png">为三个控制点Control Point, 也是拐点Inflection Point, 贝塞尔点Bezier Point|
|Subdivision Curve 细分曲线|4个点<img width="400" alt="Screen Shot 2023-02-26 at 22 52 10" src="https://user-images.githubusercontent.com/31954987/221417989-ca738cc2-477a-4b35-be7a-c0b7fe7b7f2c.png">     |       |Bernstein Polynomial 伯恩斯坦多项式 <img width="1000" alt="image" src="https://user-images.githubusercontent.com/31954987/221403753-8d47260b-07e1-42fd-b8ce-a97e4af018a6.png">|||

||formula 公式|
|-|----------|
|<img width="275" alt="Screen Shot 2023-02-26 at 23 25 04" src="https://user-images.githubusercontent.com/31954987/221419940-01db1983-94de-4096-a2c4-b2c243528227.png">|P_2^2 点是 P_1' 和 P_2'的affine combination 
<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/221491705-0c5403fe-2f14-4e9f-9af0-8d3bc875de99.png"> 
<img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/221499297-48f9725a-6eb2-4a1a-aee0-3f6992ac6781.png">
<img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/221498893-789c1684-bb3c-4679-a89a-6e40c5b39283.png">

||graph 图像|formula 公式|interactive demo 可交互|
|-|-|----------|----------------------|
|Bezier 贝塞尔|<img width="275" alt="Screen Shot 2023-02-27 at 17 14 42" src="https://user-images.githubusercontent.com/31954987/221522389-e3f46fa9-f601-49e7-9cd9-4169d5f57928.png">|<img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/221529729-39b70317-5f5b-456b-a8fe-7895f9804a27.png">|https://webgl2fundamentals.org/webgl/lessons/resources/bezier-curve-diagram.html?maxDepth=4%22%3E%3C/iframe%3E |
|Chaikin 柴金|<img width="380" alt="Screen Shot 2023-03-01 at 15 02 36" src="https://user-images.githubusercontent.com/31954987/222067468-4ecf10ba-067e-4496-adbc-fdac1d44674b.png">
