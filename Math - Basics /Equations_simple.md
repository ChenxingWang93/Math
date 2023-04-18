## System of equations 稳定系统
**system of equations** is a group of two or more related equations. Generally, systems of equations can be solved, 稳定系统能有解 which means finding one or more values for the variables for which all of these equations are satisfied 为一个变量找到满足等式的一个或者多个解
> ```
> 
> ```

3种类型的稳定系统
- no solution无解 **Incompatible**: 不相容.
- it has 1 solution per variable每个变量有1个解 **Determined Compatible**: 确定兼容.
- it has infinite solutions有♾️的解 **Indeterminate Compatible**: 不确定兼容.

the system of linear equation is said to be **homogeneous** 在所有方程系统中如果 独立项 为0⃣️ 线性等式是同质的 if the independent term is zero in all the equations of the system 所有同质系统都是兼容的 every **homogeneous** is compatible (has a solution): the **trival solution** 有简单解 (where all the variable are zero).
## Type of solutions 解的类型
一个方程或一个系统方程有解的多种形式 an equation or system of equations can have solutions in multiple forms:

简单解：**Simple solutions**
- 一个解 A number: <img width="100" alt="image" src="https://user-images.githubusercontent.com/31954987/232638362-603e459c-a647-49a4-857a-720b3a549588.png">
- 多个解 Several solution: <img width="250" alt="image" src="https://user-images.githubusercontent.com/31954987/232640490-74210e23-e04d-4d68-abf3-42181b2bd365.png">

参数解：**Parametric solution** 清除一个未知数并将其转化为参数 clearing one unknown and converting the rest into parameters 
# 
- 一个参数的解 A solution with 1 parameter, i.e. a straight line (in this case the line <img width="125" alt="image" src="https://user-images.githubusercontent.com/31954987/232641583-f07723cb-d5a2-420a-93fb-969b4ff5c278.png">) 
<img width="350" alt="image" src="https://user-images.githubusercontent.com/31954987/232644453-2786a818-18d3-4385-93e7-fb1dfa786d0a.png">
- A 2-parameter solution 一个 2 参数的解：i.e. a plane: 一个平面
<img width="500" alt="5b4fef554b2300bbad3611f6552eefa" src="https://user-images.githubusercontent.com/31954987/232661819-f673f91e-91d5-4faf-846d-2e0af0229096.png">

## Algebraic solution 代数解
两种解题思路two methods for solving systems of equations

> ```
> y = x + 3
> ```

- 换元Substitution: 消除等式中的变量用其他替代 to clear a variable in one of the equations and substitute it in the other 
> ```
> 2x - 3(x + 3) = 10
> -x - 9 = 10
> x = -19
> y = -16
> ```

- 消元Elimination: 通过 操作其中一个等式 或者 减掉一个等式 eliminate a variable by manipulating one of the equations and substrating it from the other. This is possible because we remember that both equations are worth the same on both sides of the equality,等式两侧都是 and we add the same on both sides of the equality of an equation.
> ```
> y = x + 3
> -x + y = 3
> -2x + 2y = 6
> {-2x + 2y = 6} + {2x - 3y = 10}
> 0 - y = 16
> ```

- 等号Equalization: 选择一个变量并清楚最少2个等式找到其值
> ```
> y - 3 = (10 - 3y)/2
> ```

## Matrix solutions 矩阵解
处理大量数据，矩阵比代数解和基本代数 更有能量 matrices give more power than[[#Algebraic solution|basic algebra]]when working with a lot of data. 如果要用代数解一个 100个未知数 和100个等式 的系统方程就很痛苦，但矩阵解就很容易if we had to solve a system of equation with 100 equations and 100 unknown with algebra it would be a pain, but with matrices it is really simple.



## Rouchè-Fröbenius check 

## Gauss-Jordan solution 高斯 - 乔丹 解

## Inverse matrix solution 逆矩阵解

## Cramer solution 克拉默解
