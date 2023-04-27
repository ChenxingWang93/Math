let's assume for now that w = 1, 因此，任何在3D(x, y, z)中的点 any point in 3D space can be represented in 4D as (x, y, z, 1). 我们能够变换3D 变换矩阵为4D 变换矩阵 transform 3d transformation matrics into 4d transformation matrics like this:

<img width="350" alt="8767e66869dd0e979fcd7761764ee61" src="https://user-images.githubusercontent.com/31954987/234808804-9157bf90-546d-45c1-8afb-9a98c9b15119.png"> -> <img width="200" alt="7910a0b3c33854f2e0e49fbd48df42c" src="https://user-images.githubusercontent.com/31954987/234813933-fd2bf818-f760-4912-98a2-21ee1d188212.png">

due to the matrix algebra rules,根据矩阵代数规则 we can express translation as a matrix multiplication.用矩阵乘法表示translation
<img width="150" alt="图片" src="https://user-images.githubusercontent.com/31954987/226094617-d1916755-35df-4928-a863-59835533a1df.png"> * <img width="300" alt="图片" src="https://user-images.githubusercontent.com/31954987/226094442-ff3470c5-8689-459e-ae7b-cddead099605.png"> = <img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/226094706-6f200c15-03f7-4cf9-af15-9951bab8db67.png">

这个矩阵的乘法是线性仿射 this matrix multiplication is an **affine transformation** (so it's also linear) 4d矩阵不能转换点到4d空间中，4D matrices cannot translate points in 4D,4d零向量 会被变换到4d零向量 and 4D zero vector will always be transformed back into the 4D zero vector. 这个在3d中 work 的原因是 The reason this works in 3D is that we are [[Linear transformations#Shearing|shearing]] the 4D space, 在3d中的 translation 如果我们and that results in a translation in 3D. 如果我们在x，y 检查3d剪切函数 If we check the 3D shearing function in  x,y , 与2d 变换相同 it looks exactly as the translation matrix in 2D:

<img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/226095615-db71e051-ee34-408e-9f80-baae3834af25.png"> * <img width="225" alt="图片" src="https://user-images.githubusercontent.com/31954987/226095480-1ca46835-b4ad-4b7c-8dca-9a23136c5854.png"> = <img width="300" alt="图片" src="https://user-images.githubusercontent.com/31954987/226095554-74fb6a9f-7ee8-438b-bad1-c6f96cdae22f.png">

using a 3*3 matrix for 2d and a 4*4 matrix for 3d. we need to convert these matrices to 3d or 4d respectively like shown above
