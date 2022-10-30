
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _chain complex_ is a [[complex]] in an [[additive category]] (often assumed to be an [[abelian category]]).

The archetypical example, from which the name derives, is the [[singular chain complex]] $C_\bullet(X)$ of a [[topological space]] $X$.

Chain complexes are the basic objects of study in [[homological algebra]].

### Basic

A _chain complex_ $V_\bullet$ is a sequence $\{V_n\}_{n \in \mathbb{Z}}$ of [[abelian groups]] or [[modules]] (for instance [[vector spaces]]) or similar equipped with linear maps $\{d_n : V_{n+1} \to V_n\}$ such that $d^2 = 0$, i.e. the composite of two consecutive such maps is the [[zero morphism]] $d_n \circ d_{n+1} = 0$.

A basic example is the [[singular chain complex]] of a [[topological space]], or the [[de Rham complex]] of a [[smooth manifold]]. Another type of example occurs with the [[Dold-Kan correspondence]] as the [[Moore complex]] of a [[simplicial abelian group]] or similar. Both the first and the third of these types of example correspond, on the surface, to chain complexes in which the grading is by $\mathbb{N}$, not $\mathbb{Z}$.  Dually the [[de Rham complex]] example can be included by indexing by the non-positive integers,  but  by defining them to take trivial, that is zero, values in other dimensions they become chain complexes in the sense used here. The more general definition is important as it is (i) more inclusive and (ii) leads to objects that behave well with respect to shift / translation operators, (see below).

