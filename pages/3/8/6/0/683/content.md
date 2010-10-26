
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--





#Contents#

* automatic table of contents goes here
{:toc}

## Idea 

In great generality, a _homotopy limit_ is a way of constructing appropriate sorts of [[limit]]s in a [[higher category theory|(weak) higher category]] and in general and in [[(∞,1)-category]] theory in particular, using some _presentation_ of that higher category by a [[category theory|1-categorical]] structure.  The general study of such presentations is [[homotopy theory]].

In classical homotopy theory, the presentation is given by a [[category with weak equivalences]], possibly satisfying extra axioms such as those of a [[homotopical category]], a [[category of fibrant objects]], or a [[model category]].  Such structures are considered to present an [[(∞,1)-category]], and homotopy limits give a way of constructing the appropriate sort of [[limit in a quasi-category|(∞,1)-categorical limits]].

In [[enriched homotopy theory]], the presentation is given by an [[enriched model category]] or an [[enriched homotopical category]], and it may presents an "enriched $(\infty,1)$-category" or be a more powerful presentation of a bare $(\infty,1)$-category (notably if the enrichment is over [[sSet]]).  In the [[enriched category theory]] context the appropriate notion is a [[weighted limit|weighted]] homotopy limit, which may construct "weighted $(\infty,1)$-limits" in the presented "enriched $(\infty,1)$-category" or may be a more powerful tool for constructing plain $(\infty,1)$-categorical limits (in particular if the enrichment is over [[sSet]]).  Note that as yet, no fully general notion of "enriched $(\infty,1)$-category" exists; see [[homotopical enrichment]].

Maybe the most commonly encountered setup for homotopy limits is that where the [[(∞,1)-category]] in question is [[presentable (∞,1)-category|presented]] by a [[simplicial model category]]. See also [[homotopy Kan extension]], of which (globally defined) homotopy (co)limits are a special case.


## Definitions 

As for ordinary [[limit]]s,
there are two ways to define homotopy limits:

* with explicit constructions that satisfy a _local_ universal property: the homotopy limit object "represents homotopy-coherent cones up to homotopy."

* as [[derived functor]]s of a [[homotopy Kan extension]] that satisfy a _global_ universal property: the homotopy limit _functor_ is "universal among homotopical approximations to the strict limit functor."

One of the central theorems of the subject is that in good cases, the two give equivalent results; see below.


### Global definition {#GlobalDefinition}

Let $C$ be a [[category with weak equivalences]] and let $D$ be a (small) [[diagram]] category.  Make the [[functor category]] $[D,C]$ into a category with weak equivalences by taking the weak equivalences to be those [[natural transformation]]s which are objectwise weak equivalences in $C$.

The ordinary [[limit]] and [[colimit]] operations over $D$-diagrams are (as described there) the left and right [[Kan extension]] of the functor $const : C \to [D,C]$

$$
  [D,C]
  \stackrel{\stackrel{\overset{colim = Lan const}{\to}}{\overset{const}{\leftarrow}}}{\underset{lim = Ran const}{\to}}
  C
  \,.
$$

The (globally defined) _homotopy limit_ and _colimit_ are accordingly the right and left [[homotopy Kan extension]] of the constant diagram functor:

* The **homotopy limit** of a functor $F : D \to C$ is, if it exists, the image of $F$ under the right [[derived functor]] of the [[limit]] functor $lim_D : [D,C] \to C$ with respect to the given weak equivalences on $C$ and the objectwise weak equivalences on $[D,C]$:
$$
  holim_D F := (\mathbb{R} lim_D)F
  \,.
$$

* The **homotopy colimit** of a functor $F : D \to C$ is, if it exists, the image of $F$ under the left [[derived functor]] of the [[colimit]] functor $colim_D : [D,C] \to C$ with respect to the given weak equivalences on $C$ and the objectwise weak equivalences on $[D,C]$:

$$
  hocolim_D F := (\mathbb{L} colim_D)F
  \,.
$$


In the enriched case, this must be suitably modified to deal with [[weighted limit|weighted limits]] as well as enrichment of both $C$  and $D$.

In particular, if $C$ is equipped with the extra structure of a [[simplicial model category]] and $K$ is an (small) [[sSet]]-[[enriched category]] we may also hope to equip the [[enriched functor]] category $[D,C]$ with the structure of a simplicial model category.  There are two different "canonical" such structures:

* the _projective_ [[model structure on functors]] $[D,C]_{proj}$;

* the _injective_ [[model structure on functors]] $[D,C]_{inj}$

(both of which have the same objectwise weak equivalences and are in fact [[Quillen equivalence|Quillen equivalent]]).   When these model structures exist (as they do when $C$ is [[combinatorial model category|combinatorial]]), limit and colimit constitute then two $sSet$-enriched [[Quillen adjunction]]s

$$
  [D,C]_{proj}
   \stackrel{\overset{colim}{\to}}{\underset{const}{\leftarrow}} 
  C
$$

and

$$
  [D,C]_{inj}
   \stackrel{\overset{const}{\leftarrow}}{\underset{lim}{\to}} 
  C
  \,.
$$

(All proofs and other technical details on this are at [[homotopy Kan extension]].)

These present directly the corresponding [[adjoint (∞,1)-functor]]s (as described there)

$$
  (\infty,1)Func(D,C^\circ)
  \stackrel{\to}{\stackrel{\leftarrow}{\to}}
  C^\circ
$$

