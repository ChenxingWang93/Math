欧拉角包含代表朝向作为三个相互垂直的轴的三次旋转euler angles consist of representing an orientation as three rotations about three manually perpendicular axis，任何轴的任何旋转顺序都any axis and any order of rotations will work, 但转换就是 heading-pitch-bank 转换。

考虑[[Cartesian space|left-handed y-up 3D cartesian space]] 在3D图像系统中常用的used in 3D graphics，以及对应的3d and corresponding direction for 3d rotation 旋转方向。应用欧拉角的过程是 the process to apply Euler angles is following:

1. identity rotation
2. **heading rotation:** positive local y-axis rotation
3. **pitch rotation:** positive local x-axis rotation
4. **bank rotation:** positive local z-axis rotation

**yaw-pitch-roll**(航空领域)

- **heading = yaw = Azimuth**
- **pitch = Attitude = Elevation**
- **Yaw = Roll = Tilt = Twist**

**yaw-pitch-roll**（逆向）

对象本地坐标系object local coordinate (**body axis**)

每次旋转后都会改变change after each rotation

称之为**intrinsic conversion**

还能使用 **fixed axes**

旋转会是 “absolute”

为达到相同的结果，在逆向**in the opposite order**应用旋转

**extrinsic convention**


> ```
> 如果忘记 yaw
> 使用 intrisic conversion
> 首先应用 **heading** (local Y rotation)
> 然后 **Pitch** (local X rotation)
> 
> 如果应用 相同的 **pitch** (global X rotation)
> 相同的 **heading** (global Y rotation)
> ```

## Aliasing
旋转的representation 并不是独一无二的，so called **aliasing** 

like in the [[Introduction to polar coordinates|polar coordinates]]
欧拉角能有aliasing 混叠，3角并非完全相互独立。

```

```











