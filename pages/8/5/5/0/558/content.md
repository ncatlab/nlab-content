
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The _homotopy hypothesis_ is the assertion that

* [[∞-groupoid]]s are equivalent to [[topological space]].

or rather the stronger statement that

* [[n-groupoid]]s are equivalent to [[homotopy n-type]]s for all $n \in \mathbb{N}$

and moreover

* this equivalence is induced by the [[fundamental ∞-groupoid]] construction.

What this actually means in detail depends on which definition [[∞Grpd]] is being used and to which precise incarnation of [[Top]] it is being compared to. 

There are some definitions of [[∞-groupoid]]s for which the homotopy hypothesis is a proven _theorem_ . Depending on where in the spectrum between [[geometric definitions of higher categories]] and [[algebraic definitions of higher categories]] a given definition of $\infty$-groupoids is located, the statement may be more or less obvious. 

For instance there is some justification for _defining_ an $\infty$-groupoid to _be_ equivalently a topological space. For this definition the homotopy hypothesis is of course a tautology.

A definition of $\infty$-groupoid that is still very geometrical but much more combinatorial is that given by [[Kan complex]]es. For these the homotopy hypothesis has a (non-trivial but fairly tractable) proof. The equivalence between Kan complexes and [[CW-complex]]es obtained this way is at the heart of all traditional [[homotopy theory]].

A genuine algebraic definition of $\infty$-groupoids for which the homotopy theory has a (non-trivial but tractable) proof is given by [[algebraic Kan complex]]es. 

However for other algebraic definition of $\infty$-groupoids not much indication for how to prove the homotopy hypothsis is known. The definition of [[Trimble ∞-category]] stands out as an algebraic definition that has the notion of [[fundamental ∞-groupoid]] built right into it, but also here it seems unclear at the moment how to make progress with proving the homotopy hypothesis.

In fact, generally the homotopy hypothesis is regarded as a _consistency condition_ for definitions in [[higher category theory]]:

* Any definition of [[(n,r)-category]] should be such that there is a [[fundamental infinity-groupoid|fundamerntal n-groupoid]]-construction with values in the corresponding [[(n,0)-categories]] which makes these equivalent to [[homotopy n-type]]s.

One way to justify this condition is by recourse to the proven cases of the homotopy hypothesis: experience shows that the collections of all three models --  topological spaces, Kan complexes, algebraic Kan complexes -- provide a model for [[∞Grpd]] that supports the general abstract [[higher category theory]] -- specifically [[(∞,1)-category theory]] -- that one expects in analogy to how [[Set]] supports ordinary [[category]] theory.  Any other definition of $\infty$-groupoids is hoped/required to reproduce this, and hence is hoped/required to satisfy the homotopy hypothesis.

Apart from having different models of $\infty$-groupoids that lend themselves more or less to a comparison with topological spaces, there is also the issue as to how to conceive of the notion of _equivalence_ between $\infty$-groupoids.

The usual, unstated, implication is that the notion of _equivalence_ of [[n-groupoid]]s used to model [[homotopy n-type]]s is the appropriate *[[n-category]]-theoretic* notion of [[equivalence of categories|equivalence]].  It is in this way that, for instance, it is known that 1-[[groupoid]]s model homotopy 1-types (see below).

The reason this is important to specify is that there are other notions of equivalence on categorical structures which model homotopy types in other ways.  For example, if we declare a functor between categories to be a weak equivalence iff its [[nerve]] is a weak equivalence of [[simplicial set]]s, then _all_ homotopy types can be modeled by 1-categories in this way; see the [[Thomason model structure]] for 1-categories.

Finally, in analogy to the homotopy hypothesis, there are also attempts to relate general [[∞-categories]] which need not be groupoidal to [[directed space]]s, in which a morphism which is not invertible would model a path in the space that can only be traversed in one direction.



## Realizations

We discuss various different definitions of [[]n-groupoid]]s and [[∞-groupoid]]s and the formulation and proof of the homotopy hypothesis for them, to the extent that it is available.


### For groupoids

+-- {: .un_prop}
###### Proposition


The [[2-category]] [[Grpd]] of [[groupoid]]s, [[functor]]s, and [[natural transformation]]s is equivalent to the 2-category of [[homotopy n-type|homotopy 1-types]], [[continuous map]]s, and [[homotopy]] classes of homotopies.

=--

### For 2-groupoids

(...) [[2-groupoid]]s model all [[homotopy n-type|homotopy 2-type]]s (...)

[[strict 2-groupoid]]s suffice (...)

### For Gray-groupoids

(...) [[Gray-groupoid]]s model all [[homotopy n-type|homotopy 3-type]]s (...)

It is known that not all homotopy 3-types can be modeled by strict 3-groupoids, but that [[Gray-category|Gray-categories]] ([[semi-strict infinity-category|semi-strict 3-categories]]) suffice; the obstruction is the [[Whitehead product]] which arises from a nontrivial [[interchanger]]. 

(...)


### For Kan complexes {}

