
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _globular theory_ is much like an _[[algebraic theory]]_ / _[[Lawvere theory]]_ only that where the former has [[objects]] labeled by [[natural numbers]], a globular theory has objects labeled by [[pasting diagrams]] of [[globes]]. The [[models]] of "homogeneous" globular theories are precisely the algebras over [[globular operads]].

## Definition


+-- {: .num_defn #CategoryOfGlobularSite}
###### Definition

Write

* $Str \omega Cat \in Cat$ for the category of [[strict ∞-categories]];

* $\Theta \hookrightarrow Str\omega Cat$ for the the **[[Theta category]]**, the [[full subcategory]] on the strict $\omega$-categories [[free construction|free]] on [[∞-graphs]]([[globular sets]]) (the [[pasting diagrams]]);

* $i \colon \Theta_0 \to \Theta$ for the [[wide subcategory|wide]] non-full subcategory on the morphism induced from morphisms of the underlying [[∞-graphs]]  (this means that these morphisms in $\Theta_0$ send $n$-globes to single $n$-globes, not to pastings of them).

* $\mathbb{G} \hookrightarrow \Theta_0$ for the [[full subcategory]] on the pasting diagrams given by a single globe -- the **[[globe category]]**.

=--

+-- {: .num_defn #GlobularSite}
###### Definition

The **globular site** is the category $\Theta_0$ from def. \ref{CategoryOfGlobularSite} equipped with the structure of a [[site]] by taking the [[covering]] families to be the jointly [[epimorphism|epimorphic]] families.

=--


+-- {: .num_defn #GlobularTheory}
###### Definition

A **globular theory** (or rather its [[syntactic category]]) is a [[wide subcategory]] inclusion

$$
  i_A \colon \Theta_0 \to \Theta_A
$$

of the globular site, def. \ref{GlobularSite}, such that every [[representable functor]] $\Theta_A(-,T) \colon \Theta_A^{op} \to $ [[Set]] is a $\Theta_A$-model: 

A **$\Theta_A$-[[model]]** is a [[presheaf]] $X \in PSh(\Theta_A)$ which
restricts to a [[sheaf]] on the globular site, $i_A^* X \in Sh(\Theta_0) \hookrightarrow PSh(\Theta_0)$.

Write

$$
  Mod_A \hookrightarrow PSh(\Theta_A)
$$

for the [[full subcategory]] of the [[category of presheaves]] on the $\Theta_A$-models. This is the category of $\Theta_A$-models.

=--

([Berger, def. 1.5](#Berger))

+-- {: .num_defn #CoversAndImmersions}
###### Definition

Given an globular theory $i_A \colon \Theta_0 \to \Theta_A$ a morphism in $\Theta_A$ is 

* an **$A$-cover** if...;

* an **immersion** if...

=--

+-- {: .num_defn #HomogeneousTheory}
###### Definition

A globular theory $i_A \colon \Theta_0 \to \Theta_A$ is **homogeneous** if it contains a [[subcategory]] $\Theta^{cov}_A \to \Theta_A$ of $A$-covers, def. \ref{CoversAndImmersions} such that every morphism in $\Theta_A$ factors uniquely as an $A$-cover, def. \ref{CoversAndImmersions}, followed by an immersion, def. \ref{CoversAndImmersions}.

=--

([Berger, def. 1.15](#Berger))

## Properties

### Relation to $\omega$-graphs

+-- {: .num_prop}
###### Proposition

The [[category of sheaves]] over the globular site 
is [[equivalence of categories|equivalent]] to the category of [[∞-graphs]] 

$$
  \omega Graph \simeq Sh(\Theta_0)
  \,.
$$

=--

([Berger, lemma 1.6](#Berger))

### Relation to globular operads

The ([[syntactic categories]] of) homogenous globular theories, def. \ref{HomogeneousTheory} are the [[categories of operators]] of [[globular operads]]: 


+-- {: .num_prop}
###### Proposition

A [[faithful functor|faithful]] [[monad]] $\underline{A}$ on [[∞-graphs]] encodes algebras over a [[globular operad]] $A$ precisely if 

1. the induced globular theory $\Theta_A \hookrightarrow Alg_{\underline{A}}$ is homogeneous, def. \ref{HomogeneousTheory};

1. every $\underline{A}$-[[algebra over a monad|algebras]] factors uniquely into an $A$-cover followed by an $\underline{A}$-free $\underline{A}$-algebra morphism.

=--

([Berger, prop. 1.16](#Berger))

## Examples

### The theory of $\omega$-categories

The [[Theta category]] itself, equipped with the definition inclusion $i \colon \Theta_0 \to \Theta$, def. \ref{CategoryOfGlobularSite}, is the globular theory of [[∞-categories]].

In particular:

+-- {: .num_prop }
###### Proposition

The category $Str\omega Cat$ of [[strict ∞-categories]] is [[equivalence of categories|equivalent]] to that of $\Theta$-models, def. \ref{GlobularTheory}. Hence it is the [[full subcategory]] of that of [[∞-graphs]] which satisfy the [[Segal condition]] with respect to the canonical inclusion $\Theta_0 \to Theta$: we have a [[pullback]]

$$
  \array{
    Str\omega Cat 
     &\underoverset{\simeq}{N}{\to}& Mod_\Theta &\hookrightarrow&      
PSh(\Theta)
    \\
    \downarrow^{\mathrlap{U}} && \downarrow^{} && \downarrow
   \\
   \omega Graph &\stackrel{\simeq}{\to}& Sh(\Theta_0) &\hookrightarrow& PSh(\Theta_0)
  }
  \,.
$$


=--

([Berger, theorem 1.12](#Berger))


## References

Section 1 of

* [[Clemens Berger]], _A cellular nerve for higher categories_, Advances in Mathematics 169, 118-175 (2002) ([pdf](http://math1.unice.fr/~cberger/nerve.pdf))
 {#Berger}

[[!redirects globular theories]]

[[!redirects globular site]]
[[!redirects cellular site]]
