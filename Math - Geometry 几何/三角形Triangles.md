## **Triangle Meshes** 三角网格
a triangle is defined by three vertices and it's contained in a [[Planes#Plane for more points|plane that we can infere from its vertices]]) the order of those vertices matter because because it usually determines the front and the back side of the triangle. vertices的顺序很关键，因为它通常定义了三角面的前后 In a [[Cartesian space|left-handed system]]在左手定则的笛卡尔空间中

if the three vertices are called <img width="90" alt="image" src="https://user-images.githubusercontent.com/31954987/228116552-88c82bae-c53c-4301-b333-89414b92ab9e.png"> we can define the edges and their length easily:<img width="150" alt="image" src="https://user-images.githubusercontent.com/31954987/228119410-a2e3cc37-e9c0-4ef5-b451-456489937025.png">
minus: 尾尾相连
add: 头尾相连

the perimeter of a triangle is: <img width="200" alt="image" src="https://user-images.githubusercontent.com/31954987/228120996-35fd34fd-e270-4c58-8286-67d2f14e8f90.png"> 周长

the interior angles through the [[Trigonometry|law of sines and cosines]]: <img width="400" alt="image" src="https://user-images.githubusercontent.com/31954987/228121742-5ddbf7b4-16eb-4862-b31e-3bf8b99d21bc.png"> 内角

## **Area** 面积
### **2D**

a classic way to compute the area of a triangle from the base and the height(any triangle defines half a parallelogram) 一种典型的方式 计算三角形的面积 base& height 定义平行四边形

<img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/228130265-da0f2d5a-9841-461f-87dd-d4f80e882dfe.png">

如果我们不知道三角形的高the height of the triangle，但知道边长side length, 能使用Heron's formula 苍鹭公式
基于<img width="25" alt="image" src="https://user-images.githubusercontent.com/31954987/228131049-9403b1c1-e31e-4a6f-85e0-1cd23fc355c8.png">（半个周长）half the perimeter
<img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/228131202-3f51f131-6a6c-4f6a-b54c-df0e5fea7a80.png">


