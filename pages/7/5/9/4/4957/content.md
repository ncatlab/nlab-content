+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Local geometric morphism and relative local topos

+-- {: .num_defn}
###### Definition

A **local geometric morphism** $f : E \to S$ between [[topos]]es $E,S$ is 

*  a [[geometric morphism]]

   $$
    (f^* \dashv f_*) \colon E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  S
   $$

*  such that a further [[right adjoint]] $f^! : S \to E$ exists 

   $$
    (f^* \dashv f_* \dashv f^!) : 
    E
    \stackrel{\overset{f^*}{\longleftarrow}}{\stackrel{\underset{f_*}{\longrightarrow}}{\underset{f^!}{\longleftarrow}}}
    S
   $$

*  and such that one, hence all, of the following equivalent conditions hold:

   1. The right adjoint $f^!$ is an $S$-[[indexed functor]].
   1. $f$ is [[connected geometric morphism|connected]], i.e. $f^*$ is [[full and faithful functor|fully faithful]].
   1. The right adjoint $f^!$ is fully faithful.
   1. The right adjoint $f^!$ is [[cartesian closed functor|cartesian closed]].

=--

When we regard $E$ as a topos over $S$, so that $f$ is regarded as its [[global section]] geometric morphism in the category of toposes over $S$, then we say that $E$ is a **local $S$-topos**.  In this case we may label the functors involved as

$$
  (Disc \dashv \Gamma \dashv Codisc) : 
    E
    \stackrel{\overset{Disc}{\longleftarrow}}{\stackrel{\underset{\Gamma}{\longrightarrow}}{\underset{Codisc}{\longleftarrow}}}
    S
$$

to indicate that if we think of $\Gamma$ as sending a [[space]] to its underlying $S$-object of points by forgetting [[cohesive topos|cohesion]], then $Disc$ creates the [[discrete space]]/[[discrete object]] and $Codisc$ the [[codiscrete space]]/[[codiscrete object]] on an object in $S$.

This is especially common when $S=$ [[Set]], in which case the final condition is automatic since all functors are $Set$-indexed. Hence in that case we have the following simpler [definition](local). 

### Local topos
 {#LocalTopos}

+-- {: .num_defn #local}
###### Definition

A [[sheaf topos]] $\mathcal{T}$ is a **local topos** if the [[global section]] [[geometric morphism]] $\mathcal{T} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}} Set$ has a further [[right adjoint]] $CoDisc$, making an [[adjoint triple]]  $(LConst \dashv \Gamma \dashv CoDisc)$

$$
  CoDisc \colon Set \hookrightarrow \mathcal{T}. 
$$ 

(As just stated, it is automatic in the case over $Set$ that this is furthermore a [[full and faithful functor]].) 

=-- 

+-- {: .num_remark}
###### Remark

Another way of stating this is that a Grothendieck topos is local if and only if the terminal object $1$ is [[connected object|connected]] and [[projective object|projective]] (since this means precisely that $\Gamma = \hom(1, -)$ preserves colimits, and therefore has a right adjoint by virtue of an [[adjoint functor theorem]]). Another term for this: we say $1$ is _[[tiny object|tiny]]_ ([[atomic object|atomic]]). Notice the similarity to the concept of _[[amazing right adjoint]]_ (the difference being that this is a right adjoint not to the external but to the [[internal hom]] out of 1.)

=--

Note also that in an infinitary-[[extensive category]] an object is connected as soon as $\hom(X,-)$ preserves *binary* coproducts (see [[connected object]]).  Moreover, a coproduct-preserving functor between toposes preserves coequalizers as soon as it preserves epimorphisms, since any coequalizer can be constructed as the quotient of an equivalence relation generated using images and countable coproducts and quotients of equivalence relations are effective.  Thus, we can say that a Grothendieck topos is local iff $\hom(1,-)$ preserves binary coproducts and epis.  Moreover, a cospan $A \to C \leftarrow B$ in a topos is a coproduct diagram iff $A$ and $B$ are disjoint monos whose union is all of $C$; thus $\hom(1,-)$ preserves binary coproducts as soon as it preserves the initial object and binary unions.  This leads to the following equivalent form of "locality" that makes sense even for elementary toposes:

+-- {: .num_defn} 
###### Definition 
An [[elementary topos]] $E$ is *local* if the terminal object $1$ is 

