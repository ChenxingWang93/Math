<img width="225" alt="图片" src="https://user-images.githubusercontent.com/31954987/229277479-201f4b13-dd25-4966-bc59-6c7b5c409cf7.png">


<img width="300" alt="图片" src="https://user-images.githubusercontent.com/31954987/229277354-c16ea1ac-be22-4fee-834c-7d40ee375b6d.png">

    ---A ⬇--- 

<img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/229297773-198f8458-196e-41f1-800b-18ec6e8fa9e7.png">  <img width="24" alt="图片" src="https://user-images.githubusercontent.com/31954987/229297930-3b1a9a51-a2dc-4ad0-ac94-0dc1f8cc8204.png"> = <img width="85" alt="图片" src="https://user-images.githubusercontent.com/31954987/229298041-dc64ab6e-8d37-44b8-ab40-9e6e095c7db2.png"> = <img width="22" alt="图片" src="https://user-images.githubusercontent.com/31954987/229345223-40c952ed-a8f2-449f-947f-61e1fc1fb992.png">


<img width="24" alt="图片" src="https://user-images.githubusercontent.com/31954987/229297930-3b1a9a51-a2dc-4ad0-ac94-0dc1f8cc8204.png"> :e_2

A 的第二列告诉我们 R^3 中的第二个基本向量 如何映射到 R^2，如果我们水平堆叠标准基础向量到 3*3 矩阵中，每个基础向量如何以单一矩阵乘法的形式映射到R^2

              ⬇蓝 ⬇红 ⬇黄  ⬇蓝 ⬇红 ⬇黄

<img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/229297773-198f8458-196e-41f1-800b-18ec6e8fa9e7.png"> <img width="85" alt="图片" src="https://user-images.githubusercontent.com/31954987/229345617-bbe68d84-3d2d-4cc3-a569-c803f7a58f78.png"> = <img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/229297773-198f8458-196e-41f1-800b-18ec6e8fa9e7.png">

表达任意transformed 2-vector 作为<img width="150" alt="图片" src="https://user-images.githubusercontent.com/31954987/229347002-a090f082-e4cc-45ab-a820-373fb2c0f45b.png"> 的线性组合linear combination, where 系数coefficient 是未变换3-vector 的 component. 例如<img width="150" alt="图片" src="https://user-images.githubusercontent.com/31954987/229347277-feb8c3e8-02c4-4ef9-a39c-fed38c80dab3.png">

    ---A ⬇---  -x ⬇-  -f(x)⬇-
<img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/229350684-9b4344a2-58b6-4d80-9fee-f3d6ed926e19.png"> <img width="40" alt="图片" src="https://user-images.githubusercontent.com/31954987/229350773-292fbe22-ee41-4270-9d8c-76e185bcf6e8.png"> = <img width="40" alt="图片" src="https://user-images.githubusercontent.com/31954987/229350887-4d2332c8-5e81-468c-af19-ac48ac142e63.png">    (1)

    f(e_1)⬇  f(e_2)⬇f(e_3)⬇               f(x)⬇
<img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/229351206-4fa85679-e70e-45f0-ab2e-a08ce72d5bdf.png"> = <img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/229351325-7defb479-8ed6-4de3-aabb-3f3cb47fdcfa.png"> = <img width="45" alt="图片" src="https://user-images.githubusercontent.com/31954987/229351370-66d87630-3395-4780-85fb-d27761696bb5.png">     (2)

<img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/229352774-bf036e0e-b5ee-4aa8-8a00-d3c6e1b5924e.png">

### 视觉化矩阵变换 visualizing matrix transformations
      A⬇   x⬇  f(x)⬇
<img width="150" alt="图片" src="https://user-images.githubusercontent.com/31954987/229354277-73e1bf19-7635-45c9-a5fb-be2aa16c0cfd.png">

可视化两个重要的属性two important properties, A 的第一列代表 标准基础向量 the first columns of A represent where the standard basis vectors in R^2 land in this transformed vector space.    

![图片](https://user-images.githubusercontent.com/31954987/229362069-029cda93-171d-49d6-80f7-3872ed253166.png)

**Figure 1. (A)** a vector X is a 线性结合linear combination standard basis vectors标准基础向量
**(B)** The vector f(x) is a linear combination of the transformed standard basis vectors.变换的标准基础向量的线性结合

second, in the new vector space, the vector <img width="30" alt="image" src="https://user-images.githubusercontent.com/31954987/230031655-5e364ac3-0ca5-4cf5-af0c-a0e5d755114d.png"> is a linear combination of these transformed vectors. 颜色化单位向量coloring unit squares 观察他们如何变换seeing how they are transformed, 不仅一个向量由矩阵变换，而是所有的<img width="35" alt="image" src="https://user-images.githubusercontent.com/31954987/230033385-f4837d13-2843-4eaa-8307-2e13b380abb4.png"> 变换一个 <img width="50" alt="image" src="https://user-images.githubusercontent.com/31954987/230033650-574bedbf-339d-4787-97eb-d5b25460e160.png"> 的矩阵，矩阵的行列式也可视化了。

### 线性变换的类型 types of linear transformations

矩阵变换如何代表线性函数，什么样的变换能够用矩阵来执行what kind of transformations can we perform with matrices?矩阵线性变换的结果是只能以特定的方式调整一个向量空间 the consequence of the linearity of matrix transformation is that we can only modify a vector space in particular ways 例如旋转，缩放，剪切，投影 by rotating, reflecting, scaling, shearing and projecting, 线性变换的特点是在变换前均匀分布的点在变换后也是均匀分布的 the hallmark of a linear transformation is that evenly spaced points before the transformation are evenly spaced after the transformation (figure 2a)

![image](https://user-images.githubusercontent.com/31954987/230068474-f3257e01-b68c-49c2-a582-ca1f8039e73e.png)

figure 2: (A) 线性变换的例子：未变换的R^2, 沿着x轴缩放, 旋转, 投影到R, 反射y-axis, 剪切(B)非线性变换的R^2

### 对角矩阵 diagonal matrices
如果我们把矩阵的列看作定义一个新的向量自空间think of the columns of the matrix as defining a new vector subspace, 那么就能清晰地看到在变换的向量x 中的每一个部件只调整对角中的一个值each component in a transformed vector x is only modified by one value on the diagonal
