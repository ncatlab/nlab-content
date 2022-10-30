
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}
 
## Idea {#Idea}

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[space]]s inside of which [[geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : \mathcal{E} \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  \mathcal{E} 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  Set
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]) .

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi_0 : \mathcal{E} \to Set$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected components]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $(n-1)$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$. See [[cohesive (∞,1)-topos]].

In total this gives a quadruple of [[adjoint functor]]s

   $$
    (\Pi_0 \dashv Disc \dashv \Gamma \dashv Codisc) : 
    \mathcal{E}
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    Set
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extenson to such a quadruple of adjoints, satisfying some further properties.

Notice that most objects in a cohesive topos are far from being just sets with extra structure: while the functor $\Gamma$ does produce the set of points underlying an object $X$ in the cohesive topos, it may happen that $X$ is very non-trivial but that nevertheless $\Gamma(X)$ has very few [[global element|points]] (possibly none, with the axioms so far). The [[subcategory]] of objects in $E$ that we may think of as point sets equipped with extra structure is the [[quasitopos]] $Conc_\Gamma(E)$ of the [[concrete sheaves]] inside $E$

$$
  Set 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(\mathcal{E}) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  \mathcal{E}
  \,.
$$

It is the fact that $\mathcal{E}$ is a [[local topos]] that allows to identify $Conc_\Gamma(E)$.

To ensure that there is a minimum of points, one can add further axioms. From the above adjunctions one gets a canonical natural morphism

$$
  \Gamma X \to \Pi_0 X
$$

from the points of $X$ to the set of connected pieces of $X$. Demanding this to be an [[epimorphism]] is demanding that _each piece has at least one point_ .

Moreover, one can demand that the cohesive pieces of product or power spaces are the products of the cohesive pieces of the factors.  For powers of a single space, this is demanding that for all $S \in Set$ the following canonical map is an [[isomorphism]]:

$$
  \Pi_0(X^S) \xrightarrow{\simeq} (\Pi_0(X))^S
  \,.
$$

For more general products, it would be a similar map $\Pi_0(\prod_i X_i) \to \prod_i \Pi_0(X_i)$.  See the examples at [[cohesive site]] for concrete illustrations of these ideas.


## Definition


+-- {: .un_defn}
###### Definition

A [[topos]] $\mathcal{E}$ over some base topos $\mathcal{S}$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathcal{S}
$$

is **cohesive** if it has the following [[stuff, structure, property|properties]]:

*  it is _local_ and _connected_ in the following sense:

   1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

   1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is [[fully faithful functor|fully faithful]];

   1. it is _strongly connected_ : $f_!$ preserves even all [[finite]] [[product]]s;

   1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be connected);

In total this means that a topos $\mathcal{E}$ is cohesive over $\mathcal{S}$ if we have a quadruple of [[adjoint functor]]s
   
$$
 (f_! \dashv f^* \dashv f_* \dashv f^!) : 
 \mathcal{E}
  \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
  \mathcal{S}
$$

such that $f_!$ preserves products.

=--

There are several further axioms that one may want to impose in order to formalize the concept of cohesion.

+-- {: .un_defn}
###### Definition

For $f : \mathcal{E} \to \mathcal{S}$ a cohesive topos, we say that 
**cohesive pieces have points** in $\mathcal{E}$ if the [[natural transformation]]

$$
  f_* X
  \stackrel{f_* (\iota_X)}{\to}
  f_* f^* f_! X
  \stackrel{\simeq}{\to}
  f_! X
$$

is an [[epimorphism]] for all $X \in \mathcal{E}$. This is equivalent to the transformation

$$
  f^* S \stackrel{\simeq}{\to} f^* f_* f^! S \stackrel{\epsilon_{f^! S}}{\to} f^! S
$$

being a [[monomorphism]] for all $S \in \mathcal{S}$ .


We say **pieces of powers are powers of pieces** if for all $S \in \mathcal{S}$ and $X \in E$ the natural morphism

$$
  f_! (X^{f^* S}) \stackrel{\simeq}{\to} (f_!(X))^S
$$

