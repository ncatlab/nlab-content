<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents
* automatic table of contents goes here
{:toc}

## Idea 

Bousfield localization is a procedure that to a [[model category]] structure $C$ assigns a new one with more weak equivalences.

A _left Bousfield localization_ $C_{loc}$ of a model category $C$ is another model category structure on the same underlying category with the same cofibrations, but more weak equivalences. Similarly for _right Bousfield localization_ and fibrations.

It follows that the identity functor between a model category and its left (right) Bousfield localization preserves weak equivalences and cofibrations (fibrations) and hence yields a [[Quillen adjunction]]

$$
  C_{loc} \stackrel{\leftarrow}{\to} C
  \,.
$$

But a very special one: left (right) Bousfield localization, by increasing the collection of weak equivalences, reduces the collection of fibrant (cofibrant) objects, and hence picks a smaller subcategory of fibrant-and-cofibrant objects. Indeed, 

+-- {: .standout}

Bousfield localization is a model category version of reflecting onto a [[reflective subcategory]].

=--

Indeed -- at least when $C$ is a [[combinatorial simplicial model category]] -- Bousfield localization is an example of a [[localization of a simplicial model category]] and under [[presentable (infinity,1)-category|passage to the sub-category of fibrant-cofibrant objects]] this Quillen adjunction becomes the inclusion of a [[reflective (∞,1)-subcategory]]

$$
  {C_{loc}}^\circ \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  C^\circ
$$

hence of a [[localization of an (∞,1)-category]].

Such a localization is determined by the collection $S$ of _[[local object|local weak equivalences]]_ in $C$, and alternatively by the collection of $S$-[[local object]]s in $C$. Indeed, ${C_{loc}}^\circ$ is the full $(\infty,1)$-subcategory on the cofibrant and fibrant and $S$-local objects of $C$.


## Definition 

We first give a simpler definition, that however involves more assumptions. The more sophisticated definition does not need these assumptions. We'll see below how these two definitions relate.

### Simple version 

Let $C$ be a [[proper model category|left proper]] [[simplicial model category]]. 

Let $S \subset cof_C \subset Mor(C)$ be a subclass of cofibrations with cofibrant domain.

We want to characterize objects in $C$ that "see elements of $S$ as weak equivalences". Notice that in an ordinary catgegory $C$, by the [[Yoneda lemma]] a morphism $f : A \to B$ is an [[isomorphism]] precisely if for all objects $X$ the morphism

$$
  Hom_C(f,X) : Hom_C(B,X) \to Hom_C(A,X)
$$

is an [[isomorphism]] (of sets, i.e. a [[bijection]]). So we can "test isomorphism by homming them into objects".

This phenomenon we use now the other way round:

+-- {: .un_def }
###### Definition
**($S$-local objects and $S$-local weak equivalences)

Say that

* a fibrant object $X$ is an $S$-[[local object]] if for all $s : A \hookrightarrow B$ in $S$ the morphism

  $$
    C(s,X) : C(B,X) \to C(A,X)
  $$

  is a trivial [[Kan fibration]];

* conversely, say that a cofibration $f : A \hookrightarrow B$ is an $S$-local weak equivalence if for all $S$-local fibrant objects $X$ the morphism $C(f,X) : C(B,X) \to 
C(A,X)$ is a trivial [[Kan fibration]].

=--

+-- {: .un_def }
###### Definition
**(left Bousfield localization)**

The left Bousfield localization $L_S C$ of $C$ at $S$ is, if it exsists, the new [[cofibrantly generated model category]] structure on $C$ with

* cofibrations are the same as before, $cof_{L_S C } = cof_C$;

* acyclic cofibrations are the cofibrations that are $S$-local weak equivalences.

=--

Assume that $L_S C$ exists. Then we have the following direct consequences of this definition:

+-- {: .un_lemma }
###### Observation

The fibrant objects of $L_S C$ are precisely the 
original fibrant objects that are also $S$-[[local object]]s.

=--


+-- {: .proof}
###### Proof

The new acyclic cofibrations are the smallest staurated class containing all the old acyclic cofibrations as well as all elements in $S$. (...explain more...).

=--



+-- {: .un_lemma }
###### Observation

The $S$-local weak equivalences between $S$-local fibrant objects are the original weak equivalences.

=--

+-- {: .proof}
###### Proof

(This is currently proven towards the end of the big proof below. Will move that up here.)

=--






### More sophisticated version


Let $C$ be a category equipped with a [[model category]] structure and let 

$$
  S \subset Mor(C)
$$ 

be a [[class]] of morphisms in $C$. 




An $S$-[[local object]] $X$ is one such that the [[derived hom space]] functor $\mathbf{R}Hom(-,X)$ sends morphisms in $S$ to weak equivalences. An $S$-local morphism $f$ is one such that $\mathbf{R}Hom(f,-)$ sends local objects to weak equivalences.

