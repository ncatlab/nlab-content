

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}




\begin{remark}
**(terminology)**
The term  _[[simplicial groupoid]]_ is often used for a [[simplicial object]] in the [[category]] [[Grpd]] of [[groupoids]] whose [[simplicial set]] of objects is simplicially constant. We will write $s Grpd$ for the category of such simplicial groupoids.

Perhaps a more accurate term for this concept is **simplicially enriched groupoid**, and conceptually it is often the [[sSet-enriched category]]-[[structure]] that is useful. Because of this it is advisable to check the use being made of the term when consulting the literature. This is more fully discussed at *[[simplicial category]]*.
\end{remark}


## Definition

Write $sGrpd$ for the [[category]] of [[simplicial groupoids]].

There is a [[model category]] structure on $sGrpd$ whose

* [[fibrations]] are those morphisms $f \colon H \to K$ such that 

  1. for every [[object]] $x$ of $H$ and every [[morphism]] $\omega \colon f(x) \to y$ in $K_0$ there is a morphism $\hat \omega : x \to z$ of $H_0$ such that $f(\hat \omega) = \omega$;

  1. for every object $x$ in $H$ the induced morphism $f \colon H(x,x) \to K(f(x), f(x))$ is a [[Kan fibration]].

* [[weak equivalences]] are those morphisms $f \colon H \to K$ such that

  1. $f$ induces in [[isomorphism]] on [[connected components]] $\pi_0 f \colon \pi_0 H \to \pi_0 K$;

  1. for each object $x$ of $H$ the induced morphism $H(x,x) \to K(f(x), f(x))$ is a weak equivalence in the [[model structure on simplicial groups]] or equivalently in the [[model structure on simplicial sets]].


## Properties

+-- {: .num_prop}
###### Proposition

We have a [[Quillen adjunction]]

$$
  (G \dashv \bar W) : 
  Grpd^\Delta
   \stackrel{\overset{G}{\leftarrow}}{\underset{\bar W}{\to}}
  sSet_{Quillen}  
$$

where both $G$ and $\bar W$ preserve all [[weak equivalence]]s.

=--

This appears for instance as 
([Goerss & Jardine, theorem 7.8](#GoerssJardine))

+-- {: .num_remark}
###### Remark

When restricted to simplicial groupoids of the form $(B G)_\bullet$ for $G_\bullet$ a [[simplicial group]] and $B G_n$ its [[delooping]] [[groupoid]] this produces a standard presentation of [[looping and delooping]] for [[infinity-group]]s. See there for more details.

=--

## Related concepts

* [[model structure on simplicial sets]]

* [[model structure on presheaves of simplicial groupoids]]

## References

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]],  *Homotopy theory and simplicial groupoids*, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], after corollary 7.3 in chapter V of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack; 
