
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# The specialisation order
* table of contents
{: toc}

## Idea

The __specialisation order__ is a way of turning any [[topological space]] $X$ into a [[preorder]]ed set (with the same underlying set).

## Definition

+-- {: .un_defn}
###### Definition 
Given a topological space $X$ with topology $\mathcal{O}(X)$, the specialization order $\leq$ is defined by either of the following two equivalent conditions: 

1. $x \leq y$ if and only if $x$ belongs to the [[topological closure]] of $\{y\}$; we say that $x$ is a __specialisation__ of $y$. 

1. $x \leq y$ if and only if $\forall_{U \colon \mathcal{O}(X)} (x \in U) \Rightarrow (y \in U).$

(Note: some authors use the opposite ordering convention.) 
=-- 

### In dependent type theory

In [[dependent type theory]], given a type $X$, the type of [[subtypes]] of $X$ is the [[function type]] $X \to \Omega$, where $\Omega$ is the [[type of all propositions]] with the type reflector type family $P:\Omega \vdash \mathrm{El}_\Omega(P) \; \mathrm{type}$. 

A [[topological space]] is a type $X$ with a type of subtypes $O(X)$ with canonical [[embedding]] $i_O:O(X) \hookrightarrow (X \to \Omega)$, called the open sets of $X$, which are closed under finite intersections and arbitrary unions. 

Given a topological space $(X, O(X))$, we define the [[relation]] 

$$x:X, U:O(X) \vdash x \in U \; \mathrm{type}$$ 

by 

$$x \in U \coloneqq \mathrm{El}_\Omega((i_O(U))(x))$$

By definition of the type of all propositions and its type reflector, $x \in U$ is always a [[h-proposition]] for all $x:X$ and $U:O(X)$. 

The **specialization order** is given by the type 

$$x \leq y \coloneqq \prod_{U:O(X)} (x \in U) \to (y \in U)$$

In plain English, $x \leq y$ whenever for all open sets $U$ in $O(X)$, if $x$ is in $U$, then $y$ is in $U$. 

## Properties

\begin{theorem}
The specialization order is always a [[preorder]]. 
\end{theorem}

\begin{proof}
We work in [[dependent type theory]]. Let $(X, O(X))$ be a [[topological space]]. The specialization order is given by the type 

$$\prod_{U:O(X)} (x \in U) \to (y \in U)$$

Since $x \in U$ and $y \in U$ are both [[h-propositions]], and h-propositions are closed under [[function types]] and [[dependent product types]], the specialization order is also valued in [[h-propositions]]. In addition, for all elements $x:X$, there is an element

$$\mathrm{refl}_{SpecOrd}(x):\prod_{U:O(X)} (x \in U) \to (x \in U)$$

defined by the [[identity function]] on $x \in U$

$$\mathrm{refl}_{SpecOrd}(x)(U) \coloneqq \mathrm{id}_{x \in U}$$

and for all elements $x:X$, $y:X$, and $z:X$, there is a function 

$$\mathrm{trans}_{SpecOrd}(x, y, z):\left(\prod_{U:O(X)} (x \in U) \to (y \in U)\right) \times \left(\prod_{U:O(X)} (y \in U) \to (z \in U)\right) \to \left(\prod_{U:O(X)} (x \in U) \to (z \in U)\right)$$

defined by [[composition]] of the functions $f(U):(x \in U) \to (y \in U)$ and $g(U):(y \in U) \to (z \in U)$ dependent upon open set $U:O(X)$:

$$\mathrm{trans}_{SpecOrd}(x, y, z)(f, g)(U) \coloneqq g(U) \circ f(U)$$

Since the type 

$$\prod_{U:O(X)} (x \in U) \to (y \in U)$$

is a [[relation]] valued in [[h-propositions]] which satisfies [[reflexivity]] and [[transitivity]], it is a [[preorder]]. 
\end{proof}

$X$ is $T_0$ if and only if its specialisation order is a [[partial order]].  $X$ is $T_1$ iff its specialisation order is [[equality]].  $X$ is $R_0$ (like $T_1$ but without $T_0$) iff its specialisation order is an [[equivalence relation]].  (See [[separation axioms]].)

Given a [[continuous map]] $f: X \to Y$ between topological spaces, it is order-preserving relative to the specialisation order.  Thus, we have a [[faithful functor]] $Spec$ from the category of $\Top$ of topological spaces to the category $\ProSet$ of preordered sets.

In the other direction, to each proset $X$ we may associate a topological space whose elements are those of $X$, and whose open sets are precisely the upward-closed sets with respect to the preorder. This topology is called the [[specialization topology]]. This defines a functor 

$$i \colon ProSet \to Top$$ 

which is a full embedding; the [[essential image]] of this functor is the category of [[Alexandroff spaces]] (spaces in which an arbitrary intersection of open sets is open). Hence the category of prosets is equivalent to the category of Alexandroff spaces. 

In fact, we have an adjunction $i \dashv Spec$, making $ProSet$ a [[coreflective subcategory]] of $Top$. In particular, the counit evaluated at a space $X$, 

$$i(Spec(X)) \to X,$$ 

is the identity function at the level of sets, and is continuous because any open $U$ of $X$ is upward-closed with respect to $\leq$, according to the second equivalent condition of the definition of the specialization order. 

This [[adjunction]] restricts to an [[adjoint equivalence]] between the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and finite topological spaces. The unit and counit are both identity functions at the level of sets, so we in fact have an equivalence between these categories as [[concrete categories]]. 

## Related entries

* [[finite topological space]]

* [[separation axioms in terms of lifting properties]]

* [[specialization topology]]

[[!redirects specialization orders]]

[[!redirects specialisation order]]
[[!redirects specialisation orders]]

[[!redirects specialization ordering]]
[[!redirects specialization orderings]]

[[!redirects specialisation ordering]]
[[!redirects specialisation orderings]]

[[!redirects specialization preorder]]
[[!redirects specialization preorders]]

[[!redirects specialisation preorder]]
[[!redirects specialisation preorders]]