We write $sSet_{Quillen}$ for [[sSet]] equipped with the standard [[model structure on simplicial sets]]. The cofibrant-fibrant objects in $sSet_{Quillen}$ are precisely the [[Kan complex]]es.

Also we write $Top_{Quillen}$ for [[Top]] equipped with the standard [[model structure on topological spaces]].

+-- {: .un_theorem}
###### Theorem

There is a [[Quillen equivalence]]

$$
  (|-| \dashv Sing) : Top \stackrel{\overset{|-|}{\leftarrow}}{\underset{Sing}{\to}} sSet_{Quillen} 
  \,,
$$

where the [[left adjoint]] $|-|$ is [[geometric realization]] and the [[right adjoint]] $Sing(-)$ is forming the [[singular simplicial complex]] $Sing(-)$.

This induces an [[equivalence of (∞,1)-categories]] of the corresponding [[presentable (infinity,1)-category|presented]] [[(∞,1)-categories]] 

* [[Top]] \simeq [[∞Grpd]]

=--

### For algebraic Kan complexes {#ForAlgebraicKanComplexes}

An [[algebraic Kan complex]] is an [[algebraic definition of higher categories|algebraic definition of higher groupoids]] obtained by taking the ordinary definition of [[Kan complex]] and equipping these with _choices_ of [[horn]]-fillers. These choice encode specified composition operations, specified [[associator]]s for these, specified _pentagonators_ and so on.

Algebraic Kan complexes constitute a genuine algebraic model in that they are precisely the [[algebras over a monad]] on [[sSet]].

+-- {: .un_theorem}
###### Theorem

The [[transferred model structure|transferred]] [[model structure on algebraic fibrant objects|model structure on algebraic Kan complexes]] is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on simplicial sets]]

$$
  (F \dashv U) : Alg Kan \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}  
   sSet_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The proof is spelled out at [[model structure on algebraic fibrant objects]].

=--

+-- {: .un_remark}
###### Remark


With the above [homotopy hypothesis-theorem for Kan complexes](ForKanComplexes) this gives a zig-zag of Quillen equivalences between $Alg Kan$ and $Top$

$$
  Alg Kan 
    \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}  
   sSet_{Quillen}
     \stackrel{\overset{|-|}{\to}}{\underset{Sing}{\leftarrow}}
    Top
  \,.
$$

This already yields the homotopy hypothesis for algebraic Kan complexes at the level of the corresponding [[presentable (∞,1)-category|presented (∞,1)-categories]] (as discussed there)

$$
  Alg C^\circ \simeq Top^\circ
  \,.
$$

=--

But there is also a direct Quillen equivalence:

+-- {: .un_def}
###### Definition

Write $\Delta^n$ and $\Lambda^n_k$ for the topological $n$-[[simplex]] and its $k$-[[horn]].

Fix any choice of [[retract]]s 

$$
  R(n,k) : \Delta^n \to \Lambda^n_k
$$

for all topological [[horn]] inclusions $\Lambda^n_i \hookrightarrow \Delta^n$. 

For $X$ any [[topological space]] equip the [[singular simplicial complex]] $Sing X$ with the stucture of an [[algebraic Kan complex]] by taking the filler of $\Lambda_k[n] \to Sing X$ to be given by the $(|-| \dashv Sing)$-[[adjunct]] of $\Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k \to X$. Write $\Pi_\infty(X) \in Alg Kan$ for the resulting algebraic Kan complex.

This construction constitutes a functor

$$ 
  \Pi_\infty(-) : Top \to Alg C
  \,,
$$


with $U \Pi_\infty = Sing$.

=--

+-- {: .un_remark}
###### Remark

The choices of fillers in $\Pi_\infty(X)$ may be thought of as explicit choice of reparameterizations of paths in $X$. These choices are arbitrary, but by the general statement at [[model structure on algebraic fibrant objects]], any two chocies yield equivalent objects.

=--

+-- {: .un_def}
###### Definition

Given choices $R(-,-)$ of horn retracts as above, define a functor

$$
  |-|_r : Alg Kan \to Top
$$

called **reduced geometric realization** by taking it on an object $A \in Alg Kan$ to be given by the [[coequalizer]]

$$
  |A|_r := \lim_{\to}(\coprod_{\Lambda[n]_k \to A} \Delta^n \stackrel{\to}{\to} |U A|)
  \,,
$$

where $|U A|$ is the ordinary [[geometric realization]] of the underlying simplicial set of $A$ and where the two maps are

1. the image under $|-|$ of the distinguished fillers $\Delta[n] \to U A$ of $A$;

1. the composite $\Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k \to |U X|$ .


=--

+-- {: .un_prop}
###### Proposition

The functor $|-|_r$ is [[left adjoint]] to $\Pi_\infty$.

$$
  (|-|_r \dashv \Pi_\infty)
  \,.
$$

=--

