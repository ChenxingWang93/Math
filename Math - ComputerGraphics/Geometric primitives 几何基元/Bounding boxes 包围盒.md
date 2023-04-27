## Representing AABB 代表AABB
包围盒bounding boxes 是最基础的几何基元geometry primitives 用来描述对象的体积 volume. 有两种类型的包围盒bounding boxes:
- 轴向对齐包围盒 Axially Aligned Bounding Box(AABB). 对齐到 XYZ 轴 Aligned to XYZ axes.
- 任意方向的包围盒 Arbitrarily Oriented Bounding Box(OBB)

> ```
> **AABB** 更容易创建与使用, **OBB** 是有方向的 **AABB**, 因此，所有在 **AABB** 上的操作能被运用到 **OBB**上 且applying orientation.
> 区别并不在于盒子本身，而是操作making operations in[[Introduction to matrices#Geometric definition|coordinate space aligned with bounding box]].
> ```

> ```
> 在此我们会关注 3D AABB, 但是 所有会运用到 放弃第三维度的 二维  everything will be applied in 2D dropping the 3rd dimension
> ```

## Computing AABB 计算AABB
定义 AABB 包围盒的 两个顶点 **two corners** are <img width="100" alt="a29c46984ec792fd9f16bf65b811727" src="https://user-images.githubusercontent.com/31954987/234482257-b2230ca7-8366-44a0-8139-f21378477507.png">,
所有在包围盒AABB内的点<img width="70" alt="61f536b4af16d437648c94934c8ec10" src="https://user-images.githubusercontent.com/31954987/234483070-75a8253c-e7d3-43cb-8252-cae22a85dd52.png">满足不等式 all the points inside a bounding box AABB satisfy the inequalities:

<img width="150" alt="704acb07fa6786e7628c69db7e888e6" src="https://user-images.githubusercontent.com/31954987/234483664-f5916ed9-732e-4c0c-810c-79498ca1b49a.png">
包围盒的中心 **c** 被定义为

<img width="200" alt="4965e6d51053238d5f6b4eee1b7b689" src="https://user-images.githubusercontent.com/31954987/234751858-7188e852-5f9b-4c0a-ae40-45dbd5e9ea81.png">  
**size vector s** 是 p_{min} 到 p_{max} 的向量，包含宽度、高度与盒子在各个维度的尺寸。 **radius vector** 是 s/2, 或者 从center c to p_{max}的向量。
<img width="170" alt="7c655dd67b1b494764d3ca08bd16d64" src="https://user-images.githubusercontent.com/31954987/234785333-5cd6f0f5-d4f2-462e-9be0-235f62bf1931.png">

> ```
> to unambiguously define an AABB we need at least 2 of 4 vectors P_{min}, P_{max}, c and s. The most common way to define an AABB is through p_{min} and p_{max}.
> ```

## AABB vs Bounding spheres 边界球体
为一系列给定点计算包围盒computing bounding box 很容易。
首先，maximum P_{min} and minimize P_{max}
Then, 比较所有点的所有维度compare them with all the dimensions of all the points
and, 保存找到的最小与最大值save the found minimums and maximums

> ```
> 
> // Define AABB operations 定义 AABB 操作
> void AABB3::empty() { 
> min.x = min.y = min.z = FLT_MAX;
> max.x = max.y = max.z = −FLT_MAX ;
> }
> 
> void AABB3::add (const Vector3 &p) { 
> if (p.x < min.x) min.x = p.x;
> if (p.x > max.x) max.x = p.x;
> if (p.y < min.x) min.y = p.y;
> if (p.y > max.x) max.y = p.y;
> if (p.z < min.x) min.z = p.z;
> if (p.z > max.x) max.z = p.z;
> }
> 
> // Apply them to compute the AABB of a set of points 计算系列点的AABB
> const int N;
> Vector3 list [N];
> 
> AABB3 box;
> box.empty();
> 
> for (int i = 0; i < N; ++i) {
>         box.add(list[i]);
> }
> ```

## Fast OBB to AABB 快速 OBB 到 AABB

