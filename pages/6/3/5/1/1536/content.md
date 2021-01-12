
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

In any context it is of interest to ask which kind of [[morphisms]] 

$$
  \array{
    E
    \\
    \downarrow^{\mathrlap{p}}
    \\
    C
  }
$$

arise as [[pullbacks]] along a classifying morphism $S_p : C \to U$ to 
some universal object $U$ of some universal morphism 

$$
  \array{
    \hat U
    \\
    \downarrow^{\mathrlap{p_{univ}}}
    \\
    U
  }
  \,.
$$

The **Grothendieck construction** describes this in the context of [[Cat]]: a morphism $p : E \to C$ of [[category|categories]] -- i.e. a [[functor]] -- is called a [[fibered category]] or [[Grothendieck fibration]] if it is encoded in a [[pseudofunctor]]/[[2-functor]] $S_p : C^{op} \to Cat$.

The reconstruction of $p$ from the pseudofunctor $S_p$ is the **Grothendieck construction** 

$$
  \int \;\; : \;\; Func(C^{op}, Cat) \to Cat/C
$$

which is a [[2-functor]] from the [[2-category]] of pseudofunctors $C^{op} \to Cat$ to the [[overcategory]] of [[Cat]] over $C$.

The essential image of this functor consists of [[Grothendieck fibration]]s and this establishes an [[equivalence of 2-categories]]

$$
  \int : Func(C^{op}, Cat) \stackrel{\simeq}{\to} Fib(C) 
$$

between 2-functors $C^{op} \to Cat$ and [[Grothendieck fibration]]s over $C$.

When restricted to pseudofunctors with values in [[Grpd]] $\subset$ [[Cat]] this identifies the [[fibration fibered in groupoids|Grothendieck fibrations in groupoids]]

$$
  \int \;\;:\;\; Func(C^{op}, Grpd) \stackrel{\simeq}{\to} FibGrpd(C) 
  \,.
$$

This equivalence notably allows one to discuss [[stack]]s equivalently as pseudofunctors or as groupoid fibrations (in each case satisfying a [[descent]] condition with respect to a [[Grothendieck topology]] on $C$).

The Grothendieck construction is one of the central aspects of [[category theory]], together with the notions of universal constructions such as [[limit]], [[adjunction]] and [[Kan extension]]. It is expected to have suitable analogs in all sufficiently good contexts of [[higher category theory]]. Notably there is an [[(∞,1)-Grothendieck construction]] in [[(∞,1)-category]] theory.

The Grothendieck construction can also be generalized beyond fibrations, to the correspondence between [[displayed categories]] and arbitrary categories over $C$.


## Definition 

Let [[Cat]] be the [[2-category]] of [[categories]], [[functor]]s and [[natural transformation]]s.  In line with the philosophy of [[generalized universal bundles]], the "universal [[Cat]]-[[bundle]]" is $Cat_{*,\ell} \to Cat$.  Here $Cat_{*,\ell}$ denotes the (2-)category of "lax-[[pointed object|pointed]]" [[categories]], also known as the "lax slice" of $Cat$ under the [[terminal category]] $*\in Cat$.  Its objects are pointed categories, i.e. pairs $(A,a)$ where $A$ is a category and $a$ is an object of $A$, and its morphisms $(A,a) \to (B,b)$ are pairs $(f,\gamma)$ where $f\colon A\to B$ is a functor and $\gamma\colon f(a)\to b$ is a morphism in $B$.  The projection $Cat_{*,\ell} \to Cat$ is just the forgetful functor.

Then if $F\colon C \to Cat$ is a [[pseudofunctor]] from a category $C$ to $Cat$, the **Grothendieck construction** for $F$ is the (strict) [[2-pullback]] $ p : \int F \to C$ of $Cat_{*,\ell} \to Cat$ along $F$:

$$
  \array{
    \int F &\to& Cat_{*,\ell}
    \\
    {}^{p}\downarrow && \downarrow
    \\
    C &\overset{F}{\to}& Cat
  }
  \,.
$$

This means that

