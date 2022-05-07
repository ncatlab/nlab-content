
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


+-- {: .num_remark} 
###### Remark

By the discussion at _[[universal complex orientation on MU]]_ we have:

For $V$ a [[complex vector bundle]] with [[Thom space]] $Th(V)$, its [[Thom class]] in any [[complex-oriented cohomology theory]] $E$ is classified by the composite

$$
  Th(V) 
    \longrightarrow
  M U
   \overset{\sigma^E}{\longrightarrow}
  E 
  \,,
$$

where $\sigma$ represents the complex orientation as a map of [[homotopy-commutative ring spectra]] on the [[Thom spectrum]] [[MU]].
 
In this perspective via classifying morphisms of [[ring spectra]], the statement of Prop. \ref{RationalToddClassIsChernCharacterOfThomClass} becomes that the Todd character is the composite of the complex orientation $\sigma^E$ with the [[Chern character]]

$$
  Td 
    \;\colon\;
  M \mathrm{U}
    \overset{ \sigma^{KU} }{\longrightarrow}
  KU 
    \overset{ ch }{\longrightarrow}
  H^{ev}\mathbb{Q}
$$



In particular, on [[cohomology rings]] $E_\bullet \coloneqq \pi_\bullet(E) \coloneqq  \widetilde E(S^\bullet)$ this composite of ring spectrum maps is the _[[Todd genus]]_ on the [[complex cobordism ring]], factored as

$$
  Td_{2\bullet}
  \;\colon\;
  \Omega^\mathrm{U}_{2\bullet}
  \;=\;
  (M\mathrm{U})_{2\bullet}
    \overset{ }{\longrightarrow}
  KU_{2\bullet}
    \overset{ch_{2\bullet}}{\longrightarrow}
  \mathbb{Q}
  \,.
$$

=--

(see [Smith 73, p. 303 (3 of 10)](#Smith73), following [Conner-Floyd 66, Section 6](#ConnerFloyd66))


## Related theorems

* [[e-invariant is Todd class of cobounding (U,fr)-manifold]]

* [[Grothendieck-Riemann-Roch theorem]]

## References

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 6 and p. 99 (first line) in:  _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

Proof is spelled out in:

* {#Karoubi78} [[Max Karoubi]], Theorem V4.4 of: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))


Discussion in terms of [[Brown representability theorem|representing]] [[ring spectra|ring]] [[spectra]]:


* {#Smith73} [[Larry Smith]], Section 1 of: _The Todd character and the integrality theorem for the Chern character_, Illinois J. Math. Volume 17, Issue 2 (1973), 301-310 ([euclid:ijm/1256051760](https://projecteuclid.org/euclid.ijm/1256051760))

* Matthias Jonas Spiegel, Section 2.3.2 of: _K-Theory of Intersection Spaces_, 2013 ([doi:10.11588/heidok.00015738](https://doi.org/10.11588/heidok.00015738))

also

* {#ConnerSmith69} [[Pierre Conner]], [[Larry Smith]], Section 9 of: _On the complex bordism of finite complexes_, Publications Mathématiques de l'IHÉS, Tome 37 (1969) , pp. 117-221 ([numdam:PMIHES_1969__37__117_0](http://www.numdam.org/item/?id=PMIHES_1969__37__117_0))


[[!redirects the rational Todd class is the Chern character of the Thom class]]

