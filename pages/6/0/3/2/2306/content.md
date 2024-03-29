
#Contents#
* table of contents
{:toc}

## Idea

The _Lazard ring_ is a [[commutative ring]] which is 

* the universal [[coefficient]] [[ring]] for commutative 1-dimensional [[formal group laws]].

and by [[Quillen's theorem on MU|Quillen's theorem]] also

* the [[cohomology ring]] that the [[complex cobordism cohomology theory]] assigns to the point.


## Definition

The _Lazard ring_ may be presented by generators $a_{i j}$ with $i,j \in \mathbb{N}$

$$
  L = \mathbb{Z}[a_{i j}] / (relations\;1,2,3\;below)
$$

and relations as follows

1. $a_{i j} = a_{j i}$

1. $a_{10} = a_{01} = 1$; $\forall i \neq 1: a_{i 0} = 0$

1. the obvious associativity relations imposed by $\ell(x, \ell(y, z)) = \ell(\ell(x, y), z)$ 

where we write 
$$
  \ell(x,y) = \sum_{i,j} a_{i j} x^i y^j \in L[[x,y]].
$$

In other words, $\ell(x, y)$ becomes the universal 1-dimensional [[formal group law]] as a formal power series in two variables with coefficients in the Lazard ring, Theorem \ref{walking} below.


## Properties

### As classifying ring for formal group laws

+-- {: .num_theorem #walking}
###### Theorem

For any [[ring]] $S$ with [[formal group law]] $g(x,y) \in S[ [x,y] ]$ there is a unique ring [[homomorphism]] $L \to S$ that sends $\ell$ to $g$.

=--

review includes ([Hopkins 99, theorem 2.3, theorem 2.5](#Hopkins99))

+-- {: .num_remark}
###### Remark

Passing to [[formal dual]] [[spectrum of a commutative ring|ring spectra]], this says that $Spec(L)$ is something like the [[moduli space]] for formal groups.
By [[Quillen's theorem on MU]], the lift of $L$ to [[higher algebra]] is the [[E-infinity ring]] [[MU]] and the [[E-infinity ring spectrum]] $Spec(MU)$ is something like the derived moduli stack for formal group laws.

=--

### Lazard's theorem

[[Lazard's theorem]] states:

+-- {: .num_theorem}
###### Theorem

The Lazard ring is [[isomorphism|isomorphic]] to a [[graded ring|graded]] [[polynomial ring]]

$$
  L \simeq \mathbb{Z}[t_1, t_2, \cdots]
$$

with the [[variable]] $t_i$ in degree $2 i$.

=--

review includes ([Hopkins 99, theorem 2.5](#Hopkins99), [Lurie 10, lect 2, theorem 4](#LurieLect2))

### As the complex cobordism cohomology ring

By [[Quillen's theorem on MU]] the Lazard ring is the [[cohomology ring]] of [[complex cobordism cohomology theory]].

+-- {: .num_theorem}
###### Theorem

Let $M P $ denote the peridodic [[complex cobordism cohomology theory]]. Its [[cohomology ring]] $M P(*)$ over the point together with its [[formal group law]] is naturally isomorphic to the universal Lazard ring with its formal group law $(L,\ell)$.

=--

+-- {: .num_remark}
###### Remark

This can be used to make a cohomology theory out of a [[formal group law]] $(R,f(x,y))$. Namely, one can use the classifying map $M P({*}) \to R$
to build the [[tensor product]] 

$$
  E^n(X) := M P^n(X) \otimes_{M P({*})} R,
$$ 
for any $n\in\mathbb{Z}$.
This construction could however break the left exactness condition. However, $E$ built this way will be left exact if the ring morphism $M P({*}) \to R$ is a flat morphism. This is the [[Landweber exactness]] condition (or maybe slightly stronger). See at _[[Landweber exact functor theorem]]_.

=--

## Related entries

* for some context see _[[A Survey of Elliptic Cohomology - cohomology theories]]_

* [[Landweber exact functor theorem]]

* [[Lazard's theorem]]

## References

* [[Michel Lazard]], *Sur les groupes de Lie Formels à un Paramètre*, Bull. Soc. France **83** (1955) &lbrack;[numdam:BSMF_1955__83__251_0](http://www.numdam.org/item/?id=BSMF_1955__83__251_0)&rbrack;


* [[Daniel Quillen]], _On the formal group laws of unoriented and complex cobordism theory_, Bull. Amer. Math. Soc. Volume 75, Number 6 (1969), 1293-1298.  ([Euclid](http://projecteuclid.org/euclid.bams/1183530915))

* {#Adams74} [[John Adams]], part II.5 of _[[Stable homotopy and generalised homology]], University of Chicago Press, Chicago, Ill., 1974, Chicago Lectures in Mathematics.

* {#Kochmann96} [[Stanley Kochmann]], section 4.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Hopkins99} [[Mike Hopkins]], _Complex oriented cohomology theories and the language of stacks_, 1999 course notes ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))


* {#LurieLect2} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 2 _Lazard's theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture2.pdf))

* {#LurieLect3} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 3 _Lazard's theorem (continued)_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture3.pdf))
 

[[!redirects Lazard's ring]]