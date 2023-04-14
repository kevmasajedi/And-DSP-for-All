# Linearity
Linearity is a desirable property. It makes things more predictable. If you need one egg to bake a cake, you'll need four eggs to bake four. That's linear. But suppose you're not in the mood for cakes and want to just have some hard-boiled eggs! If you need 15 minutes for one, you'll still need just 15 minutes (or something around that) for ten. That's non-linear.

So, linear things are predictable, while non-linear things can be more tricky to predict. It can be said that _linearity makes things predictable_. 

That was for breaking the ice. Now, suppose we have a function that takes a number _x_, multiplies it by 5: $f(x)=5x$ Now consider the following cases:
* $x=3 => f(3) = 15$
* $x=3+1 => f(3+1) = 5(3+1) = 5*3 + 5*1 = f(3) + f(1)$
* $x = 2 * 3 => f(2*3) = 5*2*3 = 2*5*3 = 2*f(3)$

The above cases, show that the function is linear. More generally, a linear function must satisfy two properties, for _every input_:
1. Additivity: $f(x + y) = f(x) + f(y)$
2. Homogeneity: $f(ax) = af(x)$

And voila! That's the formal definition of linearity.
