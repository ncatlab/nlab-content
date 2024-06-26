
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The _Landweber exactness criterion_ determines whether a given [[formal group law]] arises as the formal group law defined by a [[weakly periodic cohomology theory]].

Notice that since every [[formal group law]] over a [[ring]] $R$ is classified by a ring homomorphism $f : MP({\ast}) \to R$ where by [[Quillen's theorem on MU|Quillen's theorem]] $MP({\ast})$ is the [[Lazard ring]]. So for every formal group one obtains a contravariant [[functor]] on [[topological space]]s given by the [[extension of scalars]]-assignment

$$
  X \mapsto A_f^n(X) := MP^n(X) \otimes_{MP({*})} R
  \,,
$$

where $MP^\bullet$ denotes the [[complex cobordism cohomology theory]] and where the [[tensor product]] is taken using the $R$-[[module]] structure on $MP({*})$ induced by $f$.

The point of Landweber-exactness is that if $f$ is Landweber exact (i.e. if the corresponding [[formal group law]] is) then this construction defines a [[cohomology theory]] $A^\bullet(-)$.
 

## Definition

+-- {: .num_prop}
###### Proposition 
**Landweber criterion**  Let $f(x,y)$ be a [[formal group law]] and $p$ a [[prime]],
$v_i$ the [[coefficient]] of $x^{p^i}$ in 

$$
  [p]_f(x) \coloneqq \underset{p\,\text{summands}}{\underbrace{x+_f\cdots+_f x}}
  \,.
$$

If $v_0,\ldots,v_i$ form a [[regular sequence]] for all $p$ and $i$ then $f(x,y)$ is Landweber exact and hence gives a 
[[cohomology theory]] via the the formula above.

=--

See at _[[Landweber exact functor theorem]]_

## Examples

+-- {: .num_example}
###### Example 

Let $g_a(x,y)=x+y$ be the formal [[additive group]]. 
Then $[p]_a(x)= p x$ and so $v_0=p$, $v_i=0$ for all $i\ge1$.
The [[regular sequence|regularity]] condtions imply that
the [[zero map]] $R/(p)\to R/(p)$ must be [[injective]].  This implies that $R$ contains the [[rational numbers]] as a subring.

Note that the [[ordinary cohomology]] $HP^*(X,R)=\prod_k H^{n+2k}(X,R)$ is a [[cohomology theory]] over any [[ring]] $R$.

=--


+-- {: .num_example}
###### Example 

$g_m(x,y)=xy+x+y$, $[p]_m(x)=(x+1)^p-1$, $v_0=p$, $v_1=1$, $v_i=0$ for all $i \gt 1$.
The regularity conditions are trivial.
Hence we know that $K^*(X)=MP^*(X)\otimes_{MP(\bullet)} \mathbb{Z}$ is a cohomology theory.

=--


## Related entries

* [[Landweber exact functor theorem]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

## References


* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, 
Lecture 15 _Flat modules over $\mathcal{M}_{FG}$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture15.pdf))
 {#LurieLecture15}

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 16 _The Landweber exact functor theorem_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture16.pdf)) 

[[!redirects Landweber exactness criterion]]
[[!redirects Landweber criterion]]