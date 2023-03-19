对于方形矩阵 for square matrices 有一个特殊的标量称之为行列式 there is a special scaler named **determinant** of the matrix. 有一个非常有用的属性与数学解it has very useful properties in linear algebra and geometric interpretations.

## 数学解 Math interpretation
the determinant of a matrix *M* is denoted as ***|M|*** or det M. The determinant of a 2x2 matrix looks like this:

<img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/226096870-9a522225-6e4b-4391-8149-675e9a304241.png">
对角线相乘 multiplying the diagonals, 减去第二个对角线and subtracting the second diagonal to the first one. 3x3 matrix 行列式更加令人费解 the determinant of a 3x3 matrix is significantly more convoluted:

<img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/226171123-76736325-2534-45ff-9c38-f379284dc0a7.png">
<img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/226171422-aa238dbc-6906-4063-a439-b32644aa5e59.png">

<img width="250" alt="triple product" src="https://user-images.githubusercontent.com/31954987/226171323-15e908ea-ea7b-4e30-a691-dcd890ddc47a.png">
更好地记住它的方式，if we consider the 3 rows of a 3 * 3 matrix as basic vectors, 行列式是一个三乘三的积 the determinant is the ***triple product*** 
<img width="350" alt="图片" src="https://user-images.githubusercontent.com/31954987/226171679-92b301a0-03fa-4ce9-9a94-2aa8de756cff.png">

the computation of the determinant for bigger matrices become very complex, and of course it is pointless to try to memorize it. But we should know some important properties about determinants:

- The determinant of the identity matrix is one: 单位矩阵的行列式是1
- The determinant of a product is equal to the product of determinants: 乘积的行列式等于行列式的乘积
- A matrix and its transpose have the same determinant: 矩阵及其转置具有相同的行列式
- If any row or column in a matrix is all 0s, the determinant is 0. 
- Exchanging any pair of rows or columns negates the determinant. 否定行列式 