Write $W_S \subset Mor(C)$ for the collection of $S$-local morphisms. Notice that this contains all the weak equivalences of $C$

$$
  W_C \subset W_S
  \,.
$$

+-- {: .un_def }
###### Definition (Bousfield localization)

The **left Bousfield localization** of $C$ with respect to $S$ is, if it exists, a [[model category]] structure $L_S C$ on $C$ such that

* the class of cofibrations of $L_S C$ equals that of $C$

  $$
    cof_{L_S C} = cof_C
  $$

* the class of weak equivalences of $L_S C$ equals the class of $S$-[[local equivalence]]s of $C$

  $$
    W_{L_S C} = W_S \subset W_C
  $$

The **right Bousfield localization** is defined analogously, with the role of fibrations and cofibrations exchanged.

=--



## Existence proof for combinatorial model categories

We discuss the existence of Bousfield localization in the context of [[combinatorial model category|combinatorial model categories]]. A similar existence result is available in the slightly more general context of [[cellular model category|cellular model categories]], but for the combinatorial case a somewhat better theory is available. 

By the corollary to [Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) on presentations for [[combinatorial model category|combinatorial model categories]] we have that every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to a [[proper model category|left proper]] [[simplicial model category|simplicial]] combinatorial model category. 

Therefore there is little loss in assuming this extra structure, which the following statement of the theorem does.


+-- {: .un_theorem }
###### Theorem

If $C$ is a 

* [[proper model category|left proper]] 

* [[simplicial model category|simplicial]]

* [[combinatorial model category]] 

* and $S \subset Mor(C)$ is a small [[set]] of morphisms, 

then the left Bousfield localization $L_S C$ does exist as a [[combinatorial model category]].

Moreover, it satisfies the following conditions:

* the fibrant objects of $L_S C$ are precisely the $S$-[[local object]]s of $C$ that are fibrant in $C$;

* $L_S C$ is itself a left [[proper model category]]

* $L_S C$ is itself a [[simplicial model category]].


=--

+-- {: .proof}
###### Proof

