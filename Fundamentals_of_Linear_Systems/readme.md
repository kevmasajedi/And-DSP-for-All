# Fundamentals of Linear Systems

Mathematicians are historically weak on their marketing departments. How can you coin a more boring term than a _linear system_? It's actually a game-changer, however. These systems, which simply have a linear relationship between inputs and outputs, are the bedrock of modern engineering.

These systems enable us to model and control complex systems like aircraft, robots, and power grids. They allow us to understand the motion of planets, the behavior of subatomic particles, and even the spread of epidemics.

## Linear Time Invariant Systems ▶️
Understanding _LTI Systems_ is a milestone in learning about DSP. As the name suggests, these systems - which by the way, I think have a cooler ring to their name than just linear - exhibit __time invariance__ and __linearity__.  _Time invariance_ means that the system's behavior doesn't change over time, while _linearity_ means that the system's output is proportional to its input. LTI systems are incredibly predictable - and this predictability is what makes these systems useful in modeling real electical, mechanical, biological and _you-name-it_ phenomena.  

But being LTI, is only half of the story. The other half is how to actually predict the behavior of an LTI system. For that should know about __convolution__ and __impulse response__. For now, consider _convolution_ to be just a mathematical operation, like multiplication, division, etc... and consider _impulse response_ as something like revving an engine up, to test its performance. Suppose you could know everything about an engine's response, just by revving it up! That's what LTI systems are about: _The response of the system to any input can be found using convolution by the system's impulse response_.

Below, are the modules that provide deeper insights on the terms mentioned above:
* [Linearity](linearity/readme.md) 📈
* [Time Invariance](time_invariance/readme.md) 🦥
* [Impulse Response](impulse_response/readme.md) 🔨
* [Convolution](convolution/readme.md) ✳️

## An Intuitive Example 🪄
Now that you have worked your way through the above definitions, It's the time for an intuitive example to show how these properties actually fit together. Suppose we have a close to ideal _impulse_ like this:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/d1.jpg?raw=true" width="500px" /></p>

And we have a system - in this case, a fictional _filter_ - which gives us this _impulse response_. This is our $f(\tau)$:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/d2.jpg?raw=true" width="500px" /> </p>

We're interested to know, how this filter, would change an input of _1 hertz sine-wave_, which is our $g(\tau)$:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/d3.jpg?raw=true" width="500px" /> </p>

As we've learned, to convolve $f$ and $g$, we need to reflect and offset one of the functions. Here we've $g(t-\tau)$ along with $f(\tau)$:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/d4.jpg?raw=true" width="500px" /> </p>

At last, we're ready to slide these functions over each other and calculate the __integral of the product of the two functions__. Which is plotted in black, and is the convolution of f and g: $(f*g)(t)$:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/d5.gif?raw=true" width="500px" /> </p>

## Causality and Stability ⚖️

A system is __causal__ if its output only depends on the past and present inputs and not on future inputs. You might ask, How can the output of the system, depend on the future? Well, in this context, we mean that the system should not try to predict or anticipate the future inputs. If the system in any way tries to anticipate the future, whether by using a random number, or tossing a coin or by taroot cards, it is not casual.

More formally, you remember that the _impulse_ is corresponded with _dirac delta function_ which is 1 at $t=0$, and 0 everywhere else. So, It only makes sense that for a casual system, its impulse response $h(t)$ must be equal to zero for all $t<0$ 

$$h(t)=0 ;  t<0$$

And what do we mean by __stability__? Obviously, you do not expect a stable system to be _triggered into chaos_ by just a reasonable, finite input. You expect a voice recorder, that when you speak a bit louder, it record your a bit louder, but not infinitely louder, like, catching fire. _That's unstable!_

Formally, there's this term, _BIBO stability_. It is a guarantee that if input to the system is bounded (not infinite), the output of the system will also be bounded. Hence, Bounded-Input results in Bounded-Output (BIBO).

The mathematical condition for a LTI-system to be BIBO stable, is that its _impulse response_ should be _absolutely summable_. Meaning that if you sum-up all the values of $h(t)$ for every $t$, your sum should appraoch a limit, not infinity. Or:

