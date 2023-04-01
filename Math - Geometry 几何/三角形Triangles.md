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

the formulas to compute the area for the three edge(e_1,e_2,e_3) in 2d are the following:

<img width="250" alt="image" src="https://user-images.githubusercontent.com/31954987/228286908-557626ed-2b1b-4f8a-a48f-d973c44e4a0d.png">

<img width="250" alt="image" src="https://user-images.githubusercontent.com/31954987/228287426-6b43cf25-d01b-460b-94ca-0f5e9de19f0c.png">

由上述化简后得到结果 simplify formula and will end up with the following:
<img width="450" alt="image" src="https://user-images.githubusercontent.com/31954987/228288117-0628324e-5940-4aa0-acb2-3e485c2244ad.png">


## **3D** 三维
we use the cross product to compute the area. 使用叉积计算面积 Remember that the [[Vector operations#Vector cross product|cross product]] is the area of the parallelogram formed on two sides by a and b.两个邻边a与b Since the area of the triangle is half the area of the enclosing parallelogram,三角形面积是平行四边形面积的一半 w>e can simply make this:

<img width="150" alt="image" src="https://user-images.githubusercontent.com/31954987/228141302-bd81c066-758f-45fd-8f4a-1e85f66a3a4a.png">

## 重心空间 Barycentric Space
a triangle is always contained in a plane,一个三角形通常包含在一个平面上，but trying to work with them directly in 3D(global coordinate) is hard 直接在全局坐标中对他们进行操作是困难的，a very handy coordinate system to easily work with the points on the surface of the triangle is the ***Barycentric Space*** 

any point inside the triangle can be expressed as ***weighted average*** of the vertices 在三角形内部的点，能被表示为各个顶点的加权平均 so call ***barycentric coordinate*** the conversion from barycentric coordinate to standard 3d space works like below: 重心坐标系向标准3d空间转化的原理是:



