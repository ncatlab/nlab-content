
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

There is another axiom which uses the fact that derivatives of functions are well defined in the [[ordered local ring|ordered local]] [[local Artin algebra|Artin $F$-algebra]] $F[\epsilon]/\epsilon^2$ by the equation $f(x + \epsilon) = f(x) + f'(x) \epsilon$:

**Axiom of sine and cosine functions:** _Let $F[\epsilon]/\epsilon^2$ be the ordered local Artin $F$-algebra, with non-zero non-positive non-negative [[nilpotent element]] $\epsilon \in F[\epsilon]/\epsilon^2$ where $\epsilon^2 = 0$ and canonical $F$-algebra homomorphism $h:F \to F[x]/x^2$. There exists unique functions $\sin:F \to F$ and $\cos:F \to F$ and functions $\sin':F[\epsilon]/\epsilon^2 \to F[\epsilon]/\epsilon^2$ and $\cos':F[\epsilon]/\epsilon^2 \to F[\epsilon]/\epsilon^2$ such that for every element $x \in F$, $h(\sin(x)) = \sin'(h(x))$, $h(\cos(x)) = \cos'(h(x))$, $\sin'(x + \epsilon) = \sin'(x) + \cos'(x) \epsilon$, $\cos'(x + \epsilon) = \cos'(x) - \sin'(x) \epsilon$, $\sin'(0) = 0$, and $\cos'(0) = 1$._

### In the dual numbers

The [[dual number]] real algebra $\mathbb{D} \coloneqq \mathbb{R}[\epsilon]/\epsilon^2$ has a notion of sine and cosine function, which are the solutions to the system of functional equations $\sin(x + \epsilon) = \sin(x) + \cos(x) \epsilon$ and $\cos(x + \epsilon) = \cos(x) - \sin(x) \epsilon$ with $\sin(0) = 1$ and $\cos(0) = 1$. 

## In constructive mathematics

In classical mathematics, one could prove that the [[modulated Cantor real numbers]] $\mathbb{R}_C$ are [[sequentially Cauchy complete]] and equivalent to the [[HoTT book real numbers]] $\mathbb{R}_H$. However, in constructive mathematics, the above cannot be proven; while the HoTT book real numbers $\mathbb{R}_H$ are still sequentially Cauchy complete, the modulated Cantor real numbers $\mathbb{R}_C$ in general cannot be proven to be sequentially Cauchy complete. In particular, this means that the sequence 

$$\sum_{i = 0}^{n} \frac{(-1)^i x^{2 i}}{(2 i)!}$$ 

does not have a limit for all modulated Cantor real numbers $x \in \mathbb{R}_C$. However, the sequence, by definition of $\mathbb{R}_C$, does have a limit for all [[rational numbers]] $x \in \mathbb{Q}$; this means that one could restrict the [[domain]] of the cosine function to the rational numbers $\cos:\mathbb{Q} \to \mathbb{R}_C$, and define it in the usual manner:

* For all rational numbers $x \in \mathbb{Q}$, there exists a unique modulated Cantor real number $\cos(x) \in \mathbb{R}_C$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then $-\epsilon \lt \sum_{i = 0}^{n} \frac{(-1)^i x^{2 i}}{(2 i)!} - \cos(x) \lt \epsilon$.

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

Discussion in [[constructive analysis]]:

* [[Errett Bishop]], §7 in: *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* [[Errett Bishop]], [[Douglas Bridges]] §7 in: *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

See also:



* Wikipedia, _[Sine and cosine](https://en.wikipedia.org/wiki/Sine_and_cosine)_

[[!redirects cos]]

[[!redirects cosine function]]
[[!redirects cosine functions]]