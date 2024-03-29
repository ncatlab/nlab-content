# Hahn series

* table of contents
{: toc}

## Idea

A Hahn series is a generalization of a [[formal power series]] which allows non-integer exponents and transfinite sums, as long as the exponents are well-ordered.

## Definition

Let $G$ be a [[linear order|linearly]] [[ordered abelian group]], and $k$ a field.

+-- {: .un_defn}
###### Definition
The ring of **Hahn series** with [[value group]] $G$, denoted $k[t^G]$ (or sometimes $k[[t^G]]$ or $k((t^G))$), is the ring of functions $f\colon G \to k$ such that $\{x \in G : f(x) \neq 0\}$ is [[well-ordered]] as as a subset of $G$ (or, sometimes, as a subset of the opposite poset $G^{op}$). Addition is defined pointwise, and multiplication is defined by the [[convolution]] product: 
$$(f \cdot g)(x) = \sum_{y+z = x \in G} f(y)g(z)$$
=-- 

Notationally, we may write a Hahn series $f\colon G \to k$ as $\sum_{x\in G} f(x) t^x$.

## Properties

+-- {: .un_theorem}
###### Theorem
The ring $k[t^G]$ is a field. If $k$ is [[algebraically closed field|algebraically closed]], then $k[t^G]$ is algebraically closed provided that $G$ is [[divisible group|divisible]]. 
=-- 

As a corollary, if $G$ is divisible, $k[t^G]$ is [[real closed field|real closed]] if $k$ is real closed. This is because the adjunction of a square root of $-1$ would make $k[t^G]$ algebraically closed, since this gives the same result as constructing the Hahn series over the algebraically closed field $k[\sqrt{-1}]$.

The [[valuation ring|multiplicative valuation]] $v(f)$ of an element $f\in k[t^G]$ is the least $x \in G$ for which $f(x) \neq 0$.  This yields a [[valuation ring]], such a valuation ring determines and is determined by a valuation on a [[field]].  The field $k[t^G]$ is a [[complete metric space|complete]] [[ultrametric space]] (and indeed a [[spherically complete field]]) with respect to this valuation, *but* unlike for [[formal power series]] the formal series $\sum_{x\in G} f(x) t^x$ do not actually "converge" in this metric.


## Examples

* If $G=\mathbb{R}$, then we have Hahn series such as
  $$ t^1 + t^{3/2} + t^{5/3} + t^{7/4} + \cdots $$

* Via Conway normal forms, the ring of Hahn series with $k=\mathbb{R}$ and with value group the [[surreal numbers]] is isomorphic to the surreal numbers themselves.  In other words, the surreals are a [[fixed point]] of the "Hahn series with real coefficients" [[functor]] on the [[category]] of abelian groups.  However, the surreals are not the [[inductive type|initial fixed point]] of this functor, since there are surreals that appear as exponents in their own Conway normal form --- for instance, the [[∞-numbers]].

* Well-based [[transseries]] can be constructed by iterating the Hahn series construction.

* If $G=\mathbb{Z}$, then a Hahn series is precisely a [[formal Laurent series]], i.e. $k[t^{\mathbb{Z}}] = k((t))$.

* If $G=\mathbb{Q}$, then $k[t^{\mathbb{Q}}]$ properly contains the [[Levi-Civita field]], as the subclass of those Hahn series whose support is finite below any fixed rational.

* More generally, any Hahn series field $k[t^G]$ contains the [[Novikov field]] of $k$ with value group $G$.

## Related pages

* [[formal power series]]
* [[formal Laurent series]]
* [[Puiseux series]]
* [[Novikov series]]
* [[Ribenboim power series]]
* [[finiteness space]]
