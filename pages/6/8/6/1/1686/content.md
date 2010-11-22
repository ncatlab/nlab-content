
> under construction


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea


A _cohomology spectral sequence_ is a sequence of certain [[cochain complex]]es such that each is in each entry the [[cochain cohomology]] of the previous one.

Spectral sequences are used as computational tools in [[homological algebra]] and more generally in [[homotopy theory]].  Notably they are used to compute composition of [[derived functor]]s.

Traditionally this is considered on [[model structure on chain complexes|model catgories of chain complexes]] in some [[abelian category]] for which fibrant replacement is given by injective resolution of [[chain complex]]es.
But more generally there is a notion of [[nonabelian cohomology|nonabelian]]/unstable spectral sequences, called **homotopy spectral sequences**.


## Definition

Throughout, let $\mathcal{A}$ be an [[abelian category]]. 

### Spectral sequence


+-- {: .un_defn}
###### Definition

A __cohomology spectral sequence__ in $\mathcal{A}$ is 

* a family $(E^{p,q}_r)$ of [[object]]s in $\mathcal{A}$, for all [[integer]]s $p,q,r$ with $r\geq 1$ 

  (these are said to form the __$r$-th page__ of the spectral sequence)

* for each $p,q,r$ as above a [[morphism]] (called the __differential__) 
  
  $$
    d^{p,q}_r:E^{p,q}_r\to E^{p+r,q-r+1}_r
  $$ 

  satisfying $d_r^2 = 0$ (more precisely, $d_r^{p+r,q-r+1}\circ d_r^{p,q} = 0$

* [[isomorphism]]s $\alpha_r^{p,q}: H^{p,q}(E_r)\to E^{p,q}_{r+1}$ where 
  the [[chain cohomology]] is given by
  
  $$
    H^{p,q}(E_r) = \mathrm{ker} d^{p,q}_r/ \mathrm{im} d^{p-r,q+r-1}_r
   \,.
  $$

=--

Analogously a **homology spectral sequence** is collection of objects $(E_{p,q}^r)$ with the differential $d_r$ of degree $(-r,r-1)$.



### Convergence

+-- {: .un_defn}
###### Definition

A spectral sequence $(E_r)$ **collapses** at the $r$th term if $E_r \simeq E_{r+1} \simeq \cdots =: E_\infty$

A spectral sequence $(E_r)$ **converges** at $(p,q)$ if there exists finite $r$ such that $E_r^{p,q} \simeq E_{r+1}^{p,q} \cdots =: E_\infty^{p,q} $. One writes this as

$$
  E^{p,q}_r \Rightarrow E^{p,q}_\infty
  \,.
$$

A spectral sequence is said to **degenerate** in the $E_r$-term if $d^{p,q}_{r'} = 0$ for all $r'\geq r$. Then clearly $E_\infty^{p,q} = E_r^{p,q}$.


Specifically, for $(E^n)_{n \in \mathbb{Z}}$ a family of objects, (thought of as a page with $E^n$ on each place $(p,q)$ of the $n$-th diagonal $p+q = n$) and we say that a spectral sequence $(E^{p,q}_r)$ **converges** to $(E^n)$ and write

$$
  E_r^{p,q} \Rightarrow E^{p+q}
$$

if for each $n$ there is a decreasing filtration  $E^n  \cdots \supset F^p E^n \supset F^{p+1} E^n \supset \cdots$ and isomorphisms $E^{p,q}_\infty \to F^p E^{p+q}/F^{p+1} E^{p+q}$. 

=--

+-- {: .un_remark}
###### Remark

In applications one is interested in computing the $E^n$ and uses spectral sequences converging to this as tools for approximating $E^n$ in terms of the given filtration.

Therefore usually spectral sequences are required to converge in each degree, or even that for each pair $(p,q)$ there exists an $r_0$ such that for all $r\geq r_0$, $d_r^{p-r,q+r-1} = 0$.

=--





### Graphical presentation

## Examples

### Filtered complexes

### Exact couples

### Grothendieck spectral sequence

Let $\mathcal{A} \stackrel{F}{\to} \mathcal{B} \stackrel{G}{\to} \mathcal{C}$ be two [[left exact functor]]s between [[abelian categories]].
Write $R^p F : \mathcal{D} \to Ab$ for the [[cochain cohomology]] of the [[derived functor]] of $F$ in degree $p$ etc. 


+-- {: .un_theorem}
###### Theorem

For each $A \in \mathcal{A}$ there is a cohomology spectral sequence

$$
  E_r^{p,q} := (R^p G \circ R^q F)(A) 
$$

that converges to the right derived functor of the composite functor


$$
  E_r^{p,q} \Rightarrow R^{p+q} (G \circ F)(A).
$$

=--

#### Leray spectral sequence

The _Leray spectral sequence_ is the special case of the Grothendieck spectral sequence for the case where the two functors being composed are a push-foward of sheaves of a abelian groups along a [[continuous map]] $f : X \to Y$ followed by the push-forward $X \to *$ to the point. This yields a spectral sequence that computes the [[abelian sheaf cohomology]] on $X$ in terms of the abelian sheaf cohomology on $Y$.

+-- {: .un_theorem}
###### Theorem

Let $X, Y$ be suitable [[site]]s and $f : X \to Y$ be a morphism of sites. Let $\mathcal{C} = Ch_\bullet(Sh(X,Ab))$ and $\mathcal{D} = Ch_\bulle(Sh(Y,Ab))$ be the [[model structure on chain complexes|odel categories of complexes of sheaves of abelian groups]]. The [[direct image]] $f_*$ and [[global section]] functor $\Gamma_Y$ compose to $\Gamma_X$:

$$
  \Gamma_X : \mathcal{C} \stackrel{f_*}{\to} \mathcal{D} \stackrel{\Gamma_Y}{\to} Ch_\bullet(Ab)
  \,.
$$

Then for $A \in Sh(X,Ab)$ a sheaf of abelian groups on $X$ there is a cohomology spectral sequence

$$
  E_r^{p,q} := H^p(Y, R^q f_* A)
$$

that converges as

$$
  E_r^{p,q} \Rightarrow H^{p+q}(X, A)
$$

and hence computes the cohomology of $X$ with coefficients in $A$ in terms of the cohomology of $Y$ with coefficients in the push-forward of $A$.

=--

## Properties

### Convergence of the double-complex spectral sequence


+-- {: .un_theorem}
###### Theorem

(...)

=--

## References

### Abelian/stable theory

A useful brief review of standard definitions and facts about spectral sequences is 

* [[Hal Schenck]], _Chapter 9: Cohomology and spectral sequences_ ([pdf](http://www.math.uiuc.edu/~schenck/tapp.pdf))

### Nonabelian / unstable theory {#ReferencesNonabelian}

Homotopy spectral sequences in model categories are discussed in 

* A. Bousfield, _Cosimplicial resolutions and homotopy spectral sequences in model categories_ ([arXiv:math/0312531](http://arxiv.org/abs/math/0312531)).

Spectral sequences in a categories with [[zero morphism]]s are discussed in 

* [[Marco Grandis]], _Homotopy spectral sequences_ ([arXiv:1007.0632](http://arxiv.org/abs/1007.0632))
