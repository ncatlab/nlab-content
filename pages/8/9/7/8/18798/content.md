
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

See at _[[trigonometric function]]_.

## Definitions

The _cosine function_ is the [[function]] $\cos \;\colon\; \mathbb{R} \to \mathbb{R}$ from the [[real numbers]] to themselves which is characterized by the following equivalent conditions:

1. $\cos$ is the unique [[solution]] among [[smooth functions]] to the [[differential equation]]/[[initial value problem]]

   $$ 
     cos'' = -cos 
   $$

   (where a prime indicates the [[derivative]]) subject to the [[initial conditions]] 

   $$ 
     \begin{aligned}
       cos(0) &= 1
       \\
       cos'(0) & = 0
       \,.
     \end{aligned}
   $$

1. ([[Euler's formula]]) $\cos$ is the [[real part]] of the [[exponential function]] with [[imaginary number|imaginary]] argument

   $$
     \begin{aligned}
       \cos(x) & = Re\left( \exp(i x) \right)
       \\
       & = \frac{1}{2}\big( \exp(i x) + \exp(- i x)\big)
     \end{aligned}
     \,.
   $$

1. $\cos$ is the unique function given by the infinite [[series]]

$$\cos(x) \coloneqq \sum_{i = 0}^{\infty} \frac{(-1)^i x^{2 i}}{(2 i)!}$$

### In arbitrary Archimedean ordered fields

In general, [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[fields]] which are not [[sequentially Cauchy complete]] do not have an cosine function. Nevertheless, the cosine map is still guaranteed to be a [[partial function]], because every Archimedean ordered field is a [[Hausdorff space]] and thus a [[sequentially Hausdorff space]]. Therefore an [[axiom]] could be added to Archimedean ordered fields $F$ to ensure that the cosine partial function is actually a total function:

**Axiom of cosine function:** _For all elements $x \in F$, there exists a unique element $\cos(x) \in F$ such that for all positive elements $\epsilon \in F_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then  $-\epsilon \lt \left(\sum_{i = 0}^{n} \frac{(-1)^i x^{2 i}}{(2 i)!}\right) - \cos(x) \lt \epsilon$._

### In the dual numbers

The [[dual number]] real algebra $\mathbb{D} \coloneqq \mathbb{R}[\epsilon]/\epsilon^2$ has a notion of sine and cosine function, which are the solutions to the system of functional equations $\sin(x + \epsilon) = \sin(x) + \cos(x) \epsilon$ and $\cos(x + \epsilon) = \cos(x) - \sin(x) \epsilon$ with $\sin(0) = 1$ and $\cos(0) = 1$. 

## Related concepts

* [[periodic function]]

* [[trigonometry]]

* [[sine]]

* [[arccos]]

* [[exponential]]

* [[exponential ring]]

* [[Euler's formula]]

* [[trigonometric identity]]

## References

* Wikipedia, _[Sine and cosine](https://en.wikipedia.org/wiki/Sine_and_cosine)_

[[!redirects cos]]

[[!redirects cosine function]]
[[!redirects cosine functions]]