
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

$Pr(\infty,1)Cat$ is the [[(∞,1)-category]] of [[locally presentable (∞,1)-categories]] and [[(∞,1)-colimit]]-preserving [[(∞,1)-functors]] between them ([[Lawvere distributions]]).


Recall that a [[presentable (∞,1)-category]] is a [[localization of an (∞,1)-category|localization]] of a [[(∞,1)-category of (∞,1)-presheaves]]. In particular it has all small [[colimits]]. An [[(∞,1)-functor]] $C \times D \to E$ from the cartesian [[product]] of two presentable $(\infty,1)$-categories is _bilinear_ if it respects colimits in both variables.


It turns out that there is a _universal_ such bilinear functor

$$
  C \times D \to C \otimes D
  \,,
$$

which thereby defines a [[tensor product of presentable (∞,1)-categories]]. This defines a [[monoidal (infinity,1)-category|monoidal structure]] on presentable $(\infty,1)$-categories, which is in fact [[symmetric monoidal (infinity,1)-category|symmetric]]. 

The collection $Pr(\infty,1)Cat$ of presentable $(\infty,1)$-cateories with colimit-preserving [[(∞,1)-functors]] between them (i.e. with "*linear*" functors between them!), is an $(\infty,1)$-generalization of the category $Set Mod$ of ordinary categories and [[bimodules]] or [[profunctors]], or [[distributors]] between them. See [[distributor]] and in particular the discussion there about the equivalent reformulation in terms of colimit-preserving functors.

Using $Pr(\infty,1)Cat$ with its notion of "linearity" one obtains a very general notion of $\infty$-linear algebra. This is described at [[geometric ∞-function theory]].

## Definition

### Unstable version

Write $Pr(\infty,1)Cat_1$ for the [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-categories]] whose

* objects are [[presentable (∞,1)-category|presentable (∞,1)-categories]];

* morphisms are [[(∞,1)-colimit]]-preserving [[(∞,1)-functors]].


### Stable version

The symmetric monoidal structure on presentable $(\infty,1)$-categories restricts to one on presentable [[stable (∞,1)-category|stable (∞,1)-categories]].

The tensor unit of stable presentable $(\infty,1)$-categories is the [[stable (∞,1)-category of spectra]].


## Properties

### Adjoint functor theorem

A functor between locally presentable $(\infty,1)$-categories:

* is a [[left adjoint]] if and only if it preserves small colimits (hence, in particular, is accessible), and
* is a [[right adjoint]] if and only if it preserves small limits and is accessible.

### Hom-objects

+-- {: .num_defn}
###### Definition

For $C, D \in Pr(\infty,1)Cat$, let 

$$
  Func^L(C,D) \subset Func(C,D)
$$

be the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that preserve all small [[(∞,1)-colimits]] (equivalently, are left adjoints).

=--

Evidently $Func^L(C,D)$ would be the hom-$(\infty,1)$-category of an enhancement of $Pr(\infty,1)Cat$ to an $(\infty,2)$-category; its maximal sub-$\infty$-groupoid is the hom-$\infty$-groupoid $Pr(\infty,1)Cat(C,D)$.

+-- {: .num_prop}
###### Proposition

For all $C,D$ we have that $Func^L(C,D)$ is itself locally presentable.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.3.8]].

### Embedding into $(\infty,1)Cat$
 {#EmbeddingIntoCat}

+-- {: .num_prop #LimitsAndColimits}
###### Proposition

All small [[limit in a quasi-category|limits and colimits]] exists in $Pr(\infty,1)Cat$. The limits are preserved by the embedding $Pr(\infty,1)Cat \hookrightarrow $ [[(∞,1)Cat]].

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.3.13]].


### Tensor product 

+-- {: .num_prop}
###### Proposition

Let $C_1, \cdots, C_n$ be a finite collection of locally presentable $(\infty,1)$-categories. There exists a locally presentable $(\infty,1)$-category $C_1 \otimes \cdots \otimes C_n$ and an [[(∞,1)-functor]] 

$$
  C_1 \times \cdots \times C_n \to C_1 \otimes \cdots \otimes C_n
$$

(the [[tensor product]]) such that

1. it preserves [[(∞,1)-colimit]]s in each variable;

1. for every $D \in Pr(\infty,1)Cat$, composition with $f$ produces an [[equivalence of (∞,1)-categories]] 

$$
  Func_{(\infty,1)}^L(C_1 \otimes \cdots \otimes C_n,D)
  \stackrel{\simeq}{\to}
  Func^{L}_{(\infty,1)}(C_1 \times \cdots \times C_n,D)
  \hookrightarrow
  Func^{}_{(\infty,1)}(C_1 \times \cdots \times C_n,D)
$$

onto the full [[sub-(∞,1)-category]] of those functors, that preserves colimits in each argument.

=--

