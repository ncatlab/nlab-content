
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

There is another axiom which uses the fact that derivatives of functions are well defined in the [[ordered local ring|ordered local]] [[local Artin algebra|Artin $F$-algebra]] $F[\epsilon]/\epsilon^2$ by the equation $f(x + \epsilon) = f(x) + f'(x) \epsilon$:

**Axiom of sine and cosine functions:** _Let $F[\epsilon]/\epsilon^2$ be the ordered local Artin $F$-algebra, with non-zero non-positive non-negative [[nilpotent element]] $\epsilon \in F[\epsilon]/\epsilon^2$ where $\epsilon^2 = 0$ and canonical $F$-algebra homomorphism $h:F \to F[x]/x^2$. There exists unique functions $\sin:F \to F$ and $\cos:F \to F$ and functions $\sin':F[\epsilon]/\epsilon^2 \to F[\epsilon]/\epsilon^2$ and $\cos':F[\epsilon]/\epsilon^2 \to F[\epsilon]/\epsilon^2$ such that for every element $x \in F$, $h(\sin(x)) = \sin'(h(x))$, $h(\cos(x)) = \cos'(h(x))$, $\sin'(x + \epsilon) = \sin'(x) + \cos'(x) \epsilon$, $\cos'(x + \epsilon) = \cos'(x) - \sin'(x) \epsilon$, $\sin'(0) = 0$, and $\cos'(0) = 1$._

### In the dual numbers

The [[dual number]] real algebra $\mathbb{D} \coloneqq \mathbb{R}[\epsilon]/\epsilon^2$ has a notion of sine and cosine function, which are the solutions to the system of functional equations $\sin(x + \epsilon) = \sin(x) + \cos(x) \epsilon$ and $\cos(x + \epsilon) = \cos(x) - \sin(x) \epsilon$ with $\sin(0) = 1$ and $\cos(0) = 1$. 

## In constructive mathematics

In classical mathematics, one could prove that the [[modulated Cantor real numbers]] $\mathbb{R}_C$ are [[sequentially Cauchy complete]] and equivalent to the [[HoTT book real numbers]] $\mathbb{R}_H$. However, in constructive mathematics, the above cannot be proven; while the HoTT book real numbers $\mathbb{R}_H$ are still sequentially Cauchy complete, the modulated Cantor real numbers $\mathbb{R}_C$ in general cannot be proven to be sequentially Cauchy complete. In particular, this means that the sequence 

$$\sum_{i = 0}^{n} \frac{(-1)^i x^{2 i + 1}}{(2 i + 1)!}$$ 

does not have a limit for all modulated Cantor real numbers $x \in \mathbb{R}_C$. However, the sequence, by definition of $\mathbb{R}_C$, does have a limit for all [[rational numbers]] $x \in \mathbb{Q}$; this means that one could restrict the [[domain]] of the sine function to the rational numbers $\sin:\mathbb{Q} \to \mathbb{R}_C$, and define it in the usual manner:

* For all rational numbers $x \in \mathbb{Q}$, there exists a unique modulated Cantor real number $\sin(x) \in \mathbb{R}_C$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \in \mathbb{N}$, if $n \geq N$, then $-\epsilon \lt \sum_{i = 0}^{n} \frac{(-1)^i x^{2 i + 1}}{(2 i + 1)!} - \sin(x) \lt \epsilon$.

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

Discussion in [[constructive analysis]]:

* [[Errett Bishop]], §7 in: *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* [[Errett Bishop]], [[Douglas Bridges]] §7 in: *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

See also

* Wikipedia, _[Sine and cosine](https://en.wikipedia.org/wiki/Sine_and_cosine)_

* {#Trimble} [[Todd Trimble]], _[[toddtrimble:Characterization of sine]]_


[[!redirects sin]]

[[!redirects sine function]]
[[!redirects sine functions]]