is an [[isomorphism]]

(this morphism is the [[internal hom]]-[[adjunct]] of 
$
  S \times f_!(X^{f^* S}) 
   \stackrel{\simeq}{\to}
  f_!f^*(S) \times f_!(X^{f^* S})
   \stackrel{\simeq}{\to}
  f_!(f^*(S) \times X^{f^* S})
  \to
  f_!(X)
$

where we use that by definition $f^*$ is full and faithful and then that $f_!$ preserves products).

=--

These two axioms are considered in [Lawvere, Axiomatic cohesion](#LawvereAxiomatic).

+-- {: .un_defn}
###### Definition

For $f : \mathcal{E} \to \mathcal{S}$ a cohesive topos, we say that 
its **subobject classifier is contractible** if for the [[subobject classifier]] $\Omega \in \mathcal{E}$ we have

$$
  f_!(\Omega) \simeq *
  \,.
$$

This implies that for all $X \in \mathcal{E}$ also $f_! \Omega^X \simeq *$.


=--

This appears as axiom 2 in ([Lawvere, Categories of spaces](#LawvereCatsOfSpaces)).


## Properties {#Properties}

Let $f : \mathcal{E} \to \mathcal{S}$ be a cohesive topos. 

It comes canonically with various [[subcategories]], sub-[[quasi-toposes]] and [[subtopos]]es of interest. 

### Subtoposes of discrete and codiscrete objects {#DiscreteSubtop}

The topos $\mathcal{S}$ is a subtopos of $f = (\Pi_0 \dashv Disc \dashv \Gamma dashv CoDisc) : \mathcal{E}\to \mathcal{S}$ by a [[geometric embedding]] in two ways.

1. By the fact that $f$ is a [[local geometric morphism]] we have that $Disc$ is a [[full and faithful functor]], hence that

   $$
    (\Pi_0 \dashv Disc) : \mathcal{S} \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\hookrightarrow}}
     \mathcal{S}
   $$

   is a geoemtric embedding. This is the **subtopos of discrete objects** .

1. The fact that $f$ is a [[local geometric morphism]] implies, in particular, that $CoDisc$ is a full and faithful functor, hence that

   $$
     (\Gamma \dashv CoDisc)
     \mathcal{S} 
       \stackrel{\overset{f_*}{\leftarrow}}{\underset{f^!}{\hookrightarrow}} 
     \mathcal{E}
   $$ 

   is a [[subtopos]]. This is the **subtopos of codiscrete objects**.


=--

### Quasitoposes of concrete objects {#ConcreteObjects}

Let $(C,J)$ be a [[site]] with of definition for $\mathcal{E}$ with [[coverage]] $J$, so that $\mathcal{E} = Sh_J(C) \hookrightarrow PSh(C)$. Since by the [above](#DiscreteSubtop) $Set \stackrel{CoDisc}{\hookrightarrow} \mathcal{E}$ is a subtopos, we have that $Set$ is itself a [[category of sheaves]] on $C$

$$
  Set \simeq Sh_K(C) \stackrel{CoDisc}{\hookrightarrow} Sh_J(C) \hookrightarrow PSh(C)
$$

which must correspond to another [[coverage]] $K$:  $Set \simeq Sh_K(C)$. Since we have this sequence of inclusions, we have an inclusion of coverages $J \subset K$.


+-- {: .un_defn}
###### Definition

A **[[concrete sheaf|concrete object]]** of the cohesive topos $\mathcal{E}$ is a $(J,K)$-[biseparated presheaf]] on $C$. 

The [[quasitopos]]

$$
  Conc(\mathcal{E}) := BiSep_{(J,K)}(C) \hookrightarrow \mathcal{E}
$$

we call the **subcategory of concrete objects** of $\mathcal{E}$.

=--


### Objects with one point per cohesive piece

+-- {: .un_theorem}
###### Theorem


Let $(\Pi \dashv Disc \dashv \Gamma \dashv Codisc) :  \mathcal{E} \to \mathcal{S}$ be a cohesive topos with $\Gamma X \to \Pi X$ an [[epimorphism]] for all $X$.

Let $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ be the [[full subcategory]] on those objects $X$ for which $\Gamma X \to \Pi X$ is an [[isomorphism]]. Then

1. $\mathcal{L}$ is a [[reflective subcategory]] and a [[coreflective subcategory]]

   $$
     (s_! \dashv s^* \dashv s_*)
     : 
     \mathcal{E}
       \stackrel{\overset{s_!}{\to}}{\stackrel{\overset{s^*}{\leftarrow}}{\underset{s_*}{\to}}}
     \mathcal{L} 
   $$

1. $s_*$ preserves [[coproduct]]s.

1. the components of the reflector $X \to s_! s^* X$ are [[epimorphism]]s.

=--

This is [theorem 2](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf#page=5) in ([Lawvere](#Lawvere)).

+-- {: .proof}
###### Proof

Since $\Gamma$ is a [[left adjoint]] it preserves [[colimit]]s, as does of course $\Pi$. Therefore the collection of objects for which $\Gamma X \to \Pi X$ is an isomorphism is closed under colimits and hence $\mathcal{L}$ has all colimits and the inclusion $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ obviously preserves them. 

To apply the [[adjoint functor theorem]] to deduce that therefore $s^*$ has a right adjoint $s_*$ it is sufficient to argue that $\mathcal{L}$ is a [[locally presentable category]]. To see this, notice that $\mathcal{L} \hookrightarrow \mathcal{E}$ is the [[inverter]] of $\Gamma \to \Pi$, a certain [[2-limit]] in [[Cat]].  Since the 2-category of [[accessible categories]] and [[accessible functors]] is closed under (non-strict) [[2-limit]]s in [[Cat]], it follows that $\mathcal{L}$ is accessible. Since we already know that it is also cocomplete it follows that it must be locally presentable.

Since $\Pi$ by assumption preserves finite products and $\Gamma$ preserves all products, it follows that $L$ is also closed under finite products and in particular contains the [[terminal object]] $*$. Since $\mathcal{E}$, being a [[topos]], is an [[extensive category]], it follows that $s_*$ preserves coproducts.

(...details...)

Using that $\Gamma X \to \Pi X$ is an epi, we find that $\mathcal{L}$ is also closed under [[subobject]]s: if $Y \hookrightarrow X$ is a [[monomorphism]] then if in

$$
  \array{
     \Gamma Y &\to& \Gamma X
     \\
     \downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     \Pi Y &\to& \Pi X
  }
$$

the right vertical morphism is an iso, then so is the left vertical one.

(...details...).

It then also follows that $\mathcal{L}$ is closed under arbitrary products.

(...details...)

This implies the existence of $s_!$ and the fact that $X \to s^* s_! X$ is epi.

(...details...)

=--



## Examples

### Over a cohesive site

A class of examples is obtained from toposes over a [[cohesive site]]:

+-- {: .un_theorem}
###### Theorem

Let $C$ be a [[cohesive site]]. The [[sheaf topos]] $Sh(C)$ is cohesive.

=--

See [[cohesive site]] for examples.

#### Diffeological spaces

+-- {: .un_prop}
###### Proposition

The site [[CartSp]] with the standard [[open cover]] [[coverage]] is a [[cohesive site]] and even an [[(∞,1)-cohesive site]]. 

=--

+-- {: .un_prop}
###### Proposition

The quasitopos $Conc(Sh(CartSp))$ of [concrete objects](#ConcreteObjects)
in the cohesive topos over $CartSp$ is the category of [[diffeological space]]s.

=--

+-- {: .proof}
###### Proof

A sheaf $X$ on $CartSp$ is a [[separated presheaf]] with respect to the further localization given by $CoDisc$ precisely if the canonical morphism (the [[unit of an adjunction|unit]] of $(\Gamma \dashv CoDisc)$)

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that this is equivalent to 

$$
  Hom(U,X) \simeq X(U) \to Hom(U,CoDisc \Gamma X)
$$

being a monomorphism for all $U \in C$ (where in the first step we used the [[Yoneda lemma]]). By the adjunction relation this is equivalently

$$
  X(U) \to Set(\Gamma(U), \Gamma(X))
  \,.
$$

This being a monomorphism is precisely the condition on $X$ being a [[concrete sheaf]] on $CartSp$ that singles out diffeological spaces among all sheaves on $CartSp$.

=--


#### Smooth toposes

+-- {: .un_prop}
###### Proposition

The site [[ThCartSp]] with the standard [[open cover]] [[coverage]] is a [[cohesive site]] and even an [[(∞,1)-cohesive site]]. 

=--


The corresponding cohesive topos is the [[Cahiers topos]] $ \simeq Sh(ThCartSp)$. This is a [[smooth topos]] that models the axioms of 
[[synthetic differential geometry]].


### Simplicial sets {#SimplicialSets}

Let $C = \Delta$ be the [[simplex category]], regarded as a [[site]] with the trivial [[coverage]].

The corresponding [[sheaf topos]] $Sh(\Delta)$ is the [[presheaf topos]] $E = PSh(\Delta) = $ [[sSet]] of [[simplicial set]]s. 

We have for $X \in sSet$

* $\Gamma : X \mapsto X_0$;

* $\Pi_0 : X \mapsto \pi_0(X) = X_0/X_1$, the set of [[simplicial homotopy group|connected components]].

And for $S \in Set$:

* $Disc S$ the constant simplicial set on $S$;

* $Codisc S$ the simplicial set which in degree $k$ has the set of $(k+1)$-tuples of elements of $S$.


If $X, Y \in sSet$ are [[Kan complex]]es, then $\Pi_0(Y^X)$ is the set of [[simplicial homotopy]]-classes of maps $X \to Y$. We can therefore write the [[homotopy category]] of Kan complexes as

$$
  Ho_{KanCplx}(X,Y) = \Pi_0(Y^X)
  \,.
$$

### Counter-examples {#CounterExamples}

+-- {: .un_example}
###### Counter-Example

Let $G$ be a non-trivial [[finite group]] of [[cardinality]] $n$. Write $\mathbf{B}G = \{\bullet \stackrel{g}{\to} \bullet | g \in G\}$ for its [[delooping]] [[groupoid]]. The [[presheaf topos]]

$$
  PSh(\mathbf{B}G) \simeq G Set
$$

is the category of [[permutation representation]]s of $G$. It comes with a triple of adjoint functors

$$
  (\Pi_0 \dashv Const \dashv \lim_\leftarrow) : G Set 
    \stackrel{\overset{\lim_\to}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\to}}}
   Set
  \,.
$$


The colimit over a representation $(V, \rho) : \mathbf{B}G \to Set$ is [[quotient]] set $V/\rho(G)$. So we have

$$
  \Pi_0(G) \simeq *
$$

but

$$
  \Pi_0(G \times G) \simeq \bar n
  \,,
$$

where $G$ denotes the fundamental representation of $G$ on itself. Therefore $\Pi_0$ does not preserve products in this case.

=--



## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* **cohesive topos** / [[cohesive (∞,1)-topos]]




## References

The axioms for a cohesive topos originate in

* [[Bill Lawvere]], _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_ , preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.144.6357&rep=rep1&type=pdf))
{#LawvereCatsOfSpaces}

where however the term "cohesive topos" was not yet used. Under the name _categories of cohesion_ these axioms are discussed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#LawvereAxiomatic}

(This demands the conditions that "cohesive piece have points" and "pieces of powers are powers of pieces" as part of the definition of "category of cohesion".)

This builds on a series of precursors of attempts to identify axiomatics for [[gros topos]]es.

In 

* [[Bill Lawvere]], _Categories of space and quantity_ in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter, Berlin, New York (1992)

  a proposal for a general axiomatization of [[homotopy]]/[[homology]]-like "extensive quantities" and [[cohomology]]-like "intensive quantities") as covariant and contravariant functors out of a distributive category are considered.

The left and right adjoint to the global section functor as a means to identify discrete spaces and codiscrete space is mentioned

* [[Bill Lawvere]] _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

on [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14).

[[!redirects cohesive topos]]
[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]
