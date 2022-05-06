
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop #RationalToddClassIsChernCharacterOfThomClass} 
###### Proposition
**([[Todd class]] in [[rational cohomology]] is [[Chern character]] of [[Thom class]])**

Let $V \to X$ be a [[complex vector bundle]] over a [[compact topological space]]. Then the [[Todd class]] $Td(V) \,\in\, H^{ev}(X; \mathbb{Q})$ of $V$ in [[rational cohomology]] equals the [[Chern character]] $ch$ of the [[Thom class]] $th(V) \,\in\, K\big( Th(V) \big)$ in the [[complex topological K-theory]] of the [[Thom space]] $Th(V)$, when both are compared via the [[Thom isomorphisms]] $\phi_E \;\colon\; E(X) \overset{\simeq}{\to} E\big( Th(V)\big)$:

$$
  \phi_{H\mathbb{Q}}  
  \big( 
    Td(V)
  \big) 
  \;=\;
  ch\big( th(V) \big)
  \,.
$$

More generally , for $x \in K(X)$ any class, we have

$$
  \phi_{H\mathbb{Q}}  
  \big(
    ch(x)
    \cup
    Td(V)
  \big) 
  \;=\;
  ch\big( \phi_{K}(x) \big)
  \,,
$$

which specializes to the previous statement for $x = 1$.

=--

([Karoubi 78, Chapter V, Theorem 4.4](#Karoubi78))

## Related theorems

* [[e-invariant is Todd class of cobounding (U,fr)-manifold]]

* [[Grothendieck-Riemann-Roch theorem]]

## References

The statement appears without proof in:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], p. 99 (first line) in:  _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

Proof is spelled out in:

* {#Karoubi78} [[Max Karoubi]], Theorem V4.4 of: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))


[[!redirects the rational Todd class is the Chern character of the Thom class]]

