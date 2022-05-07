
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
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
  {#Idea}

Given a [[pointed (∞,1)-category]] $\mathcal{C}$ (such as that [[presentable (∞,1)-category|presented]] by the [[classical model structure on pointed topological spaces]]), the _Toda bracket_ ([Toda 62](#Toda62)) is the operation that takes a sequence of 3 [[composition|composable]] [[1-morphisms]]

$$
  X_0
    \overset{\;\;f_1\;\;}{\longrightarrow}  
  X_1
    \overset{\;\;f_2\;\;}{\longrightarrow}  
  X_2
    \overset{\;\;f_3\;\;}{\longrightarrow}  
  X_3
$$

in $\mathcal{C}$, equipped with a [[pair]] of overlapping [[null homotopies]] 

\begin{xymatrix@C=15pt}
  X_0
  \ar[rr]
    |-{ \;f_1\; }
  \ar@/^2.6pc/[rrrr]
    ^-{0}
    _-{\ }="s1"
  &&
  X_1
  \ar[rr]
    |-{ \;f_2\; }
  \ar@/_2.6pc/[rrrr]
    _-{0}
    ^-{\ }="t2"
  &&
  X_2
  \ar[rr]
    |-{ \;f_3\; }
  &&
  X_3
  %
  \ar@{=>} 
    "t2"+(0,+6); "t2"
    ^-{ \phi_2 }
  \ar@{=>}
    "s1"; "s1"+(0,-6)
    ^-{ \phi_1 }
\end{xymatrix}

to the [[higher homotopy]]-[[equivalence class]] of their [[pasting diagram|pasting]]-composite, which is a [[2-morphism]] [[loop]] (on the [[zero morphism|zero]] [[1-morphism]]) in the [[(∞,1)-categorical hom space]] $\mathcal{C}(X_0,X_1) \in $ [[∞Groupoids]], hence an element in its [[fundamental group]] $\pi_1 \mathcal{C}(X_0,X_1)$:

\begin{xymatrix@=15pt}
  &&
  &&
  X_0
  \ar[dd]
    _-{ f_1 }
    ^>>{\ }="t1"
  \ar[rr]
    _>>{\ }="s1"
  &&
  0
  \ar[dd]
  \\
  \\
  X_0
  \ar@/^2pc/[rr]
    ^-{ 0 }
    _-{\ }="ss"
  \ar@/_2pc/[rr]
    _-{ 0 }
    ^-{\ }="tt"
  &{\phantom{AAAA}}&
  X_3
  &
  :=
  &
  X_1
  \ar[dd]
    ^>>{\ }="t2"
  \ar[rr]
    |-{ \;f_2\; }
    _>>{\ }="s2"
  &&
  X_2
  \ar[dd]
    ^-{ f_3 }
  &&
  \in 
  \;
  \pi_1 
  \mathcal{C}
  \big(
    X_0, X_3
  \big)
  \\
  \\
  &&
  &&
  0 
  \ar[rr]
  &&
  X_3
  %
  \ar@{=>} "s1"; "t1"
    ^-{ \phi_1 }
  \ar@{=>} "s2"; "t2"
    ^-{ \phi_2 }
  \ar@{=>} 
    "ss"; "tt"
    |-{
      \mathclap{\phantom{\vert^{\vert}}}
      \scalebox{.6}{$
          (\phi_2 \cdot f_1)
          \circ
          (f_3 \cdot \phi_1)
      $}
      \mathclap{\phantom{\vert_{\vert}}}
    }
\end{xymatrix}

Or rather, the Toda bracket is equivalently taken to be the [[homotopy class]] of the [[1-morphism]]
$
  \vdash 
  \big(
    (\phi_2 \cdot f_1)
      \circ
    (f_3 \cdot \phi_1)
  \big)
$
that _classifies_ this [[homotopy]], via the [[universal property]] of [[homotopy fibers]]/[[homotopy cofibers]]:

* if $\mathcal{C}$ admits [[finite (∞,1)-colimits]] or at least [[reduced suspensions]] $\Sigma(-)$ ([[homotopy cofibers]] of [[zero morphisms]]), so that this [[2-morphism]] between [[zero morphisms]] induces a [[1-morphism]]

  $$
    \Sigma X_0
      \overset{
        \big\langle
          f_1, f_2, f_3
        \big\rangle_{(\phi_1,\phi_2)}
      }
      {\longrightarrow}
    X_3
  $$

* if $\mathcal{C}$ admits [[finite (∞,1)-limits]] or at least [[based loop space objects]] $\Omega(-)$ ([[homotopy fibers]] of [[zero morphisms]]), so that this [[2-morphism]] between [[zero morphisms]] induces a [[1-morphism]]

  $$
    X_0
      \overset{
        \big\langle
          f_1, f_2, f_3
        \big\rangle_{(\phi_1,\phi_2)}
      }
      {\longrightarrow}
    \Omega X_3
    \,,
  $$

or both, as we shall assume for ease of notation,
then the Toda bracket is the [[homotopy class]] of this 1-morphism in the [[homotopy category of an (infinity,1)-category|homotopy category]]:

\[
  \label{TheTodaBracketDependingOnTheNullHomotopies}
  \array{
  \big\langle
    f_1, f_2, f_3
  \big\rangle_{(\phi_1,\phi_2)}
  \;\coloneqq\;
  \big[
    \vdash 
    (\phi_2 \cdot f_1)
      \circ
    (f_3 \cdot \phi_1)
  \big]
  \;
  \in
  &&
  \pi_0 \mathcal{C}
  \big(
    \Sigma X_0, X_3
  \big)
  \\
  &
  \;\simeq\;
  &
  \pi_0 \mathcal{C}
  \big(
    X_0, \Omega X_3
  \big)
  \\
  &
  \;
  \simeq
  \;
  &
  \pi_1 \mathcal{C}
  \big(
    X_0, X_3 
  \big)
  }
  \,.
\]


\begin{imagefromfile}
    "file_name": "TodaBracketHomotopyDiagrammatically.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/M-Theory+as+Mf-Theory)"
\end{imagefromfile}

Here the last [[pasting diagram]] on the bottom right shows the [[homotopy cofiber]]-construction equivalently realized via [[mapping cones]] (ordinary [[cofiber coproducts]] after [[cofibrant resolution|resolving]] points to [[cones]]), by which one may present the top [[homotopy coherent diagram]] in, for instance, any [[pointed model category|pointed]] [[cofibration category]]- or [[model category]]-[[presentable (infinity,1)-category|presentation]] of the [[pointed (∞,1)-category]] $\mathcal{C}$.

(It is in this last form, by "consecutively extending maps over cones", that the Toda bracket was introduced in [Toda 62](#Toda62), and in which it is still presented in most references to date. The above [[homotopy coherent diagram|homotopy-diagrammatic]] formulation follows [[schreiber:M-Theory as Mf-Theory|SS21]]. If anyone knows of another citeable reference that presents the Toda bracket in this more abstract-homotopy/$(\infty,1)$-category theoretic way, then let's add the pointer here.)


More precisely,  traditionally authors want the Toda bracket to be independent of the choice of [[null homotopies]] $(\phi_1,\phi_2)$ and thus regard (eq:TheTodaBracketDependingOnTheNullHomotopies) in a suitable [[quotient set]] of
$
  Ho(\mathcal{C})
  \big(
    X_0, \Omega X_3
  \big)
$
where this dependence is quotiented out. Often authors take the plain Toda bracket to *be* the [[subset]] 

\[
  \label{TheTodaBracketDependingOnTheNullHomotopies}
  \array{
  \big\langle
    f_1, f_2, f_3
  \big\rangle
  \;\coloneqq\;
  \left\{
    \big\langle
      f_1, f_2, f_3
    \big\rangle_{(\phi_1,\phi_2)}
    \left\vert
    \array{
      0 
        &\overset{\phi_1}{\Rightarrow}&  
      f_2 \circ f_1
      \\ 
      f_3 \circ f_2
        &\underset{\phi_2}{\Rightarrow}&  
      0
    }
    \right.
  \right\}
  \;
  \subset
  &&
  \pi_0 \mathcal{C}
  \big(
    \Sigma X_0, X_3
  \big)
  \\
  &
  \;\simeq\;
  &
  \pi_0 \mathcal{C}
  \big(
    X_0, \Omega X_3
  \big)
  \\
  &
  \;
  \simeq
  \;
  &
  \pi_1 \mathcal{C}
  \big(
    X_0, X_3 
  \big)
  }
\]

of all the classes (eq:TheTodaBracketDependingOnTheNullHomotopies) as one varies the [[null homotopies]] $(\phi_1,\phi_2)$.

In any case, the Toda bracket may be thought of as being in [[homotopy theory]] what the [[Massey product]] is in [[cohomology theory]]: It is a "[[secondary characteristic class|secondary]] invariant", which exists when/since "primary invariants" -- namely the [[homotopy classes]] of the morphisms $f_2 \circ f_1$ and $f_3\circ f_2$ -- vanish, as witnessed by the [[null homotopies]].

A generalization of the Toda bracket produces an invariant for sequences of morphisms, equipped with consecutive pair-wise null-homotopies, which may contain possibly more than three morphisms; this _higher Toda bracket_ was maybe first considered in [Cohen 68, Sec. 2](#Cohen68)

\linebreak

## Preliminaries

Consider a sequence of maps $ A_0 \to A_1 \to A_2 \to A_3 $.  If the composites $A_0 \to A_2 $ and $ A_1\to A_3$ are nulhomotopic, then one has a diagram
$$\begin{array}{ccccc}
A_0 & \to & A_1 & \to & * \\
\downarrow & & \downarrow & & \downarrow \\
* & \to & A_2 & \to & A_3
\end{array} $$
any choice of homotopies in the two squares gives a map $ \Sigma A_0 \to A_3 $.


Define $C$ and $D$ to be the cofibers of $A_0 \to A_1$ and $A_1\to A_2$, respectively. A choice of homotopy $ A_0 \to A_2 \sim 0 $ corresponds to a choice of factorization $ A_1 \to C \to A_2 $, which gives a diagram of pushout squares

$$\begin{array}{ccccccc}
A_0 & \to & A_1 & \to & * \\
\downarrow & & \downarrow & & \downarrow \\
* & \to & C &\to & \Sigma A_0  & \to & *\\
 & & \downarrow & & \downarrow & & \downarrow \\
 & & A_2 & \to & D & \to & C'
\end{array}$$

It is to be noted that the map $ \Sigma A_0 \to D $ and possibly the object $C'$ depend on the choice of factor $ C \to A_2 $, but that $A_2 \to D$ does not, in any meaningful sense, so depend: this is just the structure map of the cofiber of $A_1\to A_2$.  Note that the cofiber $C'$ of $C\to A_2$ is thus equivalent to that of $\Sigma A_0 \to D$; but again the role of choices must be studied.

## Definitions

A sequence of maps $A_0 \to A_1 \to \cdots \to A_n$ will be called *a bracket sequence* (a novel phrase for the purposes of this entry) in either of two cases:

* $n = 3$ and the composites $A_0 \to A_2$ and $A_1 \to A_3$ are nulhomotopic; OR
* $n \gt 3$, and (using the preceding notations), there are choices of factor $C\to A_2$ and $ D \to A_3 $ such that the induced sequence $ \Sigma A_0 \to D \to A_3 \to \cdots \to A_n$ is a bracket sequence.

In all cases, a bracket sequence leads to a three-map sequence
$$ \Sigma^m A_0 \to D_m \to A_{m+2} \to A_{m+3} $$
in which consecutive maps compose trivially, and so there are induced choices of maps
$$ \Sigma^{m+1} A_0 \to A_{m+3} .$$

The collection of all such maps, taking all compatible variations, is the **Toda Bracket** of the bracket sequence.

Among the bracket sequences, a particular family arises which here will be called _null-bracket_ (again, a novel phrase).  A sequence will be called null-bracket if

* $n=2$ and $A_0 \to A_2$ is trivial, OR
* $n \gt 2$, and there is a choice of factorization $ A_1 \to C \to A_2 $ such that the sequence $ C \to A_2 \to \cdots \to A_n $ is null-bracket.

If the Toda bracket for a bracket sequence includes the trivial map $\Sigma^{m+1} A_0 \to A_{m+3}$ then the sequence is null-bracket.

## Applications

By definition, if a sequence is a bracket sequence AND NOT a null-bracket sequence, it follows that all the relevant maps $\Sigma^{k} A_0 \to A_n$ are nontrivial.  Things like these Toda brackets have been studied by many _(FIXME: references later)_ and especially the length-three brackets used by H. Toda to describe most of $\pi_k \mathbb{S}^n$ for $k \lt 31$ or so.

In ([Cohen, 1968](#Cohen68)) is given a criterion for stable maps of spheres to inhabit non-null Toda brackets; this turns out to be most of $\pi_* \mathbb{S}$, and furthermore the maps in the bracket sequences can be chosen from a very small set (_FIXME_: be more precise! degree maps $n \iota$, [[Hopf map]]s $\eta, \theta,\sigma$, and $\alpha_p$... )

## Related concepts

* [[Massey product]]

* [[e-invariant]]

## References

The concept of Toda brackets is due to:

* {#Toda62} [[Hirosi Toda]], _Composition Methods in Homotopy Groups of Spheres_, Annals of Mathematics Studies Volume 49, Princeton University Press (1962) ([jstor:j.ctt1bgzb5t](https://www.jstor.org/stable/j.ctt1bgzb5t))

Higher Toda brackets were introduced in:

* {#Cohen68} Joel Cohen, Section 2 of: _The decomposition of stable homotopy_, Annals of Mathematics (2) 87 (2): 305&#8211;320 (1968) ([doi:10.2307/1970586](https://doi.org/10.2307/1970586))

Further discussion: 

* {#Kochmann96} [[Stanley Kochmann]], section 5.7 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


* [[Hans-Joachim Baues]], _On the cohomology of categories, universal Toda brackets and homotopy pairs_, K-Theory __11__:3, April 1997, pp. 259-285 (27) ([doi:10.1023/A:1007796409912](http://dx.doi.org/10.1023/A:1007796409912))

* Boryana Dimitrova, _Universal Toda brackets of commutative ring spectra_, poster, Bonn 2010 ([pdf](http://www.math.uni-bonn.de/people/grk1150/YWT2010/YWT_Dimitrova.pdf))

* [[Constanze Roitzheim]], [[Sarah Whitehouse]], _Uniqueness of $A_\infty$-structures and Hochschild cohomology_ ([arxiv/0909.3222](http://arxiv.org/abs/0909.3222))

* [[Steffen Sagave]], _Universal Toda brackets of ring spectra_, Trans. Amer. Math. Soc., 360(5):2767-2808, 2008 ([math.KT/0611808](http://arxiv.org/abs/math/0611808))

[[!redirects Toda Brackets]]

[[!redirects Toda brackets]]
