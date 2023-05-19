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
- **they cannot interpolate** (we must use other system for interpolations/animations) 无法拟合
- **take more memory** (e.g. if we need to store all the rotations in an animation)(占据更多内存)
- **hunmans unreadable** they think in angles 人类不可读
- matrices can be ill-formed 
- not easy to understand, although easier than exponential maps and quaternions 理解指数映射 四元数


2.[[Euler angles]]
## **Pros:**
- **easy for humans to understand**, they are just angles, this makes Euler angles the right choice if we need to show or set the value of rotation nummerically.
- **take little memory**(smallest possible representation of an orientation) 朝向的最小可能表现形式
- **easily compressed**(e.g. to a fixed point system). the data loss due to **quantization** is spread evenly and the absolute numeric difference between two values is proportional to the difference perceived(与矩阵和四元数不同，需要存储非常小的数值，因为被存储的数值都是 sines and cosines)
- **Any set of 3 numbers is a valid 3D rotation** 有效的3维旋转 矩阵与四元数

## **Cons**
- painful to interpolate due to **gimbal lock** 云台锁❕❕但这不可避免
- **cannot rotate points between coordinate spaces directly** must always convert to a rotation matrix. 总是要转化为旋转矩阵
- **cannot concatenate multiple rotations** 无法连接多个旋转
- **aliasing** 混叠 (easier to solve than Euler angles)
- difficult to understand.

3.[[Quaternions]]
## **Pros:**
- **reliable quality interpolations** 可靠的拟合质量
- **fast concatenation of rotations and inversion** 快速 连接 旋转与倒置
- fast conversion from and to matrix form. 从矩阵 到矩阵 的转换
- **only four numbers**  只有 4 个数
- **only two distinct representations for a given rotation**(no aliasing) 2 种 独特表示形式

matrices > quaternions > euler angles

## **Cons**
- **can rotate points between coordinate spaces directly**, but usually this is not used. instead, they are converted to a rotation matrix. 无法在坐标空间间旋转点，转化为旋转矩阵
- **can become invalid** because of bad input data or accumulated error. we solve this by regularly normalizing the quaternions to make sure that they remain unit(magnitude=1).
- the **most difficult system** for humans to work with 最困难的系统
- cannot compress/ quantize well directly. 无法直接压缩量化
