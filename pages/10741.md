
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### In ordinary cohomology
  {#InOrdinaryCohomology}

For $n \in \mathbb{N}$ with $n \gt 1$, consider [[continuous functions]] between [[spheres]] of the form

\[
  \label{TheMap}
  f \;\colon\; S^{2n-1} \longrightarrow S^n
  \,.
\]

The [[homotopy cofiber]] of $f$ (the [[attaching space]] induced by $f$)

$$
  C_f \;\coloneqq\; S^n \underset{S^{2n-1}}{\cup} D^{2n}
$$

has [[ordinary cohomology]] 

$$
  H^k(C_f, \mathbb{Z})
  \simeq
  \left\{
    \array{  
      \mathbb{Z} & for\; k = n, 2n;
      \\
      0 &  otherwise
    }
  \right.
  \,.
$$

Hence for $\alpha_n, \beta_{2n}$ generators of the [[cohomology groups]] in degree $n$ and $2n$ (unique up to choice of sign), respectively, there exists an [[integer]] $HI(f)$ which expresses the [[cup product]] square of $\omega_n$ as a multiple of $\beta_{2n}$:

\[
  \label{HopfInvariantFormula}
  \alpha_n \cup \alpha_n \;=\; HI(f) \cdot \beta_{2n} 
  \,.
\]

This [[integer]] $HI(f) \in \mathbb{Z}$ is called the _Hopf invariant_ of $f$ (e.g. [Mosher-Tangora 86, p. 33](#MosherTangora86)).


This depends on the choices made only up to sign. In particular it has a well-defined mod-2 reduction image $[HI(f)] \in \mathbb{F}_2 = \mathbb{Z}/2\mathbb{Z}$ (in [[cyclic group of order 2|Z/2]]), and as such it is the [[Steenrod square]] 

$$
  [HI(f)] \cdot (-)
    \;\colon\; 
  \mathbb{F}_2
  \;\simeq\;
  H^n
  \big(
    C_f;
    \, 
    \mathbb{F}_2
  \big) 
  \stackrel{Sq^n}{\longrightarrow}
  H^{2n}
  \big(
    C_f;
    \, 
    \mathbb{F}_2
  \big) 
   \;\simeq\;
  \mathbb{F}_2
  \,.
$$

### In generalized cohomology
 {#InGeneralizedCohomology}

Here is a more abstract picture of the Hopf invariant in abstract [[homotopy theory]] (following [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)):

Let $E$ be a [[multiplicative cohomology theory]], assumed to vanish in degree $2n - 1$

\[
  \label{ECohomologyVanishingInDegree2nMinus1}
  \widetilde E
  \big(
    S^{2n-1} 
  \big)
  \,\simeq\,
  \pi_{2n-1}(E)
  \,\simeq\,
  0
  \,.
\]


We write
$
  E_n \;\coloneqq\; \Omega^\infty \Sigma^n E
$
for its classifying spaces, hence for the component spaces of its [[Brown representability theorem|representing]] [[spectrum]].

(For the case of [[ordinary cohomology]] $E = H \mathbb{Z}$ we have $E_n \,\simeq\, K(\mathbb{Z},n)$ an [[Eilenberg-MacLane space]].)

Now let 

$$
  S^{2n-1} \overset{f}{\longrightarrow} S^n
$$

be a map (eq:TheMap). Then its $E$-Hopf invariant "is" the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]] of [[pointed homotopy types]] (see also at _[[e-invariant is Todd class of cobounding (U,fr)-manifold]]_):

\begin{imagefromfile}
        "file_name": "HopfInvariantPastingDiagram.jpg",
        "web": "nlab",
        "width": 480,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting the Hopf invariant",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}


* the top square is defined to be a [[homotopy pushout]], exhibiting the [[attaching space]] $C_f$;

* the total rectangle is defined to be a [[homotopy pushout]], exhibiting the [[suspension]] of $S^{2n-1}$ to $S^{2n}$;

* the bottom square is hence a [[homotopy pushout]] by the [[pasting law]];

* by assumption (eq:ECohomologyVanishingInDegree2nMinus1) the restriction of $\Sigma^{2n} 1$ to $S^{2n-1}$ trivializes, exhibited by a choice of [[homotopy]] filling the full top part of the diagram; and by the [[universal property]] of the top homotopy-pushout this corresponds equivalently to the dashed morphism $c$;

* {#RestrictionOfCupSquareTrivializes} the restriction of the [cup square cohomology operation](cohomology+operation#CupPowersInMultiplicativeCohomology) on $c$ to $S^n$ trivializes: $c$ factors through the $n$ component space of the [[connective cover]] $E\langle 0\rangle$, whence its [cup square](cohomology+operation#CupPowersInMultiplicativeCohomology) (by the discussion at _[connective cover -- For ring spectra](connective+cover#ForRingSpectra)_) factors through the $2n$-connective $2n$th component space of the same connective cover (as in a standard argument in [[complex oriented cohomology theory]], e.g. [Lurie, Lec. 4. Exmpl. 8](complex+oriented+cohomology+theory#LurieLecture), or see [[The Relation of Cobordism to K-Theories|Conner-Floyd 66, Part I, Cor. 7.2]]):

\begin{xymatrix}
  S^n
  \ar[r]
    _>>>{\ }="s"
  \ar[d]
    ^>>>{\ }="t"
  &
  \Omega^{\infty-n}
  \big(
    E\langle0\rangle
  \big)
  \ar[d]
    ^-{ (-)^{2_{\cup}} }
  \ar[r]
    ^-{ \;\
      \Omega^{\infty-n}( 
        \epsilon_E 
      )
    \; }
  &
  \Omega^{\infty-n}
  \big(
    E
  \big)
  \ar[d]
    ^-{ (-)^{2_{\cup}} }
  \\
  \ast
  \ar[r]
  &
  \Omega^{\infty-2n}
  \big(
    E\langle0\rangle
  \big)  
  \ar[r]
    _-{ \;
      \Omega^{\infty-2n}
      ( \epsilon_E )
    \;}
  &
  \Omega^{\infty-2n}
  \big(
    E
  \big)
  %
  \ar@{=>}
    ^-{ \exists ! }
    "s"; "t"
\end{xymatrix}

* This yields the [[homotopy]]  filling the full bottom part of the diagram above; and by the [[universal property]] of the bottom homotopy-pushout this corresponds equivalently to a dashed morphism $S^{2n} \to E_{2n}$, labeled by  some class

  $$
    \kappa 
    \,\in\,
    \pi_0(E)
    \,\simeq\,
    \widetilde E(S^0)
    \overset{\Sigma^{2n}}{\longrightarrow}
    \widetilde E(S^{2n})
    \,
    =
    \,
    \big[
      S^{2n} \longrightarrow E_{2n}
    \big]
    \,; 
  $$

* finally, by the homotopy-pushout property of the total rectangle, this class $\kappa$ also labels the total homotopy filling the full diagram.

We see that:

* for $E = H \mathbb{Z}$ being [[ordinary cohomology]], $\kappa \,\in\, \mathbb{Z}$ is the traditional Hopf invariant as discussed [above](#InOrdinaryCohomology);

* for $E = KU$ being [[complex topological K-theory]], $\kappa \,\in\, \mathbb{Z}$ is the Hopf invariant in K-theory as used in [Adams-Atiyah 66](Hopf+invariant+one#AdamsAtiyah66).

In the case that the map $f$ is one the classical [[Hopf fibrations]], the [[attaching space]] above is a [[projective space]] (by the discussion at _[[cell structure of projective spaces]]_) and the choice of homotopy $c$ is the choice of an _orientation_ in $E$-cohomology theory to second stage. Specifically:

\begin{imagefromfile}
        "file_name": "OrientationInECohomologyAndHopfInvariant.jpg",
        "web": "nlab",
        "width": 600,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting orientation and the Hopf invariant",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}


* for the [[complex Hopf fibration]] $f = h_{\mathbb{C}}$ the attaching space is [[complex projective space]] $\mathbb{C}P^2$ and the choice of homotopy $c$ is a choice of [[complex oriented cohomology theory|complex orientation]] to second stage;

* for the [[quaternionic Hopf fibration]] $f = h_{\mathbb{H}}$ the attaching space is [[quaternionic projective space]] $\mathbb{H}P^2$ and the choice of homotopy $c$ is a choice of [[quaternionic oriented cohomology theory|quaternionic orientation]] to second stage.


{#PastingDiagramForHomotopyWhiteheadIntegral}  Moreover, the de-composition of this [[pasting diagram]] exhibits the [[homotopy Whitehead integral]]/[[functional cup product]]-formula for the Hopf invariant:

\begin{imagefromfile}
        "file_name": "EWhiteheadIntegralPastingDiagram.jpg",
        "web": "nlab",
        "width": 700,
        "unit": "px",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting the homotopy Whitehead integral",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}



## Properties

### Generic values

For $n$ odd, the Hopf invariant necessarily vanishes. For $n$ even however, then there is a homomorphism

$$
  \pi_{2n-1}(S^n) \longrightarrow  \mathbb{Z}
$$

whose [[image]] contains at least the even integers.


### Hopf invariant one

A famous open question in the 1950s was which maps $f$ (eq:TheMap) have _Hopf invariant one_, namely $[HI(f)] = 1$ (eq:HopfInvariantFormula).

The _[[Hopf invariant one theorem]]_ ([Adams60](Hopf+invariant+one#Adams60)) states that the only maps of Hopf invariant one, $[HI(f)] = 1$, are the [[Hopf constructions]] on the four real [[normed division algebras]]:

* the [[real Hopf fibration]];

* the [[complex Hopf fibration]];

* the [[quaternionic Hopf fibration]];

* the [[octonionic Hopf fibration]].

### Via Sullivan models

+-- {: .num_prop #RecognitionFromSullivanModels}
###### Proposition

By standard results in [[rational homotopy theory]], every [[continuous function]]

$$
  S^{4k-1} \overset{f}{\longrightarrow} S^{2k}
$$

corresponds to a unique [[dgc-algebra]] [[homomorphism]] 

$$
  CE
  \big( 
    \mathfrak{l}S^{4k-1}
  \big)
  \overset{ CE(\mathfrak{l}f) }{\longleftarrow}
  CE
  \big( 
    \mathfrak{l}S^{2k}
  \big)
$$

between [[Sullivan models]] [[rational n-sphere|of n-spheres]].

The unique free [[coefficient]] of this homomorphism $CE(\mathfrak{l}f)$ is the Hopf invariant $HI(f)$ of $f$:

\begin{center}
\begin{imagefromfile}
  "file_name": "HopfInvariantFromSullivanModels.jpg",
  "width": 530
\end{imagefromfile}
\end{center}

=--


### Whitehead integral formula

See at _[[Whitehead integral formula]]_ and see the references [below](#ReferencesWhiteheadIntegralFormula)


## Related concepts

* [[Hopf invariant one]]

* [[Whitehead integral formula]]

  * [[functional cup product]]

  * [[Hopf-Wess-Zumino term]]

* [[e-invariant]]

* [[Hopf degree theorem]]

* [[EHP spectral sequence]]

## References

### General


* {#Husemoller66} [[Dale Husemöller]], chapter 15 of: _Fibre Bundles_, Graduate Texts in Mathematics 20, Springer New York (1966) ([doi:10.1007/978-1-4757-2261-1](https://link.springer.com/book/10.1007/978-1-4757-2261-1))

* {#MosherTangora86} [[Robert Mosher]], [[Martin Tangora]], p. 33 of _Cohomology operations and applications in homotopy theory_, Harper & Row 1986 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/moshtang.pdf))

* [[John Michael Boardman]], B. Steer, _On Hopf Invariants_  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/boarstee.pdf))

* Michael Crabb, [[Andrew Ranicki]], _The geometric Hopf invariant_ ([pdf](http://www.maths.ed.ac.uk/~aar/slides/hopfbeam.pdf))

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 12 of: _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

* [[Gereon Quick]], _The Hopf invariant one problem via K-theory_, lecture notes in: _[Advanced algebraic topology](https://folk.ntnu.no/gereonq/Math231br.html)_, 2014 ([[QuickHopfInvariant.pdf:file]])


See also:

* Wikipedia, _[Hopf invariant](http://en.wikipedia.org/wiki/Hopf_invariant)_

And see the references at _[[Hopf invariant one]]_ for more, in particular for the formulation via [[topological K-theory]].

### Whitehead's integral formula
  {#ReferencesWhiteheadIntegralFormula}

Discussion via [[differential forms]]/[[rational homotopy theory]] (see also at [[functional cup product]]):

* {#Whitehead47} [[J. H. C. Whitehead]], _An expression of Hopf's invariant as an integral_, Proc. Nat. Acad. Sci. USA 33 (1947), 117–123 ([jstor:87688](https://www.jstor.org/stable/87688))

* [[Hassler Whitney]], Section 31 in _Geometric Integration Theory_, 1957 ([pup:3151](https://press.princeton.edu/titles/3151.html))

* {#Haefliger78} [[André Haefliger]], p. 3 of _Whitehead products and differential forms_, In: P.A. Schweitzer (ed.), _Differential Topology, Foliations and Gelfand-Fuks Cohomology_, Lecture Notes in Mathematics, vol 652. Springer 1978 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Prop. 17.22 in _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* Lee Rudolph, _Whitehead's Integral Formula, Isolated Critical Points, and the Enhancement of the Milnor Number_, Pure and Applied Mathematics Quarterly Volume 6, Number 2, 2010 ([arXiv:0912.4974](https://arxiv.org/abs/0912.4974))

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], Section 14.5 of: _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (1981, 2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))

* {#SinhaWalter13} [[Dev Sinha]], [[Ben Walter]], _Lie coalgebras and rational homotopy theory II: Hopf invariants_, Trans. Amer. Math. Soc. 365 (2013), 861-883  ([arXiv:0809.5084](https://arxiv.org/abs/0809.5084), [doi:10.1090/S0002-9947-2012-05654-6](https://doi.org/10.1090/S0002-9947-2012-05654-6))

* {#FSS19} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_, Comm. Math. Phys. 2020 ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

[[!redirects Hopf invariants]]

