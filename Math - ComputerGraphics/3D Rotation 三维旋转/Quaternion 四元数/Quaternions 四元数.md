a quaternion expresses a rotation as a scalar <img width="30" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/f581f76b-acd7-47af-9608-a3edd5f32600"> and a 3D vector <img width="30" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/58fe2b10-48f8-4647-b13d-34f95c15eb84">

unlike vectors, there is no distinction between "row" & "column" quaternion. 无 行 列 的明显差异

The difference is just aesthetic.

<img width="60" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/fa5ccff4-3f45-448d-945f-ae7615e549e6"> 

<img width="130" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/94735636-e796-4d0c-9fc8-b8a61dc0c4fc">

[Axis-angle form and exponential maps|exponential maps],

represent a rotation simply with an angle <img width="20" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/88d88cc4-161a-40d1-b298-8fe2b9d01b40"> 带角度的旋转

and an axis <img width="20" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/cd993062-f3e4-4648-995c-e155b0a9b609"> 一个轴

<img width="300" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/0fec17c1-73b0-4416-a91d-340f5b171d56">

<img width="30" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/f581f76b-acd7-47af-9608-a3edd5f32600"> 对应 <img width="20" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/88d88cc4-161a-40d1-b298-8fe2b9d01b40">

<img width="30" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/58fe2b10-48f8-4647-b13d-34f95c15eb84"> 对应 <img width="20" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/cd993062-f3e4-4648-995c-e155b0a9b609">


## Negation 否定式
四元数有许多运算，最基本的是取 负 `Negating` 

<img width="400" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/f3570c5c-69c6-4f8e-a81b-3f988904cf36">

右侧订正 

<img width="225" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/92ce28f8-e089-4bdc-9bbe-f0e529972127">

## Identity 
an **identity quaternion** is a quaternion that does not apply any rotation. there are two of them:

there are two of them:

- 当 \theta 为 360º 偶数倍, then cos(\theta) = 1 我们得到 第1 种形式
- 当 \theta 为 360º 奇数倍, then cos(\theta) = -1 我们得到 第2 种形式
- 无论哪种形式 sin(\theta) = 0, <img width="25" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/e8ebb70e-58a3-41b6-828e-121409680c57">值 不相关

## Magnitude 大小
