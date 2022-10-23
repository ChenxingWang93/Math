## How to Understand Derivatives: The Product, Power and Chain Rules  //如何理解派生品：乘积、幂和🔗链规则
My take on derivatives:
- function f: We have a system to analyze //
- f'(aka df/dx): moment-by-moment behavior //瞬时⌚️行为
- (h = f + g): f is just part of a bigger system //函数f只是更大系统的一部分
- Using the behavior of the parts, to predict the behavior of the whole

每一部分都有 "point of view" about how much change it added. Combine every point of view to get the overall behavior

|Concept|Intuition|
|-------|---------|
|Function f(x)| Turns input(x) into output(y)|
|Derivative of f(x)| Wiggle x, how much does y change?<img width="610" alt="Screen Shot 2022-10-18 at 00 55 05" src="https://user-images.githubusercontent.com/31954987/196237711-e0922a55-e10b-4663-9774-7a0ebd4cd19a.png">|
|Derivative of system 导数|Combined perspective of each part|
|Addition Rule[f+g]' ➕|Add contributions from f and g|
|Product Rule[f*g]' ✖️|Add contributions:a slice from f,a slice from g|
|Power Rule[x^n] 幂|Combine N different perspectives|
|Chain Rule|Zoom into a perspective's root cause|


### Functions: Anything, Anything But Graphs // 函数图像之外的理解
#### 不要一下子就想到"f(x) = x^n"的函数图像
#### derivative rules are about machinery.
#### the function as the process "input(x) => f => output(y)"
![image](https://user-images.githubusercontent.com/31954987/196243399-e98cd22e-6f31-4334-a2cf-52a96a4667be.png)

####
|||constant lead cam 恒定lead凸轮⬇|
|---|---|---|
|<img width="625" alt="Screen Shot 2022-10-18 at 01 28 36" src="https://user-images.githubusercontent.com/31954987/197349664-7f5fcb7c-c8f3-487b-a8be-e6f1882d4c91.png">   |<img width="625" alt="Screen Shot 2022-10-23 at 00 12 52" src="https://user-images.githubusercontent.com/31954987/197349739-2b63b97f-1715-4593-a548-e4c6a1b1fea4.png">|<img width="626" alt="Screen Shot 2022-10-23 at 00 16 13" src="https://user-images.githubusercontent.com/31954987/197350245-88420328-8750-4c6c-9271-54a20a65fbf6.png">|


|reciprocal cam 倒数凸轮⬇|||
|---|---|---|
|<img width="625" alt="Screen Shot 2022-10-23 at 00 27 20" src="https://user-images.githubusercontent.com/31954987/197350650-630fa9ff-d35c-4048-8bc8-2ccbaf321d23.png">   |<img width="625" alt="Screen Shot 2022-10-23 at 00 29 03" src="https://user-images.githubusercontent.com/31954987/197350776-8b697382-417b-40b7-abbe-e821ec1039a3.png">   |<img width="628" alt="Screen Shot 2022-10-23 at 01 20 49" src="https://user-images.githubusercontent.com/31954987/197353808-e78162bb-2c79-4ba7-9d1b-b490155e2243.png">   |


|square cam 平方凸轮⬇|tangent cam 正切⬇||
|---|---|---|
|<img width="627" alt="Screen Shot 2022-10-23 at 01 56 06" src="https://user-images.githubusercontent.com/31954987/197355639-3b5b8d26-459e-457c-9dd1-51d5b5ff3ed8.png">   |<img width="628" alt="Screen Shot 2022-10-23 at 01 59 22" src="https://user-images.githubusercontent.com/31954987/197355746-df36fae6-0e70-4f51-ab4d-082f0830015a.png">   |<img width="627" alt="Screen Shot 2022-10-23 at 02 04 33" src="https://user-images.githubusercontent.com/31954987/197355958-c5cb3ab4-d49b-4015-aa27-7c4703945b46.png">   |



#### the machine computes functions like addition and multiplication with gears -- you can _see the mechanics unfolding_
![image](https://user-images.githubusercontent.com/31954987/197349596-004c238e-0b56-469c-93c5-5271c5669b81.png)


### Wiggle Wiggle Wiggle // 摆动 摆动 摆动
### Addition and Subtraction // ➕ &➖
#### ![image](https://user-images.githubusercontent.com/31954987/197357542-57e35080-267d-4be3-96ea-cbe23f1e2f6a.png)
#### ![image](https://user-images.githubusercontent.com/31954987/197357557-b5f69a1d-f2f1-40d0-baee-36572ee376af.png)


### df vs df/dx //
#### sometimes we use _df_, other times _df/dx_
- _df_ is a general notion of "however much f changed"
- _df/dx_ is a specific notion of "however much f changed, in terms of how much x changed"
#### In calculus,sometimes we want to think about the actual change, not the ratio. Working at the "df" level gives us room to think about how the function wiggles overall. We can eventually scale it down in terms of a specific input.
![image](https://user-images.githubusercontent.com/31954987/197356866-620a356b-80c3-45d9-801d-4b87cfdd67d2.png)


### Multiplication (Product Rule) // ✖️
![image](https://user-images.githubusercontent.com/31954987/197372039-c58e6c0f-0366-4086-9520-408d16443257.png)
#### see how each part contributes from its own point of view, and combine them:
- total change in h = f's contribution(from f's point of view) + g's contribution(from g's point of view)
![image](https://user-images.githubusercontent.com/31954987/197372555-b7337121-abeb-441c-b9b8-40d169942a85.png)
what's going on?
- we have our system: f and g are multiplied, giving h(the area of rect)
- Input "x" changes by dx off in the distance. f changes by some amount df. Similarly, g changes by its own amount dg. Because f and g changed, the area of the rectangle changes too.
- What's the area change from f's point of view? Well, f knows he changed by df, but has no idea what happened to g. From f's perspective, he's the only one who moved and will add a slice of area = df * g
- Similarly, g doesn't know how f changed, but knows he'll add as slice of area "dg * f" 
#### the overall change in the system(dh) is the two slices of area
![image](https://user-images.githubusercontent.com/31954987/197372845-14985733-d665-4ea8-9e3a-b21094621d08.png)

#### then "divide by dx" to write this in terms of how much x changed:
![image](https://user-images.githubusercontent.com/31954987/197372930-081edcbc-63b3-41fb-acc6-e98af7896e68.png)




### The Chain Rule // 链规则
#### g depends on f, which depends on x:
![image](https://user-images.githubusercontent.com/31954987/197373032-9dbf27bc-f2de-4164-967d-2e287e7f50a4.png)
![image](https://user-images.githubusercontent.com/31954987/197373033-2d597097-acd5-4d07-a49b-822dd5c6fd5b.png)

#### 




### Chain Rule: Example Time // 链规则
