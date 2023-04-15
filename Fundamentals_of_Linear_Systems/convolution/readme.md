# Convolution ✳️
Convolution is itself, an intimidating word and giving a general mathematical definition of it, would make everything even more convoluted. However, when you think about the concept of convolution, in more concrete ways, it is arguably intuitive.

Essentially, when you convolve two functions, you:
1. Reflect one of the functions, about the _y-axis_.
2. You slide one function over the other, and multiply them point-by-point.
3. Calculate the area under the curve resulting from the above operations.

To have an intuitive grasp, take a look at this gif. 

![](https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/convolution/c1.gif?raw=true)

In the above example, the __blue__ function $f(\tau)$ is convoluted with __red__ function $g(\tau)$. In order to do that, $g(\tau)$ is __reflected $g(-\tau)$__ and __offseted $g(t-\tau)$__ to slide over $f(\tau)$. The __area under product of the two $f(\tau)g(t-\tau)$__ is calculated at each point and plotted with __black__. That's the convolution of these two function, which is $(f*g)(t)$.

So, in other words: When you convolve two functions, you reflect one of the functions about the y-axis, and calculate the _integral_ of the _product of the two functions_. 

And that should give you an intuitive, practical grasp of the concept of convolution.

## Footnotes 📝
When a function is symmetric about the y-axis (like the red square in above example), it is called an __even function__. In case of even functions, $f(x)$ is equal to $f(-x)$. So it doesn't matter if you reflect them.