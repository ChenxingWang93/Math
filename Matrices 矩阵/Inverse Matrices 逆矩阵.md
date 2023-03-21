there is a special operation for ***square matrices*** 方阵 called ***inverse*** 逆
## Math interpretation 数学解释
the inverse of a square matrix <img width="40" alt="图片" src="https://user-images.githubusercontent.com/31954987/226263793-f6b47b1b-a3e0-4085-9e95-58dd433d2bb6.png"> 逆矩阵
 is denoted as <img width="75" alt="图片" src="https://user-images.githubusercontent.com/31954987/226263675-475783f6-468b-44fa-9630-e32348240c3e.png">
 
 <img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/226265167-db1c0ac9-f620-4b3e-928d-d8f71cfbd8b3.png">
可逆矩阵具有以下特性 invertible matrices have the following properties:

- 所有列与行都是线性独立的 all the columns and all the rows are **linearly independent**
- the equation <img width="125" alt="图片" src="https://user-images.githubusercontent.com/31954987/226274173-3c3bf5e4-0838-4cfe-a22c-8403db504b81.png"> is true only if <img width="85" alt="图片" src="https://user-images.githubusercontent.com/31954987/226274379-dfb01402-9ce6-4f7e-a5fb-e61de7594309.png">
- 行列式非零 the determinant is not zero, the determinant of noninvertible matrices is zero 非逆矩阵是零
- 逆逆为原矩阵 <img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/226284079-581718e7-df85-4591-a026-a0fc0435b9f0.png">
- the inverse of the identity is the identity: <img width="125" alt="图片" src="https://user-images.githubusercontent.com/31954987/226284577-f6360a51-883e-4635-a005-ade173e421ff.png">
- 逆的转置是转置的逆 the inverse of the transpose is the transpose of the inverse <img width="250" alt="图片" src="https://user-images.githubusercontent.com/31954987/226285325-d4a183e9-ef11-4918-b0a4-f94f1685c2c8.png">
- 积的逆是逆的积 the inverse of a product is the product of the inverses:<img width="250" alt="图片" src="https://user-images.githubusercontent.com/31954987/226291011-01111915-09fd-4017-becd-2098334784b7.png">
- 逆的行列式 原矩阵行列式的倒数 the determinant of the inverse is the reciprocal of the determinant of the original matrix: <img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/226306112-d5009bf5-0a08-4db8-8b64-a27866754db0.png">

> ```
> 经典的计算一个矩阵是否是可逆的方式是计算其行列式，如果不是 0⃣️ 那矩阵就是可逆的
> the classic way to find out if a matrix is invertible is computing its determinant. if it's not zero, then the matrix is invertible
> ```

there are many ways of computing the inverse of matrix, although the most common ones are **classical adjoint and gaussian elimination.** 最经典的是伴随与高斯消元法则

## Geometric interpretation 几何解释
