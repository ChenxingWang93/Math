bounding boxes are one of the most common geometric primitives used to describe simply the volume of an object. There are 2 types of bounding boxes:
包围盒：常见的几何基元，描述对象的体积，2种包围盒类型
- Axially Aligned Bounding Box **(AABB)**. Aligned to the XYZ axes.
- Arbitrarily Oriented Bounding Box **(OBB)**.


## 表示AABB Representing AABB
the two **corners** that define an AABB bounding box are <img width="100" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773239-a0d4cc6e-7fca-4cb5-a85c-6bc175fd796c.png"> all the points <img width="50" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773286-a3cc13cd-d522-4497-9e60-fb144ff20f73.png"> inside a bounding box AABB satisfy the inequalities:

- <img width="500" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773608-f40691e3-ad0a-413a-b693-ed6ea81b8d06.png">
the center of the bounding box <img width="15" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773785-6cb11efe-6d8e-4284-a061-0d0c00df4873.png"> is defined by: <img width="250" alt="图片" src="https://user-images.githubusercontent.com/31954987/227773870-f86546ec-434d-486d-8dc1-f721531ec68a.png">
the **size vector** <img width="20" alt="图片" src="https://user-images.githubusercontent.com/31954987/227775769-e2999496-4323-4fa7-99da-3e334e9d3f5c.png">
 is the vector from <img width="75" alt="图片" src="https://user-images.githubusercontent.com/31954987/227774682-bec1936b-d4e1-4430-85d8-4abe431ad778.png"> to <img width="75" alt="图片" src="https://user-images.githubusercontent.com/31954987/227775562-ef2a58b3-0d96-4342-9c32-1b4f311699ed.png">
 and contains the width, height and length of the box in each dimension. sometimes we'll also find the **radius vector**, which is simply <img width="50" alt="图片" src="https://user-images.githubusercontent.com/31954987/227775639-f57a2a32-4f57-49b7-9ff8-ba4ab78fea8d.png">
 or the vector from the center <img width="25" alt="图片" src="https://user-images.githubusercontent.com/31954987/227775690-49e4dd33-e7b5-4cc4-bf52-8cac0c48c6af.png">
to <img width="75" alt="图片" src="https://user-images.githubusercontent.com/31954987/227775562-ef2a58b3-0d96-4342-9c32-1b4f311699ed.png">

> ```
> to unambiguously define an AABB we need at least 2 of 4 vectors P_{min}, P_{max}, c and s. The most 
> common way to define an AABB is through P_{min} and P_{max}.
> ```

