
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[(∞,1)-category]]_ may be formulated [[internalization|internal]] to any other $(\infty,1)$-category with sufficient propoerties (with a rich enough [[internal logic]]). This generalizes the notion of _[[internal category]]_ from [[category theory]] to [[(∞,1)-category theory]].

## Idea 

Let $\mathcal{C}$ be an [[(∞,1)-category]].

A general abstract way of defining an $(\infty,1)$-category $A$ _internal to_ $\mathcal{C}$ -- also called a _$(\infty,1)$-category object_ in $\mathcal{C}$ is to say that this is a [[simplicial object]] $A : \Delta^{op} \to \mathcal{C}$. The condition that the object $A_k$ in degree $k \in \mathbb{N}$ is to be thought of as the _object of sequences of composable morphisms of length $k$_ of $A$ is formalized by asking the canonical morphisms $A_k \to A_1 \times_{A_0} \cdots \times_{A_0} A_1$ (into the iterated [[(∞,1)-pullback]] over the [[source]] and [[target]] maps) to be an [[equivalence in an (∞,1)-category|equivalence in]] $\mathcal{C}$. In fact, this is literally just the definition of an [[internal category]] but interpreted in the [[internal logic]] of the $(\infty,1)$-category $\mathcal{C}$. Accordingly one may just as well equivalently speak just of a category object_ in $\mathcal{C}$.

Indeed, the obvious strengthening of this definition to enforce invertibility of [[morphisms]] yields the notion of [[groupoid object in an (∞,1)-category]], which could also be called an _[[internal ∞-groupoid]]_.

