
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
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

Let $k$ be a commutative ring. Let $\infty CAlg_k := (sCAlg_k)^\circ$ be the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial T-algebras|model structure on simplicial commutative associativ k-algebras]].

Recall from the discussion there the [[homotopy group]] functor

$$
  \pi_* : sCAlg_k \to CAlg_k
  \,.
$$

For $X \in \infty CAlg_k^{op}$ we write $\mathcal{O}(X)$ for the corresponding object in $\infty CAlg_k$.

+-- {: .un_defn}
###### Definition

A morphism $Spec A  \to Spec B$ in $sCAlg_k^{op}$ is an [[étale morphism]] if

1. The underlying morphism $Spec \pi_0(A) \to Spec \pi_0(B)$ is an [[étale morphism]] of [[scheme]]s;

1. for each $i \in \mathbb{N}$ the canonical morphism

   $$
     \pi_i(A) \otimes_{\pi_0(A)} \pi_0(B) \to \pi_i(B)
   $$

   is an [[isomorphism]].   

=--

+-- {: .un_defn}
###### Definition

The **&#233;tale $(\infty,1)$-site** is the [[(∞,1)-site]] whose underlying $(\infty,1)$-category is the [[opposite (∞,1)-category]] $\infty CAlg_k$ and whose [[covering]] famlies $\{Spec A_i \to Spec B\}$ are those collections of morphisms such that

1. every $Spec A_i \to Spec B$ is an &#233;tale morphism

2. the underlying decategorified family $\{Spec \pi_0(A_i) \to Spec \pi_0(B)\}$ is a covering family in the 1-[[étale site]].

=--

This appears as ([To&#235;nVezzosi, def. 2.2.2.12](#ToenVezzosi)) and as ([Lurie, def. 4.3.3; def. 4.3.13](#Lurie)).

## Related concepts

* [[étale morphism]], [[étale site]], [[étale cohomology]]

* **&#233;tale $(\infty,1)$-site**

## References

In its [[presentable (∞,1)-category|presentation]] as a [[model site]] the &#233;tale $(\infty,1)$-site is given in definition 2.2.2.12 of

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))
{#ToenVezzosi}.

A discussion in the context of [[structured (∞,1)-topos]]es is in section 4.3 of

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#Lurie}

[[!redirects étale (∞,1)-site]]
[[!redirects etale (∞,1)-site]]

[[!redirects etale (infinity,1)-site]]