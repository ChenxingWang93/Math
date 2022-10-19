## Permeation //排列
![image](https://user-images.githubusercontent.com/31954987/196244660-4d4c8244-f474-4625-ba33-9ae0158c644a.png)

## Combination //组合
![image](https://user-images.githubusercontent.com/31954987/196244816-379cde61-66f3-4d5a-8e69-fef362e10a16.png)

### Why do we multiply combinations? 为什么有乘法组合
#### when working on a combination problem, we usually multiply.But sometimes addition -- how do we know which is which? building up mental model 心智模型

### Mental Model: Different Dimensions 不同维度
#### you have 4 shirts and 8 pants, how many outfits can you make? In essence, you are picking a spot on below grid.
![image](https://user-images.githubusercontent.com/31954987/196743298-22062c1e-5a63-4818-b8e2-0e703f40022f.png)

#### We have _4 * 8 = 32_ options

#### Now we had 4 shirts and 8 pants and had to pick a single item to sell. 
![image](https://user-images.githubusercontent.com/31954987/196750100-eadc94c1-a8b9-44df-a2c9-438914d67aa8.png)

#### Randomly pick any item along the line and have _4 + 8 = 12_ options

#### "different dimensions v.s. same dimension" or "grid v.s. line".

### Mental Model: AND vs OR
Another interpretations is AND(multiplication) v.s. OR(addition).
```
pick among 4 shirts AND among 8 pants = 4 * 8 = 32 choices
```
```
pick among 4 shirts OR among 8 pants = 4 + 8 = 12 choices
```
#### Writing out the scenario is often easier to think through, especially with numerous dimensions (shirts, pants, hats, shoes, socks)，as you internalize the analogies, you will recognize whether _multiplication_ or _addition_

#### Randomly pick any item along the line and have _4 + 8 = 12_ options
