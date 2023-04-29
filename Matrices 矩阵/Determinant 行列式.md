对于方形矩阵 for square matrices 有一个特殊的标量称之为行列式 there is a special scaler named **determinant** of the matrix. 有一个非常有用的属性与数学解it has very useful properties in linear algebra and geometric interpretations.

## 数学解 Math interpretation
the determinant of a matrix *M* is denoted as ***|M|*** or det M. The determinant of a 2x2 matrix looks like this:

<img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/227769368-d886632b-c6e8-457f-b2cd-f597745c3406.png">
对角线相乘 multiplying the diagonals, 减去第二个对角线and subtracting the second diagonal to the first one. 3x3 matrix 行列式更加令人费解 the determinant of a 3x3 matrix is significantly more convoluted:

<img width="200" alt="图片" src="https://user-images.githubusercontent.com/31954987/227769116-d7006491-04ae-4393-a0e0-03af2174ddf7.png">

<img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773001-8a8b769f-13bc-4d18-9b20-5d1f3e6314fa.png">

<img width="250" alt="triple product" src="https://user-images.githubusercontent.com/31954987/226171323-15e908ea-ea7b-4e30-a691-dcd890ddc47a.png">
更好地记住它的方式，if we consider the 3 rows of a 3 * 3 matrix as basic vectors, 行列式是一个三乘三的积 the determinant is the **triple product** 
<img width="350" alt="图片" src="https://user-images.githubusercontent.com/31954987/226171679-92b301a0-03fa-4ce9-9a94-2aa8de756cff.png">

the computation of the determinant for bigger matrices become very complex, and of course it is pointless to try to memorize it. But we should know some important properties about determinants:

- The determinant of the identity matrix is one: 单位矩阵的行列式是1 <img width="105" alt="图片" src="https://user-images.githubusercontent.com/31954987/226546382-cc600f37-1f8d-45bb-be1e-e9d152249110.png">
- The determinant of a product is equal to the product of determinants: 乘积的行列式等于行列式的乘积 <img width="215" alt="图片" src="https://user-images.githubusercontent.com/31954987/226546543-92008b24-4ef5-4fec-9271-6c5073fe495e.png">

- A matrix and its transpose have the same determinant: 矩阵及其转置具有相同的行列式<img width="185" alt="图片" src="https://user-images.githubusercontent.com/31954987/226546823-9260b183-bc0f-4363-b0fa-048ee2310713.png">

- If any row or column in a matrix is all 0s, the determinant is 0. 
- Exchanging any pair of rows or columns negates the determinant. 否定行列式


## 几何解 Geometry interpretation
