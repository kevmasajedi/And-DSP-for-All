# Time Invariance 🦥
In general sense, a system is time-invariant if its behavior remains the same over time. Think of a calculator, no matter what time it is, it always gives the same answer to the same inputs. On the other hand, there is time-dependence. Like, sometimes math is fun!

That was easy, but in the context of DSP, we need to think of time invariance, in a more sophisticated way. Suppose you have a time-dependent input function $x(t)$. It can be a radio-wave from your favorite apocalypse news station. You also have a time-dependent output function $y(t)$. It can be the sound wave coming out of your radio. Now, the question is: _Is your "radio" time invariant? _ To answer that, suppose the station starts the program with a 10 minute delay. In other words, you'll have $x(t+10)$. Will your radio output has exactly that amount of delay, or $y(t+10)$ ? Of course, it does. So although both input and output are time dependent, your radio is time-invariant. 

We're now ready for a formal definition: A system is _time-invariant_  if a time delay on the input $x(t+\delta)$ directly results in a time-delay of the output $y(t+\delta)$. In a time-invariant system, the relationship between the input function $x(t)$ and the output function $y(t)$ is constant with respect to time $t$. 

And that's the way with _time invariance_. 
Clock itself, never stops ticking.