This is ([Nikolaus, prop. 3.4](#Nikolaus)).

+-- {: .proof}
###### Proof

We check the hom-isomorphism. A morphism $f : |A|_r \to X$ is
by definition of the coequalizer the same as a map $\tilde f : |A| \to X$ such that for each horn $h : \Lambda[n]_k \to A$ with distinguished filler $\hat h : \Delta[n] \to A$ the composites

$$
  \Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k 
  \stackrel{|h|}{\to} |U A|
  \stackrel{\tilde f}{\to}
  X
$$

and

$$
  \Delta^n \stackrel{|\hat h|}{\to} |U A| \stackrel{\tilde f}{\to} X
$$

are equal. This means equivalently that the $(|-| \dashv Sing)$-[[adjunct]] $\tilde \tilde f : U A \to Sing X$ sends distinguished fillers in $A$ to distinguished fillers in $\Pi_\infty(X)$ and is hence a morphism in $Alg Kan$.

the constructon shows that the map $(f : |A|_r \to X) \mapsto (\tilde \tilde f : A \to \Pi_\infty(X))$ thus obtained is a bijection.

=--

+-- {: .un_theorem}
###### Theorem

We have an identity

$$
  \array{
    && Alg Kan
    \\
    & {}^{\mathllap{U}}\swarrow 
    & \Downarrow^{=}& 
    \nwarrow^{\mathrlap{\Pi_\infty}}
    \\
    sSet &&\underset{Sing}{\leftarrow}&& Top
  }
$$

and a [[natural isomorphism]]

$$
  \array{
    && Alg Kan
    \\
    & {}^{\mathllap{F}}\nearrow 
    & \Downarrow^{\simeq}& 
    \searrow^{\mathrlap{|-|_r}}
    \\
    sSet &&\underset{|-|}{\to}&& Top
  }
  \,.
$$


=--

This is ([Nikolaus, corollary 3.5](#Nikolaus))

+-- {: .proof}
###### Proof

The identity is evident by definition of $\Pi_\infty$. 

Using this, we have that 

$$
  (|-|_r \circ F \dashv U \circ \Pi_\infty = Sing)
  \,.
$$

So $|-|_r \circ F$ is another [[left adjoint]] to $Sing$ and hence naturally isomorphism to $|-|$.

=--


+-- {: .un_corollary}
###### Corollary


The adjunction 

$$
  (|-|_r \dashv \Pi_\infty)
  : 
  Alg C \to Top
$$

constitutes a [[Quillen equivalence]]


=--

This is [Nikolaus, corollary 3.6](#Nilkolaus)

+-- {: .proof}
###### Proof

By the above theorem and the <a href="http://ncatlab.org/nlab/show/Quillen+equivalence#TwoOutOfThree">2-out-of-3-property</a> of Quillen equivalences.

=--



### For $n$-fold groups

It is also known since the work of Loday and Porter that _strict_ $n$-[[n-fold category|fold categories]] also model all [[homotopy n-type]]s.

Loday proved in

* J.-L. Loday, _Spaces with finitely many non-trivial homotopy groups_, J. Pure Appl. Algebra
24 (1982), 179-202.

that the homotopy category of [[cat-n-group]]s is equivalent to that of pointed connected homotopy $n$-types.

Regis Pellissier produces in his 2003 thesis a Quillen equivalence between Segal groupoids and Topological Spaces:

* [arXiv](http://arxiv.org/abs/math/0308246)

For reviews see for instance

* Ronald Brown, _Computing Homotopy Types Using Crossed $N$-Cubes of Groups_ ([arXiv](http://arxiv.org/abs/math/0109091))

* Simona Paoli, _Internal categorical structures in homotopical algebra_, to appear in _Towards Higher Categories_, eds. J. Baez and P. May.  ([pdf](http://www.maths.mq.edu.au/~simonap/paoli_IMA.pdf))

Strict $n$-fold categories can in fact be considered as modeling certain diagrams of spaces, or structured spaces, which is useful for computing with "[[higher van Kampen theorems]]."  In general, we have some functors
$$\Xi:({diagrams of spaces })\leftrightarrow ({higher groupoids}):B $$
such that:
1. $\Xi$ is homotopically defined and preserves certain colimits;
1. $\Xi \circ B$ is equivalent to Id;
1. There is a natural transformation $Id \rightarrow B \circ \Xi$ preserving some homotopical information. 

The purpose of 1. is to be able to calculate some homotopical information. The purpose of 2. is to show that the diagrams used reflect the algebraic structure of the higher groupoids. Detailed references can be found at the [Higher dimensional group theory](http://www.bangor.ac.uk/r.brown/hdaweb2.htm) web site. 

Trying to be more explicit about some colimits of certain higher groupoids has yielded some interesting algebraic constructions, for which some examples required computational group theory!

## References

An introductory survey is given in

* [[John Baez]], _The Homotopy Hypothesis_ ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

The homotopy hypothesis for [[algebraic Kan complex]]es is established and discussed in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

Some related literature is listed at

* [[Ronnie Brown]], _Higher dimensional group theory_ ([web](http://www.bangor.ac.uk/r.brown/hdaweb2.htm). 