Chain complexes crucially come with their _[[chain homology]]_ [[groups]]. When regarding [[chain maps]] between them that induce [[isomorphisms]] on these groups ([[quasi-isomorphisms]]) as [[weak equivalences]], chain complexes form a useful presentation for aspects of [[stable homotopy theory]]. More on this aspect [below](#MeaningInHomotopyTheory).


### Meaning in homotopy theory
 {#MeaningInHomotopyTheory}

By the [[Dold-Kan correspondence]] there is an equivalence between the category of *[[connective chain complex|connective]] chain complexes of abelian groups* and the category of *abelian [[simplicial group|simplicial groups]]*. The functor

$$NCC:AB^\Delta^{op}\to Ch_\bullet^+(AB)$$

giving this equivalence is called [[Moore complex|normalized chain complex functor]] or [[Moore complex|Moore complex functor]].

In particular this reasoning shows that connective chain complexes of abelian groups are a model for abelian [[infinity-group|∞-groups]] (aka [[Kan complex|Kan complexes]] with abelian group structure).  This correspondence figures as part of the [[cosmic cube]]-classification scheme of [[n-category|n-categories]].


## Definition
 {#Definition}

### In components
 {#InComponents}

Let $\mathcal{C}$ be an [[abelian category]].

+-- {: .num_defn}
###### Definition

A ($\mathbb{Z}$-graded) **chain complex** in $\mathcal{C}$ is 

* a collection of [[objects]] $\{C_n\}_{n\in\mathbb{Z}}$, 

* and of [[morphisms]] $\partial_n : C_n \to C_{n-1}$

$$ 
  \cdots \overset{\partial_3}{\to} C_2 \overset{\partial_2}{\to} C_1 \overset{\partial_1}{\to} C_0 \overset{\partial_0}{\to} C_{-1} \overset{\partial_{-1}}{\to} \cdots
$$

such that 

$$
  \partial_n  \circ \partial_{n+1} = 0
$$ 

(the [[zero morphism]]) for all $n \in \mathbb{Z}$.  

=--

A [[homomorphism]] of chain complexes is a [[chain map]] (see there). Chain complexes with chain maps between them form the [[category of chain complexes]] $Ch_\bullet(\mathcal{C})$.

One uses the following  terminology for the components of a chain complex, all deriving from the example of a [[singular chain complex]]:

+-- {: .num_defn}
###### Definition

For $C_\bullet$ a chain complex

* the morphisms $\partial_n$ are called the **[[differentials]]** or **[[boundary]] maps**;

* the [[element in an abelian category|elements]] of $C_n$
  are called the **$n$-[[chains]]**;

* the elements in the [[kernel]] 

  $$
    Z_n \coloneqq ker(\partial_{n-1})
  $$

  of $\partial_{n-1} : C_n \to C_{n-1}$ are called the **$n$-[[cycles]]**;

* the elements in the [[image]] 

  $$
    B_n \coloneqq im(\partial_n)
  $$

  of $\partial_{n} : C_{n+1} \to C_{n}$ are called the **$n$-[[boundaries]]**;

Notice that due to $\partial \partial = 0$ we have canonical inclusions

$$
  0 \hookrightarrow B_n \hookrightarrow Z_n \hookrightarrow C_n
  \,.
$$

* the [[cokernel]] 

  $$
    H_n \coloneqq Z_n/B_n
  $$

  is called the degree-$n$ **[[chain homology]]** of $C_\bullet$.

$$
  0 \to B_n \to Z_n \to H_n \to 0
  \,.
$$


=--

The [[duality|dual]] notion:

+-- {: .num_defn}
###### Definition

A **[[cochain complex]]** in $\mathcal{C}$ is a chain complex in the [[opposite category]] $\mathcal{C}^{op}$. Hence a tower of objects and morphisms as above, but with each [[differential]] $d_n : V^n \to V^{n+1}$ increasing the degree.

=--

+-- {: .num_remark}
###### Remark

One also says **homologically graded** complex, for the case that the differentials lower degree, and _cohomologically graded_ complex for the case where they raise degree.

=--

+-- {: .num_remark}
###### Remark

Frequently one also considers $\mathbb{N}$-graded (or _nonnegatively graded_) chain complexes (for instance in the [[Dold-Kan correspondence]]), which can be identified with $\mathbb{Z}$-graded ones for which $V_n=0$ when $n\lt 0$.  Similarly, an $\mathbb{N}$-graded _cochain_ complex is a cochain complex for which $V_n=0$ when $n\lt 0$, or equivalently a chain complex for which $V_n=0$ when $n\gt 0$.

=--



### In terms of translations

Note that in particular, a chain complex is a [[graded object]] with extra structure.  This extra structure can be codified as a map of graded objects $\partial:V\to T V$, where $T$ is the 'shift' endofunctor of the category $Gr(V)$ of graded objects in $C$, such that $T(\partial) \circ \partial = 0$.  More generally, in any pre-additive category $G$ [[category with translation|with translation]] $T : G \to G$, we can define a **chain complex** to be a [[differential object]] $\partial_V : V \to T V$ such that $V \stackrel{\partial_V}{\to} T V \stackrel{T(\partial_V)}{\to} T T V$ is the [[zero morphism]].  When $G= Gr(C)$ this recovers the original definition.

## Examples
 {#Examples}

Common choices for the ambient [[abelian category]] $\mathcal{C}$ include [[Ab]], $k$[[Vect]] (for $k$ a [[field]]) and generally $R$[[Mod]] (for $R$ a [[ring]]), in which case we obtain the familiar definition of an (unbounded) chain complex of [[abelian groups]], [[vector spaces]] and, generally, of  [[modules]].


### In $k$-vector spaces

In $C =$ [[Vect]]$_k$ a chain complex is also called a [[differential graded vector space]], consistent with other terminology such as [[differential graded algebra]] over $k$.  This is also a special case in other ways: every chain complex over a field is [[formal dg-algebra|formal]]: [[quasi-isomorphism|quasi-isomorphic]] to its [[homology]] (the latter considered as a chain complex with zero differentials).  Nothing of the sort is true for chain complexes in more general categories.

The [[category of chain complexes]] of vector spaces carries the [[tensor product of chain complexes]] and a [[braiding]] which makes it a [[symmetric monoidal category]]. The corresponding [[commutative monoids]] are the [[differential graded-commutative algebras]].

### In super vector spaces 

A chain complex in [[super vector spaces]] is a [[chain complex in super vector spaces]]. The category of these carries a [[symmetric monoidal category]]-[[structure]] and the corresponging [[commutative monoids]] are the [[differential graded-commutative superalgebras]].

### In chain complexes

A chain complex in a category of chain complexes is a [[double complex]].


### Singular and cellular chain complex

For $X$ a [[topological space]], there is its [[singular simplicial complex]].

More generally, for $S$ a [[simplicial set]], there is the chain complex
$S \cdot R$ of $R$ [[chains on a simplicial set]].

### Of a simplicial abelian group

For $A_\bullet$ a [[simplicial abelian group]], there is a chain complex $C_\bullet(A)$, the [[alternating face map complex]], and a chain complex $N_\bullet(A)$, the [[normalized chain complex]] of $A$.

The [[Dold-Kan correspondence]] says that this construction establishes an [[equivalence of categories]] between non-negatively-graded chain complexes and [[simplicial abelian groups]].

## Properties

### Model structure 

There is a [[model category]] structure on the category $Ch(A)$ of chain complexes in an [[abelian category]]. Its [[homotopy category]] is the [[derived category]] of $A$.

See [[model structure on chain complexes]].

## Related concepts

[[!include chains and cochains - table]]


* [[category of chain complexes]]

  * **chain complex**, [[connective chain complex]], [[bounded chain complex]]

  * [[chain map]], [[quasi-isomorphism]]

  * [[chain homotopy]]

  * [[model structure on chain complexes]]

  * [[elliptic chain complex]]

* [[cochain complex]]

* [[filtered chain complex]]

* [[perfect chain complex]]

* [[homological algebra]]

* [[rational stable homotopy theory]]

## References


* [[Charles Weibel]], section 1.1 _[[An Introduction to Homological Algebra]]_.

* [[Masaki Kashiwara]], [[Pierre Schapira]], section 11 of _[[Categories and Sheaves]]_,

* [[Urs Schreiber]], [chapter II](https://ncatlab.org/schreiber/show/Introduction+to+Homological+algebra#ChapterOnChainComplexes) of  _[[schreiber:HAI|Introduction to Homological Algebra]]_



  

[[!redirects chain complexes]]
