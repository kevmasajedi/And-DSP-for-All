# Complex Numbers 🐇🕳️

Complex numbers may seem, well, complex, but they are actually just as real as the ordinary numbers we use every day. You see, while ordinary numbers can be plotted on a straight line, complex numbers require a two-dimensional plane to fully represent them. This plane has a real axis and an imaginary axis, and any complex number can be expressed as a combination of a real number and an imaginary number.

The term "imaginary" has caused quite a bit of confusion over the years when it comes to complex numbers. It was originally coined by mathematician René Descartes in the 17th century, and at the time it was meant to convey the idea that these numbers weren't "real" in the same sense that ordinary numbers are. Unfortunately, this term has led many people to mistakenly think that complex numbers are somehow less important or less fundamental than other kinds of numbers.

But the truth is that "imaginary" is really a misnomer, because complex numbers have just as much mathematical and physical significance as any other kind of number. In fact, complex numbers are essential to a wide range of fields, from electrical engineering to quantum mechanics.

## Evolution (and Denial) of Number Systems

In the earliest days of human civilization, people only needed to work with whole numbers, or integers, to keep track of things like livestock and food supplies. As societies became more complex and developed systems of trade and commerce, the need for fractions, or rational numbers, arose.

Later on, mathematicians discovered the existence of irrational numbers, such as the square root of 2, which cannot be expressed as a simple fraction. This discovery challenged the very foundations of mathematics and led to the development of new techniques like calculus. According to legend, Pythagoras and his followers were averse to the idea of irrational numbers because they believed that all numbers could be expressed as ratios of integers, or in other words, as fractions. A Pythagorean disciple named Hippasus discovered the irrationality of the square root of 2 and shared this knowledge with his colleagues. Some accounts even suggest that Pythagoras himself was so disturbed by the discovery of irrational numbers that he ordered Hippasus to be put to death, as punishment for revealing this unsettling truth!

As mathematical knowledge continued to advance, the concept of negative numbers was introduced, allowing for the representation of debt, loss, and other phenomena. Negative numbers and zero have too faced their fair share of opposition and skepticism over the years. The concept of negative numbers didn't really gain widespread acceptance until the 17th century, when mathematicians like René Descartes and John Wallis began to use them in their work.

Zero, meanwhile, was a topic of debate for centuries. In some cultures, such as ancient India, zero was recognized as a number in its own right and was used in mathematical calculations. But in Europe, the idea of zero was viewed with skepticism and even hostility for many years.

In fact, some early accounts suggest that the ancient Greeks saw zero as a kind of "empty" or "meaningless" concept, and that they believed that all numbers had to represent something concrete in the real world. It wasn't until the 13th century that the Italian mathematician Fibonacci introduced the concept of zero to Europe, helping to pave the way for its eventual acceptance and use in modern mathematics.

So you see, even concepts that seem simple and straightforward to us today, like negative numbers and zero, have faced denial and opposition. And that brings us to _complex numbers:_

## Evolution (and Denial) of Complex Numbers
For many centuries, mathematicians were skeptical of the idea of complex numbers, which include both real and imaginary parts. In fact, the term "imaginary" was originally intended as a derogatory term, reflecting the belief that these numbers were somehow less significant or less real than ordinary numbers.

Despite this skepticism, however, some mathematicians continued to explore the properties of imaginary numbers.In the 16th century, the Italian mathematician Gerolamo Cardano was one of the first to recognize that certain equations, such as $x^2 + 1 = 0$, had no solutions in the real number system. Cardano introduced the concept of imaginary numbers, which he referred to as "fictitious" or "impossible" numbers. He recognized that these numbers could be used as a tool to find real solutions to certain equations that were previously thought to be unsolvable. However, Cardano and other mathematicians of his time still viewed imaginary numbers with suspicion.

In the 17th century, the mathematician John Wallis suggested that imaginary numbers could be thought of as a "vehicle" that carried one from a real question to a real answer. In other words, while imaginary numbers themselves might not be "real" in the same sense as ordinary numbers, they could be used to find real solutions to certain equations and problems. Wallis recognized that complex numbers allowed mathematicians to solve equations that were previously thought to be impossible to solve using real numbers alone. 

While Wallis's ideas about complex numbers were initially met with skepticism, they paved the way for a new understanding of these numbers. One of the most important breakthroughs in this area came in the late 18th and early 19th centuries, when the mathematician Carl Friedrich Gauss began to investigate the properties of complex numbers in more detail. Gauss was particularly instrumental in advancing our understanding of complex numbers. He developed what is now known as the fundamental theorem of algebra, which states that every polynomial equation has at least one complex root. This theorem was a major breakthrough in the study of complex numbers, and it helped to establish them as a legitimate and important area of mathematics.

In fact, the concept of complex numbers eventually became so important that mathematicians began to view them as just as fundamental as the real numbers that we use every day. Today, complex numbers are an essential tool for understanding everything from the behavior of waves to the structure of the universe itself, and they continue to play a crucial role in the ongoing development of mathematics and science.

## Mathematical Definitions
 In mathematics, a complex number is defined as a number of the form $a + bj$, where a and b are real numbers and $j$ is an imaginary unit, satisfying the equations:

$$ j^2 = -1 $$

$$ j = \sqrt{-1} $$ 
 
The real part of a complex number $z = a + bj$ is denoted as $Re(z) = a$, and the imaginary part is denoted as $Im(z) = b$. You can think of them like coordinates on a two-dimensional plane, which we call the complex plane. The real part $a$ corresponds to horizontal axis and the imaginary part $b$ corresponds to vertical axis. 

<p align="center"><img src="https://github.com/kevmasajedi/And-DSP-for-All/blob/main/Fundamentals_of_Linear_Systems/complex_numbers/c1.jpg?raw=true" width="500px" /></p>

### Polar Representation:
Representing complex numbers in _polar coordinates_ makes many calculations, much easier. Instead of the form $ z = a + bj $ you can use the polar form:

$$ z = re^{j\theta} $$

Where:

$$ |z| = r = \sqrt{a^2 + b^2} $$

$$ ∠z = \theta = tan^{-1}(\frac{b}{a}) $$

You might wonder what all this means. Well, the polar representation of a number is a way of expressing it in terms of its __magnitude__ and __angle__. $r$ is the magnitude which is found using Pythagorean theorem. and $\theta$ is the angle which is found using the inverse tangent function, _in radians_. It is also common to show the magnitude as $|z|$ and angle as $∠z$:

$$ z = |z| e^{j∠z} $$