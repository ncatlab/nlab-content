

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
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

The [[e-invariant]] is, a priori, a [[homotopy invariant]] of [[morphisms]] in the [[stable homotopy category]], hence in particular of the [[stable homotopy groups of spheres]]. Under the identification of the latter, via the [[Pontrjagin-Thom isomorphism]], with the [[framed bordism ring]], the [[e-invariant]] turns out to equal the [[Todd class]] of any [[coboundary|cobounding]] [[(U,fr)-manifold]] ([Conner-Floyd 66](#ConnerFloyd66)).

## Preliminaries

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
 
## Statement

+-- {: .num_prop #EInvariantIsToddClassOnCoboundingUFrManifold} 
###### Proposition
**([[Todd class]] on [[coboundary|cobounding]] [[(U,fr)-manifolds]] computes [[e-invariant]])**

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


## Related statements

* [[rational Todd class is Chern character of Thom class]]


## References

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 16.2 in: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

[[!redirects e-invariant is Todd class of cobounding (U,fr)-manifolds]]