by precomposition with a cofibrant replacement functor (for the colimit) and a fibrant replacement functor (for the limit).

For instance for $Q_{proj} : [D,C] \to [D,C]$ a cofibrant replacment for the projective [[model structure on functors]] we have

$$
  hocolim F \simeq colim Q_{proj}(F)
  \,.
$$

This is sometimes called the **Quillen formula** for computing homotopy colimits. Analogously with $P_{inj}$ a fibrant replacement functor for the injective model structure, we have

$$
  holim F \simeq lim P_{inj}(F)
  \,.
$$

In some applications it is, however, inconvenient to to produce a projectively cofbrant  replacement of a colimit diagram. There is another formula that produces an equivalent result: let $Q'_{proj}$ a cofibrant replacement functor for $[D^{op}, sSet_{Quillen}]_{proj}$ (notice the [[opposite category]]) and $Q_{inj}$ one for $[D,C]_{inj}$. Let $* \in [D^op,sSet]$ [[simplicial presheaf]] constant on the terminal simplicial set and $Q'_{proj}(')$ its projective cofibrant replacement. 

Then we also have the [[coend]] expression

$$
  hocolim F \simeq \int^{D}
  Q'_{proj}(*) \cdot Q_{inj}(F)
  \,,
$$

where in the integrand we have the [[copower|tensoring]] of the [[simplicial model category]] $C$ over [[sSet]]. 

If $D$ happens to be a [[Reedy model category]] we can equivalently use in this expression also the [[Reedy model structure]]s $[D,C]_{Reedy}$ and $[D^{op}, C]_{Reedy}$ and obtain the homotopy colimit as

$$
  hocolim F \simeq \int^{D}
  Q'_{Reedy}(*) \cdot Q_{Reedy}(F)
  \,,
$$


This formula is sometimes called the **Bousfield-Kan formula** (see also [[Bousfield-Kan map]]). The coend is a [[weighted limit]] and this formula for the plain homotopy colimit can be understood the left derived _weighted_ colimit which trivial weight (the underived weight is trivial, but becomes non-trivial after derivation -- this extra complexity helps reduce the complexity for the replacement for the functor $F$ itself).

In detail, let $V$ be a [[monoidal model category]] and $C$ a $V$-[[enriched model category]] (for instance $V = sSet_{Quillen}$ as in the above discussion). Let $D$ be a small $V$-[[enriched category]]. Then for a any given [[weighted limit|weight]]

$$
  W : D^{op} \to V
$$

we have a $V$-[[adjunction]]

$$
  [D,C]
  \stackrel{\overset{W \otimes_D (-)}{\to}}{\underset{const(-)^{W}}{\leftarrow}}
  D
  \,,
$$

where the [[left adjoint]] is the weighted colimit given by the [[coend]]

$$
  W \otimes_D F = \int^{d \in D} W(d) \otimes F(d)
$$

(with the [[copower|tensoring]] over $V$ in the integran) and where the [[right adjoint]] is formed using the [[power|cotensor]] over $V$.

The crux now is that as $W$ varies, the left adjoint here is a left [[Quillen bifunctor]]

$$
  \int (-)\cdot (-)
  :
  [D^{op}, V] \times [D,C]
  \to 
  C
  \,.
$$

For details on this see [[Quillen bifunctor]] or around page 9 of

* Nicola Gambino, _Weighted limits in simplicial homotopy theory_ ([pdf](http://www.crm.cat/Publications/08/Pr790.pdf)).

From the fact that this is a Quillen bifunctor and using the observation that for the _trivial_ weight $W = const 1$ the wighted colimit reduces to an ordinary colimit, follows the above Bousfield-Kan-type formula for the homotopy colimit.


### Local definition 

The local definition requires making precise the notion of a _[[homotopy]] commutative cone_ over a diagram. 

For the case of [[SimpSet]]-[[enriched category|enrichment]] one elegant way to do so is in terms of suitable [[weighted limit]]s as described in the example section at [[weighted limit]]: a homotopy commutative cone with tip $c \in C$ over a diagram $F : K \to C$ in an $\Simp\Set$-enriched category $C$ is a natural transformation 
$W \Rightarrow C(c,F(-)) : K \to \Simp\Set$ where the _weight_ functor $W$ is not constant on the point, as for ordinary limits, but is given by $W : k \mapsto N(K/k)$.


The same idea works if we are enriched over a category $V$ that is not $\SimpSet$ but is itself enriched over $\Simp\Set$, such as [[topological space]]s or [[spectrum|spectra]], since then any $V$-category becomes a $\Simp\Set$-category as well in a natural way.  Finally, although a general [[model category]] need not be enriched over anything, it is always "almost" enriched over $\Simp\Set$, and so one can still make sense of this using the techniques of _framings_ and _resolutions_; see the books of Hirschhorn and Hovey.

Following the reasoning described in Example 1 of [[representable functor]] one then defines the homotopy limit $L$ of a functor $F: K \to C$ to be a representing object for such homotopy cones, in the sense that we have a (weak) equivalence
$$ Map(X,L) \simeq HoCones(X,F)$$
of [[hom-objects]] (spaces or simplicial sets in the classical context; enriched hom-objects in the enriched context).


### Global versus local

The global definition is formulated in terms of [[weak equivalence|weak equivalences]] only, while the local definition is formulated in terms of [[homotopy|homotopies]] only.  However, in practical cases, derived functors exist because their input objects (in this case, the diagram $F$) can be replaced by "good" (fibrant and/or cofibrant) objects in such a way that weak equivalences become _homotopy_ equivalences.  The derived functor of $lim$ at the input object $F$ is then computed by applying the ordinary functor $lim$ to a good replacement $R F$ of $F$.

It then turns out that the "good" (precisely, "fibrant") replacement $R F$ "builds in" precisely the right homotopies so that an ordinary cone over $R F$ is the same as a homotopy-commutative cone over $F$.  Therefore, $lim (R F)$, which is the global homotopy-limit of $F$, is a representing object for homotopy-commutative cones over $F$, and thus is also a local homotopy-limit of $F$.  There is a dual argument for colimits using cofibrant replacements.

Formal versions of this argument can be found in many places.  Perhaps the original statement can be found in XI.8.1 of:

* A. K. Bousfield and D. M. Kan, _Homotopy limits, completions, and localizations_.

(As was often the case with Kan's papers at that time, there are some details omitted from that treatment, but most are, as he claimed, quite easy to complete.)  For another approach in an algebraic context, there is a description in Illusie's thesis.

An abstract version in modern language, with proof, can be found in

* Michael Shulman, [Homotopy limits and colimits and enriched homotopy theory](http://arxiv.org/abs/math/0610194).


#### Strictness 

Another notable difference between the local and global definitions is that the global definition can only ever define the homotopy limit up to weak equivalence (isomorphism in the homotopy category), while in the local definition we _could_ require, if we wanted to, an actual isomorphism
$$ Map(X,L) \cong HoCones(X,F)$$
of hom-objects, rather than merely a weak equivalence.  By analogy with [[strict 2-limit|strict 2-limits]], we may call such an object a **strict homotopy limit**.

Frequently a strict homotopy limit does in fact exist, and can be constructed as a [[weighted limit]] in the ordinary (enriched) category in question.  In such cases, the strict homotopy limit may be easier to compute with than an arbitrary homotopy limit merely known to have the up-to-weak-equivalence universal property.  Thus, sometimes when people say [[generalized the|the]] homotopy limit they refer mean a _strict_ homotopy limit.

When a strict homotopy limit exists, an arbitrary homotopy limit may be defined as an object which is (weakly) equivalent to the strict homotopy limit.

### Derivators {#Derivators}

It is noteworthy that the homotopy limit and colimit in a [[category with weak equivalences]] are drastically different from the from the ordinary [[limit]] and colimit in the corresponding [[homotopy category]]: the universal property of the full $(\infty,1)$-categorical limits and colimits crucially does take into account the explicit higher cells and does not work just up to any higher cells.

This (obvious) observation is a very old one and can be seen to be one of the driving forces behind the insight that just working with [[homotopy categories]] misses crucial information, something which today is understood as the statement that a homotopy category is just the [[decategorification]] of an [[(∞,1)-category]].

While the full theory of [[(∞,1)-categories]] is one way to impose the correct notion of higher categorical limits, there are other ways to deal with issue. Due to [[Alexander Grothendieck]] is the technique of using **[[derivator]]s** for keeping track of homotopy limits.

Roughly, the idea of a derivator is that while the single [[homotopy category]] $Ho(C)$ of a category $C$ with weak equivalences is not sufficient information, the homotopy limit of a diagram in $[D,C]$ _is_ encoded in the homotopy category $Ho([D,C])$ of that [[functor category]] (this is after all the domain of the plain 1-categorical [[derived functor]] of the limit functor). Accordingly, what is called the [[derivator]] of a category with weak equivalences $C$ is a collection of _all_ the homotopy categories $Ho([D,C])$ of _all_ the possible [[diagram]] categories $[D,C]$, as $D$ runs over all small categories. See there for more details.


## Homotopy limits versus higher categorical limits

As a special case of enriched homotopy theory, we may consider model categories or homotopical categories that are enriched over a notion of $n$-category as presentations for $(n+1)$-categories.  (Here we allow $n$ to also be of the form [[(n,r)-category|(n,r)]], with the obvious convention that $(n,r)+1 = (n+1,r+1)$ and $\infty+1=\infty$.)  For example:

* [[simplicial set]]s are models for $\infty$-[[infinity-groupoid|groupoids]] ($(\infty,0)$-categories), so [[simplicial model category|simplicial model categories]] are presentations for $(\infty,1)$-categories.  Of course, arbitrary model categories are also presentations for $(\infty,1)$-categories, but simplicial model categories are easier to work with, and in particular easier to construct homotopy limits in.

* A [[Cat]]-enriched category is just a [[strict 2-category]], so a [[model 2-category]] or [[homotopical 2-category]] is a presentation of a weak [[2-category]] (or [[bicategory]]).

* A $(2Cat,\otimes_{Gray}$)-enriched category is a [[Gray-category]], and a [[model Gray-category]] or [[homotopical Gray-category]] is a presentation of a weak [[3-category]] (or [[tricategory]]).

If $C$ is a category enriched over $(n-1)$-categories and we are considering it to _be_ an $n$-category (which happens to be strict at the bottom level), it is natural to define a "weak equivalence" in the underlying ordinary category of $C$ to be a morphism that is an $n$-category-theoretic [[equivalence of categories|equivalence]].  We call this the _natural_ or _trivial_ homotopical structure on $C$.  In certain cases (such as $n=2)$ it can be made into a model structure, also called _natural_ or _trivial_.

Since higher categorical limits are generally defined as representing objects for cones that commute up to [[equivalence]], it is unsurprising that if $C$ has a natural homotopical structure, locally-defined homotopy limits and $n$-limits coincide.  For $n=1$ this is trivial.  For $n=2$ it is proven in the paper of Gambino referenced below (particularly section 6).  For $n=(\infty,1)$ it is proven in (among other places) Lurie's book, section 4.2.4.  The case $n=3$ ought to be approachable in theory, but doesn't seem to have been done (probably partly because the general theory of 3-limits is fairly nonexistent).

On the other hand, we may also consider a category $C$ enriched over $n$-categories with a _larger_ class of weak equivalences than just the $n$-categorical equivalences.  Then $C$ presents an $n$-category (its "homotopy $n$-category") obtained by formally turing these weak equivalences into $n$-categorical equivalences.  Homotopy limits in $C$ with this homotopical structure should then present $n$-limits in its homotopy $n$-category.  In the case $n=(\infty,1)$ this is also essentially in Lurie's book; for other values of $n$ it may not be in the literature.


## Examples 

### General weighted colimit formula for homotopy colimits {#WeightedColimitFormula}

Let 

* $C$ be a [[combinatorial model category|combinatorial]] [[simplicial model category|simplicial]] [[model category]] 

* let $D$ be a [[small category|small]] [[simplicially enriched category]] 

  (possibly an ordinary [[locally small category]] regarded as a [[SSet]]-[[enriched category]] in the tautological way) 

* and let $F : D \to C$ be an [[SSet]]-[[enriched functor]].

There is a general formula for the homotopy colimit over $F$ in terms of a [[coend]] or [[weighted colimit]] in $C$, using the following ingredients:

#### Ingredients 

for $C$ a [[combinatorial simplicial model category]] as above and for $D$ any [[simplicially enriched category]] there is the projective and the injective [[global model structure on functors]] on the [[enriched functor category]] $[D,C]$.

* In the projective model structure $[D,C]_{proj}$ the fibrations and the local equivalences are objectwise those of $C$

* In the injective model structure $[D,C]_{inj}$ the cofibrations and the local equivalences are objectwise those of $C$.

Each of these is itself a [[combinatorial simplicial model category]], so in particular the [[small object argument]] applies in these using which one obtains cofibrant replacement functors

$$
  Q_{proj} : [D, C] \to [D, C]
$$

and

$$
  Q_{inj} : [D, C] \to [D, C]
  \,.
$$

That $C$ is a [[simplicial model category]] implies in particular that it is [[copower|tensored]] over [[SSet]] and that the tensoring functor

$$
  \otimes : C \times SSet \to C
$$

is a left [[Quillen bifunctor]]. By the properties of Quillen bifunctors discussed there, it follows that the [[coend]]s over the [[copower|tensor]] in the form

$$
  \int^D (-) \otimes (-) : [D^{op},SSet]_{proj} \times [D,C]_{inj} \to C
$$

and in the form

$$
  \int^D (-) \otimes (-) : [D^{op},SSet]_{inj} \times [D,C]_{proj} \to C
$$

both themselves left [[Quillen bifunctor]]s. 

Write

$$
  {*} : D^{op} \to SSet
$$

for the functor that sends everything to the identity on the singleton set. This is the tensor unit in the [[monoidal category]] $[D^{op},SSet]$.


#### General formula

+-- {: .un_theorem }
###### Theorem

With the above assumptions and ingredients, the homotopy colimit over $F : D \to C$ is given either by 

$$
  hocolim F = \int^D Q_{proj}({*}) \otimes Q_{inj}(F) 
$$

or by

$$
  hocolim F = \int^D Q_{inj}({*}) \otimes Q_{proj}(F) 
  \,.
$$



=--

+-- {: .proof}
###### Proof

By the fact that the [[coend]] over the [[copower|tensor]] appearing here is a [[Quillen bifunctor]].

This is disucssed for instance in section 4 of

* [[Nicola Gambino]], _Weighted limits in simplicial homotopy theory_ ([pdf](http://www.crm.cat/Publications/08/Pr790.pdf))

=--

#### Examples

##### Homotopy colimits over simplicial diagrams

Let $D = \Delta^{op}$ be the [[opposite category]] of the [[simplex category]]. 

+-- {: .un_prop }
###### Proposition

A cofibrant replacement of the [[terminal object]] ${*}$ in the projective [[global model structure on functors]] $[\Delta, SSet]$ is the the [[fat simplex]]-functor that assigns to $[n]$ the [[nerve]] of [[opposite category]] of the [[undercategory]] of $\Delta^{op}$ under $[n]$

$$
  N(-/\Delta^{op})^{op} : \Delta \to SSet
  \,.
$$

=--

+-- {: .proof}
###### Proof

For instance prop 14.8.8 in 

* Hirschhorn, _Model categories and their localization_ 

=--

Notice that if $F : \Delta^{op} \to C$ takes values in cofibrant objects of $C$, then it is itself cofibrant as an object of $[\Delta^{op},C]_{inj}$. In that case no further cofibrant replacement of $F$ is necessary and it therefore follows with the general formula and the above proposition that the homotopy colimit over $F$ is given by the formulas

$$
  hocolim F = \int^{[n] \in \Delta} N([n]/\Delta)^{op} \otimes F(n)
  \,.
$$

This is famously the formula introduced and used by Bousfield and Kan (but there originally missing the necessary condition that $F$ be objectwise cofibrant). See [[Bousfield-Kan map]].

##### Homotopy pushouts

Let in the above general formula $D = \{a \leftarrow c to b\}$ be the [[walking]] [[span]]. Ordinary [[colimit]]s parameterized by such $D$ are [[pushout]]s. Homotopy colimits over such $D$ are **homotopy pushouts**.

In this simple case, we have the following simple observation:

+-- {: .un_lemma }
###### Observation

For $D$ as above, the terminal functor ${*} : D \to SSet$ is already cofibrant in $[D,SSet]_{inj}$.

=--

Moreover

+-- {: .un_lemma }
###### Observation

For $D$ as above, a functor $F : D \to C$ is cofibrant in $[D,C]_{proj}$ if 

* it sends both morphisms $c \to a$ and $c \to b$ to cofibrations 

* it sends $c$ (and hence also $a$ and $b$) to cofibrant objects in $C$.

=--

Since a coend $\int {* } \otimes F$ over a tensor product where the first factor in the integrand in the tensor unit is just an ordinary [[colimit]] over the remaining $F$, it follows that if $F$ is of the form of the above observation, then the ordinary colimit over $F$ already computes the homotopy pushout:

$$
  hocolim F = \lim_\to F
  \,.
$$

The dual version of this statement (for homotopy limits and homotopy pullbacks) is discussed in more detail in the examples below.
 

### Homotopy pullbacks {#HomotopyPullbacks}

Here we consider special cases of [[homotopy pullback]] in more detail.

Let $D = \{ 1\to 0 \leftarrow 2\}$ be the pullback [[diagram]], so that limits over it compute [[pullback]]s, and assume that $F : D \to C$ is such that
$$
  F(1) \to F(0) \leftarrow F(2)
$$
satisfies
* $F(i)$ is fibrant for all $i$;
* and either $F(1) \to F(0)$ or $F(2) \to F(0)$ is a fibration;

then

* $holim_D F$ exists;
* and is weakly equivalent to the ordinary limit $holim_D F \stackrel{\simeq}{\to} lim_D F$.

Conversely this means that on an arbitrary pullback diagram  $holim_D F$ can be computed by finding a natural transformation $F \Rightarrow R F$ whose component morphisms are weak equivalences and such that $R F$ satisfies the above conditions.


#### Based loop objects 


For $B$ any [[pointed object]] with point $pt \stackrel{pt_B}{\to} B$ the homotopy pullback of the point along itself is the [[loop space object]] of $B$

$$
  \array{
    \Omega_{pt} &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& B
  }
  \,,
$$

i.e.

$$
  holim(  pt \stackrel{pt_B}{\to}  B \stackrel{pt_B}{\leftarrow} pt)
  \;\stackrel{\simeq}{\to}\;
  \Omega_{pt} B
  \,.
$$

One way to compute this using the above prescription by noticing that the [[generalized universal bundle]] $\mathbf{E}_{pt} B$ provides a fibrant replacement of the pullback diagram in that we have

$$
  \array{
     pt &\to& B &\leftarrow& pt
     \\
     \downarrow^{\simeq} && \downarrow^{Id} && \downarrow^{Id}
     \\
    \mathbf{E}_{pt}B &\to& B &\leftarrow& pt
  }
$$

with all vertical morphisms weak equivalences and with the left bottom horizontal morphism a fibration.

More on that in the further examples below.

#### Fibration sequences 

If $C$ is a [[pointed object]], with point ${*} \to C$, then for a homotopy pullback of the form

$$
  \array{
     A &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     B &\to& C
  }
$$

the sequence $A \to B \to C$ is called a [[fibration sequence]]. The object $A$ is the _homotopy kernel_ or _homotopy fiber_ of $B \to C$. Since homotopy pullback squares compose to homotopy pullback squares, the homotopy kernel of a homotopy kernel is not trivial, but is a [[loop space object]]

$$
  \array{
     \Omega C &\to& A &\to& {*}
     \\
     \downarrow && \downarrow && \downarrow
     \\
     {*} &\to& B &\to& C
  }
  \,.
$$


#### Homotopy pullback of a point over a group / universal bundles {#GroupDeloop}

As a special case of the above general example we get the following.

Let $C =$ [[Grpd]] equipped with the [[canonical model structure]]. Write $G$ for a [[group]] regarded as a discrete monoidal groupoid (elements of $G$ are the objects of the groupoids and all morphisms are identities) write and $\mathbf{B}G$ for the corresponding one-object [[groupoid]] (single object, one morphism per element of $G$). Write $pt$ for the terminal groupoid (one object, no nontrivial morphism). 
Notice that there is a unique functor $pt \to \mathbf{B}G$.
Then we have
$$
  holim
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       pt &\to& \mathbf{B}G
    }
  \right)
  \stackrel{\simeq}{\to}
  G
  \,.
$$
To see this, we compute using the above prescription by finding a weakly equivalent pullback diagram such that one of its morphisms is a fibration. This is achived in particular by the [[generalized universal bundle]]
$pt \stackrel{\simeq}{\to} \mathbf{E}G \to\gt \mathbf{B}G$, where $\mathbf{E}G$ is the [[action groupoid]] $G//G$ of $G$ 
acting on itself by multiplication from one side. So we have a weak equivalence of pullback diagrams
$$
  \array{
     pt &\to& \mathbf{B}G &\leftarrow& pt
     \\
     \downarrow^{\simeq} && \downarrow^= &&
     \downarrow^= 
     \\
     \mathbf{E}G &\to& \mathbf{B}G &\leftarrow& pt 
  }
$$
and the homotopy limit in question is weakly equivalent to the ordinary limit over the lower diagram. That is directly seen to be $Disc(Obj(\mathbf{E}G)) = Disc(Obj(G//G)) = Disc(G)$ which we just write as $G$:
$$
  holim 
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       pt &\to& \mathbf{B}G
    }
  \right)
  \stackrel{\simeq}{\to}
  lim
  \left(
    \array{
       && pt
       \\
       && \downarrow
       \\
       \mathbf{E}G &\to& \mathbf{B}G
    }
  \right)  
  = G
  \,.
$$
This example is important in the context of [[groupoidification]] and [[geometric function theory]], as described there. A closely related example is the following: a functor $\rho:\mathbf{B}G\to {Top}$ is the datum of a toplogical space $X$ equipped with an action of $G$. Then, $colim(\rho)=X/G$ whereas $hocolim(\rho)=\mathbf{E}G\times_G X$, see [[equivariant cohomology]].

#### Homotopy pullback of a subgroup over a group 

The above example generalizes straightforwardly
to the case where the trivial 
inclusion $pt \to \mathbf{B}G$ is replaced by any inclusion  $\mathbf{B}H \hookrightarrow \mathbf{B}G$ of any subgroup $H$ of $G$ pretty much literally by replacing $pt$ by $\mathbf{B}H$ throughout. 

One finds

$$
  holim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{B}H &\to& \mathbf{B}G
   }
  \right)
  \stackrel{\simeq}{\to}  H \backslash\backslash G//H
$$

where on the right we have the [[action groupoid]] of $H \times H$ acting on $G$ by multiplication from the left (first factor) and the right (second factor).

To see this, we again build a fibrant replacement of the pullback diagram. Following the constructions at [[generalized universal bundle]] consider first the groupoid $\mathbf{E}_{\mathbf{B}H}G$ given by the pullback diagram

$$
  \array{
    \mathbf{E}_{\mathbf{B}H}G &\to& \mathbf{B}H
    \\
    \downarrow && \downarrow
    \\
    [I, \mathbf{B}G] &\stackrel{d_0}{\to}& \mathbf{B}G
    \\
    \downarrow^{d_1} 
    \\
    \mathbf{B}G
  }
  \,.
$$

As at [[generalized universal bundle]] one proves that the left vertical morphism
$\mathbf{E}_{\mathbf{B}H}G \to \mathbf{B}G$ is a fibration.

Now, notice (which was implicit in the above example) that since $[I,\mathbf{B}G]$ is a [[path object]] in a [[category of fibrant objects]] we have a [[section]]
$
  \mathbf{B}G \stackrel{\simeq}{\to}^\sigma  [I, \mathbf{B}G] 
$
of $[I,\mathbf{B}G] \stackrel{d_0}{\to} \mathbf{B}G$. In the above pullback diagram this induces a morphism 
$
  \mathbf{B}H \stackrel{\sigma}{\to} \mathbf{E}_{\mathbf{B}H}G
$ 
making the obvious diagram commute. Now, the latter morphism, being the pullback of an acyclic fibration is an acyclic fibration, so its right inverse $\sigma$ is a weak equivalence. This way we obtain the morphism of pullback diagrams

$$
  \array{
    \mathbf{B}H &\to& \mathbf{B}G &\leftarrow& \mathbf{B}H
    \\
    {}^\simeq\downarrow^{\sigma} && \downarrow^{Id} 
     && \downarrow^{Id} 
    \\
    \mathbf{E}_{\mathbf{B}H}G &\to \gt& \mathbf{B}G &\leftarrow& \mathbf{B}H
  }
$$
which is objectwise a weak equivalence and such that the horizontal morphism on the bottom left is a fibration. By the above statement the ordinary limit of the lower horizontal diagram is weakly equivalent to the homotopy limit we are looking for. But this is manifestly the desired action groupoid:

$$
  holim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{B}H &\to& \mathbf{B}G
   }
  \right)
  \stackrel{\simeq}{\to}
  \lim\left(
   \array{
     && \mathbf{B}H
     \\
     && \downarrow
     \\
     \mathbf{E}_{\mathbf{B}H} G &\to& \mathbf{B}G
   }
  \right)
  \simeq
  \lim\left(
   \array{
     && [I,\mathbf{B}G]
     \\
     && \downarrow^{d_0 \times d_1}
     \\
     \mathbf{B}H \times \mathbf{B}H 
     &\to& \mathbf{B}G \times \mathbf{B}G
   }
  \right)
  =
  H \backslash\backslash G//H
  \,.
$$

This example, too, is important at [[geometric function theory]].



#### Homotopy span traces

* see the homotopy span traces discussed at 
  [[span trace]] for more examples of homotopy pullbacks


### Homotopy colimits over simplicial diagrams {#OverSimplicialDiagrams}

+-- {: .un_prop}
###### Proposition

Every [[simplicial set]] is the homotopy colimit over its cells.

Precisely: for $X \in $ [[sSet]] a [[simplicial set]], let 

$$
  \tilde X : \Delta^{op} \to Set \hookrightarrow sSet
$$

be the corresponding [[bisimplicial set]] which in degree $k$ is the the constant simplicial set on the set $X_k$ of $k$-simplices. 

For the standard homotopical structure on $sSet^{\Delta^{op}}$, the homotopy colimit over $\tilde X$ is equivalent to the origianal $X$:

$$
  hocolim \tilde X \stackrel{\simeq}{\to} X
$$

in the standard [[model structure on simplicial sets]].

=--

+-- {: .proof}
###### Proof

Use the [[Reedy model structure]] $[\Delta^{op}, sSet_{Quillen}]_{Reedy}$. With the coend recipe for the hocolim discussed above, it follows that the hocolim is the [[coend]]

$$
  \int^{[k] \in \Delta} Q'_{Reedy}(*) \times Q_{Reedy}(\tilde X)
  \,,
$$

where $Q'_{Reedy}(\cdots)$ is a cofibrant resolution in the Reedy model structure $[\Delta,sSet_{Quillen}]_{Reedy}$ and $Q_{Reedy}(...)$ in $[\Delta^{op}, sSet_{Quillen}]_{Reedy}$. But by the discussion at <a href="http://ncatlab.org/nlab/show/Reedy+model+structure#SimplexCategory">Reedy model structure -- simplex category</a> we have that

* $\tilde X$ is always cofibrant in $[\Delta^{op},sSet_{Quillen}]_{Reedy}$;

* a cofibrant resolution of the point in $[\Delta, sSet_{Quillen}]_{Reedy}$ iss given by $\Delta[-] : \Delta \to sSet$.

It follows that the hocolim is given by 

$$
  \int^{[k] \in \Delta} \Delta[k] \times X_k
  \,.
$$

By the [[co-Yoneda lemma]] this is [[isomorphic]] to $X$.

=--


+-- {: .un_remark}
###### Remark

This kind of argument has many immediate generalizations. For instance for $C = [K^{op}, sSet_{Quillen}]_{inj}$ the injective [[model structure on simplicial presheaves]] over any small category $K$, or any of its left [[Bousfield localization of model categories|Bousfield localizations]], we have that the cofibrations are objectwise those of simplicial sets, hence objectwise monomorphisms, hence it follows that every simplicial presheaf $X$ is the hocolim over its simplicial diagram of component presheaves.

=--

For the following write $\mathbf{\Delta} : \Delta \to sSet$ for the [[fat simplex]].  

+-- {: .un_prop}
###### Observation

The fat simplex is Reedy cofibrant.

=--


+-- {: .proof}
###### Proof

By the discussion at [[homotopy colimit]], the fat simplex is cofibrant in the projective [[model structure on functors]] $[\Delta, sSet_{Quillen}]_{proj}$. By the [general properties](#Properties) of Reedy model structures, the identity functor $[\Delta, sSet_{Quillen}]_{proj} \to [\Delta, sSet_{Quillen}]_{Reedy}$ is a [[Quillen adjunction|left Quillen functor]], hence preserves cofibrant objects.

=--


+-- {: .un_prop}
###### Corollary

For $X \in [\Delta^{op}, C]$ a Reedy cofibrant object, the [[Bousfield-Kan map]]

$$
  \int^{[n]} \mathbf{\Delta}[n] \cdot X_n
  \to
  \int^{[n]} \Delta[n] \cdot X_n  
$$

is a weak equivalence in $C$.

=--

+-- {: .proof}
###### Proof

The [[coend]] over the [[copower|tensor]] is a left [[Quillen bifunctor]]

$$
  \int (-)\cdot (-) : [\Delta,sSet_{Quillen}]_{Reedy} \times
    [\Delta^{op}, C]_{Reedy}
$$

(as discussed there). Therefore with its second argument fixed and cofibrant it is a [[Quillen adjunction|left Quillen functor]] in the remaining argument. As such, it preserves weak equivalences between cofibrant objects (by the [[factorization lemma]]). By the above discussion, both $\mathbf{\Delta}[n]$ and $\Delta[-]$ are indeed cofibrant in $[\Delta,sSet_{Quillen}]_{Reedy}$. Clearly the functor $\mathbf{\Delta}[-] \to \Delta[-]$ is objectwise a weak equivalence in $sSet_{Quillen}$, hence is a weak equivalence.

=--

### Homotopy colimits over diagrams of spaces


+-- {: .un_theorem}
###### Theorem

Let $X$ be a [[topological space]], write $Op(X)$ for its [[category of open subsets]] and let

$$
  \chi : C \to Op(C)
$$

a [[functor]] out of a [[small category]] $C$ such that

* for each point $x\in X$ the [[full subcategory]] $C_x$ of objects $c$ such that $\chi(x)$ contains $x$ has a [[weak homotopy equivalence|weakly]] [[contractible]] [[nerve]].

Then:

the canonical morphism in [[sSet]] out of the [[colimit]]

$$
   {\lim_\to} Sing \circ \chi \to Sing(X)
$$ 

into the [[singular simplicial complex]] of $X$ exhibits $Sing(X)$ as the [[homotopy colimit]]  $hocolim Sing \circ \chi$.


=--

See [[higher homotopy van Kampen theorem]] for details.

### Descent objects

_Descent objects_ as they appear in [[descent|descent and codescent]] are naturally conceived as homotopy limits. See also [[infinity-stack]].

### Homotopy (co)limits of simplicial pre(sheaves) {#SimpSheaves}

The local [[model structure on simplicial presheaves]] $SPSh(C)_{proj/inj}^{loc}$ over a [[site]] $C$  serve as [[models for ∞-stack (∞,1)-toposes]]. 

Here we discuss some properties of homotopy limits and colimits in such model categories of simplicial presheaves.

#### Preservation of homotopy pullback by inverse images

For $C, C'$ two [[site]]s, a [[geometric morphism]] $p : Sh(C) \stackrel{\leftarrow}{\to} Sh(C')$  of [[Grothendieck topos|sheaf topos]]es induces correspondingly an [[adjunction]]

$$
  p : SSh(C) \stackrel{\leftarrow}{\to} SSh(C') : p^*
$$

of simplicial (pre)sheaves. One would like this to extend to a [[Quillen adjunction]] that recalls the fact that it came from a geometric morphism by the fact that the [[left adjoint]] [[inverse image]] functor $SSh(C') \to SSh(C)$ preserves finite homotopy limits.

In particular, if $C$ and $C'$ have the same underlying category but $C'$ the trivial [[coverage]], then the [[geometric morphism]] in question is the inclusion of a [[reflective subcategory]] which typically induces a [[Bousfield localization]] of model categories that models the injection of a [[reflective (∞,1)-subcategory]] of [[∞-stack]]s into $\infty$-presheaves. Here the morphism $SPSh(C') \to SPSh(C)$ is $\infty$-stackification and should preserve finite homotopy limits.

The following result says that a strong version of this statement is true, at least for the preservation of homotopy pullbacks.


+-- {: .un_theorem }
###### Theorem

Let $p : Sh(C) \to Sh(C')$ be a [[geometric morphism]] of [[Grothendieck topos]]es. Let $p^* : Sh(C') \to Sh(C)$ be the corresponding [[inverse image]] functor and let $s p^* : SSh(C') \to SSh(C)$ be its degreewise extension to functor of [[simplicial presheaf|simplicial sheaf]] categories.

Regarded as a functor between the corresponding [[local model structure on simplicial sheaves|local injective model structures on simplicial sheaves]] on both sides

$$
  s p^* : SSh(C')_{inj}^{loc} \to SSh(C)_{inj}^{loc}
$$

this functor preserves homotopy pullbacks.

=--

+-- {: .proof}
###### Proof

This appears as theorem 1.5 in

* [[Charles Rezk]], _Fibrations and homotopy colimits of simplicial sheaves_ ([arXiv](http://arxiv.org/abs/math/9811038))

=--



## References 

The classical reference is 

* A. K. Bousfield and D. M. Kan, _Homotopy limits, completions, and localizations_.  Springer LNM 304.  

see in particular chapter XI.

An inroduction is 

* [[Dan Dugger]], _A primer on homotopy colimits_ ([pdf](http://www.uoregon.edu/~ddugger/hocolim.pdf))


* Wojciech Chacholski and Jerome Scherer, _Homotopy theory of diagrams_ ([arXiv](http://arxiv.org/abs/math.AT/0110316)) 

This includes a global definition of homotopy (co)limit as [4.1, p. 14](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=19), and discusses how to compute them (co)limits concretely using local constructions.  For instance the above statement on the computation of homotopy pullbacks is proposition [2.5, p. 15](http://arxiv.org/PS_cache/math/pdf/0110/0110316v1.pdf#page=20)

* Philip Hirschhorn, _Model categories and their localizations_.  Defines and studies (local) homotopy limits in model categories.

* Dwyer, Hirschhorn, Kan, Smith, _Homotopy limit functors in model categories and homotopical categories_.  Defines global homotopy limits in homotopical categories and computes them using local constructions.

* Michael Shulman, [Homotopy limits and colimits and enriched homotopy theory](http://arxiv.org/abs/math/0610194).  Constructs and compares local and global weighted homotopy limits in enriched homotopical categories.

* Nicola Gambino, _Homotopy limits for 2-categories_ ([pdf](http://www.lacim.uqam.ca/~gambino/homotopy.pdf)), published as: Mathematical Proceedings of the Cambridge Philosophical Society 145 (2008) 43-63.)  Proves that homotopy limits in a 2-category with its natural model structure coincide with 2-categorical [[strict 2-limit|pseudo-limits]], and hence give [[2-limit]]s.

* [[Jacob Lurie]], [[Higher Topos Theory]].  Lots of stuff about $(\infty,1)$-categories, including the computation of homotopy limits (section 4.2.4).

* Andre Hirschowitz, Carlos Simpson.  [Descent pour les n-champs](http://arxiv.org/abs/math.AG/9807049).  Probably there is some good stuff in here about homotopy limits and limits in $(\infty,n)$-categories.


+--{.query}
[[Tim Porter|Tim]]  Mike, are you intending to treat the case of when the domain category, $D$ is the above, is enriched as well? This would handle the example of homotopy limts of homotopy coherent diagrams, both in Vogt's sense and in the simplicially enriched case looked at by Bourn and Cordier. This would also allow the $G$ in one of the examples to be a simplicial or topological group, or to be (?) and A-infinity category. (Some of those examples may be already dealt with in others of the entries as different people classify things in different ways.)

Perhaps some of the more classical referencs, Vogt, Bousfield-Kan etc. might be included for completeness.

[[Mike Shulman|Mike]]: Yes, certainly; my paper referenced above deals with the case when $D$ is enriched as well.  There are cofibrancy technicalities, of course.  I'm not against including the classical references, although I find them fairly impenetrable myself.

=--

[[!redirects homotopy limits]]
[[!redirects homotopy colimit]]