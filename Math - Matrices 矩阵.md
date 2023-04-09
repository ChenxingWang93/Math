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

<img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/230285441-b82a792a-4d35-4a58-ba4a-8d59c2eebc94.png"><img width="35" alt="image" src="https://user-images.githubusercontent.com/31954987/230334769-dbed3666-6a34-422f-bdf3-5e55825f93e1.png"> = <img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/230340002-737d9250-390d-45fa-b74d-ac70b6daaef4.png"> 

对角矩阵限制它如何修改一组向量diagonal matrix is constrained in how it can modify a set of vectors(Figure 3) it can stretch the i-th component of a vector with a_i > 1, or it can reflect the i-th component with a_i > 0. shear a vector subspace with a diagonal matrix.

![image](https://user-images.githubusercontent.com/31954987/230342247-1bb9bf06-5555-481b-b1b3-e86dce945d4e.png)
(A)unit square. (B)Rotation by flipping columns.(C) Reflection by changing the sign of a column.Note that this transformation is unachievable through rotation. (D) Stretching by multiplying a column by a scalar. 
单位矩阵是一个对角矩阵 identity matrix is a diagonal matrix where ∀i, a_i = 1, 意味着标准基础向量并没有改变 meaning the standard basis vectors are not changed, 行列式为1 因为没有修改向量空间 the determinant of 1 because it does not modify a vector subspace.

### 剪切矩阵 shear matrix
shear matrix is so-named because you can imagine the unit square shearing.单位面积剪切 we can achieve shear with an off-diagonal element: 非对角线元素实现剪切


<img width="125" alt="image" src="https://user-images.githubusercontent.com/31954987/230357466-ef4fc1a7-abe2-4275-b3bf-e6e30291ac12.png"><img width="35" alt="image" src="https://user-images.githubusercontent.com/31954987/230334769-dbed3666-6a34-422f-bdf3-5e55825f93e1.png"> = <img width="300" alt="image" src="https://user-images.githubusercontent.com/31954987/230352644-49a0332a-c6dd-407a-b514-8a81835579a4.png"> 

如果没有非对角beta，变换沿着x_1 拉伸a_1, 非对角元素意味着变换向量的第一个部件off-diagonal element means that a transformed vector's 1-st component is a linear combination of beta and a_1 结果是单位面积剪切this results in a unit square that is sheared bc one dimension is now a function of two dimensions

![image](https://user-images.githubusercontent.com/31954987/230518743-f5345c5d-67af-4723-bb87-1505d50f2395.png)

(left)a unit square and (right) the unit square sheared with an off-diagonal element beta

### 垂直矩阵 orthogonal matrix

### 证明矩阵是线性变换 proof that matrices are linear transformations
<img width="200" alt="image" src="https://user-images.githubusercontent.com/31954987/230542136-181f06ad-2116-4a3a-9568-ca2cda544455.png">

A 是 m*n 向量，A的 第i-th 列，a_i, 是一个 m-vector 向量 有 n 组向量 vectors，让 **v** **u** 成为两个 n-vectors

<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/230543217-11e757c1-e6e0-41ca-b0cb-00635ec48126.png">

#### 属性1Property 1
<img width="500" alt="image" src="https://user-images.githubusercontent.com/31954987/230585840-064cb4b2-0cd1-4104-a542-09970ae3f986.png">

#### 属性2Property 2

