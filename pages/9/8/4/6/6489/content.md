
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Bridgeland stability conditions on a [[triangulated category]] are certain data which give a derived analogue of the Mumford's stability.

The concept originally arose as a formalization of reaction processes of [[D-branes]] for the [[B-model]] [[topological string]]. These are (hypothetical) physical objects that appear in different species labeled by [[objects]] in a [[triangulated category|triangulated]] [[derived category]] (of [[quasicoherent sheaves]] on some [[Calabi-Yau variety]]). Whenever there is a process 

$$
  A \leftrightarrow B \oplus C
$$

by which a brane of type $A$ may decay into a brane of type B and a brane of type C (much like a [[chemical reaction]]), this is witnessed by the fact that there is a [[homotopy fiber sequence]] (a distinguished triangle in the [[triangulated category]]) of the form

$$
  B \longrightarrow A \longrightarrow C
  \,.
$$

(See [Aspinwall 04](#Aspinwall04), search the document for the keyword "decay".)

Mathematically such a [[homotopy fiber sequence]] in a [[triangulated category]] precisely expresses the fact that $A$ is a "twisted [[direct sum]]" of $B$ and $C$ ([[extension]], [[semidirect product]]), hence much like the plain [[direct sum]], but with some "interaction" included.

In addition there are then _Bridgeland stability conditions_ on such [[triangulated categories]] of topological D-branes, which determine which of these reaction processes lead to stable compounds (whence the term!), i.e. whether, in the above example, the brane of type $A$ will really decay into branes of type B and C, or if conversely the latter will fuse. (See again [Aspinwall 04](#Aspinwall04), search the document for the keyword "stability".)





## Definition

Let $\mathcal{A}$ be an [[abelian category]] and $K(\mathcal{A})$ be its [[Grothendieck group]]. A **stability function**, sometimes also called a _central charge_, is a  [[linear map]] 

\[
  \label{StabilityFunction}
  Z 
  \;\colon\; 
  K(\mathcal{A})
  \longrightarrow 
  \mathbb{C}
\] 

such that for all non-[[zero objects]], the [[image]] of $Z$ lies in the [[upper half-plane|semi-upper half plane]] 

$$
  H
  \;=\;
  \left\{
    r exp(i\pi \phi) 
    \;\vert\; 
    r \gt 0
    \;\text{and}\;
    0 \lt \phi \leq 1
  \right\}
$$ 

The _phase_ $\phi(E)$ of an object $E$ is just the [[complex phase]] $\phi$ that occurs in the representation from $H$. Alternatively, by plotting $Z(E)$ in the 
[[complex plane]], the phase is the argument (slope) divided by $\pi$. The phase of $E$ will be denoted $\phi(E)$.

An object $E$ is called **semi-stable** if for all non-trivial [[subobjects]] $F\subset E$ we have the property that 

\[
  \label{SemiStability}
  \phi(F)\leq \phi(E)
\]


An object $E$ is called **stable** if for all non-trivial, proper [[subobjects]] $F\subset E$ we have the property that $\phi(F)$ &lt; $\phi(E)$.

A stability function $Z:K(\mathcal{A})\to \mathbb{C}$ (eq:StabilityFunction) is said to have the **Harder-Narasimhan property** if for any non-[[zero object]] $E$ there exists a finite [[filtered object|filtration]] by [[subobjects]] 

$$
  0=E_0 \subset E_1 \subset \cdots \subset E_n =E
$$ 

such that the [[quotients]] 

$$
  F_i=E_i/E_{i-1}
$$ 

are all semi-stable (eq:SemiStability) and satisfy 

$$
  \phi(F_1) \gt \phi(F_2) \gt \cdots \gt\phi(F_n)
  \,.
$$

Suppose $\mathcal{D}$ is a [[triangulated category]] (usually arising as the [[derived category]] of some [[abelian category]]). A **slicing**, $\mathcal{P}$, is a choice of [[additive category|additive]] [[full subcategories]] $\mathcal{P}(\phi)$ for each $\phi \in \mathbb{R}$ satisfying 

1. $\mathcal{P}(\phi +1)=\mathcal{P}(\phi)[1]$

2. If $\phi_1 \gt \phi_2$ and $A_j\in \mathcal{P}(\phi_j)$, then $Hom(A_1, A_2)=0$.

3. Any object has a finite filtration by the slicing: 

   If $E\in \mathcal{D}$, then there exists $\phi_1 \gt \cdots \gt \phi_n$ and a sequence $0=E_0\to E_1 \to \cdots \to E_n = E$ such that the cone $E_{j-1}\to E_j \to F_j \to E_{j-1}[1]$ satisfies $F_j\in \mathcal{P}(\phi_j)$.

A **stability condition** on $\mathcal{D}$ is a pair $\sigma = (Z, \mathcal{P})$ consisting of a stability function and slicing satisfying the relation that given a non-zero object $E\in \mathcal{P}(\phi)$, then there is a non-zero positive real number $m(E)$ such that $Z(E)=m(E)exp(i\pi \phi)$. This justifies the repeated notation of $\phi$, since this says that if an object lies in a particular slice $\phi$, then it must also have phase $\phi$.

## Key Results

Bridgeland proves that an equivalent way to give a stability is to specify a heart of a bounded [[t-structure]] on $\mathcal{D}$ and give a stability function the heart that satisfies the Harder-Narasimhan property.

Under reasonable hypotheses, one can put a natural topology on the space of stability conditions, $Stab(\mathcal{D})$, under which the space becomes a [[complex manifold]]. Most work using this fact has been done where $\mathcal{D}=D^b(Coh(X))$ where $X$ is a smooth, projective [[algebraic variety|variety]] over $\mathbb{C}$ so that $\mathcal{D}$ is $\mathbb{C}$-linear and $K(\mathcal{D})$ is finitely generated.

$Stab(X)$ has a locally finite wall and chamber decomposition. The philosophy is that if one fixes a numerical condition $v$ and considers the [[moduli space]] of $\sigma$-stable sheaves as $\sigma$ varies through $Stab(X)$, then the moduli spaces $M_\sigma(v)\simeq M_{\sigma '}(v)$ should be isomorphic if $\sigma$ and $\sigma'$ are in the same chamber. Bayer and Macri have shown this is true for K3 surfaces, and upon crossing a wall the moduli spaces are related by a [[birational map]].

## Examples

A motivating example is the following. Let $X$ be a non-singular, [[algebraic curve|projective curve]] over $\mathbb{C}$. Let $\mathcal{A}=Coh(X)$ be the category of [[coherent sheaf|coherent sheaves]] on $X$. The standard stability function is $Z(E)=-deg(E) + i rk(E)$. The classical notion of the slope of a vector bundle is $\mu(E)=\frac{rk(E)}{deg(E)}$. When constructing a moduli of vector bundles using [[geometric invariant theory|GIT]] one needs to consider only slope (semi-)[[stable vector bundle|stable]] vector bundles. One can immediately see that a vector bundle is slope (semi-)stable if and only if it is (semi-)stable with respect to this stability function. Thus stability conditions are a generalization of classical notions of stability.

## Related concepts

* [[wall crossing]] of [[BPS states]]

## References

### Related pre-Bridgeland work

Bridgeland's work was motivated as a formalizatioon of ideas on $\Pi$-stability of [[D-branes]] for the [[topological string]], as discussed in

* [[Michael Douglas]], _D-branes, categories and $N=1$ supersymmetry, J.Math.Phys. __42__ (2001) 2818&#8211;2843;  

* [[Michael Douglas]] _Dirichlet branes, homological mirror symmetry, and stability_, Proc. ICM, Vol. III (Beijing, 2002), 395&#8211;408, Higher Ed. Press, Beijing, 2002

* {#Aspinwall04} [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](https://arxiv.org/abs/hep-th/0403166))


### General

* {#BridgelandA} [[Tom Bridgeland]], _Stability conditions on triangulated categories_, Ann. of Math. 166 (2007) 317&#8211;345,[math.AG/0212237](http://arxiv.org/abs/math/0212237); 
 

* [[Tom Bridgeland]], _Spaces of stability conditions_, Proc. of symposia in pure math. __80__, 2009, [math/0611510](http://arxiv.org/abs/math/0611510). 

* bourwiki: [Bridgeland stability conditions](http://bourwiki.org/wiki/Bridgeland_stability_conditions)

* R. Pandharipande, R.P. Thomas, _Stable pairs and BPS invariants_, [arXiv:0711.3899](http://arxiv.org/abs/0711.3899)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](http://arxiv.org/abs/0811.2435)

* Rina Anno, Roman Bezrukavnikov, Ivan Mirkovi&#263;, _A thin stringy moduli space for Slodowy slices_, [arxiv/1108.1563](http://arxiv.org/abs/1108.1563) 

* [[Tom Bridgeland]], Ivan Smith, _Quadratic differentials as stability conditions_, [arxiv/1302.7030](http://arxiv.org/abs/1302.7030)
 
* [[Daniel Huybrechts]], _Introduction to stability conditions_ ([arXiv:1111.1745](https://arxiv.org/abs/1111.1745))

### Introductions and lectures

* [[Anton Geraschenko]], _notes from an introductory talk_ ([pdf](http://math.berkeley.edu/~anton/written/AspectsModuli/AspectsModuli.pdf))

### Relation to stable branes in string theory

Relation to stable [[B-branes]] and [[fractional D-branes]]:

* [[Aaron Bergman]], _Stability Conditions and Branes at Singularities_,  Journal of High Energy Physics 2008.10 (2008): 07 ([arXiv:hep-th/0702092](http://arxiv.org/abs/hep-th/0702092))

* {#MalyshevVerlinde07} Dmitry Malyshev, [[Herman Verlinde]], _D-branes at Singularities and String Phenomenology_, Nucl.Phys.Proc.Suppl.171:139-163, 2007 ([arXiv:0711.2451](https://arxiv.org/abs/0711.2451))


### Relation to moduli space theory

* Arend Bayer, Emaneule Macri, _Projectivity and Birational Geometry of Bridgeland Moduli Spaces_ ([arXiv:1203.4613](http://arxiv.org/abs/1203.4613))

[[!redirects Bridgeland stability conditions]]

[[!redirects Bridgeland stability]]

