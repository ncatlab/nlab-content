
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A [[presheaf]] on a [[site]] is a _sheaf_ if its value on any object of the site is given by its compatible values on any [[covering]] of that object.

See also

* [[motivation for sheaves, cohomology and higher stacks]].


## Definition

There are several equivalent ways to characterize sheaves. We start with the general but explicit componentwise definition and then discuss more [[category theory|general abstract]] equivalent reformulations. Finally we give special discussion applicable in various common special cases.

### General definition in components
 {#GeneralDefinitionInComponents}

The following is an explicit component-wise definition of sheaves that is fully general (for instance not assuming that the [[site]] has [[pullback]]s).

+-- {: .num_defn #GeneralComponentwiseDefinition}
###### Definition

Let $(C,J)$ be a [[site]] in the form of a [[small category]] $C$ equipped with a [[coverage]] $J$.

A [[presheaf]] $A \in PSh(C)$ is a **sheaf** with respect to $J$ if

* for every [[covering]] family $\{p_i : U_i \to U\}_{i \in I}$ in $J$

* and for every _[[matching family|compatible family]] of elements_, given by tuples $(s_i \in A(U_i))_{i \in I}$ such that for all $j,k \in I$ and all [[morphisms]] $U_j \stackrel{f}{\leftarrow} K \stackrel{g}{\to} U_k$ in $C$ with $p_j \circ f = p_k \circ g$ we have $A(f)(s_j) = A(g)(s_k) \in A(K)$

then

* there is a _unique_ element $s \in A(U)$ such that $A(p_i)(s) = s_i$ for all $i \in I$.


=--

+-- {: .num_remark}
###### Remark

If in the above definition there is _at most_ one such $s$, we say that $A$ is a [[separated presheaf]] with respect to $J$.

=--

In this form the definition appears for instance in  ([Johnstone, def. C2.1.2](#Johnstone)).-


### General definition abstractly
 {#GeneralDefinitionAbstractly}

We now reformulate the [above component-wise definition](#GeneralComponentwiseDefinition) in [[category theory|general abstract]] terms.

Write

$$
  j : C \hookrightarrow PSh(C)
$$

for the [[Yoneda embedding]].

+-- {: .num_defn}
###### Definition

Given a [[covering]] family $\{f_i : U_i \to U\}$ in $J$, its **[[sieve]]** is the presheaf $S(\{U_i\})$ defined as the [[coequalizer]]

$$
   \coprod_{j,k} j(U_j) \times_{j(U)} j(U_k) 
     \stackrel{\overset{}{\to}}{\to}
   \coprod_i j(U_i) \to S(\{U_i\}) 
$$

in $PSh(C)$.

=--

Here the [[coproduct]] on the left is over the [[pullbacks]]

$$
  \array{
    j(U_j) \times_{j(U)} j(U_k) &\stackrel{p_j}{\to}& j(U_j)
    \\
    {}^{\mathllap{p_k}}\downarrow && \downarrow^{\mathrlap{j(f_j)}}
    \\
    j(U_k) &\stackrel{j(f_k)}{\to}& j(U)
  }
$$

in $PSh(C)$, and the two morphisms between the coproducts are those induced componentwise by the two projections $p_j, p_k$ in this pullback diagram.

+-- {: .num_remark}
###### Remark

Using that [[limits]] and [[colimits]] in a [[category of presheaves]] are computed objectwise, we find that the [[sieve]] $S(\{U_i\})$ defined this way is the presheaf that sends any $K \in C$ to the set of [[morphisms]] $K \to U$ in $C$ that factor through one of the $f_i$.

=--

+-- {: .num_remark}
###### Remark

For every [[covering]] family there is a canonical morphism

$$
  i_{\{U_i\}} :  S(\{U_i\}) \to j(U)
$$

that is induced by the [[universal property]] of the [[coequalizer]] from the morphisms $j(f_i) : j(U_i) \to j(U)$ and $j(U_j) \times_{j(U)} j(U_k) \to j(U)$.

=--

+-- {: .num_defn}
###### Definition

A **sheaf** on $(C,J)$ is a [[presheaf]] $A \in PSh(C)$ that is a [[local object]] with respect to  all $i_{\{U_i\}}$: an object such that for all [[covering]] families $\{f_i : U_i \to U\}$ in $J$ we have that the [[hom-functor]] $PSh_C(-,A)$ sends the canonical morphisms $i_{\{U_i\}} : S(\{U_i\}) \to j(U)$ to [[isomorphisms]].

$$
  PSh_C(i_{\{U_i\}}, A) : 
  PSh_C(j(U), A) \stackrel{\simeq}{\to} PSh_C(S(\{U_i\}), A)
  \,.
$$

=--

Equivalently, using the [[Yoneda lemma]] and the fact that the [[hom-functor]] $PSh_C(-,A)$ sends [[colimits]] to [[limits]], this says that the diagram

$$
  A(U) 
   \to 
  \prod_i A(U_i)
   \stackrel{\to}{\to}
  \prod_{j,k} PSh_C(j(U_j) \times_{j(U)} j(U_k), A)
$$

is an [[equalizer]] diagram for each covering family.

This is also called the **[[descent]] condition** for descent along the covering family.

+-- {: .num_remark}
###### Remark

For many examples of sites that appear in practice -- but by far not for all -- it happens that the pullback presheaves $j(U_j) \times_{j(U)} \times j(U_k)$ are themselves again representable, hence that the [[pullback]] $U_j \times_U U_k$ exists already in $C$, even before passing to the [[Yoneda embedding]]. 

In this special case we may apply the [[Yoneda lemma]] once more to deduce

$$
  PSh_C(j(U_j) \times_{j(U)} j(U_k), A)
  \simeq
  A(U_j \times_U U_k)
  \,.
$$

Then the sheaf condition is that all diagrams

$$
  A(U) 
   \to 
  \prod_i A(U_i)
   \stackrel{\to}{\to}
  \prod_{j,k} A(U_j \times_U U_k)
$$

are [[equalizer]] [[diagram]]s.

=--

+-- {: .num_prop}
###### Proposition

The condition that $PSh_C(S(\{U_i\}), A)$ is an [[isomorphism]] is equivalent to the condition that the set $A(U)$ is isomorphic to the set of [[matching families]] $(s_i \in A(U_i))$ as it appears in the [above component-wise definition](#GeneralComponentwiseDefinition).

=--

+-- {: .proof}
###### Proof

We may express the set of [[natural transformation]]s $PSh_C(j(U_j) \times_{j(U)} j(U_k), A)$ (as described there) by the [[end]]

$$
  PSh_C(j(U_j) \times_{j(U)} j(U_k), A)
  \simeq
  \int_{K \in C}
   Set( C(K,U_j) \times_{C(K,U)} C(K,U_k) , A(K))
  \,.
$$

Using this in the expression of the [[equalizer]]

$$
  \prod_i A(U_i)
  \simeq
  \prod_i 
  \int_{K \in C}
   Set( C(K,U_i), A(K))
  \stackrel{\to}{\to}
   \prod_{j,k}
  \int_{K \in C}
   Set( C(K,U_j) \times_{C(K,U)} C(K,U_k) , A(K))
$$

as a [[subset]] of the product set on the left manifestly yields the componenwise definition above.

=--

+-- {: .num_defn}
###### Definition

A **morphism of sheaves** is just a morphism of the underlying presheaves.
So the [[category of sheaves]] $Sh_J(C)$ is the [[full subcategory]] of the [[category of presheaves]] on the sheaves:

$$
  Sh_J(C) \hookrightarrow PSh(C)
$$

=--

### Characterizations over special sites

We discuss equivalent characterizations of sheaves that are applicable if the underlying [[site]] enjoys certain special properties.

#### Characterizations over sites of opens
 {#CharacterizationsOverSitesOfOpens}

An important special case of sheaves is those over a [[(0,1)-site]] such as a [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$. 
We consider some equivalent ways of characterizing sheaves among presheaves in such a situation.

(The following was mentioned in Peter LeFanu Lumsdaine's comment [here](http://mathoverflow.net/questions/23268/geometric-intuition-for-limits/23276#23276)).

+-- {: .num_prop #AsContinuousFunctorOverOpenSubsets}
###### Proposition

Suppose $Op = Op(X)$ is the [[category of open subsets]] of some [[topological space]] regarded as a [[site]] with the canonical [[coverage]] where $\{U_i \hookrightarrow U\}$ is [[covering]] if the [[union]] $\cup_i U_i \simeq U$ in $Op$.

Then a [[presheaf]] $\mathcal{F}$ on $Op$  is a **sheaf** precisely if for every [[complete category|complete]] [[subcategory|full subcategory]] $\mathcal{U} \hookrightarrow Op$, $\mathcal{F}$ takes the [[colimit]] in $Op$ over $\mathcal{U} \hookrightarrow Op$ to a [[limit]]:


$$
  \mathcal{F}(\underset{\to}{lim} \mathcal{U}) \simeq \underset{\leftarrow}{lim} \mathcal{F}(\mathcal{U})
  \,.
$$

=--

+-- {: .proof}
###### Proof

A complete full subcategory $\mathcal{U} \hookrightarrow Op$ is a collection $\{U_i \hookrightarrow X\}$ of [[open subsets]] that is closed under forming [[intersections]] of subsets. The [[colimit]] 

$$
  \underset{\to}{\lim} (\mathcal{U} \hookrightarrow Op) 
  \simeq
  \cup_{i \in I} U_i
$$

is the [[union]] $U \coloneqq \cup_{i \in I} U_i$ of all these open subsets. Notice that by construction the component maps $\{U_i \hookrightarrow U\}$ of the colimit are a [[covering]] family of $U$.

Inspection then shows that the [[limit]] $\underset{\leftarrow}{\lim}_{i \in I} \mathcal{F}(U_i)$ is the corresponding set of [[matching families]] (use the description of [limits in terms of products and equalizers](http://ncatlab.org/nlab/show/limit#ConstructionFromProductsAndEqualizers) ). Hence the statement follows with def. \ref{GeneralComponentwiseDefinition}.

=--

#### Characterization over canonical topologies
 {#CharacterizationOverCanonicalTopologies}

The above prop. \ref{AsContinuousFunctorOverOpenSubsets} shows that often sheaves are characterized as contravariant functors that take some [[colimits]] to [[limits]]. This is true in full generality for the following case

+-- {: .num_prop #AsContinuousFunctorsOnCanonicalTopology}
###### Proposition

Let $\mathcal{T}$ be be a [[topos]], regarded as a [[large site]] when equipped with the [[canonical topology]]. Then a [[presheaf]] (with values in [[small sets]]) on $\mathcal{T}$ is a sheaf precisely if it sends all [[colimits]] to [[limits]].

=--



## Sheaves and localization


We now describe the derivation and the detailed description of various aspects of sheaves, the [[descent]] condition for sheaves and [[sheafification]], relating it to all the related notions

* [[geometric embedding]]

  * [[localization]]

  * [[homotopy category]]

* [[coverage]]

  * [[Grothendieck topology]]

  * [[Lawvere-Tierney topology]]

* [[local isomorphism]]

  * [[sieve]]

    * [[cover]]

    * [[hypercover]]

  * [[dense monomorphism]]

  * [[local epimorphism]]


We start by assuming that a [[geometric embedding]] into a [[presheaf]] category is given and derive the consequences.

So let $S$ be a [[small category]] and write $PSh(S) = PSh_S = [S^{op}, Set]$ for the corresponding [[topos]] of [[presheaf|presheaves]].

Assume then that another topos $Sh(S) = Sh_S$ is given together with a [[geometric embedding]]

$$
  f : Sh(S) \to PSh(S)
$$

i.e. with a [[full and faithful functor]]

$$
  f_* : Sh(S) \to PSh(S)
$$

and a left [[exact functor]]

$$
  f^* : PSh(S) \to Sh(S)
$$

Such that both form a pair of [[adjoint functor]]s

$$
  f^* \dashv f_*
$$

with $f^*$ [[left adjoint]] to $f_*$.

Write $W$ for the category

$$
  Core(PSh(S)) \hookrightarrow W \hookrightarrow PSh(S)
$$

consisting of all those morphisms in $PSh(S)$ that are sent to [[isomorphism]]s under $f^*$.

$$
  W = (f^*)^{-1}(Core(Sh_S))
  \,.
$$

From the discussion at [[geometric embedding]] we know that $Sh(S)$ is equivalent to the full [[subcategory]] of $PSh(S)$ on all $W$-[[local object]]s.

Recall that an object $A \in PSh(S)$ is called a $W$-[[local object]] if for all $p : Y \to X$ in $W$ the morphism

$$
  p^* : PSh_S(X,A) \to PSh_S(Y,A)
$$

is an [[isomorphism]]. This we call the [[descent]] condition on presheaves (saying that a presheaf "descends" along $p$ from $Y$ "down to" $X$). Our task is therefore to identify the category $W$, show how it determines and is determed by a [[Grothendieck topology]] on $S$ -- equipping $S$ with the structure of a  [[site]] -- and characterize the $W$-[[local object]]s. These are (up to equivalence of categories) the objects of $Sh$, i.e. the sheaves with respect to the given [[Grothendieck topology]].


+-- {: .un_lemma}
###### Lemma

A morphism $Y \to X$ is in $W$ if and only if for every [[representable functor|representable presheaf]] $U$ and every morphism $U\to X$ the pullback $Y \times_X U \to U$ is in $W$
$$
  \array{
     Y \times_X U &\to& Y
     \\
     \downarrow^{\in W} && \downarrow^{\Leftrightarrow \in W}
     \\
     U &\to& X
  }
  \,.
$$
=--



+-- {: .proof}
###### Proof

Since $W$ is stable under [[pullback]] (as described at [[geometric embedding]]: simply because $f^*$ preserves finite limits) it is clear that $Y \times_X U \to U$ is in $W$ if $Y \to X$ is.

To get the other direction, use the [[co-Yoneda lemma]] to write $X$ as a [[colimit]] of [[representable functor|representables]] over the [[comma category]] $(Y/const_X)$ (with $Y$ the [[Yoneda embedding]]):

$$
  X \simeq colim_{U_i \to X} U_i
  \,.
$$

Then pull back $Y \to colim_{U_i \to X} U$ over the entire colimiting cone, so that over each component we have

$$
  \array{
    Y \times_X U_i &\to& Y
    \\
    \downarrow && \downarrow
    \\
    U_i &\to& X
  }
  \,.
$$

Using that in $PSh(S)$ [[commutativity of limits and colimits|colimits are stable under base change]] we get

$$
  colim_i (Y \times_X U_i) \simeq (colim_i U_i) \times_X Y
  \,.
$$

But since $X \simeq colim_i U_i$ the right hand is $X \times_X Y$, which is just $Y$. So $Y = colim_i (Y \times_X U_i)$ and we find that $Y \to X$ is a morphism of colimits. But under $f^*$ the two respective diagrams become isomorphic, since $Y \times_X U_i \to U_i$ is in $W$. That means that the corresponding morphism of colimits $f^*(Y \to X)$ (since $f^*$ preserves colimits) is an isomorphism, which finally means that $Y \to X$ is in $W$.
=--

+-- {: .un_lemma}
###### Lemma

A presheaf $A \in PSh(S)$ is a [[local object]] with respect to all of $W$ already if it is local with respect to those morphisms in $W$ whose codomain is [[representable functor|representable]]
=--


+-- {: .proof}
###### Proof

Rewriting the morphism $Y \to X$ in $W$ in terms of
colimits as in the above proof

$$
  \array{  
     colim_{U \to X} U_i \times_X Y 
      &\stackrel{\simeq}{\to}& Y 
     \\
     \downarrow && \downarrow
     \\
     colim_{U \to X} U &\stackrel{\simeq}{\to}& X
  }
$$

we find that $A(X) \to A(Y)$ equals

$$
  lim_{U \to X} (A(U) \to A(U \times_X Y))
  \,.
$$

If $A$ is local with respect to morphisms $W$ with representable codomain, then by the above if $Y \to X$ is in $W$ all the morphisms in the limit here are isomorphisms, hence

$$
  \cdots = Id_{A(X)}
  \,.
$$
=--


+-- {: .un_lemma}
###### Lemma

Every morphism $Y \to X$ in $W \subset PSh(S)$ factors as an epimorphism followed by a monomorphism in $PSh(S)$ with both being morphisms in $W$.
=--

+-- {: .proof}
###### Proof

Use factorization through [[image]] and [[coimage]], use exactness of $f^*$ to deduce that the factorization exists not only in $PSh(S)$ but even in $W$.

More in detail, given $Y \to X$ we get the diagram

$$
  \array{
    Y \times_X Y &&\to&& Y
    \\
     &&& \swarrow
    \\
    \downarrow &&Y \sqcup_{Y \times_X Y} Y && \downarrow
    \\
    & \nearrow && \searrow
    \\
    Y && \to && X
  }
  \,.
$$

Because $f^*$ is exact, the pullbacks and pushouts in this diagram remain such under $f^*$. But since $f^*(Y \to X)$ is an isomorphism by assumption, the all these are pullbacks and pushouts along isomorphisms in $Sh(S)$, so all morphisms in the above diagram map to isomorphisms in $Sh(S)$, hence the entire diagram in $PSh(S)$ is in $W$.

Since the morphism $Y \sqcup_{Y \times_X Y} Y  \to X$ out of the [[coimage]] is at the same time the [[equalizer|equalizing]] morphism into the [[image]] $lim(X \stackrel{\to}{\to} X \sqcup_Y X)$, it is a [[monomorphism]].
=--


+-- {: .un_definition}
###### Definition

The monomorphisms in $PSh(S)$ which are in $W$ are
called [[dense monomorphism]]s.

=--


+-- {: .un_lemma}
###### Lemma

Every [[monomorphism]] $Y \to X$ with $X$ [[representable functor|representable]] is of the form

$$
  Y = colim ( U \times_X U \to U  )
$$

for $U = \sqcup_{\alpha} U_\alpha$ a disjoint union of representables
=--

+-- {: .proof}
###### Proof

This is a direct consequence of the standard fact that
subfunctors are in bijection with [[sieve]]s.
=--


+-- {: .un_corollary}
###### Corollary

If a presheaf $A$ is [[local object|local]] with
respect to all [[dense monomorphism]]s, then it is already local with respect to all morphisms $Y \to X$ of the form

$$
  \array{
    Y
    \\
    \downarrow
    \\
    X
  }
  =
  colim
  \left(
  \array{
    W &\stackrel{\to}{\to}& U 
    \\
    \;\;\downarrow^{dense mono} && \downarrow^{Id}
    \\
    U \times_X U & \stackrel{\to}{\to}&  U
  }
  \right)
$$

with the left vertical morphism a [[dense monomorphism]]
 
(and with $U = \sqcup_\alpha U_\alpha$ the disjoint union (of representable presheaves) over a [[cover]]ing family of objects.)
=--


+-- {: .un_definition}
###### Definition 

The morphisms in $W$ with representable codomain 


* of the form $colim (U \times_X U \stackrel{\to}{\to} U) \to X$ as above are [[cover]]s:

* of the form $colim (W  \stackrel{\to}{\to} U) \to X$ (with $W$ a cover of $U \times_X U$) as above are [[hypercover]]s

of the representable $X$.
=--




+-- {: .un_proposition}
###### Proposition

A presheaf $A$ is $W$-local, i.e. a sheaf, already if it is local (satisfies [[descent]]) with respect to all [[cover]]s, i.e. all [[dense monomorphism]]s with codomain a [[representable functor|representable]].
=--

>[[Urs Schreiber|Urs]]: the above shows this almost. I am not sure yet how to see the remaining bit directly, without making recourse to the full machinery leading up to section VII, 4, corollary 7 in [[Sheaves in Geometry and Logic]].

So we finally conclude:


+-- {: .un_corollary}
###### Corollaries

We have:

* Systems $W$ of weak equivalences defined by choice of [[geometric embedding]] $f : Sh(S) \to PSh(S)$ are in canonical bijection with choice of [[Grothendieck topology]]. 

* A presheaf $A$ is $W$-local, i.e. local with respect to all [[local isomorphism]]s, if and only if it is local already with respect to all [[dense monomorphism]], i.e. if and only if it satisfies sheaf condition for all covering [[sieve]]s.
=--

From the _assumption_ that $f : Sh(S) \to PSh(S)$ is a [[geometric embedding]] follows at once the following explicit description of the [[sheafification]] functor
$f^* : PSh(S) \to Sh(S)$.

+-- {: .un_lemma}
###### Lemma (Sheafification)

For $A \in PSh(S)$ a presheaf, its [[sheafification]] $\bar A := f_* f^* A$ is the presheaf given by

$$
  \bar A : U \mapsto colim_{(Y \to U) \in W} A(Y)
$$
=--

+-- {: .proof}
###### Proof

By the discussion at [[geometric embedding]] the category $Sh(S)$ is equivalent to the [[localization]] $PSh(S)[W^{-1}]$, which in turn is the category with the same objects as $PSh(S)$ and with morphisms given by spans out of hypercovers in $W$

$$
  PSh(S)[W^{-1}](X,A) =
  colim_{(Y \to X) \in W} A(Y)
  \,.
$$

So we have

$$ \array {
  Sh(S) &&\stackrel{\stackrel{f_*}{\to}}{\stackrel{f^*}{\leftarrow}}&
  PSh(S)
  \\
  & \searrow_{\simeq}&\Downarrow^{\simeq}&  \downarrow
  \\
  &&
  PSh(S)[W^{-1}]
  \,.
} $$

and deduce

* by [[Yoneda lemma|Yoneda]] that $\bar A(U) = PSh_S(U, \bar A)$;

* by the [[adjoint functor|hom-adjunction]] this is $\cdots \simeq Sh_S(\bar U, \bar A)$;

*  by the equivalence just mentioned this is
$\cdots \simeq PSh_S[W^{-1}](U,A)$.
=--



+-- {: .un_remark}
###### Remark: covers versus hypercovers

For checking the sheaf condition the [[dense monomorphism]]s, i.e. the ordinary [[cover]]s are already sufficient. But for [[sheafification]] one really needs the [[local isomorphism]]s, i.e. the [[hypercover]]s. If one takes the colimit in the sheafification prescription above only over [[cover]]s, one obtains instead of sheafification the plus-construction.
=--


+-- {: .un_definition}
###### Definition: plus-construction

For $A \in PSh(S)$ a presheaf, the **plus-construction**
on $A$ is the presheaf 

$$
  A^+ : X \mapsto  colim_{(Y \hookrightarrow X) \in W } A(Y)
$$

where the colimit is over all [[dense monomorphism]]s (instead of over all [[local isomorphism]]s as for [[sheafification]] $\bar A$).
=--

+-- {: .un_remark}
###### Remark: plus-construction versus sheafification

In general $A^+$ is not yet a sheaf. It is however in general closer to being a sheaf than $A$ is, namely it is a [[separated presheaf]].


But applying the plus-construction twice yields the desired sheaf

$$
  (A^+)^+ = \bar A
  \,.
$$

This is essentially due to the fact that in the context of ordinary sheaves discussed here, all [[hypercover]]s are already of the form

$$
  colim(W \stackrel{\to}{\to} U)
$$

for $W \to U \times_X U$ a cover. For higher [[stack]]s the hypercover is in general a longer simplicial object of covers and accordingly if one restricts to covers instead of using hypercovers one will need to use the plus-construction more and more often.
=--



## Examples

The archetypical example of sheaves are _sheaves of [[function]]s_:

* for $X$ a topological space, $\mathbb{C}$ a topological space and $O(X)$ the [[site]] of open subsets of $X$, the assignment $U \mapsto C(U,\mathbb{C})$ of continuous functions from $U$ to $\mathbb{C}$ for every open subset $U \subset X$ is a sheaf on $O(X)$.

* for $X$ a complex manifold and $\mathbb{C}$ a complex manifold, the assignment $U \mapsto C_{hol}{X,\mathbb{C}}$ of holomorphic functions in a sheaf.


## Related concepts

* [[(0,1)-sheaf]] / [[ideal]]

* [[presheaf]] / [[separated presheaf]] /  **sheaf** / [[cosheaf]]

  * [[sheafification]]

  * [[abelian sheaf]], [[sheaf of abelian groups]], [[sheaf of modules]], [[quasicoherent sheaf]], [[sheaf of meromorphic functions]]

  * [[locally constant sheaf]], [[constructible sheaf]]

  * [[sheaf with transfer]]

* [[2-sheaf]] / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 

  * [[sheaf of spectra]]

* [[(∞,2)-sheaf]]

* [[(∞,n)-sheaf]]

* [[abelian sheaf cohomology]]
  
  * [[soft sheaf]]

  * [[fine sheaf]]

  * [[flabby sheaf]]

* [[descent]]

  * [[cover]]

  * [[cohomological descent]]

  * [[descent morphism]]

  * [[monadic descent]], 

    * [[Sweedler coring]]

    * [[higher monadic descent]]

    * [[descent in noncommutative algebraic geometry]]

[[!include homotopy n-types - table]]

## References

The original definition is in

* [[Jean Leray]], _L'anneau d'homologie d'une représentation_.  Comptes rendus hebdomadaires des séances de l'Académie des Sciences 222 (1946), 1366–1368.  [[Leray-0.pdf:file]]

Section C2 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
{#Johnstone}

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
* [[Yuri Manin]], _Methods of homological algebra_

A concise and contemporary overview can be found in

* {#CentazzoVitale04}C. Centazzo, [[Enrico Vitale|E. M. Vitale]], _Sheaf theory_ , pp.311-358 in Pedicchio, Tholen (eds.), _Categorical Foundations_ , Cambridge UP 2004. ([draft](https://perso.uclouvain.be/enrico.vitale/chapter7.pdf))

The book by Kashiwara and Schapira discusses sheaves with motivation from [[homological algebra]], [[abelian sheaf cohomology]] and [[homotopy theory]], leading over in the last chapter to the notion of [[stack]].

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006)

A quick pedagogical introduction with an eye towards the generalization to [[(∞,1)-sheaves]] is in 

* [[Dan Dugger]], _Sheaves and homotopy theory_, [pdf](http://ncatlab.org/nlab/files/cech.pdf)

Classics of sheaf theory on topological spaces are

* Roger Godement, _Topologie alg&#233;brique et th&#233;orie des faisceaux_, Hermann, 1958, 283 p. [gBooks](http://books.google.fr/books/about/Topologie_alg%C3%A9brique_et_th%C3%A9orie_des_fa.html?id=JVrvAAAAMAAJ)

* [[A. Grothendieck]], [[Tohoku]]

Recently, an improvement in understanding the interplay of derived functors (inverse image and proper direct image) in sheaf theory on topological spaces has been exhibited in 

* Olaf M. Schnuerer, Wolfgang Sergel, _Proper base change for separated locally proper maps_, [arxiv/1404.7630](http://arxiv.org/abs/1404.7630)

[[!redirects sheaves]]

[[!redirects sheaf of sets]]
[[!redirects sheaves of sets]]

[[!redirects 1-sheaf]]
[[!redirects (1,1)-sheaf]]

[[!redirects 1-sheaves]]
[[!redirects (1,1)-sheaves]]