* nonempty: $1\ncong 0$,

* connected: $1 = p \vee q$ implies $1 = p$ or $1 = q$, and 

* projective: every epi $U \to 1$ admits a section $t: 1 \to U$. 
=-- 


+-- {: .num_remark} 
###### Remark 
Some authors have instead used the term "local" to refer just to the condition that $1$ is connected; note this is equivalent to $Sub_E(1)$ being a [[local ring|local rig]]. In his [thesis](#Awodey), Steve Awodey upgraded this, saying that a topos is *hyperlocal* if both connectivity and projectivity are satisfied. As argued above, for a Grothendieck topos this is slightly *weaker* than locality, although the difference is only in the inclusion of the trivial topos (for if $1\cong 0$ then $E\simeq 1$).  Note that a local elementary topos, as defined above, is [[well-pointed topos|constructively well-pointed]] if and only if $1$ is additionally a [[generator]].
=-- 

+-- {: .num_example} 
###### Example 
The [[free topos]] is a local elementary topos. 
=-- 

## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

+-- {: .num_prop}
###### Proposition

A geometric morphism $f : E \to S$ is local precisely if

1. there exists a geometric morphism $c : S \to E$ such that $f \circ c \simeq id$;

1. for every other geometric morphism $g : G \to S$ the composite $c\circ g$ is an [[initial object]] in the hom-category $Topos_{/S}(g,f)$ of the [[slice category|slice]] [[2-category]]  of [[Topos]] over $S$.

=--

This is ([Johnstone, theorem 3.6.1 vi)](#Johnstone)).

+-- {: .num_remark}
###### Remark

In particular this means that the category of [[topos points]] of a local topos has a [[contractible]] [[nerve]].

=--



### General

+-- {: .num_prop}
###### Proposition

The [[global section]] geometric morphism of any local $\mathcal{S}$-topos (over a [[base topos]] $\mathcal{S}$) is a [[Grothendieck fibration]] and a [[Grothendieck opfibration]].

=--

This appears in ([Shulman](#Shulman)).

+-- {: .num_prop}
###### Proposition

The [[Freyd cover]] of a [[topos]] is a [[local topos]], and in fact freely so. Every local topos is a [[retract]] of a Freyd cover.

=--

This appears as ([Johnstone, lemma C3.6.4](#Johnstone)).

### Homotopy dimension
 {#HomotopyDimension}

+-- {: .num_prop}
###### Proposition

In a local [[sheaf topos]] over [[Set]], every [[inhabited object]] is globally inhabited:

every object $X$ for which the unique morphism $X \to *$ to the [[terminal object]] is an [[epimorphism]] has a [[global point]] $* \to X$.

=--

+-- {: .proof}
###### Proof

Since in a local topos the [[global section]] functor $\Gamma$ is a [[left adjoint]], it preserves [[epimorphisms]]. Since it is a right adjoint it preserves the terminal object. Therefore $\Gamma(X) \to \Gamma(*) \simeq *$ is an epimorphism in [[Set]], hence a [[surjection]], meaning that $\Gamma(X)$ is [[inhabited]]. Since $\Gamma(X) \simeq Hom(*,X)$ (see [[global section geometric morphism]]), the claim follows.

=--

+-- {: .num_remark}
###### Remark

In a [[topos]] every [[epimorphism]] is an [[effective epimorphism]]. Therefore $X \to *$ being an epi means that $X$ is a [[(-1)-connected]] object. Therefore the above statement says in terms of [[(infinity,1)-category theory]] that a non-trivial local topos has [[homotopy dimension]] 0.

The same is true for any [[local (infinity,1)-topos]].

=--



### Concrete sheaves

Every local topos $\Gamma : E \to S$ comes with a notion of [[concrete sheaves]], a [[reflective subcategory]] $Conc_\Gamma(E) \hookrightarrow E$ which factors the topos inclusion of $S$:

$$
  S 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(E) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  E
$$

and is a [[quasitopos]]. See [[concrete sheaf]] for details.

### Homotopy equivalence

Since a local geometric morphism has a [[left adjoint]] in the [[2-category]] [[Topos]], it is necessarily a [[homotopy equivalence of toposes]].

## Elementary Axiomatization
 {#ElementaryAxiomatization}

For any local topos $\Gamma \colon \mathcal{E} \to \mathcal{S}$, the base topos $\mathcal{S}$ is equivalent to the [[category of sheaves]] for a [[Lawvere-Tierney topology]] $j$ on $\mathcal{E}$.  A sound and complete elementary [[axiomatization]] of local maps of (bounded) toposes can be given in terms of properties of topos $E$ and topology $j$ ([AwodeyBirkedal](#AwodeyBirkedal))

We discuss first

* [the setup](#SetupForAxiomatization)

and then

* [the axioms](#TheAxioms)

themselves.


### The setup
 {#SetupForAxiomatization}

Let $\mathcal{E}$ be an [[elementary topos]] equipped with a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$.

Write $V \mapsto \sharp  V$ for the $j$-[[closure operation]] on [[subobjects]] $V \hookrightarrow X$, the _[[sharp modality]]_

$$
  \array{
    V &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \sharp  V &\to& &\to& {*}
    \\
    \downarrow && \downarrow  &&  \downarrow 
    \\
    X &\stackrel{\chi_V}{\to}& \Omega 
    &\stackrel{j}{\to}&
    \Omega
  }
$$

Write

$$
  (\Gamma \dashv coDisc)
  : 
  Sh_j(\mathcal{E})
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\to}}  
  \mathcal{E}
$$

for the [[reflective subcategory]] [[category of sheaves|of j-sheaves]].

+-- {: .num_defn #EssentialTopology}
###### Definition

We say that $j$ is an **[[essential geometric morphism|essential]] topology** if for all objects $X$ the closure operation $\sharp  : Sub(X) \to Sub(X)$ on [[posets of subobjects]] has a [[left adjoint]] $\flat \dashv \sharp $:

$$
  (U \hookrightarrow \sharp  V)
   \Leftrightarrow
  (\flat U \hookrightarrow V)
  \,.
$$

=--

This appears under the term "principal" in ([Awodey-Birkedal, def. 2.1](#AwodeyBirkedal)). 

+-- {: .num_remark}
###### Remark

We use the notation "$\flat$" and "$\sharp $" oppositely to the use on p.14 of [Awodey-Birkedal](#AwodeyBirkedal). Our convention is such that it harmonizes with the terminology at _[[cohesive topos]]_ and _[[cohesive (infinity,1)-topos]]_, where it makes interpretational sense to pronounce "$\flat$" as "flat".

=--

+-- {: .num_observation}
###### Observation

The left adjoints $\flat : Sub(X) \to Sub(X)$ for all $X \in \mathcal{E}$
extend to a functor $\flat : \mathcal{E} \to \mathcal{E}$ on all of $\mathcal{E}$.

=--

+-- {: .proof}
###### Proof

(...)

=--


+-- {: .num_prop #InternalCharacterizationOfLocalReflection}
###### Proposition

A [[Lawvere-Tierney topology]] $j$ is [essential](#EssentialTopology), $(\flat \dashv \sharp )$, precisely if for all objects $X$ there exists a least $\sharp $-[[dense subobject]] $U_X \hookrightarrow X$.

=--

This appears as ([AwodeyBirkedal, lemma 2.3](#AwodeyBirkedal)). 

+-- {: .proof}
###### Proof

By the discussion at [[category of sheaves]] we have that $\sharp $ is given by the composite

$$
  \sharp  : \mathcal{E} \stackrel{\Gamma}{\to} Sh_j(\mathcal{E}) \stackrel{coDisc}{\hookrightarrow} \mathcal{E}
  \,,
$$

where the first morphism is [[sheafification]] and the second is [[full and faithful functor|full and faithful]]. 

If now the [[left adjoint]] $\flat$ exists, it follows that this comes from a left adjoint $Disc$ to $\Gamma$ as

$$
  \flat
   : 
  \mathcal{E}
   \stackrel{\overset{Disc}{\hookleftarrow}}{\underset{\Gamma}
{\to}}
  Sh_j(\mathcal{E})
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\hookrightarrow}}
  \mathcal{E}
  : 
  \sharp 
  \,.
$$

Therefore the $(Disc \dashv \Gamma)$-[[counit of an adjunction|counit]] provides morphisms

$$
  (\flat X \to X) = (\flat X \to U_x \hookrightarrow X)
  \,,
$$

whose [[image]] factorization $U_x \hookrightarrow X$
we claim provides the least dense subobjects. 

To show that $U_X$ is dense it is sufficient to show
that 

$$
  \sharp (\flat X \to X)
  = 
  (coDisc \Gamma Disc \Gamma \to coDisc \Gamma X)
$$

is an [[isomorphism]].

Composing this morphism with $CoDisc$ of the $(Disc \dashv\Gamma)$-unit on $\Gamma X$ (which is an [[isomorphism]] since $Disc$ is a [[full and faithful functor]] by the discussion at _[fully faithful adjoint triples](adjoint+triple#FullyFaithFulAdjointTriples)_) and using the $(Disc \dashv \Gamma)$ [[triangle identity]] we have 

$$
  coDisc(
    \Gamma X 
      \stackrel{\simeq}{\to}
    \Gamma Disc \Gamma X
      \stackrel{}{\to}
    \Gamma X
  )
  = 
  coDisc ( \Gamma X \stackrel{Id}{\to} \Gamma X)
  \,.
$$

Using that also $coDisc$ is full and faithful and then [[2-out-of-3]] for [[isomorphisms]] it follows that $coDisc \Gamma Disc \Gamma X \stackrel{\simeq}{\to} coDisc \Gamma X$ hence

$$
  \sharp  \flat X \stackrel{\simeq}{\to} \sharp  X
$$

is indeed an isomorphism. 

Moreover, by one of the equivalent characterizations of [[reflective subcategories]] we have (...)


=--


+-- {: .num_defn #DiscreteObjects}
###### Definition

An object $X \in \mathcal{E}$ is called **discrete** if 
for all $\Gamma$-[[local isomorphisms]] $f : A \to B$ the induced morphism

$$
  \mathcal{E}(X,A) \to \mathcal{E}(X,B)
$$

is an [[isomorphism]] (of sets, hence a bijection).

=--

+-- {: .num_defn #ODiscreteObjects}
###### Definition

An object $X \in \mathcal{E}$ is called **o-discrete** if $\flat X \simeq X$.

=--

+-- {: .num_lemma }
###### Lemma

Every discrete object is o-discrete.

=--



### The axioms

 {#TheAxioms}

+-- {: .num_defn }
###### Definition

On $\mathcal{E}$ a [[elementary topos]] with [[Lawvere-Tierney topology]] $j$ consider the following axioms.

* **Axiom 1**. $j$ is [essential](#EssentialTopology).

* **Axiom 2 a**. There is an object $G \in \mathcal{E}$ such that every object is a [[subquotient]] of the [[product]] of a [discrete object](#DiscreteObjects) with $G$.

* **Axiom 2 b**. With $G$ as above, there is a discrete object $G'$ and an [[epimorphism]] $G' \to \flat G$.

* **Axiom 3**. For all [discrete objects](#DiscreteObjects) $D$, if the [[internal hom]] $[X,D]$ is  [o-discrete](#ODiscreteObjects), then $X$ is also discrete.

* **Axiom 4**. [Discrete objects](#DiscreteObjects) are closed under binary [[products]].

=--

+-- {: .num_theorem }
###### Theorem

These axioms characterize local geometric morphisms $\mathcal{E} \to Sh_j(\mathcal{E}) \simeq D_j(\mathcal{E})$.

If $G$ is fixed to be the terminal object (in which case Axiom 2 b becomes empty), then they characterize local and [[localic geometric morphisms]].

=--

This is ([Awodey-Birkedal, theorem 3.1](#AwodeyBirkedal)) together with the discussion around remark 3.7.

## Examples

### Easy examples
 {#EasyExamples}

+-- {: .num_example #PresheafToposOverSiteWithTerminal}
###### Example

If $C$ is a [[small category]] with a [[terminal object]] $* \in C$, then the [[presheaf topos]] $[C^{op},Set]$ is a local topos.

=--

+-- {: .proof}
###### Proof

Notice that $Set \simeq [*,Set]$ is the presheaf topos over the point category, the category with a single object and a single morphism. Therefore the constant presheaf functor

$$
  Const : Set \to [C^{op}, Set]
$$

can be thought of as sending a set $S \in Set$, hence a functor $S : * \to Set$ to the composite functor 

$$
  Const(S) \colon C \to * \stackrel{S}{\to} Set
  \,.
$$

Notice that in the presence of a terminal object in $C$, $Const$ is a [[full and faithful functor]]: a [[natural transformation]] $Const(S_1) \to Const(S_2)$ has components

$$
  \array{
    S_1 = & Const(S_1)(*) &\stackrel{f}{\to}& Const(S_2)(*) & = S_2
    \\
    & \downarrow^{\mathrm{id}} && \downarrow^{\mathrm{id}}
    \\
    & Const(S_1)(U) &\to& Const(S_2)(U)
  }
$$

where the vertical morphisms are $Const(U \to *)$, the point being that they exist for every $U \in C$ given the presence of the terminal object. It follows that such a natural transformation is given by any and one and the same [[function]] $f \colon S_1 \to S_2$.

The functor $Const$ has a [[left adjoint]] and a [[right adjoint]], and these are -- essentially by definition -- the [[colimit]] and the [[limit]] operations

$$
  (\underset{\rightarrow}{\lim} \vdash Const \vdash \underset{\leftarrow}{\lim})
$$

which send a presheaf/functor $F \colon C^{op} \to Set$ to its [[colimit]] $\underset{\rightarrow}{\lim} F \in Set$ or [[limit]] $\underset{\leftarrow}{\lim} F \in Set$, respectively. 

Since adjoints are essentially unique, it follows that the [[global section]] functor $\Gamma \colon [C^{op}, Set]$ is given by taking the limit, $\Gamma \simeq \underset{\leftarrow}{\lim}$. 

Observe that the [[terminal object]] $* \in C$ is the [[initial object]] in the [[opposite category]] $C^{op}$. But the limit over a [[diagram]] with initial object is given simply by evaluation at that object, and so we have for any $F \in [C^{op}, Set]$ that

$$
  \begin{aligned}
    \Gamma(F) & \simeq \underset{\leftarrow}{\lim} F
    \\
    & \simeq F(*) \in Set
  \end{aligned}
$$

hence that the global section functor is simply given by evaluating a presheaf on the terminal object of $C$. 

Limits and colimit _in_ a presheaf category $[C^{op}, Set]$ are computed objectwise over $C$ (see at _[[limits and colimits by example]]_). Therefore evaluation at any object in $C$ preserves in limits and colimits, and in particular evaluation at the terminal object does. Therefore $\Gamma$ preserves all colimits. Hence by the [[adjoint functor theorem]] it has a further [[right adjoint]] $CoDisc$.

We can compute it explicitly by the  [[Yoneda lemma]] and using the defining Hom-isomorphism of adjoints to be the functor $CoDisc \colon Set \to [C^{op}, Set]$ such that for $S \in Set$ the presheaf $CoDisc(S)$ is given over $U \in C$ by

$$
  \begin{aligned}
   CoDisc(S)(U) & \underoverset{Yoneda}{\simeq}{\to} Hom_{[C^{op}, Set]}(U,CoDisc(S))
    \\
    & \underoverset{adjunction}{\simeq}{\to} Hom_{Set}(\Gamma(U), S)
    \,.
  \end{aligned}
$$

So in conclusion we have an [[adjoint triple]] $(Const \vdash \Gamma \vdash CoDisc)$ where $Const$ is a [[full and faithful functor]]. By the discussion at _[fully faithful adjoint triples](adjoint+triple#FullyFaithFulAdjointTriples)_ it follows then that also $CoDisc$ is full and faithful.

=--



 


+-- {: .num_prop}
###### Proposition

The converse to prop. \ref{PresheafToposOverSiteWithTerminal} is true if $C$ is [[Cauchy complete category|Cauchy complete]].

=--



+-- {: .num_example}
###### Example

If $X$ is a [[topological space]], or more generally a [[locale]], then $Sh(X)$ is local (over Set) iff $X$ has a [[focal point]] $x$, i.e. a point whose only [[neighborhood]] is the whole space. In this case, the extra right adjoint $f^! : Set \to Sh(X)$ to the global sections functor $f_* : Sh(X) \to Set$ is given by the functor which computes the stalk at $x$. This can also be given without reference to $x$, by the formula
$$ \Gamma(U, f^!(M)) = Hom(\{\star|U=X\}, M) \cong
  \begin{cases} M, & U = X, \\ \{\star\}, & U \neq X, \end{cases} $$
for sets $M$ and open subsets $U \subseteq X$. 

=--

### Sheaves on a local site

For $C$ a [[local site]], the [[category of sheaves]] $Sh(C)$ is a local topos over $Set$.

For instance [[CartSp]] is a local site. Objects in $Sh(C)$ are [[generalized smooth spaces]] such as [[diffeological space]]s.
The further right adjoint

$$
  Codisc : Set \to Sh(CartSp)
$$

is the functor that sends a set to the [[diffeological space]] on that set with _[[codiscrete space|codiscrete]]_ smooth structure (every map of sets is smooth). 


### Relative Realizability

Let $A$ be a partial combinatory algebra and let $A\sharp\subseteq A$ be 
a sub partial combinatory algebra of $A$. Then there is a
(localic) local geometric morphism from the [[relative realizability topos]]
$\mathrm{RT}(A,A\sharp)$ to the standard [[realizability topos]]
$\mathrm{RT}(A\sharp)$. 

### Localization

Let $LocTopos$ denote the 2-category of local [[Grothendieck toposes]] (over Set) with all geometric morphisms between them.  Let $PTopos$ denote the 2-category whose objects are [[pointed topos|pointed toposes]] (i.e. (Grothendieck) toposes $E$ equipped with a geometric morphism $s\colon Set\to E$), and whose morphisms are pairs $(f,\alpha)$ such that $f\colon E\to E'$ is a geometric morphism and $\alpha\colon s'\to f s$ is a (not necessarily invertible) geometric transformation.

Note that if $E$ is a local topos with global sections geometric morphism $e^*\dashv e_*$, then the adjunction $e_*\dashv e^!$ is also a geometric morphism $Set\to E$.  In this way we have a functor $LocTopos \to PTopos$, which is a full embedding, and turns out to have a [[right adjoint]]: this right adjoint is called the **localization** of a pointed topos at its specified point.  For example:

+-- {: .num_prop #LocalizationOfPresheafTopos}
###### Proposition

If $C$ is a [[small category]] and $U$ is an object of $C$, then the localization of the [[presheaf topos]] $[C^{op},Set]$ at the point induced by $U\colon 1\to C$ can be identified with the [[presheaf topos]] $[(C/U)^{op},Set]$ over the [[over category]] of $C$ over $U$. By the general properties of [[over topos]]es, this is equivalently the over-topos $PSh(C)/U$ (where $U$ is regarded in $PSh(C)$ by the [[Yoneda embedding]]).

=--

+-- {: .num_prop }
###### Proposition


If $X=Spec(A)$ is the [[Zariski spectrum]] of a [[commutative ring]] $A$, and $P\subset A$ is a prime ideal of $A$ (i.e. a point of $X$), then the localization of $Sh(X)$ at $P\colon 1\to X$ can be identified with $Sh(Spec(A_P))$, where $A_P$ denotes the [[localization]] of $A$ at $P$.  Of course, this is the origin of the terminology.

=--

A similar construction is possible for [[bounded geometric morphism|bounded]] toposes over any base (not just Set).


### Local over-toposes 
  {#LocalOverTopoes}


+-- {: .num_prop }
###### Proposition

For $\mathcal{E}$ a [[Grothendieck topos]] and $X \in \mathcal{E}$ an object, the [[over topos]] $\mathcal{E}/X$ is local if $X$ is a [[tiny object]] ([[atomic object]]). 

=--

+-- {: .proof}
###### Proof

We check that the [[global section]] [[geometric morphism]] $\Gamma : \mathcal{E}/X \to Set$ preserves [[colimit]]s. It is given by the [[hom-functor]] out of the [[terminal object]] of $\mathcal{E}/X$, which is $(X \stackrel{Id}{\to} X)$:

$$
  \Gamma : (A \stackrel{f}{\to} X) \mapsto Hom_{\mathcal{E}/X}(Id_X, f)
  \,.
$$

The [[hom-set]]s in the [[over category]] are [[fiber]]s of the hom-sets in $\mathcal{E}$: we have a [[pullback]] diagram

$$
  \array{
      Hom_{\mathcal{E}/X}(Id_X, (A \to X)) &\to&
       Hom_{\mathcal{E}}(X,A)
      \\
      \downarrow && \downarrow^{f_*}
      \\
      * &\stackrel{Id_x}{\to}& Hom_{\mathcal{E}}(X,X)
  }
  \,.
$$

Moreover, overserve that [[colimit]]s in the [[over category]] are computed in $\mathcal{E}$.

$$
  {\lim_{\to}}_i (A_i \stackrel{f_i}{\to} X)
  \simeq
  ({\lim_\to}_i A_i) \to X
  \,.
$$

If $X$ is a [[tiny object]] then by definition we have

$$
  Hom_{\mathcal{E}}(X, {\lim}_i A_i)
  \simeq
  {\lim_\to}_i Hom_{\mathcal{E}}(X, A_i)
  \,,
$$

Inserting all this into the above pullback gives the pullback

$$
  \array{
      Hom_{\mathcal{E}/X}(Id_X, {\lim_\to}_i (A_i \to X)) &\to&
       {\lim_\to}_i Hom_{\mathcal{E}}(X, A_i)
      \\
      \downarrow && \downarrow^{f_*}
      \\
      * &\stackrel{Id_x}{\to}& Hom_{\mathcal{E}}(X,X)
  }
  \,.
$$

By [[universal colimits]] in the topos [[Set]], this pullback of a colimit is the colimit of the separate pullbacks, so that

$$
  \Gamma({\lim_\to}_i (A_i \to X)))
  \simeq
  Hom_{\mathcal{E}/X}(Id_X, {\lim_\to}_i (A_i \to X))
   \simeq
  {\lim_\to}_i Hom_{\mathcal{E}/X}(Id_X,(A_i \to X))
  \simeq
  {\lim_\to}_i \Gamma(A_i \to X)
  \,.
$$

So $\Gamma$ does commute with colimits if $X$ is tiny. By the [[adjoint functor theorem]] then the [[right adjoint]] $\nabla : Set \to \mathcal{E}/X$ does exist and so $\mathcal{E}/X$ is a local topos.

=--


+-- {: .num_remark }
###### Remark

As a special case this reproduces the [above statement](#LocalizationOfPresheafTopos) that slices $PSh(C)/j(U)$ of presheaf toposes over objects in the image of the [[Yoneda embedding]] are local: every [[representable functor]] is [[tiny object|tiny]] (see there).

=--

### Gros toposes

Let $A$ be a [[commutative ring]] (such as $\mathbb{Z}$ or a [[field]]), let $Spec A$ be the [[prime spectrum]] of $A$, and let $\mathcal{Z}_A$ be the [[big and little toposes|big]] [[Zariski site|Zariski topos]] for $A$ (i.e. the [[classifying topos]] for [[local ring|local $A$-algebras]]). For each element $a$ of $A$, we have an open subset $D (a) = \{ \mathfrak{p} \in Spec A : a \notin \mathfrak{p} \}$, and these open subsets constitute a basis for the topology on $Spec A$. The full subcategory of the frame of open subsets of $Spec A$ spanned by these basic open subsets admits a contravariant [[full and faithful functor|full embedding]] in the category of finitely-presented $A$-algebras via the functor $D (a) \mapsto A [a^{-1}]$ (the well-definedness of this functor requires a non-trivial check!), and this functor moreover has the cover lifting property, so induces a local geometric morphism $\mathcal{Z}_A \to Sh (Spec A)$.

## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]


* **local topos** / [[local (∞,1)-topos]]
  
  * [[Pi modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]




## References

Standard references include

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_  Proc. London Math. Soc.  (1989)   s3-58  (2):  281-305.  ([pdf](http://plms.oxfordjournals.org/content/s3-58/2/281.full.pdf+html))

and Chapter C3.6 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 
 {#Johnstone}

A completely [[internal logic|internal]] characterization of local toposes is discussed in

* [[Steve Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_, Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz), [[AwodeyBirkedalLocalTopos.pdf:file]])
 {#AwodeyBirkedal}

This is based on part 2 of

* [[Lars Birkedal]], _Developing Theories of Types and
Computability via Realizability_ PhD Thesis ([pdf](https://cs.au.dk/~birke/papers/devttc.pdf))

Free local constructions are considered in 

* {#Shulman} [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html)) 

Notions of local topos, with a view to logical completeness theorems, appear in Steve Awodey's thesis: 

* [[Steve Awodey]], *Logic in topoi: functorial semantics for higher-order logic*, Thesis, University of Chicago (1997). 
 {#Awodey} 
  

[[!redirects local geometric morphisms]]
[[!redirects local topos]]
[[!redirects local topoi]]
[[!redirects local toposes]]