This is  ([Lurie, NA, theorem 4.1.4](#LurieNoncommutative)).

This tensor product makes $Pr(\infty,1)Cat$ a [[symmetric monoidal (∞,1)-category]].  Indeed it is even [[closed monoidal (infinity,1)-category|closed]], since the [[hom-objects]] $Func^L$ supply [[right adjoints]] to the tensor product ([Lurie 09, Rem. 5.5.3.9](#Lurie09HTT)).

The definition of the tensor product is easy: $C \otimes D = Cts(C^{op},D)$, where $Cts$ denotes the category of continuous (small-limit-preserving) functors.  Equivalently, this is $Cocts(C,D^{op})^{op}$, where $Cocts$ denotes the category of cocontinuous (small-colimit-preserving) functors; it is tempting to write this as $Func^L(C,D^{op})^{op}$, but note that $D^{op}$ is not itself locally presentable.  However, $D^{op}$ is nevertheless cocomplete, so any cocontinuous functor $C \to D^{op}$ has a right adjoint.

To show that $Cts(C^{op},D)$ is locally presentable, recall that $C \simeq Ind_\kappa A$ for some small $\kappa$-cocomplete $A$.  Thus $Cts(C^{op},D) \simeq \kappa Cts (A^{op},D)$, where $\kappa Cts$ denotes the category of $\kappa$-limit-preserving functors; this is an accessible localization of $Fun(A^{op},D)$ and hence locally presentable.

To show that $Cts(C^{op},D)$ has the right universal property, we compute

$$
\begin{aligned}
Func^L(C,Func^L(D,E))
&\simeq \kappa CoCts (A,Func^L(D,E)) & \quad \text{(by the universal property of }\; C = Ind_\kappa(A))\\
&\simeq \kappa Cts (A^{op},Func^L(D,E)^{op})^{op} &\quad \text{(by taking opposites)}\\\\
&\simeq \kappa Cts (A^{op},CtsAcc(E,D))^{op} &\quad \text{(by the adjoint functor theorem)}\\
&\simeq CtsAcc(E,\kappa Cts (A^{op},D))^{op} &\quad (*)\\
&\simeq Func^L(\kappa Cts (A^{op},D),E) &\quad \text{(by the adjoint functor theorem)}
\end{aligned}
$$

To justify the step $(*)$, note that both sides are equivalent to some subcategory of functors $A^{op} \times E \to D$, and in both cases part of the requirement is that $\kappa$-limits be preserved in the $A^{op}$-variable and all small limits be preserved in the $E$-variable.  The remaining condition on the left is that for each $a\in A$ the corresponding functor $E\to D$ is accessible, i.e. preserves $\lambda_a$-filtered colimits for some cardinal $\lambda_a$.  On the right, the remaining condition is that the [[currying|curried]] functor $E\to \kappa Cts (A^{op},D)$ is accessible, i.e. preserves $\mu$-filtered colimits for some cardinal $\mu$.  Since $\mu$-filtered colimits commute with $\kappa$-limits as long as $\mu\ge \kappa$, such colimits in $\kappa Cts (A^{op},D)$ are pointwise, so we are at least talking about the same colimits, so the right-hand condition implies the left (take each $\lambda_a = \mu$).  On the other hand, because $A$ is small, if the left-hand condition holds we can take $\mu = \sup_{a\in A} \lambda_a$ to make the right-hand condition hold.

### Colimits

Above we remarked that the forgetful functor $Pr(\infty,1)Cat \to (\infty,1)Cat$ preserves limits.  It does not preserve colimits, but $Pr(\infty,1)Cat$ does have colimits; they are constructed by passing to right adjoints and taking the limit there.

In particular, this implies there are some cases in which colimits coincide with limits.  For instance:

+--{: .num_prop}
###### Proposition
Small coproducts in $Pr(\infty,1)Cat$ coincide with small products.
=--
+--{: .proof}
###### Proof
Let $\prod_i C_i$ be a product in $Pr(\infty,1)Cat$.  Then we have
$$
\begin{aligned}
Func^L(\prod_i C_i, D)
&\simeq Cts(D, \prod_i C_i)\\
&\simeq \prod_i Cts(D,C_i)\\
&\simeq \prod_i Func^L(C_i,D)
\end{aligned}
$$
=--

To be precise, the next result requires an enhancement of $Pr(\infty,1)Cat$ to an $(\infty,2)$-category so that we can talk about [[powers]] and [[copowers]] by small $(\infty,1)$-categories.  However, the proof gives an explicit universal property that makes sense without having to define that whole $(\infty,2)$-category.

+--{: .num_prop}
###### Proposition
The [[copower]] of $C\in Pr(\infty,1)Cat$ by a small $(\infty,1)$-category $A$ is $C^{A^{op}}$.
=--
+--{: .proof}
###### Proof
Let $P A$ denote the [[(∞,1)-presheaf (∞,1)-category]] on $A$.  This is its free cocompletion, so we have $Func^L(P A,C) \simeq C^A$.  Dually, $(P A)^{op}$ is the free completion of $A^{op}$, so we have $Cts((P A)^{op},C) \simeq C^{A^op}$.  Now we have:
$$
\begin{aligned}
Func^L(C,D)^A
&\simeq Func^L(C,D^A)\\
&\simeq Func^L(C,Func^L(P A,D))\\
&\simeq Func^L(C \otimes P A, D)\\
&\simeq Func^L(Cts((P A)^{op},C),D)\\
&\simeq Func^L(C^{A^op},D)
\end{aligned}
$$
=--

In general, this sort of argument should work for all lax colimits of lax functors; for instance, [[Kleisli objects]] should also coincide with [[Eilenberg-Moore objects]] (though this also requires enhancing $Pr(\infty,1)Cat$ to an $(\infty,2)$-category).  The corresponding 1-categorical fact is that in any [[bicategory]] with [[local colimits]] (colimits in each hom-category distributed over by composition), lax colimits of lax functors are also lax limits.


## As $\infty$-vector spaces

In some context it makes good sense to think of $Pr(\infty,1)Cat$ as a model for an $(\infty,1)$-category of "$\infty$-vector spaces", or at least "$\infty$-abelian groups".  For instance, the fact that the $(\infty,2)$-category $Pr(\infty,1)Cat$ has local colimits, making certain limits and colimits coincide, is a sort of categorification of the fact that of [[Vect]] and [[Ab]] are [[additive categories]] in which finite products and coproducts coincide.

More on this analogy is at [[integral transforms on sheaves]].  Here a small $(\infty,1)$-category $S$ is to be thought of as a _basis_ and the locally presentable $(\infty,1)$-category $C \hookrightarrow PSh_{(\infty,1)}(C)$ as the $\infty$-vector space spanned by this basis. The colimits in $C$ play the role of addition of vectors and the fact that morphisms in $Pr(\infty,1)Cat$ are colimit-presserving means that they play  the role of _linear_ maps between vector spaces. This is described also at [[Lawvere distribution]].

The monoidal product $\otimes : Pr(\infty,1)Cat \times Pr(\infty,1)Cat \to Pr(\infty,1)Cat$ plays the role of the [[tensor product]] of vector spaces, with a morphism out of $C \otimes D$ being a bilinear morphism out of $C \times D$, and the fact that $Pr(\infty,1)Cat$ is closed monoidal reflects the fact that [[Vect]] is closed monoidal.  The construction of the tensor product as $Cts(C^{op},D)$ corresponds to the fact that, at least for finite-dimensional $V$, we have $V\otimes W \cong Hom(V^\ast,W)$.

(A related decategorification of $Pr(\infty,1)Cat$ is the category [[Sup]] of [[suplattices]], which can also be thought of as analogous to abelian groups or vector spaces.)

### Applications

Combined with the fact that the embedding $Pr(\infty,1)Cat \hookrightarrow (\infty,1)Cat$ preserves limits (prop. \ref{LimitsAndColimits}), this yields some useful statements.

For instance with $Pr(\infty,1)Cat$ regarded as $\infty Vect$, for any [[∞-group]] $G$ with [[delooping]] [[∞-groupoid]] $\mathbf{B}G$, we may think of an [[(∞,1)-functor]] $\rho : \mathbf{B}G \to Pr(\infty,1)Cat$ as a linear [[representation]] of $G$: the single object of $\mathbf{B}G$ is sent to a presentable $(\infty,1)$-category $V$ and the morphisms in $\mathbf{B}G$ then define an [[action]] of $G$ on that.


## Related concepts

* [[PrCat]]

* [[Ho(CombModCat)]]

* [[2Ab]], [[2Ring]]

## References

The $(\infty,1)$-category $Pr(\infty,1)Cat$ is introduced in section 5.5.3 of

* {#Lurie09HTT} [[Jacob Lurie]], _[[Higher Topos Theory]]_ 


The monoidal structure on $Pr(\infty,1)Cat$ is described in section 4.1 of

* [[Jacob Lurie]], _[[Noncommutative Algebra]]_
{#LurieNoncommutative}

That this is in fact a symmetric monoidal structure is discussed in section 6 of

* [[Jacob Lurie]], _[[Commutative Algebra]]_

(see proposition 6.14 and remark 6.18).  This monoidal structure is exhibited as a restriction of a monoidal structure on all cocomplete $(\infty,1)$-categories in section 4.8 of

* [[Jacob Lurie]], _[[Higher Algebra]]_.


[[!redirects symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories]]


[[!redirects symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]
[[!redirects symmetric monoidal (infinity,1)-category of presentable (inf]]
[[!redirects Pr(∞,1)Cat]]


category: category
