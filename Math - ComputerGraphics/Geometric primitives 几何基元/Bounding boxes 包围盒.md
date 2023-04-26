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


## AABB vs Bounding spheres 边界球体


## Fast OBB to AABB 快速 OBB 到 AABB

