#   Intuitive Guide to Convolution //卷积的直觉引导
### Formal definition:
![image](https://user-images.githubusercontent.com/31954987/200176209-305890c2-8a6c-4dc9-88b6-780ae718a97b.png)
## **Convolution is fancy multiplication**. //卷积为乘法时 ✖️
##  Part 1: Hospital Analogy //🏥医院比喻
### a hospital treating patients with a single disease
> **A treatment plan:**治疗计划 `[3]` every patient gets 3 units of the cure on their first day.  //
> A list of patients: `[1 2 3 4 5]` patient count for the week (1 ppl Monday, 2 ppl Tuesday, etc)
### Q: 每天用药量？
> Plan * Patients = Daily Usage
>  [3] * [1 2 3 4 5] = [3 6 9 12 15]
### multiplying the plan by the patient list gives the usage for the upcoming days:
[3 6 9 12 15].


### Intuition For Convolution //卷积的直觉
### Let's say the disease mutates and requires a multi-day treatment.You create a new plan: `Plan: [3 2 1]` //如果疾病突变要求多天治疗
### that means 3 units of the cure on the 1st day, 2 on the 2nd & 1 on the 3rd..
### _flipping_ the patient list, so the first patient is on the right //第一个病人在右边
> --------Start of line
> - 5 4 3 2 1
> - Rooms
> - ------3 seperate rooms------
> -        3 2 1


> - Monday 周一
> - Rooms------------------3 2 1
> - Patients->-------5 4 3 2 1

> - Usage-------------------3 = 3


> - Wednesday 周三
> - Rooms------------------3 2 1
> - Patients->-----------5 4 3 2 1 
> - Usage-------------------9 4 1 = 14

> - Thursday 周四
> - Rooms------------------3 2 1
> - Patients->------------5 4 3 2 1
> - Usage------------------12 6 2 = 20



### Interactive Demo //交互式demo
### Application: COVID Ventilator Usage //应用: 呼吸机的使用

##  Part 2: The Calculus Definition  //函数定义

##  Part 3: Mathematical Properties of Convolution //卷积的数学属性
### Convolution is communicative: f * g = g * f //卷积是可交换的
### The integral of the convolution //卷积的积分
### Impulse Response  //脉冲响应


##  Part 4: Convolution Theorem & the Fourier Transform //卷积定理&傅立叶变换
### And in reverse... //相反
### Mini proof  //证明


##  Part 5: Application //应用
### Moving averages //移动平均值
### Derivatives //导数
### Blurring /unbluring images //模糊与取消模糊图像
### Algorithm Trick: Multiplication //算法技巧: ✖️乘法
### Fast Convolutions //快速卷积
### Convolution Neural Nets //卷积神经网络(CNN)
### LIT System Behavior //linear, time-invariant system 线性，时间不变系统
### Engineering Analogies //工程比喻
