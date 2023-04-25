[[!redirects ordinary cohomology in homotopy type theory]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

The [[ordinary cohomology|ordinary]] [[cohomology]] [[cohomology group|groups]] are [[algebra|algebraic]] [[invariants]] of [[homotopy types]], and hence of [[types]] in [[homotopy type theory]]. Typically they are much easier to compute than [[homotopy groups]]. There are many theorems in classical algebraic topology relating them other invariants such as the universal coefficient /theorem and the Hurewicz theorem.


## Definition 

There are many different flavours of [[cohomology]], but it's usually best to start simple and add features according to its use.

Let $K(G,n)$ be the [[Eilenberg-MacLane space]] of an [[abelian group]] $G$ for some $n : \mathbb{N}$. The (reduced) **_[[ordinary cohomology|ordinary]]_ cohomology group** (of degree $n$ with coefficients in $G$) of a [[pointed]] space $X$ is the following [[set]]:

$$ \bar{H}^n(X ; G) \equiv \| X \to^* K(G,n) \|_0 $$

Note that there is an [[H-space]] structure on $K(G,n)$ naturally, so for any $|f|,|g| : H^n(X;G)$ we can construct an element $|\lambda x . \mu(f(x),g(x))| : H^n(X; G)$, hence we have a [[group]].

Note for any type $X$ we can make this the **_unreduced_ cohomology** (and call it $H$ instead of $\bar{H}$) by simply adding a disjoint basepoint to $X$ giving us $X_+ \equiv X + 1$ making it pointed.

Let $E$ be a [[spectrum]], we can define the (reduced) **_generalized_ cohomology** group of degree $n$ of a [[pointed]] space $X$ is defined as:

$$ \bar{H}^n (X; E) \equiv \| X \to E_n \|_0 $$

note that $E_n$ has a natural [[H-space]] structure as by definition we have $E_n \simeq \Omega E_{n+1}$ giving us the same group operation as before. In fact, ordinary cohomology becomes a special case of generalized cohomology just by taking coefficients in the [[Eilenberg-MacLane spectrum]] $HG$ with $(HG)_n \equiv K(G,n)$.

## Properties ##

Generalized reduced cohomology satisfies the **Eilenberg-Steenrod axioms**:

* ( _Suspension_ ) There is a natural isomorphism
$$ \bar{H}^{n+1} (\Sigma X; E) \simeq \bar{H}^{n} (X; E).$$

* ( _Exactness_ ) For any cofiber sequence $X \to Y \to Z,$ the sequence
$$\bar{H}^{n} (X; E) \to \bar{H}^{n} (Y; E) \to \bar{H}^{n} (Z; E)$$ 
is an exact sequence of abelian groups.

* ( _Additivity_ ) Given an indexing type $I$ satisfying $0$-choice (e.g. a finite set) and a family $X: I \to U,$ the canonical homomorphism
$$\bar{H}^{n} (\bigvee_{i:I} X_i; E) \to \prod_{i:I}\bar{H}^{n} (X_i; E)$$
is an isomorphism.

Ordinary cohomology also satisfies the _dimension axiom_:

* $\bar{H}^{n} (X, G) = 0$ if $n \neq 0.$

## See also ##

* [[synthetic homotopy theory]]

* [[homotopy groups of spheres in homotopy type theory]]

* [[Hopf construction in homotopy type theory]]

* [[spectral sequence]]

* [[cohomology]]

* [[homology]]

## References
 {#References}

The notion of [[Whitehead generalized cohomology]], [[Brown representability theorem|i.e.]] with [[coefficients]] in any [[spectrum type]]:

* [[Evan Cavallo]], Section 3.2 of: *Synthetic Cohomology in Homotopy Type Theory* (2015) &lbrack;[pdf](https://staff.math.su.se/evan.cavallo/works/thesis15.pdf), [[Cavallo-CohomologyInHoTT.pdf:file]]&rbrack;

In the further generality of [[twisted cohomology]] with [[coefficients]] in any [[spectrum type]]:

* [[Floris van Doorn]], Def. 5.4.2 in: _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_ (2018) &lbrack;[arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [pdf](http://florisvandoorn.com/papers/dissertation.pdf)&rbrack;

Implementation of [[ordinary cohomology|ordinary]] [[integral cohomology]] (i.e. with [[coefficients]] in the [[Eilenberg-MacLane spaces]]/[[Eilenberg-MacLane spectra|-spectra]]) in [[cubical type theory|cubical]] [[Agda]]:

* [[Guillaume Brunerie]], [[Axel Ljungström]], [[Anders Mörtberg]], *Synthetic Integral Cohomology in Cubical Agda*, 30th EACSL Annual Conference on Computer Science Logic (CSL 2022) **216** (2022) $[$[doi:10.4230/LIPIcs.CSL.2022.11](https://doi.org/10.4230/LIPIcs.CSL.2022.11)$]$

Implementation of [[cohomology rings]] in [[cubical agda]]:

* [[Thomas Lamiaux]], [[Axel Ljungström]], [[Anders Mörtberg]], _Computing Cohomology Rings in Cubical Agda_ ([arxiv:2212.04182] (https://arxiv.org/abs/2212.04182))






[[!redirects cohomology in homotopy type theory]]