$$ \sum_{t=0}^{\infty}\left|h(t) \right|<\infty $$

## Differential Equations ∫
Differential equations, are a class of equations that associate _the rate of change_ of some quantity, to the quantity itself. Don't panic! If you don't like to delve into mathematics, that's ok too. Because you don't have to know a great deal about differential equations to continue learning about DSP. You just have to know how these two subjects are related.

In DSP, we deal with _discrete linear differential equations_. Every LTI system, can be represented by such equation. And that's extremely useful. Take a look at this equation:

$$ y(n) = -a_1 y(n-1) + b_0 x(n) + b_1 x(n-1) $$

This is the __most general__ form of _first order_ discrete differential equation. You remember that $x(n)$ is the input sequence and $y(n)$ is the output. So, $x(n-1)$ and $y(n-1)$ are just input and output sequences with _one sample delay_. This is great! It means, you just need to apply delays along with some coefficients to the inputs and outputs, to make a first order LTI system:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/de1.jpg?raw=true" width="500px" /> </p>

Likewise, for a _second order_ differential equation:

$$ y(n) = -a_1 y(n-1) - a_2 y(n-2) + b_0 x(n) + b_1 x(n-1) + b_2 x(n-2) $$

You just need _one_ and _two sample delays_ along with some coefficients to make a second order LTI system.

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/de2.jpg?raw=true" width="500px" /> </p>

What about higher-order systems? well, they're just a series or parallel combination of first and second-order systems. I reckon by now you should see some _real_ potential in this topic.

## Calculating Impulse Response ±
Again, you might find some intimidating statements below. Unfortunately, we can not introduce, or discuss them here. You have to pick a book for that. Differential Equations and Linear Algebra by Gilbert Strang is a good one. But __remember:__ you can just use _Wolfram Alpha_ and many other free software to solve these equations.

When you have your LTI system represented as an _n-th order discrete linear differential equation_, You don't have to actually feed input to it, to _measure_ its impulse response. You can mathematically, calculate the impulse response $h(n)$. You just have to:

* Find the _homogenous solution_ which is the solution to the equation, assuming all inputs are 0.
* Find a particular solution (i.e. by using the method of variation of parameters)

__The impulse response is the sum of the homogeneous and particular solutions of the system's differential equation with the input being an impulse function.__ 


## Sinusoids and Eigenfunctions λ
Earlier, we've made it clear that from all the complexity zoo of various types of systems, we're only going to deal with LTI systems. It was quite a deal, as we learned not only we can use LTI systems to model real-world phenomena, but they also have very desirable properties that makes such modeling easy and efficient. Now, we're going to further that deal, with another constructive limitation!

As most of the real-world systems can be modeled as LTIs, most of the real-world _signals_ can be modeled as _sinosoids_. And that's great news too. Sinusoid inputs can be represented as $x(n) = e^{jwn}$ and you know what's that? An __eigenfunction__!

Eigenfuncions, despite their name, are friendly functions that don't change faces under linear operations. As LTI systems are linear, if you feed them sinusoids, you'll get sinusoids, just with a different scale. Eigenfunction in, eigenfunction out! If $f$ be an eigenfunction, then feeding it to a LTI system $LTI[f]$ will result in:

$$ LTI[f] = \lambda f $$

So, $f$ will come out in one peace, just scaled by a constant value $\lambda$. This value is called __eigenvalue__. 

So, in a formal way, _eigenfunction_ is a special function that under linear operations, will result in same function scaled by a constant factor, called _eigenvalue_. 

## Frequency Response ∿
The __complex exponential function__ $x(n)=e^{jwn}$ is an eigenfunction. So, when a complex exponential input feeds an LTI system with impulse response $h(n)$, the output $y(n)$ is also a complex exponential of the same frequency. It is scaled by $H(\omega)$, which indicates _the scale factor of input signal depends only on its frequency_. Thus:

$$ y(n)= H(\omega) * e^{jwn} $$

