

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

(By [this Prop.](MUFr#AShortExactSequenceOfUFrBordismRings) at _[[MUFr]]_.)

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
  \Omega^{U,fr}_{\bullet+1}
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
  \big\downarrow{}^{e_{\mathbb{C}}}
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

+-- {: .proof #TheProof}
###### Proof

The first step in the proof of (eq:ToddClassesOnShortExactSequenceOfUFrBordismRings) is the observation ([Conner-Floyd 66, p. 100-101](#ConnerFloyd66)) that the representing map (eq:InTermsOfHomotopyGroupsOfQuotientedThomSpace) for a [[(U,fr)-manifold]] $M^{2k}$ cobounding a $Fr$-manifold represented by a map $f$ is given by the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]] (see also at _[[Hopf invariant]] -- [In generalized cohomology](Hopf+invariant#InGeneralizedCohomology)_):

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

From this, Conner-Floyd conclude by essentially  considering the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]]:

\begin{imagefromfile}
        "file_name": "eInvariantIsTdClassOfCoboundingUFrMfd-DiagramA.jpg",
        "web": "nlab",
        "width": 650,
        "unit": "px",
        "margin": {
            "top": -20,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting that the e-invariant equals the Todd class of any cobounding UFr-manifold",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}




Here for the identification of the [[Todd class]] $Td$ in the bottom of the diagram we used that [[the rational Todd class is the Chern character of the Thom class]].

That this Todd class equals the [[Q/Z]]-valued [[e-invariant]] follows now since the latter is the top-degree component of the [[Chern character]] of any [[complex topological K-theory]]-class $V_{2n} \coloneqq \sigma \circ c$ lifting $\Sigma^{2n} 1 \in \widetilde K(S^{2n})$ to $C_f$ ([this Prop.](Adams+e-invariant#QModZValuedEInvariantIsTopDegreeCoefficientOfChernCharacterOnCofiberSpace)).

=--

## Variants
 {#Variants}

An analogous but finer construction works for [[special unitary group]]-structure instead of [[unitary group]]-structure and in dimensions $8\bullet + 4$: 

Since on $(8 \bullet + 4)$-dimensional $SU$-manifolds the [[Todd class]] is divisible by 2 ([Conner-Floyd 66, Prop. 16.4](#ConnerFloyd66)) we have ([Conner-Floyd 66, p. 104](#ConnerFloyd66)) the following [[short exact sequence]] of [[MSUFr]]-[[bordism rings]], in variation of (eq:ToddClassesOnShortExactSequenceOfUFrBordismRings):

\[
  \label{HalfToddClassesOnShortExactSequenceOfSUFrBordismRings}
  \array{
  0 
  \to
  &
  \Omega^{SU}_{8\bullet+4}
  &
  \overset{i}{\longrightarrow}
  &
  \Omega^{SU,fr}_{8\bullet+4}
  &
  \overset{\partial}{
    \longrightarrow
  }
  &
  \Omega^{fr}_{8\bullet + 3}
  &
  \simeq
  &
  \pi^s_{8\bullet + 3}
  \\
  & 
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{\tfrac{1}{2}\mathrlap{Td}}
  &&
  \big\downarrow{}^{}
  &&
  \big\downarrow{}^{e_{\mathbb{R}}}
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
  \,.
\]

This produces $e_{\mathbb{R}}$, the [[Adams e-invariant]] with respect to [[KO]]-theory instead of [[KU]] ([Adams 66, p. 39](e-invariant#Adams66)), which, in degrees $8k + 3$, is indeed half of the e-invariant $e_{\mathbb{C}}$ for $KU$ (by [Adams 66, Prop. 7.14](e-invariant#Adams66)). 

In fact, for $k = 0$ we have:

+-- {: .num_prop #AdamseRInvariantDetectsThirdStableHomotopyGroupOfSpheres} 
###### Proposition
**([Adams 66, Example 7.17  and p. 46](e-invariant#Adams66))**

In degree 3, the [[KO]]-theoretic [[e-invariant]] $e_{\mathbb{R}}$ takes the value $\left[\tfrac{1}{24}\right] \in \mathbb{Q}/\mathbb{Z}$ on the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$  and hence reflects the full [[third stable homotopy group of spheres]]:

$$
  \array{
    \pi^s_3 
      &
      \underoverset{
        \simeq
      }{
        e_{\mathbb{R}}
      }{
        \;\;\longrightarrow\;\;
      } 
      &
    \mathbb{Z}/24 
    & 
    \subset 
    &  
    \mathbb{Q}/\mathbb{Z}
    \\
    [h_{\mathbb{H}}]
    &&\mapsto&&
    \left[\tfrac{1}{24}\right]    
  }
$$

while $e_{\mathbb{C}}$ sees only "half" of it (by [Adams 66, Prop. 7.14](e-invariant#Adams66)).

=--


## Related statements

* [[rational Todd class is Chern character of Thom class]]


## References

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 16.2 in: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

An alternative formulation via [[index theory]]:


* [[Michael Atiyah]], [[Vijay Patodi]], [[Isadore Singer]], Theorem 4.14 of: _Spectral asymmetry and Riemannian geometry. II_,  Mathematical Proceedings of the Cambridge Philosophical Society , Volume 78, Issue 3, 1975, pp. 405-432 ([doi:10.1017/S0305004100051872](https://doi.org/10.1017/S0305004100051872))

Review in:

* [[Ulrich Bunke]], [[Niko Naumann]], Section 2 of: _The f-invariant and index theory_, Manuscripta Math. 132, 365–397 (2010) ([arXiv:0808.0257](https://arxiv.org/abs/0808.0257), [https://doi.org/10.1007/s00229-010-0351-7](https://doi.org/10.1007/s00229-010-0351-7))




[[!redirects e-invariant is Todd class of cobounding (U,fr)-manifolds]]
[[!redirects e-invariant is the Todd class of cobounding (U,fr)-manifolds]]
