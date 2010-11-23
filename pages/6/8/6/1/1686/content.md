
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

Traditionally this is considered on [[model structure on chain complexes|model categories of chain complexes]] in some [[abelian category]] for which fibrant replacement is given by injective resolution of [[chain complex]]es.
But more generally there is a notion of [[nonabelian cohomology|nonabelian]]/unstable spectral sequences, called **homotopy spectral sequences**.


## Definition

Throughout, let $\mathcal{A}$ be an [[abelian category]]. 

### Spectral sequence


+-- {: .un_defn}
###### Definition

A __cohomology spectral sequence__ in $\mathcal{A}$ is 

* a family $(E^{p,q}_r)$ of [[object]]s in $\mathcal{A}$, for all [[integer]]s $p,q,r$ with $r\geq 1$ 

  (for a fixed $r$ these are said to form the __$r$-th page__ of the spectral sequence)

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
**(convergence)**

A component of a spectral sequence $(E_r)$ **converges** at $(p,q)$ if there exists finite $r$ such that $E_r^{p,q} \simeq E_{r+1}^{p,q} \cdots =: E_\infty^{p,q} $. One writes this as

$$
  E^{p,q}_r \Rightarrow E^{p,q}_\infty
  \,.
$$

A spectral sequence is said to **degenerate** in the $E_r$-term if $d^{p,q}_{r'} = 0$ for all $r'\geq r$. Then clearly it converges degreewise.

A spectral sequence is called **bounded** if for each $r$ and $n$ there are only finitely many non-vanishing terms of the form $E_r^{p,n-p}$. Also a bounded spectral sequence converges degreewise.

A spectral sequence $(E_r)$ **converges** if it converges degreewise to a graded filtration: if there is a graded object $(H^n)_{n \in \mathbb{Z}}$ equipped in each degree with a _finite_ filtration

$$
  0 \subset \cdots \subset F^{p} H^n \subset F^{p-1}H^n  \subset \cdots \subset F^0 H^n := H^n
$$

such that

$$
  E_\infty^{p,q}  \simeq F^p H^{p+q} / F^{p+1}H^{p+q}
  \,.
$$

The notation for this is

$$
  E_r^{p,q} \Rightarrow H^{p+q}
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

In applications one is interested in computing the $H^n$ and uses spectral sequences converging to this as tools for approximating $H^n$ in terms of the given filtration.

Therefore usually spectral sequences are required to converge in each degree, or even that for each pair $(p,q)$ there exists an $r_0$ such that for all $r\geq r_0$, $d_r^{p-r,q+r-1} = 0$.

=--

+-- {: .un_defn}
###### Definition
**(Collapse)**

A spectral sequence **collapses** at $r$ if in $E_r^{p,q}$ only a single row or a single column in non-vanishing.

=--

+-- {: .un_lemma}
###### Observation


If $(E_r)$ collapses at $r$, then it converges to $H^\bullet$ with $H^n$ being the unique entry $E^{p,q}_r$ on the non-vanishing row/column with $p+q = n$.

=--

### Graphical presentation

(...)

## Examples

### First quadrant spectral sequence {#FirstQuadrant}

+-- {: .un_def}
###### Definition

A **first quadrant spectral sequence** is one for wich all pages are concentrated in the first quadrant of the $(p,q)$-plane, in that

$$
  ((p \lt 0) or (q \lt 0))
  \;\;
  \Rightarrow
  E_r^{p,q} = 0
  \,.
$$


=--

+-- {: .un_lemma}
###### Observation

If the $r$th page is concentrated in the first quadrant, then so the $(r+1)st$ page. So if the first one is, then all are.

=--


+-- {: .un_lemma}
###### Observation

Every first quadrant spectral sequence converges at $(p,q)$ from $r \gt max(p,q+1)$ on

$$
  E_{max(p,q+1)+1}^{p,q} = E_\infty^{p,q}
  \,.
$$


=--

+-- {: .un_lemma}
###### Observation

If a first quadrant spectral sequence converges

$$
  E_r^{p,q} \Rightarrow H^{p+q}
$$

then each $H^n$ has a filtration of length $n+1$

$$
  0 = F^{n+1}H^n \subset F^n H^n \subset \cdots \subset F^1 H^n \subset F^0 H^n = H^n
$$

and we have

* $F^n H^n \simeq E_\infty^{n,0}$

* $H^n/F^1 H^n \simeq E_\infty^{0,n}$.

=--

### Spectral sequence of a filtered complex

(...)

#### Spectral sequence of a double complex

A [[double complex]] is naturally filtered in two ways: by columns and by rows. By the above this gives two different spectral sequences associated with it.

(...)

### Exact couples

### Spectral sequences for hyper-derived functors {#HyperDerivedFunctors}

(...)

### Grothendieck spectral sequence {#GrothendieckSpectralSequence}

Let $\mathcal{A} \stackrel{F}{\to} \mathcal{B} \stackrel{G}{\to} \mathcal{C}$ be two [[left exact functor]]s between [[abelian categories]].

Write $R^p F : \mathcal{D} \to Ab$ for the [[cochain cohomology]] of the [[derived functor]] of $F$ in degree $p$ etc. 


+-- {: .un_theorem}
###### Theorem

If $F$ sends [[injective object]]s of $\mathcal{A}$ to $G$-[[acyclic object]]s in $\mathcal{B}$ then for each $A \in \mathcal{A}$ there is a [first quadrant](#FirstQuadrant) cohomology spectral sequence

$$
  E_r^{p,q} := (R^p G \circ R^q F)(A) 
$$

that converges to the right [[derived functor]] of the composite functor


$$
  E_r^{p,q} \Rightarrow R^{p+q} (G \circ F)(A).
$$

Moreover

1. the edge maps in this spectral sequence are the canonical morphisms
 
   $$
     R^p G (F A) \to R^p (G \circ F)(A)
   $$

   induced from applying $F$ to an injective resolution 
   $A \to \hat A$ and the [[isomorphism]]

   $$
     R^q (G \circ F)(A) \to G(R^q F (A))
     \,.
   $$

1. the [[exact sequence]] of low degree terms is

   $$
     0 \to (R^1 G)(F(A)) \to R^1(G \circ F)(A)
      \to F(R^1(G(A)))
      \to (R^2 F)(G(A))
      \to R^2(G \circ F)(A)
   $$

=--

+-- {: .proof}
###### Proof

Since for $A \to \hat A$ an injective [[resolution]] of $A$ the complex $F(\hat A)$ is a chain complex not concentrated in a single degree, we have that $R^p (G \circ F)(A)$ is equivalently the [[hyper-derived functor]] evaluation $\mathbb{R}^p(G) (F(A))$.

Therefore the second spectral sequence discussed at [hyper-derived functor spectral sequences](#HyperDerivedFunctors) converges as

$$
  (R^p G)H^q(F(\hat A)) \Rightarrow R^p (G \circ F)(A)
  \,.
$$

Now since by construction $H^q(F(\hat A)) = R^q F(A)$ this is a spectral sequence

$$
  (R^p G)(R^q F) A) \Rightarrow R^p (G \circ F)(A)
  \,.
$$

This is the Grothendieck spectral sequence.

=--

#### Leray spectral sequence

The _Leray spectral sequence_ is the special case of the Grothendieck spectral sequence for the case where the two functors being composed are a push-foward of sheaves of a abelian groups along a [[continuous map]] $f : X \to Y$ followed by the push-forward $X \to *$ to the point. This yields a spectral sequence that computes the [[abelian sheaf cohomology]] on $X$ in terms of the abelian sheaf cohomology on $Y$.

+-- {: .un_theorem}
###### Theorem

Let $X, Y$ be suitable [[site]]s and $f : X \to Y$ be a morphism of sites. () Let $\mathcal{C} = Ch_\bullet(Sh(X,Ab))$ and $\mathcal{D} = Ch_\bulle(Sh(Y,Ab))$ be the [[model structure on chain complexes|model categories of complexes of sheaves of abelian groups]]. The [[direct image]] $f_*$ and [[global section]] functor $\Gamma_Y$ compose to $\Gamma_X$:

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

#### Base change spectral sequence for $Tor$ and $Ext$

For $R$ a [[ring]] write $R$[[Mod]] for its category of [[modules]].
Given a [[homomorphism]] of [[ring]]s $f : R_1 \to R_2$ and an $R_2$-[[module]] $N$ there are composites of [[base change]] along $f$ with the [[hom-functor]] and the [[tensor product]] functor

$$
  R_1 Mod \stackrel{\otimes_{R_1} R_2}{\to} R_2 Mod \stackrel{\otimes_{R_2} N}{\to} Ab
$$

$$
  R_1 Mod \stackrel{Hom_{R_1 Mod}(-,R_2)}{\to}
  R_2 Mod
  \stackrel{Hom_{R_2}(-,N)}{\to}
  Ab
  \,.
$$

The [[derived functor]]s of $Hom_{R_2}(-,N)$ and $\otimes_{R_2} N$ are the [[Ext]]- and the [[Tor]]-functors, respectively, so the Grothendieck spectral sequence applied to these composites yields a  [[base change]] spectral sequence for these.

## Properties

+-- {: .un_lemma}
###### Lemma
**(mapping lemma)**

If $f : (E_r^{p,q} \to (F_r^{p,q}))$ is a morphism of spectral sequences such that for some $r$ we have that $f_r : E_r^{p,q} \toF_r^{p,q}$ is an isomorphism, then also $f_s$ is an isomorphism for all $s \geq r$.

=--

+-- {: .un_lemma}
###### Lemma
**(classical convergence theorem)**

(...)

=--

This is recalled in ([Weibel, theorem 5.51](#Weibel)).


## References

### Abelian/stable theory

A standard textbook reference is chapter 5 of 

* [[Charles Weibel]], _An introduction to homological algebra_ Cambridge studies in advanced mathematics 38 (1994)
{#Weibel}

A useful brief review of standard definitions and facts about spectral sequences is 

* [[Hal Schenck]], _Chapter 9: Cohomology and spectral sequences_ ([pdf](http://www.math.uiuc.edu/~schenck/tapp.pdf))

### Nonabelian / unstable theory {#ReferencesNonabelian}

Homotopy spectral sequences in model categories are discussed in 

* A. Bousfield, _Cosimplicial resolutions and homotopy spectral sequences in model categories_ ([arXiv:math/0312531](http://arxiv.org/abs/math/0312531)).

Spectral sequences in a categories with [[zero morphism]]s are discussed in 

* [[Marco Grandis]], _Homotopy spectral sequences_ ([arXiv:1007.0632](http://arxiv.org/abs/1007.0632))