A proof of this making use of [Jeff Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) for [[combinatorial model category|combinatorial model categories]] appears 
as [[Higher Topos Theory|HTT, prop. A.3.7.3]] and 
as theorem 2.11 in [Bar07](http://arxiv.org/abs/0708.2067) and as theorem 4.7 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf). 

We follow [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf) for the proof that the assumptions of Smith's recognition theorem are satisfied and follow [[Higher Topos Theory|HTT, prop. A.3.7.3]] for the characterization of the fibrant objects. The details are spelled out in the following subsections.

=--


### Prerequisites for the proof 

The proof we give is self-contained, except that it builds on the following notions and facts.

#### Small objects

A [[cardinal number] $\kappa$ is _regular_ if it is not the cardinality of a union of $\lt \kappa$ sets of size $\lt \kappa$. 

A [[poset]] $J$ is a $\kappa$-[[directed set]] if all subsets of cardinality $\lt \kappa$ have a commun upper bound. A $\kappa$-[[directed colimit]] is a [[colimit]] $\lim_\to F$ over a functor $F : J \to C$.

An object $X$ in a category $C$ is a $\kappa$-[[compact object]] if $C(X,-) : C \to C$ commutes with all $\kappa$-[[directed colimit]]s. For $\lambda \gt \kappa$ every $\kappa$-compact object is also $\lambda$-compact.

This means that a morphism from a $\kappa$-compact object into an object that is a $\kappa$-directed colimit over component objects always lifts to one of these component objects.

An object is a [[small object]] if it is $\kappa$-compact for some $\kappa$.

A [[locally small category|locally small]] but possibly non-[[small category]] $C$ is an [[accessible category]] if it has a small sub-[[set]] of generating $\kappa$-[[compact object]]s such that every other object is a $\kappa$-[[directed colimit]] over such generators.

If such a category has all small colimits, it is called a [[locally presentable category]].

In particular, in a locally presentable category the [[small object argument]] for factoring of morphisms applies with respect to every set of morphisms.


#### Combinatorial model categories

A [[combinatorial model category]] is a [[locally presentable category]] that is equipped with a [[cofibrantly generated model category]] structure. So in particular there is a set of generating (acyclic) cofibrations that map between [[small object]]s. 

(If we'd require smallness of the domains of the generating cofibrations only with respect to these cofibrations themselves, we have instead the notion of [[cellular model category]].)

[Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem) says that a [[locally presentable category]] has a combinatorial model category structure already if it has weak equivalences and generating cofibrations satisfying a simple condition and if weak equivalences form an [[accessible category|accessible]] [[subcategory]] of the [[arrow category]]. This means that only two thirds of the data for a generic combinatorial model category needs to be checked and greatly facilitates checking model category structures.

[Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) implies that every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to a [[proper model category|left proper]] [[simplicial model category|simplicial]] combinatorial model category.

So we may assume without much restriction of generality that we are dealing with the localization of a [[proper model category|left proper]] [[combinatorial simplicial model category]].

Since the [[small object argument]] applies, a [[combinatorial model category]] has fibrant- and cofibrant-replacement functors $P,Q : C \to C$. 

By the axioms of an [[enriched model category]] it follows that the functor

$$
  \mathbf{R}Hom_C := C(Q(-),P(-)): C^{op} \times C \to SSet
$$

takes values in [[Kan complex]]es. This is called the [[derived hom space]] functor of $C$: we think of $\mathbf{R}Hom(X,Y)$ as the [[∞-groupoid]] of maps from $X$ to $Y$, homotopies of maps, homotopies of homotopies, etc.


#### Local objects

An ordinary [[reflective subcategory]] $C_{loc} \stackrel{\stackrel{T}{\leftarrow]}}{\hookrightarrow} C$ is specified by the preimages $S = T^{-1}(isos)$ of the isomorphisms under $T$ as the full subcategory on the $S$-[[local object]]s $X$: those such that $Hom_C(A \stackrel{s \in S}{\to}B, X)$ are isomorphisms.

The analogous statement in the context of model categories uses the [[derived hom space]] functor instead: given a collection $S \subset Mor(C)$ an object $X$ is called an $S$-[[local object]] if $\mathbf{R}Hom_C(A \stackrel{s \in S}{\to} B, X)$ are weak equivalences. 

Similarly, the collection $W_S$  of morphisms $f : E \to F$ such that for all $S$-local objects $X$ $\mathbf{R}Hom_C(f,X)$ is a weak equivalence is called the collection of $S$-[[local object|local weak equivalence]]s. 

A [lemma by Lurie](http://ncatlab.org/nlab/show/local+object#PropInModCat) says that for $A \stackrel{s \in S}{\hookrightarrow} B$ a cofibration and $X$ fibrant, $X$ is $S$-local precisely if $C(s,X) : C(B,X) \to C(A,X)$ is an [[Kan fibration|acyclic Kan fibration]]. This helps identifying the $S$-local fibrant objects.

#### Homotopy (co)limits

In an ordinary category, a [[limit]] diagram is one such that applying $Hom_C(X,-) : C \to C $ to it produces a limit diagram in [[Set]], for all objects $X$. Similarly a colimit diagram is one sent to Set-limits under all $Hom_C(-,X)$.

In a model category, this has an analog with respect to the [[derived hom space]] functor $\mathbf{R}Hom_C$. A [[homotopy limit]] diagram is one sent by all $\mathbf{R}Hom_C(-,X)$ to a homotopy limit (...). Similarly for homotopy colimits.

Sometimes ordinary (co)limits in a model category are already also homotopy colimits: 

* an [observation by Barwick](http://ncatlab.org/nlab/show/local+object#PropInModCat) shows that in a [[proper model category|left proper]] [[simplicial model category]] ordinary [[pushout]]s along cofibrations are already homotopy colimits.

* an [observation by Dugger](http://ncatlab.org/nlab/show/combinatorial+model+category#hocolims) shows that [[transfinite composition]] colimits of length $\kappa$ in a combinatorial model category are automatically homotopy colimits for sufficiently large $\kappa$.

Since these are the two operations under which $cell(cof_c \cap W_C)$ is closed, this facilitates finding this closure given that by the above the elements of $cof_C \cap W_S$ are characterized by their images under $\mathbf{R}Hom_C(-,X)$ for $S$-local $X$.


#### Size issues 

The following proof uses the [[small object argument]] several times. In particular, at one point it is applied relative to the collection $S$ of morphisms at which we localize. It is at this point that we need that assumption that $S$ is indeed a (small) [[set]], and not a proper [[class]].

For the small object argument itself, this requirement comes from the fact that it involves colimits indexed by $S$. These won't in general exist if $S$ is not a set.

The collection of $S$-local weak equivalences $W_S$, however, won't be a small set in general even if $S$ is. But for [Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) to apply we need to check that the full subcategory of $Arr(C)$ on $W_S$ is, while not small, [[accessible category|category]].

To establish this we need two [properties of accessible categories](http://ncatlab.org/nlab/show/accessible+category#Properties): the inverse image of an accesible subcategory under a functor is accessible, and the collections of fibrations, weak equivalences and acyclic fibrations in a combinatorial model category are accessible.


### The proof itself


+-- {: .standout}

**Beginning of the proof** of the existence of the left Bousfield localization of a left proper combinatorial simplicial model category at a set $S$ of morphisms.

=--


#### Recognition of the combinatorial model structure 

Using [Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem), for establishing the [[combinatorial model category]] structure, it is sufficient to 

* exhibit a [[set]] $I$ of cofibrations of $L_S C$ such that $inj(I) \subset W_{L_S C}$ and such that $cof(I) \cap W_{L_S C}$ is closed under [[pushout]] and [[transfinite composition]].

* check that the weak equivalences form an accessibly embedded accessible subcategory.

For the first item choose $I := I_C$ with $I_C$ any set of generating cofibrations of $C$, that exists by assumption on $C$. 
Then $inj(I) = inj(I_C) = fib_C \cap W_C \subset W_C \subset W_{L_S C}$.

It remains to demonstrate closure of $cof(I) \cap W_{L_S C} = cof_C \cap W_{L_S C}$ under pushout and transfinite composition.

One elegant way to see this, following [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf), is to notice that the relevant ordinary [[colimit]]s all happen to be [[homotopy colimit]]s:

* all [[pushout]]s along cofibrations in a left [[proper model category]] are homotopy pushouts (details are [here](http://ncatlab.org/nlab/show/proper+model+category#homotopy_colimits_in_proper_model_categories_9));

* all [[transfinite composition]] colimits in a [[combinatorial model category]] are homotopy colimits (details are [here](http://ncatlab.org/nlab/show/combinatorial+model+category#properties_17))

And by their definition in terms of the [[derived hom space]] functor, $S$-local weak equivalences in $C$ are preserved under [[homotopy limit|homotopy colimit]]s: 

for $K \stackrel{}{\to}L$ an $S$-local morphism -- a morphism in $W_{L_S C}$ -- and for

$$
  \array{
    K &\stackrel{\simeq_S}{\to}& L
    \\
    \downarrow && \downarrow
    \\
    K' &\to& L'
  }
$$

a [[homotopy limit|homotopy pushout]] diagram, we have (by the universal property of homotopy limits) for every object $Z$ -- in particular for every every $S$-[[local object]] $Z$ -- a [[homotopy limit|homotopy pullback]]

$$
  \array{
    \mathbf{R}Hom(L',Z) &\to&
    \mathbf{R}Hom(K',Z)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{R}Hom(L,Z) &\stackrel{\simeq}{\to}&
    \mathbf{R}Hom(K,Z)
  }
  \,,
$$

of $\infty$-groupoids. where the bottom morphism is a weak equivalence by assumption of $S$-locality of $Z$ and $(K \to L)$. But then also the top horizontal morphism is a weak equivalence for all $S$-local $Z$ and therefore $K' \to L'$ is in $W_{L_S C}$.

Similarly for [[transfinite composition]] colimits.

Therefore, indeed, $cof(I) \cap W_{L_S C}$ is closed under pushouts and transfinite composition.


#### Fibrants in $L_S C$ are the $S$-local fibrants in $C$ 

To see that the fibrant objects in $L_S C$ are precisely the $S$-local fibrant objects of $C$, use the _characterization of $S$-local cofibrations_  as precisely those cofibrations $i : A \hookrightarrow B$ such that for every _fibrant_ and $S$-local object $X$ the [[derived hom space]] functor $\mathbf{R}Hom(X,A) \to \mathbf{R}Hom(X,B)$ is an acyclic [[Kan fibration]] (this is described in detail [here](http://ncatlab.org/nlab/show/local+object#properties_12)).

To apply this fact, we modify, if necessary, the set $S$ in a convenient way without changing the class $W_S$ of $S$-[[local object|local weak equivalence]]s that it defines. 

By the lemma " _localization at cofibrations is sufficient_ " discussed  below, it follows that we may assume that $S$ contains only cofibrations while still generating the same class $W_S$ of $S$-local weak equivalences. So assume now that $S$ contains only cofibrations.

We may moreover add to $S$ any set of $S$-[[local object|local weak equivalence]]s without changing the collection of $S$-[[local object]]s and hence without changing the collection of $S$-local weak equivalences themselves. In this manner, assume now that $S$ has been enlarged such as to contain the following sets of cofibrations:

* $S$ contains all generating acyclic cofibrations of $C$, i.e. $J \subset S$;


* $S$ contains for every original morphism $f : A \to B$ in $S$ and for every $n \in \mathbb{N}$ also the canonical morphism $\tilde f : (Q_f := A \cdot \Delta^n \coprod_{A \cdot \partial \Delta^n} B \cdot \partial \Delta^n) \to B \cdot \Delta^n$, where $A \cdot \Delta^n$ etc. denotes the [[copower|tensoring]] of $C$ over [[SSet]].

We discuss why these morphisms of the latter type are indeed $S$-local cofibrations: 

to see that $\tilde f$ is indeed a cofibration notice that for every commuting diagram

$$
  \array{
    Q &\to& X
    \\
    \downarrow && \downarrow^{\in \mathrlap{fib_C \cap W_C}}
    \\
    B \cdot \Delta^n
    &\to&
    Y
  }
$$

we get, as components of the top morphism two commuting diagrams

$$
  \array{
    A  &\to& X^{\Delta^n}
    \\
    \downarrow^{\mathrlap{\in cof_C}} 
    && \downarrow^{\in \mathrlap{fib_C \cap W_C}}
    \\
    B 
    &\to&
    Y^{\Delta^n}
  }
  \;\;\;\;
  \;\;\;\;
  \;\;\;\;
  \array{
    \partial \Delta^n &\to& [B,X]
    \\
    \downarrow^{\mathrlap{\in cof_{Sset}}} 
    && \downarrow^{\in \mathrlap{fib_{SSet} \cap W_{SSet}}}
    \\
    \Delta^n
    &\to&
    [B,Y]
  }
$$

where we made use of the [[power]]ing and [[copower]]ing of the [[simplicially enriched category]] $C$ and of the [[Quillen bifunctor]] property of the [[copower]]ing which ensures that the fibrations and cofibrations are still as indicated. Therefore we have lifts in both these  diagrams and any pair of them combines as components of a lift of the first diagram. So $\tilde f$ is indeed a cofibration.

Being a cofibration, by the characterization of $S$-local cofibrations, we can check $S$-locality by homming into fibrant $S$-local objects and checking if that produces an acyclic Kan fibration.

So let $X$ be a fibrant and $S$-local object of $C$. Homming the defining [[pushout]] diagram for $Q_f$ into $X$ produces the [[pullback]] diagram

$$
  \array{
    [\partial \Delta^n,[A,X]]
    &\stackrel{\in W}{\leftarrow}&
    [\partial \Delta^n, [B,X]]
    \\
    \uparrow^{\mathrlap{\in fib}} && 
    \uparrow
    \\
    [\Delta^n,[A,X]]
    &\stackrel{\in W}{\leftarrow}&
    [A \cdot \Delta^n \coprod_{A \cdot \partial \Delta^n} B \cdot \partial \Delta^n, X]
    \\
    &{}_{\in W}\nwarrow&& \nwarrow
    \\
    &&&& [\Delta^n,[B,X]]
  }
$$ 

in [[SSet]]. Here the top and the lowest morphisms are weak equivalences by the fact that $[B,X] \to [A,X]$ is an acyclic Kan fibration by the characterization of $S$-[[local object|local cofibrations]] and the fact that [[SSet]] is an [[SSet]]-[[enriched model category]]. Similarly for the fibration on the left, which implies by right [[proper model category|properness]] of [[SSet]] that the bottom horizontal morphism is a weak equivalence, which finally implies by [[category with weak equivalences|2-out-of-3]] that the morphism in question is a weak equivalence.

This shows that we can assume $S$ to consist of only cofibrations and to contain the generating acyclic cofibrations and the morphism called $\tilde f$.

We say that given a set of morphisms $S$ and an object $X$ that $X$ has the _extension property_ with respect to $S$ if every diagram

$$
  \array{
    A &\to& X
    \\
    \downarrow^{\mathrlap{\in S}} && \downarrow
    \\
    B &\to& {*}
  }
$$

has a lift.

We claim now that the the objects of $C$ that have the extension property with respect to our set $S$ are precisely the fibrant and $S$-[[local object]]s.

In one direction, if $X$ that has the extension property with respect to $S$ it has it in particular with respect to $J \subset S$ and hence is fibrant. And it in particular has it with respect to 
$\tilde f : A \cdot \Delta^n \coprod_{A \cdot \partial \Delta^n} B \cdot \partial \Delta^n$, which means that $[B,X] \to [A,X]$ is an acyclic [[Kan fibration]]. 

Conversely, if $X$ is fibrant and $S$-local, then for all $A \to B$ in $S$ the map $[B,X] \to [A,X]$ in $SSet$ is an acyclic [[Kan fibration]] hence in particular its underlying map of sets $Hom_C(B,X) \to Hom_C(A,X)$ is a surjection, so $X$ has the extension property.

A fibrant object of $L_S W$ has the extension property with respect to $cof_C \cap W_S$, hence in particular with respect to $S$ hence is $S$-local and fibrant in $C$.

Now every fibrant object $X$ in $L_S W$ has the extension property with respect to $cof_C \cap W_S$ hence in particular with respect to $S \subset cof_c \cap W_S$, so is $S$-local and fibrant in $C$.

Conversely, if it is $S$-local and fibrant in $C$; then, as mentioned before, for all $f \in cof_C \cap W_S$ the map $[f,X]$ is an acyclic Kan fibration in [[SSet]] so that in particular $Hom_C(f,X)$ is a surjection, which means that $X$ has the extension property with respect to all $f$ and is hence fibrant in $L_S C$.


#### Fibrant replacement in $L_S W$: localization of objects 

Since by assumption $S$ is a small set, we may apply the [[small object argument]] also to $S$. If we apply it to factor all morphisms $X \to {*}$ to the [[terminal object]] we obtain a functorial factorization componentwise of the form

$$
  X \stackrel{\eta_X \in cell(S)\subset W_S}{\to} 
  T X \stackrel{inj(S)}{\to} {*}
  \,.
$$

We had remarked already in the previous argument that objects with the extension property relative to $S$, i.e. objects whose morphism to the terminal object is in $inj(S)$, are fibrant as well as $S$-[[local object|local]] in $C$.

Therefore $T$ is in particular a **fibrant approximation functor** in $L_S W$ and $\eta_S$ is the weak equivalence

$$
  \eta_S : X \stackrel{\simeq_{W_S}}{\to} T X
$$

in $L_S C$ relating an object to its fibrant approximation.




#### Accessibility of the $S$-local weak equivalences

For the [Smith recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem) to apply we still have to check that the $S$-[[local object|local weak equivalences]] $W_S$ span an [[accessible category|accessible full subcategory]] $Arr_S(C) \subset Arr(S)$ of the [[arrow category]] of $C$.

By the general [properties of accessible categories](http://ncatlab.org/nlab/show/accessible+category#Properties) for that it is sufficient to exhibit $Arr_S(C)$ as the inverse image of under functor $T : Arr_S(C) \hookrightarrow Arr(C)$ of the accessible category $Arr_W(C)$ spanned by ordinary weak equivalences in $C$.

That functor we take to be the $S$-local fibrant replacement functor from above

$$
  T : (X \to Y) \mapsto (T X \stackrel{T f}{\to} T Y)
  \,.
$$

Generally, an $S$-local weak equivalence between $S$-[[local object]]s is already an ordinary weak equivalence: by $S$-locality the [[derived hom space]] functor
$\mathbf{R}Hom(f,-)$ takes values in weak equivalences on the full subcategory of $S$-[[local object]]s, hence takes values in [[isomorphism]]s when sent forward to the full subcategory on $S$-local objects of the [[homotopy category]] $Ho_C$. By the [[Yoneda lemma]] this implies that $T f$ is an isomorphism in $Ho_C$, hence a weak equivalence in $C$.

But this means that the inverse image under $T$ of the weak equivalences in $C$ are all $S$-local weak equivalences

$$
  T^{-1}(Arr_{W_C}(C) = Arr_S(C)
  \,.
$$

Therefore this is an [[accessible category]].

+-- {: .standout}

**End of the proof** of the existence of the left Bousfield localization of a left proper combinatorial simplicial model category at a set $S$ of morphisms.

=--



## Existence for tractable ennriched model categories

The above statement is generalized to the context of [[enriched model category]] theory by the following result:

+-- {: .un_theorem }
###### Theorem (existence of enriched Bousfield localization)

Let 

* $V$ be a [[tractable model category|tractable]] [[symmetric monoidal category|symmetric]] [[monoidal model category]];

* $C$ a [[tractable model category|tractable]] [[proper model category|left proper]] $V$-[[enriched model category]]

* $S \subset Mor(C)$ a small set

(all with respect to a fixed [[Grothendieck universe]]).

Then the left enriched Bousfield localization $L_{S/V} C$ does exist and is [[proper model category|left proper]] and [[tractable model category|tractable]].

=--

+-- {: .proof}
###### Proof

This is theorem 4.46 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf))

=--



## Properties of Bousfield localization

+-- {: .un_prop }
###### Proposition (Bousfield localization is indeed a localization)

If the left Bousfield localization exists, i.e. of $L_S C$ is indeed a [[model category]] with the above definitions of cofibrations and weak equivalences, then it is indeed a [[localization of a model category]] in that there is a _left Quillen functor_

$$
  j : C \to L_S C
$$

(i.e. $j$ preserves cofibrations and trivial cofibrations and has a [[right adjoint]])

such that the total left [[derived functor]]

$$
  L j : Ho C \to Ho L_S C
$$

takes the images of $S \subset Mor(C)$ in $Ho(C)$ to [[isomorphism]]s

and every other left Quillen functor with this property factors by a unique left Quillen functor through $j$.

Moreover, the identity functor $Id_C$ on the underlying category is a [[Quillen adjunction]]

$$
  Id_C : L_S C \stackrel{\leftarrow }{\to} C : Id_C
$$

(and its itself a localization functor).

=--

+-- {: .proof}
###### Proof

The first part is theorem 3.3.19 in _ModLoc_ . The second part is prop 3.3.4, which follows directly from the following proposition.

=--

+-- {: .un_lemmaa }
###### Lemma (localization at cofibrations is sufficient)

Every combinatorial localization $B = L_{R} A$ of $A$ is already of the form $L_{S}A $ for $S$ a set of just cofibrations.

=--

+-- {: .proof}
###### Proof

See [[Higher Topos Theory|HTT, prop. A.3.7.4]]

We demonstrate that $S := J_B$ does the trick.


...

=--




The following further statements about fibrantions, cofibrations and weak equivalences in a Bousfield localization hold.

+-- {: .un_prop }
###### Proposition

Let $L_S C$ be a left Bousfield localization of $C$ then

* every weak equivalence of $C$ is also a weak equivalence of $L_S C$;

* every acyclic cofibration of $C$ is also an acyclic cofibration of $L_S C$

* the acyclic fibrations of $L_S C$ are precisely the acyclic fibrations of $C$;

* every fibration of $L_S C$ is also a fibration of $C$;.


=--


+-- {: .proof}
###### Proof

This is prop 3.3.3 in _ModLoc_ .

=--


When $C$ is a left [[proper model category]] then Bousfield localization at $S$ indeed produces a model for the subcategory of $S$-[[local object]]s in $C$:

+-- {: .un_prop }
###### Proposition (Bousfield localization as model for $S$-local obects)

Let $C$ be a left [[proper model category]] and $S$ a set of morphisms. Then the Bousfield localization $L_S C$, which exists by the above theorem, then

* the fibrant objects in $L_S C$ are precisely the fibrant $S$-[[local object]]s in $C$.

* $L_S C$ is left [[proper model category|proper]] itself;

If moreover $C$ is a [[combinatorial simplicial model category]], then $L_S C$

* inherits the structure of a [[combinatorial simplicial model category]].



=--


+-- {: .proof}
###### Proof

The first part is prop 3.4.1 and prop 3.4.4 in _ModLoc_ . The second part is item (4) of theorem 4.1.1 there.
Also prop. A.3.7.3 in [[Higher Topos Theory|HTT]].

=--


## Relation to locally presentable $(\infty,1)$-categories {#LocPresInf}

As described at [[presentable (∞,1)-category]], an [[(∞,1)-category]] $\mathbf{C}$ is presentable precisely if, as an [[simplicially enriched category]], it arises as the full subcategory of fibrant-cofibrant objects of a [[combinatorial simplicial model category]].

The _proof_ of this proceeds via Bousfield localization, and effectively exhibits Bousfield localization as the procedure that models [[localization of an (∞,1)-category]] when $(\infty,1)$-categories are modeled by model categories.

For notice that 

1. a presentable $(\infty,1)$-category $\mathbf{C}$ is one arising as the [[localization of an (∞,1)-category|localization]] 

   $$
     \mathbf{C} \simeq S^{-1} Funct(K,\infty Grpd) = S^{-1}PSh_{(\infty,1)}(K)
   $$

   of an [[(∞,1)-category of (∞,1)-presheaves]]

1. every [[(∞,1)-category of (∞,1)-presheaves]]  arises    
   $PSh_{(\infty,1)}(K)  \simeq ([K,SSet]_{inj})^\circ$ as
   the subcategory of fibrant-cofibrant objects of the 
   globale [[model structure on simplicial presheaves]];

1. in terms of the [[simplicial model category]] 
   $[K,SSet]_{inj}$ the prescription for 
   [[localization of an (∞,1)-category|localization as an (∞,1)-category]] and passing to the subcategory of fibrant-cofibrant objects of the Bousfield localization $L_S [K,SSet]_{inj}$ is literally the same: in both cases one passes to the full subcategory on the $S$-[[local object]]s.

Moreover, by [Dugger's theorem on combinatorial model categories](http://ncatlab.org/nlab/show/combinatorial+model+category#duggers_theorem_13) every [[combinatorial simplicial model category]] arises this way.

This is the argument of [[Higher Topos Theory|HTT, prop A.3.7.6]]. 

This gives a good conceptual interpretation of Bousfield localization, since the [[localization of an (∞,1)-category]] is nothing but an adjunction

$$
  \mathbf{C} \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  \mathbf{D}
$$

that exhibits $\mathbf{C}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{D}$.

So we find the diagram

+-- {: .standout}

**Localization of $(\infty,1)$-presheaf categories**

$$
  \array{
      Sh_{(\infty,1)}(K) 
     &\stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
     &
     PSh_{(\infty,1)}(K) 
     &&&
     abstract\;nonsense\;def
     \\
     \uparrow^{\simeq}
     &&
     \uparrow^{\simeq}
     &&& Lurie's theorem
     \\
     ([K^{op},SSet]_{inj}^{loc})^\circ
     &\stackrel{\stackrel{Bousfield\;loc.}{\leftarrow}}
     {\to}&
     ([K^{op},SSet]_{inj})^\circ
     &&&
     concrete\;realization
  }
  \,.
$$

=--


Here $(-)^\circ$ denotes passing to the full [[simplicially enriched category|simplicially enriched]] [[subcategory]] on the fibrant-cofibrant objects, regarding that as an [[(∞,1)-category]]. (If one wants to regard that as a [[quasi-category]], then $(-)^\circ$ also involves taking the [[homotopy coherent nerve]] of this simplicially enriched category.)



## Examples and Applications 

### Categories to which the general existence theorem applies 

The following [[model category|model categories]] $C$ are left [[proper model category|proper]] [[cellular model category|cellular]]/[[combinatorial model category|combinatorial]], so that the above theorem applies and for every [[set]] $S \subset Mor(C)$ the Bousfield localizaton $L_S C$ does exist.

* [[Top]] with its standard [[model structure on topological spaces]];

* [[SSet]] with its standard [[model structure on simplicial sets]];

* the category of [[symmetric monoidal smash product of spectra|symmetric spectra]] in a pointed left-proper cellular model category

* and so on...

If $C$ is a left [[proper model category|proper]] ([[simplicial model category|simplicial]]) [[cellular model category]], then so is

* the [[functor category]] $[D,C]$ for any ([[simplicially enriched category|simplicial]]) [[small category]]  $D$ (using the [[global model structure on functors]]);

* the [[over category]] $C/s$ for any object $x \in C$ . 

 


### Local model structure on presheaves 

Left Bousfield localization produces the _local_ [[model structure on homotopical presheaves]]. For instance the [[local model structure on simplicial presheaves]].


## References 

Bousfield localization appears as definition 3.3.1 in

* **ModLoc** Hirschhorn, _Model categories and their localization_ 

for left proper [[cellular model category|cellular model categories]].

In  proposition A.3.7.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]] .

it is discussed in the context of [[combinatorial model category|combinatorial model categories]] and of [[combinatorial simplicial model category|combinatorial simplicial model categories]] in particular.

The relation to [[localization of an (infinity,1)-category]] is also in [[Higher Topos Theory|HTT]], for the time being see the discussion at [[models for ∞-stack (∞,1)-toposes]] for more on that.

A detailed discussion of Bousfield localization in the general context of [[enriched model category]] theory is in

* [[Clark Barwick]], _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

  * Expanded version: _On left and right model categories and left and right Bousfield localization_ ([pdf](http://www.math.harvard.edu/~clarkbar/complete.pdf))

in terms of [[enriched model category|enriched]] [[tractable model category|tractable model categories]].




## Discussion 

+-- {: .query}

  _Rafael Borowiecki_: How do this relate to Bousfield localization for spectra?

  _Rafael_: Could it be the Bousfield localization of a model category of spectra?

  [[Urs Schreiber]]: could you give me a concrete reference that spells out what you are thinking of when saying "Bousfield localization of spectra"? Then I can try to look at it and see if I can answer your question. I would guess, that, yes, it must refer to the Bousfield localization of a model category o spectra.

  _Rafael_: Here the Bousfield localization is with respect to a class of morphisms S. I found a case where the Bousfield localization is with respect to a spectrum of a generalized (co)homology theory instead. I think this is what i found before:

  [Elliptic cohomology: geometry, applications, and higher chromatic analogues](http://books.google.se/books?id=ofnD0loTwC0C&pg=PA255&lpg=PA255&dq=%22Bousfield+Localization%22+invented&source=bl&ots=0pPUhszwlL&sig=uxZ9U5N1BY1zB7dOBAc5eYB_e20&hl=sv&ei=ztmASvP8O4Wy-AaCkKCzCg&sa=X&oi=book_result&ct=result&resnum=1#v=onepage&q=%22Bousfield%20Localization%22%20invented&f=false)

  [On K(1)-local SU-bordism](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf)

  [Goodwillie towers and chromatic homotopy page8](http://arxiv.org/PS_cache/math/pdf/0410/0410342v2.pdf)

  Again there are different answers for what something is.
  I will stop complaining now. Good luck Urs.

[[Urs Schreiber]]: okay, thanks. So I looked at [def 10, page 10](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf#page=10) of   [On K(1)-local SU-bordism](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf)

This, yes, is a special case of what is decribed here. But just notice the two shades of the use of the word localization here:

let me recall: given a model category $C$ we may choose a set of morphisms $S = \{f : X \to Y\}$ and then say that an object $Z$ is an $S$-[[local object]] if homming $f$ into $Z$ produces isomorphisms.

Then:

* the Bousfield localization of the entire category $C$ is (if it exists) a new model category structure on $C$ where the weak equivalences now are the $S$-[[local equivalence]]

* in as far as the Bousfield localization is a model for a [[localization of an (infinity,1)-category]] every object $Z$ will be weakly equivalent to an $S$-local one $Z_E$, in that there is a morphism $Z \to Z_E$ which is a weak equivalence. Since $Z_E$ is $S$-local in the sense of the definition just recalled, this may be thought of as being the "localization" of the object $Z$.

So what they call localization there is what happens to the _objects_ as we apply Bousfield localization to the category that they live in, essentially. That the objects in their model category happen to be spectra is not important for this general kind of statement. They could be anything.

It may help to think of this in the example where $C$ is a category of [[simplicial presheaf|simplicial presheaves]] and the Bousfield localization is at those weak equivalences that induce the local [[model structure on simplicial presheaves]]. Then the Bousfield localization

$$
  SimpPSh_{glob} \to SimpPSh_{loc}
$$

is [[infinity-stackification]]. In this case the "localization morphism on objects" $Z \to Z_E$ the morphism that make a pre-stack $Z$ weakly equivalent to ist $\infty$-stackification $Z_E$. So here localization=stackification and in terms of that the general kind of situation here may be more familiar.

_Rafael_: Ok, i have thought about it with interest. Good answer. Thx for explaining.
=--


[[!redirects bousfield localization]]
[[!redirects Bousfield localisation]]