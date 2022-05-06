
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

## Idea

A [[characteristic class]].

By the [[Hirzebruch-Riemann-Roch theorem]] the [[index]] of the [[Dolbeault operator]] is the Todd genus (e.g. [Gilkey 95, section 5.2](#Gilkey95) (more generally so for the [[Spin^c Dirac operator]]).

## Properties

### Relation to Thom class and Chern character

+-- {: .num_prop #RationalToddClassIsChernCharacterOfThomClass} 
###### Proposition
**([[rational Todd class is Chern character of Thom class]])**

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


### Relation to the Adams e-invariant
 {#RelationToAdamsEInvariant}

We discuss how the [[e-invariant]] in its [[Q/Z]]-incarnation ([this Def.](e-invariant#eInvariantInComplexTopologicalKtheoryAsRationalNumberModuloIntegers)) has a natural formulation in [[cobordism theory]] ([Conner-Floyd 66](#ConnerFloyd66)), by evaluating Todd classes on [[coboundary|cobounding]] [[(U,fr)-manifolds]].

This is Prop. \ref{EInvariantIsToddClassOnCoboundingUFrManifold} below; but first to recall some background:


+-- {: .num_remark} 
###### Remark

In generalization to how the [[U-bordism ring]] $\Omega^U_{2k}$ is [[Brown representability theorem|represented]] by [[homotopy classes]] of [[maps]] into the [[Thom spectrum]] [[MU]], so the [[(U,fr)-bordism ring]] $\Omega^{U,fr}_{2k}$ is represented by maps into the [[quotient spaces]] $MU_{2k}/S^{2k}$ (for $S^{2k} = Th(\mathbb{C}^{k}) \to Th( \mathbb{C}^k \times_{U(k)} E U(k) ) = MU_{2k}$ the canonical inclusion):

\[
  \label{InTermsOfHomotopyGroupsOfQuotientedThomSpace}
  \Omega^{(U,fr)}_\bullet
  \;=\;
  \pi_{\bullet + 2k}
  \big(
    MU_{2k}/S^{2k}
  \big)
  \,,
  \;\;\;\;\;
  \text{for any}
  \;
  2k \geq \bullet + 2
  \,.
\]

=--

([Conner-Floyd 66, p. 97](#ConnerFloyd66))


+-- {: .num_remark} 
###### Remark

The [[bordism rings]] for [[MU]], [[MUFr]] and [[MFr]] sit in a [[short exact sequence]] of the form

\[
  \label{ShortExactSequenceOfUFrBordismRings}
  0 
  \to
  \Omega^U_{\bullet+1}
  \overset{i}{\longrightarrow}
  \Omega^{U,f}_{\bullet+1}
  \overset{\partial}{
    \longrightarrow
  }
  \Omega^{fr}_\bullet
  \to
  0
  \,,
\]

where $i$ is the evident inclusion, while $\partial$ is restriction to the [[boundary]].

In particular, this means that $\partial$ is [[surjective function|surjective]], hence that every $Fr$-manifold is the boundary of a [[(U,fr)-manifold]].

=--


+-- {: .num_prop #EInvariantIsToddClassOnCoboundingUFrManifold} 
###### Proposition
**([[e-invariant is Todd class of cobounding (U,fr)-manifold]])**

Evaluation of the [[Todd class]] on [[(U,fr)-manifolds]] yields [[rational numbers]] which are [[integers]] on actual $U$-manifolds. It follows with the [[short exact sequence]] (eq:ShortExactSequenceOfUFrBordismRings) that assigning to $Fr$-manifolds the Todd class of any of their cobounding $(U,fr)$-manifolds yields a well-defined element in [[Q/Z]].

Under the [[Pontrjagin-Thom isomorphism]] between the [[framed bordism ring]] and the [[stable homotopy group of spheres]] $\pi^s_\bullet$, this assignment coincides with the [[Adams e-invariant]] in [its Q/Z-incarnation](Adams+e-invariant#TheEInvariantAsAnElementOfQModZ):

\[
  \label{ToddClassesOnShortExactSequenceOfUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^U_{\bullet+1}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{U,f}_{\bullet+1}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_\bullet
  &
  \simeq
  &
  \pi^s_\bullet
  \\
  & 
  \big\downarrow{}^{\mathrlap{Td}}
  &&
  \big\downarrow{}^{\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e}
  \\
  0 
  \to
  & 
  \mathbb{Z}
  &\overset{\;\;\;\;\;}{\hookrightarrow}&
  \mathbb{Q}  
  &\overset{\;\;\;\;}{\longrightarrow}&
  \mathbb{Q}/\mathbb{Z}
  &=&
  \mathbb{Q}/\mathbb{Z}
  }
  \,,
\]

=--

([Conner-Floyd 66, Theorem 16.2](#ConnerFloyd66))


## Related concepts

* [[genus]]

* [[Grothendieck-Riemann-Roch theorem]]

[[!include genera and partition functions - table]]

## References

Named after [[John Arthur Todd]].

Original articles:

* {#Hirzebruch56} [[Friedrich Hirzebruch]], Section 3 of: _Neue topologische Methoden in der Algebraischen Geometrie_, Ergebnisse der Mathematik und Ihrer Grenzgebiete. 1. Folge, Springer 1956 ([doi:10.1007/978-3-662-41083-7](https://www.springer.com/de/book/9783662406052))

  English translation: Section 3 of _Topological Methods in Algebraic Topology_, Classics in Mathematics, vol 131. Springer 1995 ([doi:10.1007/978-3-642-62018-8_4](https://doi.org/10.1007/978-3-642-62018-8_4))

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Sections 12, 13 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

* {#Karoubi78} [[Max Karoubi]], Chapter V.4 of: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))

On the Todd character:

* [[Pierre Conner]], [[Larry Smith]], Section 7 of: _On the complex bordism of finite complexes. II_, J. Differential Geom. Volume 6, Number 2 (1971), 135-174 ([euclid:euclid.ijm/1256051760](https://projecteuclid.org/euclid.ijm/1256051760))


* [[Larry Smith]], Section 1 of: _The Todd character and the integrality theorem for the Chern character_, Illinois J. Math. Volume 17, Issue 2 (1973), 301-310 ([euclid:ijm/1256051760](https://projecteuclid.org/euclid.ijm/1256051760))

* [[Larry Smith]], _The Todd character and cohomology operations_, Advances in Mathematics Volume 11, Issue 1, August 1973, Pages 72-92 (<a href="https://doi.org/10.1016/0001-8708(73)90003-0">doi:10.1016/0001-8708(73)90003-0</a>)



Review:

* {#Gilkey95} [[Peter Gilkey]], Section 5.2 of: _Invariance Theory: The Heat Equation and the Atiyah-Singer Index Theorem_, 1995 ([pdf](https://pages.uoregon.edu/gilkey/dirPDF/InvarianceTheory1Ed.pdf))

See also:

* Wikipedia, _[Todd class](http://en.wikipedia.org/wiki/Todd_class)_

Discussion of Todd classes for [[noncommutative topology]]/in [[KK-theory]] is in

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))


Review of the Todd genus with an eye towards generalization to the [[Witten genus]] is in the introduction of

* [[Pokman Cheung]], _The Witten genus and vertex algebras_ ([arXiv:0811.1418](http://arxiv.org/abs/0811.1418))


[[!redirects Todd classes]]


[[!redirects Todd genus]]

[[!redirects Todd character]]
[[!redirects Todd characters]]