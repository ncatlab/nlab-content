
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In joint generalization of the [[cobordism cohomology theories]] [[MU]] and [[MFr]] of [[closed manifold|closed]] $U$-manifolds and of $Fr$-manifolds, respectively, a _$(U,fr)$-manifold_ ([Conner-Floyd 66, Section 16](#ConnerFloyd66)) is a [[compact topological space|compact]] [[manifold with boundary]] equipped with [[unitary group]]-[[tangential structure]] on its [[stable tangent bundle]] and equipped with a [[trivial vector bundle|trivialization]] (stable [[framed manifold|framing]]) of that over the [[boundary]].

The corresponding [[bordism classes]] form a [[bordism ring]] denoted $\Omega^{U,fr}_\bullet$.

## Properties

### Representing spectrum

In generalization to how $\Omega^U_{2k}$ is represented by [[homotopy classes]] of [[maps]] into the [[Thom spectrum]] [[MU]], so $\Omega^{U,fr}_{2k}$ is represented by maps into the [[quotient spaces]] $MU_{2k}/S^{2k}$ (for $S^{2k} = Th(\mathbb{C}^{k}) \to Th( \mathbb{C}^k \times_{U(k)} E U(k) ) = MU_{2k}$ the canonical inclusion):

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

([Conner-Floyd 66, p. 97](#ConnerFloyd66))

### Relation to $MU$ and $MFr$

The [[bordism rings]] for [[MU]], $MUFr$ and [[MFr]] sit in a [[short exact sequence]] of the form

\[
  \label{ShortExactSequenceOfUFrBordismRings}
  0 
  \to
  \Omega^U_{\bullet+1}
  \overset{i}{\longrightarrow}
  \Omega^{U,fr}_{\bullet+1}
  \overset{\partial}{
    \longrightarrow
  }
  \Omega^{fr}_\bullet
  \to
  0
  \,,
\]

where $i$ is the evident inclusion, while $\partial$ is restriction to the [[boundary]].

In particular, this means that $\partial$ is [[surjective function|surjective]], hence that every $Fr$-manifold is the boundary of a $(U,fr)$-manifold.

 
### Relation to Todd classes and the e-invariant

+-- {: .num_prop #EInvariantIsToddClassOnCoboundingUFrManifold} 
###### Proposition
**([[e-invariant is Todd class of cobounding (U,fr)-manifold]])**

Evaluation of the [[Todd class]] on $(U,fr)$-manifolds yields [[rational numbers]] which are [[integers]] on actual $U$-manifolds. It follows with the [[short exact sequence]] (eq:ShortExactSequenceOfUFrBordismRings) that assigning to $Fr$-manifolds the Todd class of any of their cobounding $(U,fr)$-manifolds yields a well-defined element in [[Q/Z]].

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

The first step in the proof of (eq:ToddClassesOnShortExactSequenceOfUFrBordismRings) is the observation ([Conner-Floyd 66, p. 100-101](#ConnerFloyd66)) that the representing map (eq:InTermsOfHomotopyGroupsOfQuotientedThomSpace) for a $(U,fr)$-manifold $M^{2k}$ cobounding a $Fr$-manifold represented by a map $f$ is given by the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]] (see also at _[[Hopf invariant]] -- [In generalized cohomology](Hopf+invariant#InGeneralizedCohomology)_):

\begin{imagefromfile}
        "file_name": "CoboundingUFrManifoldDiagrammatically.jpg",
        "web": "nlab",
        "width": 470,
        "unit": "px",
        "margin": {
            "top": -20,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting cobounding UFr-manifolds",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

The concept of $(U,fr)$-bordism theory and its relation to the [[e-invariant]] originates with:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 16 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

Generalization to [[manifolds with corners]] and relation to the [[f-invariant]]:

* Gerd Laures, _On cobordism of manifolds with corners_, Trans. Amer. Math. Soc. 352 (2000) ([doi:10.1090/S0002-9947-00-02676-3](https://doi.org/10.1090/S0002-9947-00-02676-3))

[[!redirects (U,fr)-manifold]]
[[!redirects (U,fr)-manifolds]]

[[!redirects (U,fr)-bordism]]
[[!redirects (U,fr)-bordisms]]
[[!redirects (U,fr)-bordism ring]]
[[!redirects (U,fr)-bordism rings]]

[[!redirects (U,fr)-cobordism]]
[[!redirects (U,fr)-cobordisms]]
[[!redirects (U,fr)-cobordism ring]]
[[!redirects (U,fr)-cobordism rings]]

