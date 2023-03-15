most ppl would swap two variables x and y using a temporary variable, like below: 交换两个变量x y的数值

> ```
> tmp = x
> x = y
> y = tmp
> ```

here's a neat programming trick to swap two values without needing a temp: 整洁的编程技巧 无需temp 交换两个 值

> ```
> x = x xor y
> y = x xor y
> x = x xor y
> ```

to understand this trick, break the statements into unique values: 
> ```
> x1 = x xor y
> y1 = x1 xor y
> x2 = x1 xor y1
> ```

> ```
> x2 = x1 xor y1
> x2 = x1 xor (x1 xor y) //替换 y1
> x2 = (x1 xor x1) xor y  //重组 - 顺序对于 xor 不重要
> x2 = 0 xor y //a xor a => 0
> x2 = y  //0 xor a => a; x2 now has y's original value 
> ```

### Intuitive Understanding 直觉

> ```
> 1:  x = x xor y
> 2:  y = x xor y
> 3:  x = x xor y
> ```
