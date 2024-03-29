
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea



The _&#233;tale (∞,1)-site_ is an [[(∞,1)-site]] whose [[(∞,1)-topos]] encodes the [[derived geometry]] version of the geometry encoded by the [[topos]] over the [[étale site]].


Its underlying [[(∞,1)-category]] is the [[opposite (∞,1)-category]] $sCAlg_k^{op}$ of commutative [[simplicial algebras]] over a commutative ring $k$, whose [[covering]] families are essentially those which under [[decategorification]] become coverings in the [[étale site]] of ordinary $k$-algebras.

## Definition  

Let $k$ be a commutative ring. Let $T$ be the [[Lawvere theory]] of commutative [[associative algebra]]s over $k$. 

+-- {: .num_defn}
###### Definition

Let 

$$
  \infty CAlg_k := T Alg_\infty
$$

be the [[(∞,1)-category]] of [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]] over $T$ regarded as an [[(∞,1)-algebraic theory]].

=--

+-- {: .num_prop}
###### Proposition

Let $sCAlg_k = (T Alg)^{\Delta^{op}}$ be the [[sSet]]-[[enriched category]] of [[simplicial algebra|simplicial commutative associative k-algebras]] equipped with the standard [[model structure on simplicial T-algebras]]. Write $sCAlg_k^\circ$ for the $(\infty,1)$-category [[presentable (∞,1)-category]]. Then we have an [[equivalence of (∞,1)-categories]]

$$
  \infty CAlg_k \simeq (sCAlg_k)^\circ
  \,.
$$ 

=--

This is a special case of the general statement discussed at [[(∞,1)-algebraic theory]]. See also ([Lurie, remark 4.1.2](#Lurie)).

+-- {: .num_defn}
###### Notation


For $X \in \infty CAlg_k^{op}$ we write $\mathcal{O}(X)$ for the corresponding object in $\infty CAlg_k$ and conversely for $A \in \infty CAlg_k$ we write $Spec A$ for the corresponding object in $\infty CAlg_k^{op}$.

So $Spec \mathcal{O} X = X$ and $\mathcal{O} Spec A = A$, by definition of notation.

=--

Notice from  the discussion at [[model structure on simplicial algebras]] the [[homotopy group]] functor

$$
  \pi_* : sCAlg_k \to CAlg_k
  \,.
$$


+-- {: .num_defn}
###### Definition

A morphism $Spec A  \to Spec B$ in $\infty CAlg_k^{op}$ is an **&#233;tale morphism** if

1. The underlying morphism $Spec \pi_0(A) \to Spec \pi_0(B)$ is an [[étale morphism]] of [[schemes]];

1. for each $i \in \mathbb{N}$ the canonical morphism

   $$
     \pi_i(A) \otimes_{\pi_0(A)} \pi_0(B) \to \pi_i(B)
   $$

   is an [[isomorphism]].   

=--

+-- {: .num_defn}
###### Definition

The **&#233;tale $(\infty,1)$-site** is the [[(∞,1)-site]] whose underlying $(\infty,1)$-category is the [[opposite (∞,1)-category]] $\infty CAlg_k^{op}$ and whose [[covering]] famlies $\{Spec A_i \to Spec B\}_{i \in I}$ are those collections of morphisms such that

1. every $Spec A_i \to Spec B$ is an &#233;tale morphism

2. there is a [[finite set|finite subset]] $J \subset I$  such that the underlying decategorified family $\{Spec \pi_0(A_j) \to Spec \pi_0(B)\}_{j \in J}$ is a covering family in the 1-[[étale site]].

=--

This appears as ([To&#235;nVezzosi, def. 2.2.2.12](#ToenVezzosi)) and as ([Lurie, def. 4.3.3; def. 4.3.13](#Lurie)).

## Properties

### Derived &#233;tale geometry {#AsDerivedGeometry}

The following definition and theorem show how the &#233;tale $(\infty,1)$-site arises naturally from the [[étale site|étale 1-site]], and naturally encodes the [[derived geometry]] induced by the &#233;tale site.

+-- {: .num_defn}
###### Definition
**(&#233;tale pregeometry)**

Let $\mathcal{T}_{et}$ be the 1-[[étale site]] regarded as a [[pregeometry (for structured (∞,1)-toposes)]] as follows.

* the underlying [[(∞,1)-category]] is the 1-[[category]] 

  $$
    (CAlg_k^{sm})^{op} \hookrightarrow CAlg_k ^{op}
    \,,
  $$ 
  
  which is the full [[subcategory]] of $CAlg_k$ on those objects $A \in CAlg_k$ for which there exists an [[étale morphism]] $k[x^1, \cdots, x^n] \to A$ from the [[polynomial]] algebra in $n$ generators for some $n \in \mathbb{N}$;

* the _admissible morphisms_ in the pregeometry are the [[étale morphism]]s;

* a collection of admissible morphisms is a [[covering]] family if it is so as a family of morphisms in the [[étale site]].
 
=--

This is ([Lurie, def. 4.3.1](#Lurie)).

+-- {: .num_defn}
###### Definition
**(&#233;tale geometry)**

Let $\mathcal{G}_{et}$ be the [[geometry (for structured (∞,1)-toposes)]] given by

* the underlying [[(∞,1)-site]] is the &#233;tale $(\infty,1)$-site;

* the admissible morphisms are the &#233;tale morphisms.


=--

This is ([Lurie, def. 4.3.13](#Lurie)).


+-- {: .num_theorem}
###### Theorem

The [[geometry (for structured (∞,1)-toposes)|geometry]] generated by the &#233;tale pregeometry $\mathcal{T}_{et}$ is the &#233;tale geometry $\mathcal{G}_{et}$.

=--

This is ([Lurie, prop. 4.3.15](#Lurie)).


## Related concepts

* [[étale morphism]], [[étale site]], [[étale cohomology]]

* [[étale morphism of E-∞ rings]]

* **&#233;tale $(\infty,1)$-site**

## References

In its [[presentable (∞,1)-category|presentation]] as a [[model site]] the &#233;tale $(\infty,1)$-site is given in definition 2.2.2.12 of

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))
{#ToenVezzosi}.

A discussion in the context of [[structured (∞,1)-toposes]] is 

* [[Jacob Lurie]], section 4.3 of _[[Structured Spaces]]_
{#Lurie}

* [[Jacob Lurie]], section 3 and 4 of, _Descent theorems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XI.pdf))


See also

* [[Benjamin Antieau]], [[David Gepner]], _Brauer groups and &#233;tale cohomology in derived algebraic geometry_ ([arXiv:1210.0290](http://arxiv.org/abs/1210.0290))
 {#AntieauGepner12}


[[!redirects étale (∞,1)-site]]
[[!redirects etale (∞,1)-site]]

[[!redirects etale (infinity,1)-site]]