Therefore, a further condition is necessary to ensure that the notion of [[homotopy]] in $\mathcal{C}$ is compatible with that in $A$ (this is caled the "completeness condition", see [below](#Completeness)).

A general abstract [[(∞,1)-category theory|(∞,1)-category theoretic]] way of formalizing this is given in [Lurie, sections 1.1, 1.2](#Lurie). For historical reasons, the notion of _internal $(\infty,1)$-category_ there goes by the name _complete Segal space object_, in honor of the notion of a _[[complete Segal space]]_, which may be thought of as perceiving an ordinary [[(∞,1)-category]] as an internal $(\infty,1)$-category in $\mathcal{C} = $ [[∞Grpd]].

There are a variety of [[model category]] structures that [[presentable (infinity,1)-category|present]] the $(\infty,1)$-category of all internal $(\infty,1)$-categories in a suitable $\mathcal{C}$, which typically go as models for _complete Segal space objects_. The soundness of these models is discussed in [Lurie, section 1.5](#Lurie).


## Definition

### Category object
  {#CategoryObject}

(...)

### Nice ambient contexts
 {#SuitableAmbientContexts}

We introduce some conditions on an ambient $(\infty,1)$-category $\mathcal{C}$
such that it admits a "very good" theory of internal $(\infty,1)$-category objects.


The following definition is the specialization of the notion termed _absolute distributor_ in [Lurie, def. 1.2.1, 1.3.3](#Lurie) to [[(∞,1)-toposes]].

+-- {: .num_defn #WellSuitedTopos}
###### Definition

Call an [[(∞,1)-topos]] $\mathbf{H}$ **very well-suited for internalization** if 
it is [[locally ∞-connected (∞,1)-topos|locally]] and [[∞-connected (∞,1)-topos|globally ∞-connected]],

=--

+-- {: .num_remark}
###### Remark

Spelled out, this definition says the following.

The first condition says that the [[global section]] [[geometric morphism]] $(Disc \dashv \Gamma)$ admits an extra [[left adjoint]] $\Pi$

$$
  (\Pi \dashv \Disc \dashv \Gamma)
  :
  \mathbf{H}
   \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}
   \infty Grpd
$$

and that the [[inverse image]] $Disc$ is [[full and faithful]]. The corresponding [[full sub-(∞,1)-category]] is called that of _[[discrete objects]]_.


=--

+-- {: .num_remark}
###### Remark

In the terminology of ([Lurie](#Lurie)) this is indeed equivalent to $Disc : \infty Grpd \to \mathbf{H}$ being an "absolute distributor". The formulation there corresponds to the formulation here as follows.

Item 1) and 3) of ([Lurie, def. 1.2.1](#Lurie)) are automatically satisfied by assumption that $\mathbf{H}$ is an [[(∞,1)-topos]]. With this, item 2) of ([Lurie, def. 1.2.1](#Lurie)) and item 1) of ([Lurie, def. 1.3.3](#Lurie)) precisely encode [[locally ∞-connected (∞,1)-topos|local]] and global [[∞-connected (∞,1)-topos|∞-connectedness]] (notice that by the [[adjoint (∞,1)-functor theorem]] for [[presentable (∞,1)-categories]] the condition that $Disc$ preserves [[(∞,1)-limits]] is equivalent to it having the further [[left adjoint]] $\Pi$).

Finally notice that the version of item 4) of ([Lurie, def. 1.2.1](#Lurie)) available at time of this writing has a typo: it is indeed $\mathbf{H}^{op} \to CAT_{(\infty,1)}$ that is supposed to preserve $\infty$-limits, not $\mathbf{H} \to CAT_{(\infty,1)}^{op}$. This is clear from comparing with the proof of the next statement there, which is ([Lurie, prop. 1.2.4](#Lurie)).

So this condition is that the [[(∞,1)-functor]] 

$$
  \chi_{cod} : \infty Grpd^{op} \to CAT_{(\infty,1)}
$$ 

to the [[universe enlargement|very large]] [[(∞,1)-category of (∞,1)-categories]] which 
[[(∞,1)-Grothendieck construction|classifies]] the [[codomain fibration]] $cod : \mathbf{H}^I \to \mathbf{H}$ 
restricted along $Disc$ to the [[discrete objects]], hence assigning to an [[∞-groupoid]] $S$ the [[over-(∞,1)-topos]]

$$
  \chi : S \mapsto \mathbf{H}_{/Disc(S)},
$$

satisfies [[descent]] with respect to the [[canonical topology]], hence that it preserves [[(∞,1)-limits]] (sends [[(∞,1)-colimits]] in [[∞Grpd]] to [[(∞,1)-limits]] in $\mathbf{H}$).

But over an [[(∞,1)-topos]] the [[codomain fibration]] is always a [[canonical topology|canonical]] [[(∞,2)-sheaf]] (see there).

=--



### Completeness
  {#Completeness}

(...)

## Properties

### Model category presentations


+-- {: .num_prop }
###### Proposition

Let $C$ be a [[left proper model category|left proper]] [[combinatorial model category]] such that the [[(∞,1)-category]] that it [[presentable (∞,1)-category|presents]] is _well-suited for internalization_ in the sense discussed [above](#SuitableAmbientContexts).

Then then category $[\Delta^{op}, C]$ of [[simplicial objects]] in $C$ admits a [[left proper model category|left proper]] [[combinagtorial model category]] structure characterized by the following properties:

1. it is a [[Bousfield localization of model categories|left Bousfield localization]] of the injective [[model structure on functors]] $[\Delta^{op}, C]_{inj}$;

1. an obect $\Delta^{op} \to C$ is [[fibrant object|fibrant]] precisely if it is fibrant in $[\Delta^{op}, C]_{inj}$ and if the corresponding simplicial object $\Delta^{op}\to C^\circ$ in the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ is a complete Segal object in the sense discussed [above](#Completeness).

Moreover, the $(\infty,1)$-category [[presentable (∞,1)-category|presented]] by this is again _well suited for internalization_.

=--

This is ([Lurie, prop. 1.5.4](#Lurie)).


## Examples

### $(\infty,n)$-category

Let $\mathcal{C} := Cat_{(\infty,1]}$ be the [[(∞,1)-category of (∞,1)-categories]]. Then the $(\infty,1)$-category $Cat_{(\infty,1)}(\mathcal{C})$ of $(\infty,1)$-category objects in $\mathcal{C}$ is, up to [[equivalence of (∞,1)-categories|equivalence]], the $(\infty,1)$-category of [[(∞,2)-categories]]

$$
  Cat_{(\infty,1)}(Cat_{(\infty,1)})
  \simeq
  Cat_{(\infty,2)}
  \,.
$$

This yields an inductive construction of [[(∞,n)Cat]], the [[(∞,1)-category]] of [[(∞,n)-categories]]

$$
  Cat_{(\infty,1)}(Cat_{(\infty,1)}(\cdots (Cat_{(\infty,1)})))
  \simeq
  Cat_{(\infty,n)}
  \,.
$$

The corresponding model is that of _[[n-fold complete Segal space]]_.

## References

A general abstract formulation is in 

* [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie calculus_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 {#Lurie}

The model given by complete Segal space objects is due to

* [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_. Transactions of the American Mathematical Society 35 (2001), no. 3, 973-1007

and has since seen a multitude of further developments.

Influential but unpublished discussion of [[higher Segal spaces]] is due to [[Clark Barwick]].

[[!redirects internal (∞,1)-category]]
[[!redirects (infinity,1)-category object]]
[[!redirects (∞,1)-category object]]

[[!redirects internal (infinity,1)-categories]]
[[!redirects internal (∞,1)-categories]]
[[!redirects (infinity,1)-category objects]]
[[!redirects (∞,1)-category objects]]

[[!redirects complete Segal space object]]
[[!redirects complete Segal space objects]]
