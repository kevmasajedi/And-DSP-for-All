# Fundamentals of Linear Systems

Mathematicians are historically weak on their marketing departments. How can you coin a more boring term than a _linear system_? It's actually a game-changer, however. These systems, which simply have a linear relationship between inputs and outputs, are the bedrock of modern engineering.

These systems enable us to model and control complex systems like aircraft, robots, and power grids. They allow us to understand the motion of planets, the behavior of subatomic particles, and even the spread of epidemics.

## Linear Time Invariant Systems
Understanding _LTI Systems_ is a milestone in learning about DSP. As the name suggests, these systems - which by the way, I think have a cooler ring to their name than just linear - exhibit __time invariance__ and __linearity__.  _Time invariance_ means that the system's behavior doesn't change over time, while _linearity_ means that the system's output is proportional to its input. LTI systems are incredibly predictable - and this predictability is what makes these systems useful in modeling real electical, mechanical, biological and _you-name-it_ phenomena.  

But being LTI, is only half of the story. The other half is how to actually predict the behavior of an LTI system? Well, for that should know about __convolution__ and __impulse response__. For now, consider _convolution_ to be just a mathematical operation, like multiplication, division, etc... and consider _impulse response_ as something like revving an engine up, to test its performance. Suppose you could know everything about an engine's response, just by revving it up! That's what LTI systems are about: _The response of the system to any input can be found using convolution by the system's impulse response_.

Below, are the modules that provide deeper insights on the terms mentioned above:
* [Linearity](linearity/readme.md)
* [Time Invariance](time_invariance/readme.md)
* [Impulse Response](impulse_response/readme.md)
* [Convolution](convolution/readme.md)

## Footnotes
__Not everything is linear:__ Despite their widespread use and importance, linear systems have inherent limitations. They are only valid for systems that exhibit a linear relationship between inputs and outputs, which is often not the case for many real-world systems. Nonlinear systems, characterized by complex and unpredictable behavior, pose significant challenges for scientists and engineers. For an introduction, you can read the book _Chaos: Making a New Science_ by James Gleick.