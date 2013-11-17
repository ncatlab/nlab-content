
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Adams conjecture_ is a statement about triviality of [[spherical fibrations]] associated to certain formal differences of [[vector bundles]] ([[K-theory]] classes) via the [[J-homomorphism]]. The conjecture was stated in ([Adams 63](#Adams63)) and was proven in ([Quillen 71](Quillen71)). It serves a central role in the identification of the [[image of J]]. 



## Statements

Let $X$ be (the [[homotopy type]] of) a [[topological space]]. For $V \;\colon\; X \longrightarrow B O$ classifying a real [[vector bundle]] on $X$, the corresponding [[spherical fibration]] is classifid by the composite

$$
  J(V)
   \;\colon\;
  X \stackrel{V}{\longrightarrow} B O \stackrel{J}{\longrightarrow} B GL_1(\mathbb{S})
$$

with the delooped [[J-homomorphism]].
This descends to a map from [[topological K-theory]] to [[spherical fibrations]].

Now for $L$ a [[line bundle]] on some $X$ and for non-vanishing $k \in \mathbb{Z}$, [[John Adams]] observed that the [[spherical fibration]] associated with the difference $L^{\otimes k} - L \in K O(X)$ has the property that some $k$-fold multiple of it has trivial spherical fibration, hence that there is $N \in \mathbb{N}$ for which

$$
  J\left(
    \oplus^{k^N} (L^{\otimes k} - L)
  \right)
  = 0
  \,.
$$

Noticing that $L \mapsto L^{\otimes^k} = \Psi^k(L)$ is the $k$th [[Adams operation]] on [[K-theory]] applied to the [[line bundle]] $L$, [[John Adams]] then conjectured that the above is true for all [[vector bundles]] $V$ in the form

$$
  J\left(
    \oplus^{k^N} (\Psi^k(V) - V)
  \right)
  = 0
  \,.
$$


## Related entries

* [[J-homomorphism]]

## References

The conjecture originates in

* [[John Adams]], _On the groups $J(X)$ I: Topology , 2 (1963) pp. 181&#8211;195 
 {#Adams63}

A quick review is for instance in 

* [[Akhil Mathew]], _The Adams conjecture I_ ([web](http://amathew.wordpress.com/2013/01/23/the-adams-conjecture-i/))

The [[proof]] of the Adams conjecture is originally due to

* [[Daniel Quillen]], _The Adams conjecture_, Topology, vol 10, 1971  ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/Quillen.pdf))
 {#Quillen71}

The proof using [[algebraic geometry]] is due to 

* [[Dennis Sullivan]], _Generatics of homotopy theory and the Adams conhecture_, The Annals of Mathematics, Second Series, Vol. 100, No. 1 (Jul., 1974), pp. 1-79 ([JSTOR](http://www.jstor.org/stable/1970841), [pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/Sullivan.pdf))

Yet another proof via [[Becker-Gottlieb transfer]] is due to 

* J. Becker, D. Gottlieb, _The transfer map and fiber bundles_ Topology , 14 (1975)
 {#BeckerGottlieb75}

[[!redirects Adams' conjecture]]