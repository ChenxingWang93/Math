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
