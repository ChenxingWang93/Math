"orientation" of an object tells us what direction the object is facing “对象”的朝向告诉我们对象是面向哪里

but "orientation" is not the same as "direction". ⚠️⚠️ “朝向” 不同于 “方向”

for instance, a vector has a direction but not an orientation(we can rotate the vector around its axis and nothing changes, because it has no thickness). 一个向量如果它没有直径大小变化的话，有“方向” 而没有 “朝向”

```
**direction** be parametrized in 3D with just [[3D polar space|2 numbers]]❕❕❕先选[轴空间]再选[数字] 

**orientation** needs at least 3 numbers (using **Euler angles**) 欧拉角
```

like translation, orientation must be always given from a reference point(called **identity rotation** or **home rotation**) 类似 **移动**，**朝向** 从给定点 

旋转量 称之为 **angular displacement** 

很多在 3D 空间中描述 orientation 的方式，都各有优劣

```
the common strategy is to store rotation in eulers and/ or quaternion, 在欧拉或 四元数中存储 [旋转]

and then have a matrix that is re-computed every time the other data updates, 有一个矩阵 每每重新计算更新数据

and that is then combined with the rest of the transformations(translation, scale, etc). 最后将这些变换组合起来（移动、缩放）
```

1.[[Linear transformation#Rotation|Matrix Orientation]]

## **Pros:**
- **Rotation of vectors** is directly available 向量旋转直接有效
- format used by graphic APIs 形式是图形APIs
- **easily concatenation of multiple rotations and inversion.** 旋转与倒置
- **easily concatenation with other transformations** 串联其他变换
- unique representation for a given rotation(no aliasing) 给定旋转的独特表现形式

## **Cons:**
- they cannot interpolate ()
- 
