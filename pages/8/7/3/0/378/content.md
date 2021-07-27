
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[simplicial set|Simplicial sets]] are the archetypical combinatorial "[[model category|model]]" for the [[(∞,1)-category]] of (compactly generated weakly Hausdorff) [[topological space]]s and equivalently that of [[∞-groupoid]]s, as well as a standard model for the [[(∞,1)-category of (∞,1)-categories]] [[(∞,1)Cat]] itself.

This statement is made precise by the existence of the structure of a [[model category]] on [[sSet]], called the **[[classical model structure on simplicial sets]]**  that is a [[presentable (infinity,1)-category|presentation]] for the [[(infinity,1)-category]] [[Top]], as well as the **Joyal model structure** which similarly is a presentation of the $(\infty,1)$-category $(\infty,1)Cat$.



## Classical Model Structure

The [[classical model structure on simplicial sets]], $sSet_{Quillen}$, has the following distinguished classes of morphisms:

+-- {: .num_defn}
###### Definition

* The **cofibrations** $C$ are simply the [[monomorphism]]s $f : X \to Y$ which are precisely the levelwise injections, i.e. the morphisms of simplicial sets such that $f_n : X_n \to Y_n$ is an injection of sets for all $n \in \mathbb{N}$.

* The **weak equivalences** $W$ are **weak homotopy equivalences**, i.e., morphisms whose [[geometric realization]] is a weak homotopy equivalence of topological spaces.

=--

