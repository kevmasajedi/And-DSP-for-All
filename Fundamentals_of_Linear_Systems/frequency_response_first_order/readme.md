# Example of Frequency Response Of First-Order Systems ✏️
Consider a first-order LTI system which is represented by this discrete differential equation, with initial condition $y(-1)=0$:

$$ y(n) = x(n) + K*y(n-1) $$

To compute the impulse response, we just have to feed our system an _impulse_ δ(n)  which by definition is a function that is _1 at 0 and 0 everywhere else_. So:

* $n<0 => y(n)=0$ (from the initial condition $y(-1) = 0$ and since $δ(n) = 0$ for n ≠ 0) 
* $n = 0 => y(n) = δ(0) + Ky(-1) = 1$
* $n > 0 => y(n) = Ky(n-1) => y(n) = K^n$

Thus, the _impulse response_ $h(n)$ for values of $n \geq 0$ is:

$$h(n)= K^n$$

From the _frequency response_ definition, we shall have:

$$ H(e^{jw}) =  \sum_{n=0}^{\infty}K^n e^{-jwn} $$

This is an infinite geometric series with the first term a = 1 (when n = 0, K^n = 1) and common ratio r = K * e^(-jω). To find the sum of this series, we can use the geometric sum formula:

$$ S = \frac{a(1-r^n)}{(1-r)}$$

In this case, as the sum goes to infinity (N → ∞), we can simplify the formula:

$$ H(e^{jw}) = \frac{a}{1-r} = \frac{1}{1-K*e^{-jw}} $$

Now that we have the frequency response, we can plot its _magnitude_ $|H(e^{jw})|$ and _phase_ $∠H(e^{jw})$ to study it further.

$$ |H(e^{jw})| = \frac{1}{\sqrt{K^2 - 2Kcos(w) + 1}} $$

$$ ∠H(e^{jw}) = arctan(\frac{-Ksin(w)}{1-Kcosw}) $$

Below, you can find the magnitude (red) and phase (blue) of the frequency response plotted for values of K starting from 0 to 1:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/frequency_response_first_order/r1.gif?raw=true" width="500px" /> </p>