$H(\omega)$ is the __frequency response__ of the LTI system. More accurately, we can show this by $H(e^{jw})$, which is defined as:

$$ H(e^{jw}) =  \sum_{n=-\infty}^{\infty}h(n)e^{-jwn} $$

These two equations have a huge implication. They say, you can calculate the _frequency response_ of a system from its _impulse response_ and then you don't need to use the troublesome process of _convolution_ anymore! Instead, you simply multiply the frequency response with any input sequence.

So, just by having a representation of an LTI system, in the form of a differential equation, you can calculate its _impulse response_ then its _frequency response_, and then you can simply multiply any input to the frequency response to calculate the output. If you're interested, follow this step-by-step example here:

* [Example of Frequency Response of First Order Systems](frequency_response_first_order/readme.md) ✏️

## Characteristics of Frequency Response
Below, is the plot that shows the magnitude and phase of the frequency response for the system we examined in the previous example. The horizontal axis represents the angular frequency $\omega$, while the vertical axis shows the magnitude (red) of response in _decibels (dB)_ and the phase in radians:

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/fr1.jpg?raw=true" width="500px" /> </p>

As you can see in this plot, there are three important characteristics about the _frequency response:_

* __Periodicity__: The frequency response of a system is periodic with a period of 2π. This means that if you shift the frequency axis by 2π, the response will be identical to the original response. [Why periodic?🐇🕳](periodicity/readme.md)

* __Symmetry of Magnitude__ related to π: The magnitude of the frequency response exhibits a symmetry around π. That is, if you reflect the magnitude plot about the vertical line at π, you get the same plot. [Why symmetric?🐇🕳](magnitude_symmetry/readme.md) 

* __Anti-symmetry of Phase__ related to π: The phase of the frequency response exhibits an anti-symmetry around π. That is, if you reflect the phase plot about the vertical line at π, you get the negative of the original plot. [Why anti-symmetric?🐇🕳](phase_anti_symmetry/readme.md) 

## Units of Frequency
Above, we examined frequency response characteristics, such as _2π periodicity_ and _π symmetry of magnitude_. However, you might be wondering how these properties correspond to the unit of frequency that we're familiar with in the real world, which is _Hertz (Hz)_.

In signal processing and communication systems, the __unit of frequency is typically the same as the sampling frequency__, which is the rate at which a continuous-time signal is sampled and converted into a discrete-time signal. For example, if the sampling frequency is 10 kHz, then it means that 10,000 samples are taken per second. 

The 2π periodicity of the frequency response means that the response is periodic with a period of 2π radians per second, which corresponds to the sampling frequency in Hz. So, for our example, the periodicity of the signal is 10 kHz in the frequency domain. 

The π symmetry of the magnitude of the frequency response and π anti-symmetry of phase, mean that the response is symmetric about the __Nyquist frequency__, which is defined simply as half of the sampling frequency in Hz, or 5kHz in the case of our example.

If you decide to use _radians per second_ ($\omega$) as the unit of frequency domain, you'll need to multiply all values by 2π, as $\omega = 2 \pi f$. So, for our example, the frequency response would be periodic around 20,000π and symmetric in magnitude (and anti-symmetric in phase) around 10000π. 

In signal processing and communication systems, it is common to represent frequencies relative to the sampling frequency, rather than using absolute frequencies measured in Hz. This is because it allows for a more convenient representation of the frequency response, and makes it easier to compare and analyze different signals and systems.

To represent frequencies relative to the sampling frequency, we use a _normalized frequency_ scale, which is defined as the ratio of the actual frequency to the sampling frequency. For example, if the actual frequency is 2 kHz and the sampling frequency is 10 kHz, then the normalized frequency is 2/10 = 0.2.


## Footnotes 📝
__Not everything is linear:__ Despite their widespread use and importance, linear systems have inherent limitations. They are only valid for systems that exhibit a linear relationship between inputs and outputs, which is often not the case for many real-world systems. Nonlinear systems, characterized by complex and unpredictable behavior, pose significant challenges for scientists and engineers. For an introduction, you can read the book _Chaos: Making a New Science_ by James Gleick.