* the objects of $\int F$ are pairs $(c,a)$, where $c \in Obj(C)$ and $a \in Obj(F(c))$ 

* and morphisms in $\int F$ are given by pairs $(c \overset{f}{\to} c', F(f)(a) \overset{\alpha}{\to} a')$. This may be visualized as

$$
  \int F = 
  \left\{
  \array{
    && {*}
    \\
    & {}^a\swarrow &\seArrow^{\alpha}& \searrow^{a'}
    \\
    F(c) && \stackrel{F(f)}{\to} && F(c')
    \\
    \\
    c &&\stackrel{f}{\to}&& c'
  }
  \right\}
  \,.
$$

This extends to a 2-functor between [[bicategories]]

$$
  \int \;\; : \;\; [C, Cat] \to Cat/C
$$

from [[pseudofunctor]]s on $C$ to the [[overcategory]] of [[Cat]] over $C$.

The more commonly described version of this construction works instead on contravariant pseudofunctors, i.e. pseudofunctors $C^{op}\to Cat$.  In this case we use instead the "universal $Cat$-cobundle" $(Cat_{*,c})^{op} \to Cat^{op}$, where $(Cat_{*,c})$ is the colax slice, whose objects are  again pointed categories $(A,a)$, but whose morphisms $(A,a) \to (B,b)$ are pairs $(f,\gamma)$ where $f\colon A\to B$ and $\gamma\colon b \to f(a)$.  Now the 2-pullback

$$
  \array{
    \int F &\to& (Cat_{*,c})^{op}
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow
    \\
    C &\stackrel{F}{\to}& Cat^{op}
  }
  \,.
$$

describes a 2-functor

$$ \int \quad\colon\quad [C^{op},Cat] \to Cat/C. $$

In this case,

* the objects of $\int F$ are again pairs $(c,a)$, where $c \in Obj(C)$ and $a \in Obj(F(c))$, but

* the morphisms in $\int F$ from $(c,a)$ to $(c',a')$ are pairs $(c \overset{f}{\to} c', a \overset{\alpha}{\to} F(f)(a'))$.


## Properties

### Limits and colimits

The following results are due to ([Tarlecki, Burstall, Goguen 91](#TBG91)). 

+-- {: .num_prop}
###### Proposition

Let $F : C^{op} \to Cat$ be such that the following conditions hold.

1. $C$ is complete.
1. $F(J)$ is complete for all $J \in C$.
1. $F(f) : F(J) \to F(K)$ preserves limits for all $f : K \to J$ in $C$.

Then $\int F$ is complete.
=--

+-- {: .num_prop}
###### Proposition

Let $F : C^{op} \to Cat$ be such that the following conditions hold.

1. $C$ is cocomplete.
1. $F(J)$ is cocomplete for all $J \in C$.
1. $F(f) : F(J) \to F(K)$ has a left adjoint for all $f : K \to J$ in $C$.

Then $\int F$ is cocomplete.

=--

### As an oplax colimit
 {#AsALaxColimit}

The Grothendieck construction on $F : C \to Cat$ is equivalently the [[oplax colimit]] of $F$ (e.g [Gepner-Haugseng-Nikolaus 15](#GepnerHaugsengNikolaus15)).  That means that for each category $X$ there is an [[equivalence|equivalence of categories]]

$$
  Lax(F, \Delta X) \simeq [{\textstyle \int} F, X]
$$

that is natural in $X$, where $\Delta X$ is the constant functor with value $X$.  (See [[oplax colimit]] for an explanation of why *lax* natural transformations appear in the definition of an *oplax* colimit.)

A [[lax natural transformation]] $\alpha$ from $F$ to $\Delta X$ is given by

* for each object $c$ of $C$, a functor $\alpha_c \colon F c \to X$, and
* for each morphism $m \colon c \to d$ in $C$, a [[natural transformation]] $\alpha_m \colon \alpha_c \Rightarrow \alpha_d \circ m_*$ (writing $m_* = F m$),

such that $\alpha_{1_c}$ is the isomorphism $F 1_c \cong 1_{F c}$ given by [[pseudofunctor|pseudofunctoriality]] of $F$, and that if $m \colon c \to d$, $n \colon d \to e$ is a composable pair in $C$, then $\alpha_{n m}$ is equal to the obvious [[pasting]] of $\alpha_m$ and $\alpha_n$.

We want to show that to each such lax transformation there corresponds an essentially unique functor $\int F \to X$.  So firstly, given $\alpha$ as above, let $A$ be the functor that sends $x \in F c$ to $\alpha_c x$, and acts on arrows as

$$
  (m \colon c \to d, f \colon m_* x \to y)
  \quad \mapsto \quad
  \alpha_c x \overset{\alpha_m x}{\to}
  \alpha_d m_* x \overset{\alpha_d f}{\to} \alpha_d y
$$

That $A$ is a functor follows from the coherence properties of $\alpha$ with respect to identities and composition in $C$.

Conversely, if $A \colon \int F \to X$ is a functor, we get a lax transformation $\alpha$ as follows:

* For each $c \in C$, $\alpha_c$ is the restriction of $A$ to the category $F c$, which is the subcategory of $\int F$ whose objects are those of $F c$ and whose morphisms are those with first component an identity morphism.  This clearly makes $\alpha_c$ a functor.
* For each $m \colon c \to d$ in $C$, $\alpha_m$ has components $\alpha_c x \to \alpha_d m_* x$ given by $A$'s value at the morphism $(m,1_{m_* x})$.  This is a natural transformation because, if $k \colon x \to x'$ is a morphism in $F c$, then both sides of the naturality square are the value of $A$ at the morphism $(m, m_*k)$.

As one might expect, the coherence conditions on the resulting $\alpha$ follow from the functoriality of $A$.

It is then easy to check that these two mappings form a bijection between the objects of $Lax(F, \Delta X)$ and $[\int F, X]$.

As for the morphisms involved, the [[modifications]] between lax transformations and the [[natural transformations]] between functors, it is straightforward to show that these are in bijective correspondence too.  Hence we have shown that the above equivalence holds.

By inspecting the above proof, it is easy to see that the lax transformation associated to a functor $\int F \to X$ is a [[pseudonatural transformation]] if and only if the functor inverts (i.e. sends to an isomorphism) each member of the class $S$ of morphisms of $\int F$ whose second component is an identity.  (These are in fact the [[cartesian morphism|opcartesian]] morphisms with respect to the projection $\int F \to C$.)  The [[localization]] $\int F[S^{-1}]$ is therefore the (weak) [[2-colimit]] of $F$:

$$
  Ps(F, \Delta X) \simeq [{\textstyle \int} F, X]_{S^{-1}}
   \simeq [{\textstyle \int} F[S^{-1}], X]
$$

This last result appears in [[SGA4]] Exposé VI, Section 6.


### Local smallness

In general, a [[weighted colimit|(weighted)]] colimit of a [[large category|large]] diagram of [[locally small categories]] need no longer be locally small.  However, in the case of the oplax colimit, i.e. the Grothendieck construction, we have:

+-- {: .un_theorem}
###### Theorem
If $F:C^{op}\to Cat$ is a pseudofunctor, $C$ is locally small, and each category $F(c)$ is locally small, then the Grothendieck construction $\int F$ is also locally small.
=--
+-- {: .proof}
###### Proof
Recall that the morphisms in $\int F$ from $(c,a)$ to $(c',a')$ are pairs $(c \overset{f}{\to} c', a \overset{\alpha}{\to} F(f)(a'))$.  Local smallness of $C$ means that there is only a set of such $f$'s, and local smallness of $F(c)$ means that for each $f$ there is only a set of such $\alpha$'s.
=--

For example, consider the [[canonical indexing]] of a locally small category $A$, i.e. the pseudofunctor $Set^{op}\to Cat$ sending each set $X$ to the category $A^X$.  This satisfies the conditions of the above theorem, so its Grothendieck construction, which is the category of [[families]] of objects of $A$, is locally small.


### The equivalence between fibrations and pseudofunctors

One can characterize the _image_ of the Grothendieck construction
as consisting precisely of those objects in $Cat/C$ that are
[[Grothendieck fibration]]s.

We recall the definition of the [[bicategory]] of Grothendieck fibrations 
and [[pseudofunctor]]s and then state the main equivalence theorem.

#### The bicategory of pseudofunctors

A [[pseudofunctor]] from a 1-[[category]] $C$ to a [[2-category]] ([[bicategory]]) $A$ is nothing but a (non-strict) [[2-functor]] between bicategories, with the ordinary category regarded as a special bicategory.

We write $[C^{op}, A]$ for the [[2-functor]] 2-category from the 
[[opposite category]] of $C$ to $A$ (the $op$ here is just convention):

* objects are pseudofunctors $F : C^{op} \to A$;

* morphism are [[lax natural transformation|pseudonatural transformations]];

* 2-morphism are [[modification]]s.


#### The bicategory of fibrations

+-- {: .un_defn}
###### Definition


A [[functor]] $p : E \to C$ is a **[[Grothendieck fibration]]**
if for every object $e \in E$ and every morphism $f : c \to p(e)$
in $C$ there is a morphism $\hat f : \hat c \to e$ in $E$ that lifts
$f$ in that $p(\hat f) = f$ and which is a [[Cartesian morphism]].

A **morphism of Grothendieck fibrations $F : (p : E \to C) \to (p' : E' \to C)$ is

* a functor $F : E \to E'$

* such that

  * $F$ sends [[Cartesian morphism]]s to Cartesian morphisms;

  * the diagram

    $$
      \array{
        E &&\stackrel{F}{\to}&& E'
        \\
        & {}_{\mathllap{p}}\searrow && \swarrow_{\mathrlap{p'}}
        \\
        && C
      }
    $$

    in [[Cat]] commutes (strictly).

* a **2-morphism** between morphism $\eta : F \to F'$ is a 
  [[natural transformation]] of the underlying functors, that also makes
  the obvious diagram 2-commute, i.e. such that 
  $p' \cdot \eta$ is trivial.


Compositions are those induced from the underlying functors and natural transformations.

This defines the **[[2-category]] of Grothendieck fibrations** 

$$
  Fib(C) \hookrightarrow Cat/C
$$

over $C$, being a 2-[[subcategory]] of the [[overcategory]] of [[Cat]] over $C$.


=--

+-- {: .un_remark}
###### Remark


Cartesian lifts are not required to be unique, but are automatically unique up to a unique vertical [[isomorphism]] connecting their domains.


=--


#### Statement of the equivalence


+-- {: .un_proposition}
###### Proposition

The Grothendieck construction factors through [[Grothendieck fibration]]s over $C$

$$
  \int : [C^{op}, Cat] \to Fib(C) \hookrightarrow Cat/C
$$

and establishes an equivalence of bicategories

$$
  \int : [C^{op}, Cat] \stackrel{\simeq}{\to} Fib(C)
  \,.
$$

In fact, it is more than that: it is an equivalence of [[strict 2-categories]], in the sense of strict 2-category theory, i.e. an equivalence of $Cat$-[[enriched categories]].

When restricted to pseudofunctors that factor through [[Grpd]] $\hookrightarrow Cat$ it factors through [[fibrations in groupoids]]

$$
  \int : [C^{op}, Grpd] \to Fib_{Grpd}(C)\hookrightarrow Cat/C
$$

and establishes a similar equivalence

$$
  [C^{op}, Grpd] \simeq Fib_{Grpd}(C)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This can be verified by straightforward albeit somewhat tedious checking. Details are spelled out in section B1.3 of

* [[Peter Johnstone]], _Sketches of an Elephant_ 

The statement itself is theorem B1.3.6 there, all definitions and lemmas are on the pages before that.

=--

#### Model category version

There is refinement of the Grothendieck construction to [[model categories]]. S

See at _[[Grothendieck construction for model categories]]_.

This model category incarnation of the Grothendieck construction 
generalizes to a model category presentation of the 
[[(∞,1)-Grothendieck construction]].



### Adjoints to the Grothendieck construction {#adjunction}

The Grothendieck construction functor

$$
  \int : [C^{op}, Cat] \to Cat/C
$$

has a [[left adjoint|left]] and a [[right adjoint|right]] [[adjoint functor]].

Restricted to [[Grothendieck fibration]]s and [[fibrations in groupoids]], both of these exhibit the above equivalences as [[adjoint equivalence]]s. Notice that much of the traditional literature discusses (just) the right adjoint. 

#### The left adjoint

The [[left adjoint]] is the functor

$$
  L : (p : E \to C) \mapsto ( (-)/p : C^{op} \to Cat) 
$$

that assigns to a functor $p$ the presheaf which sends $c \in C$ to the [[comma category]] $c/p$ with objects given by pairs $(e, c \to p(e))$ and morphisms by commutative triangles

$$
  \array{
      && c &&
      \\
      & \swarrow && \searrow &
      \\
      p(e_1) &&\to&& p(e_2)
  }
$$

i.e.

$$
  L(E \stackrel{p}{\to}C) : c \mapsto c/p
  \,.
$$

This functor may equivalently be expressed as follows.

##### In terms of a cone construction {#Cone}

For given $(E \stackrel{p}{\to} C)$ consider the [[(infinity,1)-limit|(3,1)-pushout]]

$$
  \array{
    E &\hookrightarrow& E^{\triangleright}
    \\
    \downarrow^{\mathrlap{p}} &\swArrow& \downarrow
    \\
    C &\to& K(p)
  }
$$

of _[[(2,1)-categories]]_ , where $K^{\triangleright}$ is $K$ with one [[terminal object]] $v$ adjoined (a [[join of quasi-categories|join]] of categories). (Here $E$, $C$ and $E^{\triangleright}$ are 1-catgeories regarded trivially as $(2,1)$-categories and where $K(p)$ will in general be a [[(2,1)-category]] with nontrivial [[2-morphism]]s).



+-- {: .un_lemma }
###### Claim

We have

$$
  c/p \simeq Hom_{K(p)}(c,v)
  \,.
$$

And hence the left adjoint to the Grothendieck construction may be realized as the assignment that sends $p : E \to C$ to the pseudofunctor 

$$
  L(p) := Hom_{K(p)}(-, v) : C^{op} \to Cat
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is convenient to compute the weak pushout by embedding the situation from [[Cat]] into the bigger context of [[(∞,1)-categories]] and using the [[model category|model]] of that provided by [[sSet]]: the [[model structure for quasi-categories]]. This also facilitates the generalization of the argument from 1-categories to higher categories.

So consider equivalently the weak pushout diagram

$$
  \array{
    N(E) &\hookrightarrow& N(E)^{\triangleright}
    \\
    \downarrow^{\mathrlap{N(p)}} &\swArrow& \downarrow
    \\
    N(C) &\to& N(K(p))
  }
$$

of [[quasi-categories]], where $N(-)$ is the [[nerve]] operation and where $N(E)^{\triangleright} = N(E) \star *$ is the [[join of simplicial sets]] of $N(E)$ with the [[point]]. 

By the general yoga of [[homotopy colimit]]s (see there for details) we know that this $\infty$-pushout here may be computed as an ordinary [[pushout]] in the 1-category [[sSet]] if the pushout diagram $N(C) \leftarrow N(E) \to N(E)^{\triangleright} $ has the property that

* all three objects are cofibrant;

* at least one of the two morphisms is a cofibration

in the [[model structure for quasi-categories]] $sSet_{Joyal}$.

But this is trivially verified since the cofibrations in $sSet_{Joyal}$ are just the [[monomorphism]]s in [[sSet]]: the degreewise injective maps of simplicial sets. So every object in $sSet_{Joyal}$ is cofibrant and the inclusion $N(E) \hookrightarrow N(E)^{\triangleright}$ is a cofibration. 

(The same conclusion would hold for the same simple reasons in the standard [[model structure on simplicial sets]] $sSet_{Quillen}$.)

From this it follows that simply because we passed from categories to their [[nerve]]s, the computation of the weak pushout reduces to the computation of an ordinary pushout (one may think of passing to nerves as providing a cofibrant replacement: since in the nerve all composition of [[k-morphism]]s is "freed", the nerve is a suitably "puffed up" version of a category that is suitable for computing $\infty$-pushouts).

So we are reduced to computing the ordinary [[pushout]]

$$
  \array{
    N(E) &\hookrightarrow& N(E)^{\triangleright}
    \\
    \downarrow^{\mathrlap{N(p)}} && \downarrow
    \\
    N(C) &\to& Q
  }
$$
 
in [[sSet]]. The fibrant replacement of $Q$ is then the [[nerve]] of [[generalized the|the]] [[bicategory]] $K(p)$ that we are after.

As recalled at [[limits and colimits by example]] in the section [limits in presheaf categories](http://ncatlab.org/nlab/show/limits+and+colimits+by+example#limitsinpresheafcat), [[colimit]]s (and hence pushouts) in the [[presheaf]]-category [[sSet]] $= Func(\Delta^{op}, Set)$ are computed for each object $[n] \in \Delta$ as ordinary colimits in [[Set]].

For **$n=0$** we see that $Q_0$ is the collection of objects of $C$ and one additional vertex $v$:

$$
 Q_0 = N(C)_0  \coprod \{ v\} = p(Obj(E)) \coprod \{v \}
$$


For **$n=1$**  similarly we find that $Q_1$ consists of the 1-cells in in $C$ and in addition of one 1-cell $e : c \to v$ for each $e \in Obj(E)$ with $p(e) = c$ (this 1-cell is really the terminal 1-cell $e \to v$ in $E^{\triangleright}$ but with its source re-interpreted as being $p(e) = c$ according to the identification of $Q_0$ as above). In the fibrant replacement of $Q$ the composite of original 1-cells $c_1 \to c_2$ and the new 1-cells $e : c_2 \to v$ will be freely added, so that the general 1-morphism $c_1 \to v$ will consist of a 1-morphism $c_1 \to c_2$ in $C$ together with a lift of $c_2$ to $E$. This is just as in the [[comma category]] $c/p$.

For **$n=2$** we have in $Q_2$ the 2-cells in $C$ as well as one 2-cell

$$
  \array{
    c_1 &&\to&& c_2
    \\
    & \searrow &{}^{(e_1 \to e_2)}\swArrow& \swarrow
    \\
    && v
  }
$$

for each 1-cell $(e_1 \to e_2)$ in $N(E)$ with $p(e_1 \to e_2)$ = $(c_1 \to c_2)$.

In particular this means that if $e_2: c_2 \to v$ is a morphism in $Q$ and $c_1 \to c_2$ is a morphism in $C$, then the composite $c_1 \to c_2 \to v$ in $Q$ is homotopic to any compatible direct morphism $c_1 \to v$ in $Q$.

This means that forming the fibrant replacement of $Q$ in $sSet_{Joyal}$ will not throw in superfluous 1-morphisms on top of those we already discussed in the previous paragraph...


Now furthermore...

=--


This formulation of the Grothendieck construction as an adjunction

$$
  (L \dashv \int) : Fib(C) \stackrel{\leftarrow}{\to} [C^{op}, Cat]
$$

with the left adjoint given by hom-objects in a pushout object as above
is the starting point for the [[vertical categorification]] described at [[(∞,1)-Grothendieck construction]]. 

#### The right adjoint

We also have an adjunction
$$(R \vdash \int) : Fib(C) \stackrel{\leftarrow}{\to} [C^{op}, Cat]$$
where the right adjoint $R$ sends a [[Grothendieck fibration]] $F$ over $C$
to the presheaf
$$c\mapsto Hom(\int y(c), F),$$
where $\int y(c)$ is the Grothendieck construction applied to the
representable presheaf of sets (hence [[discrete categories]]) on $c$
and $Hom$ denotes the category of morphisms between two Grothendieck fibrations.

Informally, an object of $R(F)(c)$ is given by a choice of a pullback
along each morphism with codomain $c$,
and these pullbacks must be functorial.

### Behaviour under simplicial nerve

+-- {: .num_prop }
###### Proposition

For $F \colon \mathcal{D} \to Cat$ a [[functor]], let 

$$
  {\vert N(F(-))\vert} 
   \;\colon\; 
  \mathcal{D} 
    \overset{F}{\longrightarrow} 
  Cat 
   \stackrel{\vert N(-) \vert}{\to}
  Top
$$ 

be its postcomposition with [[geometric realization of categories]]

Then we have a [[weak homotopy equivalence]]

$$
  {\left\vert N\left(\int F \right) \right\vert}
    \simeq
  hocolim {\vert N(F(-)) \vert}
$$

exhibiting the [[homotopy colimit]] in [[Top]] over $\vert N(F (-)) \vert$ as the geometric realization of the [[Grothendieck construction]] $\int F$ of $F$.

=--

This is due to ([Thomason 79](#Thomason79)). 



## Generalizations 

### $n = 0$ 

The analog of the Grothendieck construction one categorical dimension down is the [[category of elements]] of a [[presheaf]].

### $n = (\infty,0)$
 {#ForInfinityGroupoids}

The analog of the Grothendieck construction for [[∞-groupoids]] is examined in detail in [Heuts-Moerdijk 13](#HeutsMoerdijk13).

The category of presheaves in groupoids is replaced by the [[model category of simplicial presheaves]] equipped with the [[projective model structure]]
and the category of Grothendieck fibrations in groupoids is replaced by the model category of simplicial sets over the [[nerve of a category|nerve]] of the source category, equipped with the [[contravariant model structure]].

In this case there is not one, but two different functors that generalize the Grothendieck construction.

The first functor $h_!$ is a [[left adjoint]], it implements the [[homotopy colimit]] using the [[diagonal]] of a [[bisimplicial set]],
and the second functor $r^*$ is a [[right adjoint]], it uses the [[codiagonal]] (also known as the [[totalization]]) of a bisimplicial set.
Both functors fit into [[adjunctions]] $h_!\dashv h^*$ and $r_!\dashv r^*$,
where the other two adjoints can be seen as rectification functors:
the right adjoint $h^*$ generalizes the cleavage construction,
whereas the left adjoint $r_!$ generalizes the comma category construction above.

The two functors $h_!$ and $r^*$ become naturally weakly equivalent once we [[derived functor|derive]] them, but they are not isomorphic.
The functor $r^*$ restricted to the full subcategory of presheaves of groupoids recovers the nerve of the classical Grothendieck construction described above.
The functor $h_!$ restricted to the same full subcategory
does not even land in quasicategories, so it doesn't give
rise to a new construction in the classical case.

### $n = (\infty,1)$  {#(oo1)case}

The analog of the Grothendieck construction for [[(infinity,1)-category|(∞,1)-categories]] is described at [[Cartesian fibration]] and at [[universal fibration of (∞,1)-categories]]. 

The correspondence between $(\infty,1)$-categorical [[cartesian fibrations]] $E \to C$ and [[(infinity,1)-presheaf|(∞,1)-presheaves]] $C \to (\infty,1)Cat^{op}$ is [[model category|modeled]] by the [[Quillen equivalence]] between the [[model structure on marked simplicial over-sets]] and the projective [[global model structure on simplicial presheaves]].

For more details see

* [[(∞,1)-Grothendieck construction]]

### Normal lax functors into $Prof$

The Grothendieck construction can be generalized from pseudofunctors into $Cat$ to normal lax functors into [[Prof]].  Instead of fibrations over $C$, such normal lax functors correspond to arbitrary functors into $C$.  See [[displayed category]] for more.


## Warning on terminology ##

The term 'Grothendieck Construction' is applied in the literature to at least two very different constructions (and as [[Alexander Grothendieck|Grothendieck]] introduced so many new ideas and constructions to mathematics, perhaps there are others!). One concerns the construction of a [[fibered category]] from a [[pseudofunctor]] and will be treated in more detail in the entry on [[Grothendieck fibration]].  The other refers to constructing the [[Grothendieck group]] is  in the context of [[K-theory]] from isomorphism classes of vector bundles on a space by the introduction of formal inverses, 'virtual bundles'.  This constructs an Abelian group from the semi-group of isomorphism classes.


## Examples

A [[representable functor]] $C(-,X) :  C^{op} \to Set \hookrightarrow Cat$ maps under the Grothendieck construction to the [[slice category]] $C/X$. The corresponding fibrations $C/X \to C$ are also called [[representable fibered categories]].

## Related concepts

* [[category of elements]]

* **Grothendieck construction**

* [[(infinity,1)-Grothendieck construction]]

* [[Grothendieck construction for monoidal categories]]

## References

Standard references are  in

* sections A1.1.7, B1.3.1 of [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}
* [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_, pp. 1--104 of [[FGA explained]]; [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406); [math.AG/0412512](http://arxiv.org/abs/math/0412512).

The [[geometric realization of categories|geometric realization]] of Grothendieck constructions has been analyzed in

* {#Thomason79} [[R. W. Thomason]], _Homotopy colimits in the category of small categories_ , Math. Proc. Cambridge Philos. Soc. 85 (1979), no. 1, 91109.

The left adjoint to the Grothendieck construction is discussed in &#167;3.1.1 of

* [[Georges Maltsiniotis]], _La th&#233;orie de l'homotopie de Grothendieck_

Limits and colimits are analysed in

* {#TBG91} [[Andrzej Tarlecki]], [[Rod M. Burstall]] [[Joseph A. Goguen]], _Some fundamental algebraic tools for the semantics of computation: Part 3. indexed categories_ , ([Theoretical Computer Science vol. 91 (1991)](https://www.sciencedirect.com/science/article/pii/030439759190085G))

The analog for simplicial sets instead of groupoids is discussed in

* {#HeutsMoerdijk13}  [[Gijs Heuts]], [[Ieke Moerdijk]], _Left fibrations and homotopy colimits_ ([arXiv:1308.0704](https://arxiv.org/abs/1308.0704)). 



See also

* [Grothendieck construction](http://en.wikipedia.org/wiki/Grothendieck_construction) (Wikipedia)
* [The Homotopy Theory of n-Fold Categories](http://www-personal.umd.umich.edu/~tmfiore/1/ThomasonNFoldBeamerSlides.pdf)
* [Inference System Integration via Logic Morphisms](http://www.kestrel.edu/home/projects/logicware/slides-9806/sld001.htm)
* [Category Theory for Computing Science](http://www.math.mcgill.ca/triples/Barr-Wells-ctcs.pdf)

A [[model category]] presentation of the Grothendieck construction see at _[[Grothendieck construction for model categories]]_.

Discussion of the Grothendieck construction as a [[lax colimit]] includes (see also at [[(infinity,1)-Grothendieck construction]])


* {#GepnerHaugsengNikolaus15} [[David Gepner]], [[Rune Haugseng]], [[Thomas Nikolaus]], _Lax colimits and free fibrations in $\infty$-categories_ ([arXiv:1501.02161](http://arxiv.org/abs/1501.02161))

The Grothendieck construction in [[enriched category theory]]:

* {#BeardsleyWong18} [[Jonathan Beardsley]], Liang Ze Wong, _The Enriched Grothendieck Construction_, Advances in Mathematics, Volume 344, 21 February 2019, Pages 234-261 ([arXiv:1804.03829](https://arxiv.org/abs/1804.03829), [doi:10.1016/j.aim.2018.12.009](https://doi.org/10.1016/j.aim.2018.12.009)) 

A [[monoidal category|monoidal]] version:

* {#MoellerVasilakopoulou19} [[Joe Moeller]], [[Christina Vasilakopoulou]], *Monoidal Grothendieck Construction*,  2019 ([arXiv:1809.00727](https://arxiv.org/abs/1809.00727))


[[!redirects Grothendieck constructions]]
[[!redirects enriched Grothendieck construction]]
[[!redirects enriched Grothendieck constructions]]
