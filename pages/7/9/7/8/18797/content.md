
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

The sine function $\sin$ is one of the basic [[trigonometric functions]].

It may be thought of as assigning to any [[angle]] the [[distance]] to a chosen axis of the point on the [[unit circle]] with that angle to that axis.


## Definitions

The _sine function_ is the [[function]] $\sin \;\colon\; \mathbb{R} \to \mathbb{R}$ from the [[real numbers]] to themselves which is characterized by the following equivalent conditions:

1. $\sin$ is the unique [[solution]] among [[smooth functions]] to the [[differential equation]]/[[initial value problem]]

   $$ 
     sin'' = -sin 
   $$

   (where a prime indicates the [[derivative]]) subject to the initial conditions 

   $$ 
     \begin{aligned}
       sin(0) &= 0
       \\
       sin'(0) & = 1
       \,.
     \end{aligned}
   $$

1. ([[Euler's formula]]) $\sin$ is the [[imaginary part]] of the [[exponential function]] with imaginary argument

   $$
     \begin{aligned}
       \sin(x) & = Im\left( \exp(i x) \right)
       \\
       & = \frac{1}{2 i}\left( \exp(i x) - \exp(- i x)\right)
     \end{aligned}
     \,.
   $$

1. $\sin$ is the unique function which 

   1. is [[continuous function|continuous]] at $0$ 

   1. satisfies the [[inequality]]

      $$ 
        1 - x^2 \;\leq\; \frac{\sin(x)}{x} \;\leq\; 1 
      $$

      and the [[equation]]

      $$ 
        \sin(3 x) \;=\; 3 \sin(x) - 4 (\sin(x))^3 
      $$

   (see [Trimble](#Trimble): *[[toddtrimble:Characterization of sine]]*. Some additional discussion at the [nForum](https://nforum.ncatlab.org/discussion/5773/a-short-note-for-todd-trimble/).)

1. $\sin$ is the unique function given by the infinite series

$$\sin(x) \coloneqq \sum_{i = 0}^{\infty} \frac{(-1)^i x^{2 i + 1}}{(2 i + 1)!}$$

### In arbitrary Archimedean ordered fields

In general, Archimedean ordered fields which are not [[sequentially Cauchy complete]] do not have an sine function. Nevertheless, the sine map is still guaranteed to be a [[partial function]], because every Archimedean ordered field is a [[Hausdorff space]] and thus a [[sequentially Hausdorff space]]. Thus, an axiom could be added to an Archimedean ordered field $F$ to ensure that the sine partial function is actually a total function:

**Axiom of sine function:** _For all elements $x \in F$, there exists a unique element $\sin(x) \in F$ such that for all positive elements $\epsilon \in F_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then  $-\epsilon \lt \left(\sum_{i = 0}^{n} \frac{(-1)^i x^{2 i + 1}}{(2 i + 1)!}\right) - \sin(x) \lt \epsilon$._

### In the dual numbers

The [[dual number]] real algebra $\mathbb{D} \coloneqq \mathbb{R}[\epsilon]/\epsilon^2$ has a notion of sine and cosine function, which are the solutions to the system of functional equations $\sin(x + \epsilon) = \sin(x) + \cos(x) \epsilon$ and $\cos(x + \epsilon) = \cos(x) - \sin(x) \epsilon$ with $\sin(0) = 1$ and $\cos(0) = 1$. 

## Properties

### Relation to other functions

See at _[[trigonometric identity]]_.


### Roots

The [[roots]] of the sine function, hence the argument where its value is [[zero]], are the [[integer]] multiples of [[pi]] $\pi \in \mathbb{R}$.
 

## Related concepts

* [[periodic function]]

* [[cosine]]

* [[arcsin]]

* [[hyperbolic sine]], [[hyperbolic cosine]]

* [[exponential]], [[exponential ring]], [[Euler's formula]]

* [[trigonometric identity]] 

* [[pi]], [[circle constant]]

## References

* {#Trimble} [[Todd Trimble]], _[[toddtrimble:Characterization of sine]]_

See also

* Wikipedia, _[Sine and cosine](https://en.wikipedia.org/wiki/Sine_and_cosine)_

[[!redirects sin]]

[[!redirects sine function]]
[[!redirects sine functions]]