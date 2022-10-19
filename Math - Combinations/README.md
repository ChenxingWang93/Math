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



### Example: Combination and Permutation Formula
![image](https://user-images.githubusercontent.com/31954987/196755492-2f95411b-980b-469a-b2f8-4fceeead6ab4.png)
#### (n!): the max volume assuming each of the n choices has its own dimension. the number of rearrangements of 8 people is 8 * 7 * 6 * 5 * 4 * 2 * 1.
#### suppose 我们只关心前3个决定 --- 🏅️、🥈、🥉.
#### in this case, we shrink our solution space by dividing out the 5 dimensions we aren't using, 我们剩下的选项是8!/5! = 8 * 7 * 6 = 336 choices
#### with the general formula:
<math xmlns="http://www.w3.org/1998/Math/MathML">
  <mfrac>
    <mrow>
      <mi>n</mi>
      <mo>!</mo>
    </mrow>
    <mrow>
      <mo stretchy="false">(</mo>
      <mi>n</mi>
      <mo>&#x2212;</mo>
      <mi>k</mi>
      <mo stretchy="false">)</mo>
      <mo>!</mo>
    </mrow>
  </mfrac>
</math>

(multiplication creates dimensions, then division remove them)

#### suppose the medals are identical: we are giving a tin can to 3 out of 8 ppl, 
#### we have to further remove dimensions, because we have 3! = 3 * 2 * 1 = 6 redundancies for each permutation in our solution space, we again shrink our solution space:
![image](https://user-images.githubusercontent.com/31954987/196758581-4b942e00-873a-4bcb-9d1c-d5d990a2fdbd.png)
#### permutation count /redundancies 排列数/冗余
#### That's what's happening with the combination and permutation formula. We create the max volume and shrink it by the dimensions we are not using.