* The **fibrations** $F$ are the **[[Kan fibration]]s**, i.e., maps $f : X \to Y$ which have the [[right lifting property]] with respect to all [[horn]] inclusions.
  $$
    \array{
      \Lambda^k[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

* A morphism $f : X \to Y$ of fibrant simplicial sets / [[Kan complex]]es is a weak equivalence precisely if it induces an [[isomorphism]] on all [[simplicial homotopy groups]].

* All simplicial sets are cofibrant with respect to this model structure. 

* The fibrant objects are precisely the [[Kan complex|Kan complexes]].

+-- {: .num_prop}
###### Proposition

The **acyclic fibrations** (i.e. the maps that are both fibrations as well as weak equivalences) between [[Kan complex]]es are precisely the morphisms $f : X \to Y$ that have the [[right lifting property]] with respect to all inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$ of boundaries of $n$-simplices into their $n$-simplices
  $$
    \array{
      \partial \Delta[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

=--

This appears spelled out for instance as ([Goerss-Jardine, theorem 11.2](#GoerssJardine)).


In fact:

+-- {: .num_prop}
###### Proposition

$sSet_{Quillen}$ is a [[cofibrantly generated model category]] with

* generating cofibrations the [[boundary]] inclusions $\partial \Delta[n] \to \Delta[n]$;

* generating acyclic cofibrations the [[horn]] inclusions $\Lambda^i[n] \to \Delta[n]$.

=--



+-- {: .num_theorem}
###### Theorem

The [[singular simplicial complex]]-functor and [[geometric realization]]

$$
  ({\vert -\vert}\dashv Sing)
  : 
  Top_{Quillen}
  \stackrel{\overset{{\vert -\vert}}{\leftarrow}}{\underset{Sing}{\to}}
  sSet_{Quillen}
$$

constitutes a [[Quillen equivalence]] with the standard [[Quillen model structure on topological spaces]].

=--

For more on this see [[homotopy hypothesis]].

### Characterisations of weak homotopy equivalences

+-- {: .num_theorem}
###### Theorem

Let $W$ be the smallest class of morphisms in $sSet$ satisfying the following conditions:

1. The class of monomorphisms that are in $W$ is closed under [[pushout]], [[transfinite composition]], and [[retracts]].
2. $W$ has the [[two-out-of-three]] property in $sSet$ and contains all the [[isomorphisms]].
3. For all natural numbers $n$, the unique morphism $\Delta [n] \to \Delta [0]$ is in $W$.

Then $W$ is the class of weak homotopy equivalences.
=--

+-- {: .proof}
###### Proof

* First, notice that the horn inclusions $\Lambda^0 [1] \hookrightarrow \Delta [1]$ and $\Lambda^1 [1] \hookrightarrow \Delta [1]$ are in $W$.
* Suppose that the horn inclusion $\Lambda^k [m] \hookrightarrow \Delta [m]$ is in $W$ for all $m \lt n$ and all $0 \le k \le m$. Then for $0 \le l \le n$, the horn inclusion $\Lambda^l [n] \hookrightarrow \Delta [n]$ is also in $W$.
* Quillen's [[small object argument]] then implies all the trivial cofibrations are in $W$.
* If $p : X \to Y$ is a trivial Kan fibration, then its right lifting property implies there is a morphism $s : Y \to X$ such that $p \circ s = id_Y$, and the two-out-of-three property implies $s : Y \to X$ is a trivial cofibration. Thus every trivial Kan fibration is also in $W$.
* Every weak homotopy equivalence factors as $p \circ i$ where $p$ is a trivial Kan fibration and $i$ is a trivial cofibration, so every weak homotopy equivalence is indeed in $W$.
* Finally, noting that the class of weak homotopy equivalences satisfies the conditions in the theorem, we deduce that it is the _smallest_ such class.

=--

As a corollary, we deduce that the classical model structure on $sSet$ is the smallest (in terms of weak equivalences) model structure for which the cofibrations are the monomorphisms and the weak equivalences include the (combinatorial) homotopy equivalences.

+-- {: .num_prop}
###### Proposition

Let $\pi_0 : sSet \to Set$ be the connected components functor, i.e. the left adjoint of the constant functor $cst : Set \to sSet$. A morphism $f : Z \to W$ in $sSet$ is a weak homotopy equivalence if and only if the induced map
$$\pi_0 K^f : \pi_0 K^W \to \pi_0 K^Z$$
is a bijection for all _Kan complexes_ $K$.

=--

+-- {: .proof}
###### Proof

One direction is easy: if $K$ is a Kan complex, then axiom SM7 for [[simplicial model categories]] implies  the functor $K^{(-)} : sSet^{op} \to sSet$ is a right [[Quillen functor]], so Ken Brown's lemma implies it preserves all weak homotopy equivalences; in particular, $\pi_0 K^{(-)} : sSet^{op} \to Set$ sends weak homotopy equivalences to bijections.

Conversely, when $K$ is a Kan complex, there is a natural bijection between $\pi_0 K^X$ and the hom-set $Ho (sSet) (X, K)$, and thus by the [[Yoneda lemma]], a morphism $f : Z \to W$ such that the induced morphism $\pi_0 K^W \to \pi_0 K^Z$ is a bijection for all Kan complexes $K$ is precisely a morphism that becomes an isomorphism in $Ho (sSet)$, i.e. a weak homotopy equivalence.

=--

### Relation to the model structure on strict $\infty$-groupoids 

> under construction

Recall the [[model structure on strict omega-groupoids]] and the [[omega-nerve]] operation

$$
  N : Str \infty Grpd \to Kan Complx
  \,.
$$

> this ought to be a Quillen functor, but is it? 

As a warmup, let $C, D$ be ordinary [[groupoid]]s and $N(C)$, $N(D)$ their ordinary [[nerve]]s. We'd like to show in detail that 

+-- {: .num_prop}
###### Proposition

A [[functor]] $F : C \to D$ is 

* [[k-surjective functor|k-surjective]] for all $k$ and hence a surjective [[equivalence of categories]] precisely if under the [[nerve]] $N(F) : N(C) \to N(D)$ it induces an acyclic fibration of Kan complexes;

=--

+-- {: .proof}
###### Proof

We know that both $N(C)$ and $N(D)$ are Kan complexes. By the above theorem it suffices to show that $N(f)$ being a surjective equivalence is the same as having all lifts

$$
  \array{
    \partial \Delta[n] &\to& N(C)
    \\
    \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
    \\
    \Delta[n] &\to& N(D)
  }
  \,.
$$


We check successively what this means for increasing $n$:

* $n= 0$. In degree 0 the boundary inclusion is that of the empty set into the [[point]] $\emptyset \hookrightarrow {*}$. The lifting property in this case amounts to saying that every point in $N(D)$ lifts through $N(F)$. 
  $$
    \array{
      \emptyset &\to& N(C)
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \Leftrightarrow
    \array{
      && N(C)
      \\
      &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \,.
  $$
  This precisely says that $N(F)$ is surjective on 0-cells and hence that $F$ is surjective on objects.

* $n=1$. In degree 1 the boundary inclusion is that of a pair of points as the endpoints of the interval
  $\{\circ, \bullet\} \hookrightarrow \{\circ \to \bullet\}$. The lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ all elements in $Hom(F(a),F(b))$ are hit. Hence that $F$ is a [[full functor]].

* $n=2$. In degree 2 the boundary inclusion is that of the triangle as the boundary of a filled triangle. It is sufficient to restrict attention to the case that the map $\partial \Delta[2] \to N(C)$ sends the top left edge of the triangle to an identity. Then the lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ the map $F_{a,b} : Hom(a,b) \to Hom(F(a),F(b))$ is injective. Hence that $F$ is a [[faithful functor]].
  $$
    \left(
    \array{
      && b 
      \\
      & {}^{Id_a}\nearrow && \searrow^{f}
      \\
      a &&\stackrel{g}{\to}&& b
    }
    \right)
    \stackrel{N(F)}{\mapsto}
    \left(
    \array{
      && b 
      \\
      & {}^{Id_a}\nearrow &\Downarrow^=& \searrow^{F(f)}
      \\
      a &&\stackrel{F(g)}{\to}&& b
    }
    \right)
  $$


=--

### Constructive version

The original [[proofs]] of the existence of the [[classical model structure on simplicial sets]] are based in [[classical mathematics]] as they use the [[principle of excluded middle]] and the [[axiom of choice]], and are hence not valid in [[constructive mathematics]]. This becomes more than a philosophical issue with the relevance of this [[model category]]-[[structure]] in [[homotopy type theory]], where [[internalization]] into the [[type theory]] requires [[constructive mathematics|constructive]] methods for interpreting [[proofs as programs]].

A constructively valid model structure on simplicial sets and coinciding with the [[classical model structure on simplicial sets|classical model structure]] if [[excluded middle]] and [[axiom of choice]] are assumed was found in [Henry 19](constructive+model+structure+on+simplicial+sets#Henry19). Alternative simpler proofs were found in [Gambino-Sattler-Szumiło 19](constructive+model+structure+on+simplicial+sets#GambinoSattlerSzumilo19). 

See at _[[constructive model structure on simplicial sets]]_.


## Joyal's Model Structure

There is a second model structure on $sSet$ -- the **[[model structure for quasi-categories]]** $sSet_{Joyal}$ -- which is different (not [[Quillen equivalence|Quillen equivalent]]) to the classical one, due to [[Andre Joyal]], with the following distinguished classes of morphisms:

* The cofibrations $C$ are monomorphisms, equivalently, levelwise injections.

* The weak equivalences $W$ are **[[equivalence of quasi-categories|weak categorical equivalences]]**, which are morphisms $u : A \rightarrow B$ of simplicial sets such that the induced map $u^* : X^B \rightarrow X^A$ of internal-homs for all [[quasi-category|quasi-categories]] $X$ induces an isomorphism when applying the functor $\tau_0$ that takes a simplicial set to the set of isomorphism classes of objects of its fundamental category.

* The fibrations $F$ are called variously **isofibrations** or **[[inner Kan fibration|quasi-fibration]]**. As always, these are determined by the classes $C$ and $W$.
Quasi-fibrations between weak Kan complexes have a simple description; they are precisely the [[inner Kan fibrations]], the maps that have the right lifting property with respect to the inner [[horn]] inclusions and also the inclusion $j_0 : * \rightarrow J$ where $*$ is the terminal simplicial set and $J$ is the nerve of the groupoid on two objects with one non-trivial isomorphism. 

All objects are cofibrant. The fibrant objects are precisely the [[quasi-categories]].

This model structure is cofibrantly generated. The generating cofibrations are the set $I$ described above. There is no known explicit description for the generating trivial cofibrations.

Importantly, this model structure is Quillen equivalent to several alternative model structures for the ''homotopy theory of homotopy theories" such as that on the category of [[simplicially enriched category|simplicially enriched categories]].

### Comparison

Every weak categorical equivalence is a weak homotopy equivalence. Since both model structures have the same cofibrations, it follows that the classical model structure is a [[Bousfield localization]] of Joyal's model structure.

The Quillen model structure is the left [[Bousfield localization of model categories|Bousfield localization]] of $sSet_{Joyal}$ at the outer [[horn]] inclusions.

## Fibrant replacement 

Fibrant replacement in $sSet_{Quillen}$ models the process of _$\infty$-groupoidification_, of freely inverting all [[k-morphism]]s in a simplicial set. Techniques for fibrant replacements $sSet_{Quillen}$ are discussed at

* [[Kan fibrant replacement]].

## Related concepts

* [[model structure on topological spaces]], [[model structure on simplicial presheaves]]

* [[model structure on semi-simplicial sets]]

## Properness

The Quillen model structure is both left and right [[proper model category|proper]].  Left properness is automatic since all objects are cofibrant.  Right properness follows from the following argument: it suffices to show that there is a functor $R$ which (1) preserves fibrations, (2) preserves pullbacks of fibrations, (3) preserves and reflects weak equivalences, and (4) lands in a category in which the pullback of a weak equivalence along a fibration is a weak equivalence.  For if so, we can apply $R$ to the pullback of a fibration along a weak equivalence to get another such pullback in the codomain of $R$, which is a weak equivalence, and hence the original pullback was also a weak equivalence.  Two such functors $R$ are

* geometric realization $sSet \to Top$, where $Top$ denotes a sufficiently [[convenient category of topological spaces]] (e.g. the category of [[k-spaces]] suffices) and
* $Ex^\infty : sSet \to Kan$, where $Kan$ is the category of [[Kan complexes]].

This can be found, for instance, in II.8.6--7 of [Goerss-Jardine](#GoerssJardine).  Another proof can be found in [Moss](#Moss), and a different proof of properness can be found in [Cisinski, Prop. 2.1.5](#Cisinski06).

## References 



[[!include classical model structure on simplicial sets -- references]]



### Joyal model structure on simplicial sets

For teferences on the *[[model structure for quasi-categories]]* see there.






