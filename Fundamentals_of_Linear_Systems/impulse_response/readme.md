# Impulse Response 🔨
Impulse is a very short, but strong pulse. It's like a loud click. When you input an impulse to a system, it produces a response, that would be its _impulse response_. 

In a more formal way, impulses are mathematically defined as _Dirac delta function_. Simply put, it's a function whose value is _zere everywhere except at zero, which has the value of 1_. It is a mathematical representation of a _infinitely short_ pulse with _infinitely high magnitude_. 

Of course, it is physically impossible to produce such an ideal pulse in reality. But it is a useful concept. For example, It is mathematically proven that such pulse, contains all frequencies. So, the impulse response of a LTI system, defines its response for _all frequencies_. 

That's extremely useful. Because you can use __convolution__ of _any input_ with the system's impulse response to directly predict its output. 

It is one of those rare cases when acting on impulse _does_ lead to good decisions!