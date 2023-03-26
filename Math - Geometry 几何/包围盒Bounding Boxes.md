bounding boxes are one of the most common geometric primitives used to describe simply the volume of an object. There are 2 types of bounding boxes:
包围盒：常见的几何基元，描述对象的体积，2种包围盒类型
- Axially Aligned Bounding Box **(AABB)**. Aligned to the XYZ axes.
- Arbitrarily Oriented Bounding Box **(OBB)**.


## 表示AABB Representing AABB
the two **corners** that define an AABB bounding box are <img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773239-a0d4cc6e-7fca-4cb5-a85c-6bc175fd796c.png"> all the points <img width="50" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773286-a3cc13cd-d522-4497-9e60-fb144ff20f73.png"> inside a bounding box AABB satisfy the inequalities:

- <img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773608-f40691e3-ad0a-413a-b693-ed6ea81b8d06.png">

