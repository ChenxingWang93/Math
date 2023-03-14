most ppl would swap two variables x and y using a temporary variable, like below: 交换两个变量x y的数值

> ```
> tmp = x
> x = y
> y = tmp
> ```

here's a neat programming trick to swap two values without needing a temp:

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

