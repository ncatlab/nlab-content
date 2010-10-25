
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The DHR superselection theory is about [[superselection sectors]] in the [[Haag-Kastler approach]] to [[AQFT]].
As such, it has to state one or more conditions on representations of the given [[Haag-Kastler net]] that specify the representations of the quasi-local algebra that are deemed physically admissible. 

It is named after [[Sergio Doplicher]], [[Rudolf Haag]] and [[John Roberts]].

In the following we consider the theory starting with a [[Haag-Kastler vacuum representation]] on [[Minkowski spacetime]].

The DHR condition says that **all expectation values (of all observables) should approach the vacuum expectation values, uniformly, when the region of measurement is moved away from the origin.** This is one possible abstraction of the situation in a high energy particle collider, where the registered events are localized both in time and in space.  

The DHR condition excludes long range forces like electromagnetism from consideration, because, by [[Stokes' theorem]], the electric charge in a finite region can be measured by the flux of the field strength through a sphere of arbitrary large radius. The DHR analysis is of interest nevertheless, because it has reached a certain maturity and is therefore an excellent object to study: see for example the [[Doplicher-Roberts reconstruction theorem]]. 

## Abstract ##
After the definition of admissible representations we collect some notions that will enable us to state a description of all admissible representations using intrinsic properties of the quasi-local algebra. The central concept that we define is that of a **transportable endomorphism**, these form the objects of a category, the [[DHR category]].

## Definition ##
We start with a [[Haag-Kastler vacuum representation]] that we assume to be irreducible and [[Haag dual]].

Let $\pi_0$ be the vacuum representation from now on, K denote double cones and $\mathcal{J}_0$ be the [[causal index set]] of double cones, just as $\mathcal{O}$ are bounded open sets and $\mathcal{J}$ the [[causal index set]] of bounded open sets.

Recall that the [[C-star algebra]]

$$
\mathcal{A} := clo_{\| \cdot \|} \bigl( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) 
$$

is called the quasi-local algebra of the given net. We will in the same way associate a [[C-star algebra]] to every open region $\mathcal{O}_0$ via

$$
\mathcal{A}(\mathcal{O}_0) := clo_{\| \cdot \|} \bigl( \bigcup_{\mathcal{O}_0 \supseteq \mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) 
$$

+-- {: .un_defn}
###### Definition
A representation $\pi$ of the local algebra $\mathcal{A}$ is called (DHR) **admissible** if $\pi | \mathcal{A}(\mathcal{K}^{\perp})$ is unitarily equivalent to $\pi_0 | \mathcal{A}(\mathcal{K}^{\perp})$ for all $K \in \mathcal{J}_0$, that is, for all double cones $K$.
=--

Note that the equivalence of the representations is required for the causal complement of _all_ double cones, not a special one, so that the characterization that "the representations can not be distinguished at space-like infinity" is misleading.  

+-- {: .un_defn}
###### Definition
Recall that a mapping 
$$
\rho: \mathcal{A} \to \mathcal{A}
$$
is called a **unital endomorphism** if $\rho$ is linear, multiplicative ($\rho(AB) = \rho(A) \rho(B)$) and $\rho(\mathbb{1})=1$.
=--

We will drop "unitarily" from now on.

For any representation $\pi$ and endomorphism $\rho$ the composition $\pi \circ \rho$ is another representation. For this reason one can hope to gain some insights into the representations by studying the endomorphisms, while the set of endomorphisms has certainly more structure than that of representations: For example, endomorphisms may have inverses, and endomorphisms form a [[monoid]] by composition.

First we define "unitarily equivalent" and "intertwiner" analog to the definition for [[representations of C-star algebras]]:

+-- {: .un_defn}
###### Definition
Two endomorphisms $\rho_1, \rho_2$ are **unitarily equivalent** if there is a [[unitary operator]] $U \in \mathcal{A}$ such that $\rho_1 = ad(U) \rho_2 = U \rho_2 U^{-1}$. The endomorphisms $ad(U)$ with $U \in \mathcal{A}$ are called **inner automorphisms** (of $\mathcal{A}$).
An element $R \in \mathcal{A}$ such that $R \rho_1 = \rho_2 R$, not necessarily unitary, is called an **intertwiner** or **intertwining operator**.
=--

The DHR selection criterion selects representations that "look like the vaccum" on the causal complement of elements of our index set (in this case the double cones). The analog for endomorphims is this:

+-- {: .un_defn}
###### Definition
An endomorphim $\rho$ is **localized** or **localizable** if there is a bounded open set $\mathcal{O} \in \mathcal{J}$ such that $\rho$ is the identity on the algebra of the causal complement $\mathcal{A}(\mathcal{O}^{\perp})$. Such an endomorphism is **localized in $\mathcal{O}$**.
=--

We have to restrict the notion of "unitarily equivalent" to a "localized" version accordingly:

+-- {: .un_defn}
###### Definition
An element $A \in \mathcal{A}$ is a **local operator** if there is a double cone K such that $A \in \mathcal{M}(K)$. In particular, a local unitary operator $U$ is a **local unitary**, and two endomorphisms are **locally unitarily equivalent** if there is a unitary as in the definition of unitarily equivalent that is a local operator. 
=--

For an endomorphism $\rho$ let $\hat \rho$ be the equivalence class with respect to locally unitarily equivalence. Then we can define:


+-- {: .un_defn}
###### Definition
A localized endomorphism is **transportable** if for every bounded open set $\mathcal{O} \in \mathcal{J}$ there is a $\rho_0 \in \hat \rho$ that is localized in  $\mathcal{O}$.
=--

Transportable endomorphisms naturally form the objects of a category, the [[DHR category]].

## Properties ##

+-- {: .un_theorem}
###### Theorem

**transportable endomorphisms are compatible with the net structure**

Let $\rho$ be a transportable endomorphism that is localized in the double cone $K_0$, then for all double cones $K \supset K_0$, $\rho$ maps $\mathcal{M}(K)$ to itself.
=--


+-- {: .un_theorem}
###### Theorem

**intrinsic characterization of admissible representations**

A representation $\pi$ of $\mathcal{A}$ is admissible iff there is a transportable endomorphism $\rho$ such that $\pi$ is unitarily equivalent to $\pi_0 \circ \rho$.
=--

Reference: This is theorem 2.1.3 in the book by Baumg&#228;rtel.

+-- {: .un_theorem}
###### Theorem

**stability of admissible representations**

(i)  finite direct sums of admissible representations are admissible.

(ii) subrepresentations of admissible representations are admissible.
=--

For transportable endomorphisms we get even more:

+-- {: .un_theorem}
###### Theorem

**products**
The product, i.e. the concatenation, of transportable endomorphisms is a transportable endomorphism. 
=--


+-- {: .un_theorem}
###### Theorem

**product of causally disjoint localized endomorphisms is commutative**

Let $\rho_1, \rho_2$ be transportable endomorphisms localized in $K_1, K_2$ respectivley with $K_1 \perp K_2$, then $\rho_1 \rho_2 = \rho_2 \rho_1$.
=--

Note that the product of equivalenc classes is well defined, and $\hat \rho_1 \hat \rho_2 = \widehat{\rho_1\rho_2}$. Therefore the theorem above implies that the product of equivalence classes is commutative.

## References ##

see [[AQFT]] ff.

Of particular relevance (besides the original work of Doplicher and Roberts) are 

* Hellmut Baumg&#228;rtel: _Operator algebraic Methods in Quantum Field Theory. A series of lectures._ Akademie Verlag 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0839.46063&format=complete))

* Hans Halvorson, Michael M&#252;ger, _Algebraic Quantum Field Theory_ ([arXiv](http://arxiv.org/abs/math-ph/0602036))

[[!redirects DHR analysis]]
[[!redirects Doplicher-Haag-Roberts superselection theory]]
[[!redirects Doplicher-Haag-Roberts superselection sector]]
[[!redirects Doplicher-Haag-Roberts superselection sectors]]