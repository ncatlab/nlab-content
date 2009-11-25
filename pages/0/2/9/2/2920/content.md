<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

Bousfield localization is a procedure that to a [[model category]] structure assigns a new one with more weak equivalences.

A _left Bousfield localization_ $C_{loc}$ of a model category $C$ is another model category structure on the same underlying category with the same cofibrations, but more weak equivalences. Similarly for _right Bousfield localization_ and fibrations.

It follows that the identity functor between a model category and its left (right) Bousfield localization preserves weak equivalences and cofibrations (fibrations) and hence yields a [[Quillen adjunction]]

$$
  C_{loc} \stackrel{\leftarrow}{\to} C
  \,.
$$

But a very special one: 

at least when $C$ is a [[combinatorial simplicial model category]] this is a [[localization of a simplicial model category]] and, moreover, under [[presentable (infinity,1)-category|passage to the sub-category of fibrant-cofibrant objects]] this Quillen adjunction becomes the inclusion of a [[reflective (∞,1)-subcategory]

$$
  {C_{loc}}^\circ \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  C^\circ
$$

hence of a [[localization of an (∞,1)-category]].

Such a localization is determined by the collection $S$ of _local weak equivalences_ in $C$, and alternatively by the collection of $S$-[[local object]]s in $C$. Indeed, ${C_{loc}}^\circ$ is the full $(\infty,1)$-subcategory on the cofibrant and fibrant and $S$-local objects of $C$.




## Definition ##

Let $C$ be a category equipped with a [[model category]] structure and let 

$$
  S \subset Mor(C)
$$ 

be a [[class]] of morphisms in $C$. 

An $S$-[[local object]] $X$ is one such that the [[(infinity,1)-categorical hom-space|derived hom-space functor]] $\mathbf{R}Hom(-,X)$ sends morphisms in $S$ to weak equivalences. An $S$-local morphism $f$ is one such that $\mathbf{R}Hom(f,-)$ sends local objects to weak equivalences.

+-- {: .un_def }
###### Definition (Bousfield localization)

The **left Bousfield localization** of $C$ with respect to $S$ is, if it exists, a [[model category]] structure $L_S C$ on $C$ such that

* the class of weak equivalences of $L_S C$ equals the class of $S$-[[local equivalence]]s of $C$;

* the class of cofibrations of $L_S C$ equals that of $C$;

* the fibrations of $L_S C$ are precisely the morphisms with the right lifting property with respect to the $S$-[[local equivalence|local cofibration]]s of $C$.

Analogously the **right Bousfield localization** is defined as above, with the role of fibrations and cofibrations exchanged throughout.

=--

Below it is discussed that this model category structure is, when it exists, indeed a [[localization of a model category]].

The following auxiliary definitions are useful for analyzing Bousfield localizations


+-- {: .un_def }
###### Definition ($S$-localization of an object)

(...)

=--

## Existence of Bousfield localizations ##

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

A proof of this making use of [Jeff Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#jeff_smiths_theorem_5) for [[combinatorial model category|combinatorial model categories]] appears 
as [[Higher Topos Theory|HTT, prop. A.3.7.3]] and 
as theorem 2.11 in [Bar07](http://arxiv.org/abs/0708.2067) and as theorem 4.7 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf). 

We follow [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf) for the proof that the assumptions of Smith's recognition theorem are satisfied and follow [[Higher Topos Theory|HTT, prop. A.3.7.3]] for the characterization of the fibrant objects:

**1) existence of the combinatorial model category structure**

Using [Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#smiths_theorem_6), for establishing the [[combinatorial model category]] structure, it is sufficient to 

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


**2) fibrants in $L_S C$ are the $S$-local fibrants in $C$**

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

**3) accessibility of the $S$-local weak equivalences**

(...)

=--

> In _ModLoc_ this is stated for left proper [[cellular model category|cellular model categories]]. Need to say something about the relation...



This statement is generalized to the context of [[enriched model category]] theory by the following result:

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



## Properties of Bousfield localization ##

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


## Relation to presentable $(\infty,1)$-categories ##

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
   [[localization of an (∞,1)-category|localization as an (∞,1)-category]] and passing to the subcategory of fibrant-cofibrant objects of the Bousfield localization $L_S [K,SSet]_{inj}$ is literally the same.

Moreover, by [Dugger's theorem on combinatorial model categories](http://ncatlab.org/nlab/show/combinatorial+model+category#duggers_theorem_13) every [[combinatorial simplicial model category]] arises this way.

This is the argument of [[Higher Topos Theory|HTT, prop A.3.7.6]]. 

This gives a good conceptual interpretation of Bousfield localization, since the [[localization of an (∞,1)-category]] is nothing but an adjunction

$$
  \mathbf{C} \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  \mathbf{D}
$$

that exhibits $\mathbf{C}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{D}$.

So we find the diagram

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
     \\
     ([K,SSet]_{inj}^{loc})^\circ
     &\stackrel{\stackrel{Bousfield\;loc.}{\leftarrow}}
     {\to}&
     ([K,SSet]_{inj})^\circ
     &&&
     concrete\;realization
  }
  \,.
$$

(Here $(-)^\circ$ denotes passing to the full subcategory of fibrant-cofibrant objects.)

## Examples and Applications ##

### Categories to which the general existence theorem applies ###

The following [[model category|model categories]] $C$ are left [[proper model category|proper]] [[cellular model category|cellular]]/[[combinatorial model category|combinatorial]], so that the aobe theorem applies and for every [[set]] $S \subset Mor(C)$ the Bousfield localizaton $L_S C$ does exist.

* [[Top]] with its standard [[model structure on topological spaces]];

* [[SSet]] with its standard [[model structure on simplicial sets]];

* the category of [[symmetric monoidal smash product of spectra|symmetric spectra]] in a pointed left-proper cellular model category

* and so on...

If $C$ is a left [[proper model category|proper]] ([[simplicial model category|simplicial]]) [[cellular model category]], then so is

* the [[functor category]] $[D,C]$ for any ([[simplicially enriched category|simplicial]]) [[small category]]  $D$ (using the [[global model structure on functors]]);

* the [[over category]] $C/s$ for any object $x \in C$ . 

 


### Local model structure on presheaves ###

Left Bousfield localization produces the _local_ [[model structure on homotopical presheaves]]. For instance the [[local model structure on simplicial presheaves]].


## References ##

Bousfield localization appears as definition 3.3.1 in

* **ModLoc** Hirschhorn, _Model categories and their localization_ 

and as proposition A.3.7.3 in

* [[Jacob Lurie]], [[Higher Topos Theory]] .

The relation to [[localization of an (infinity,1)-category]] is also in [[Higher Topos Theory|HTT]], for the time being see the discussion at [[models for ∞-stack (∞,1)-toposes]] for more on that.

A detailed discussion of Bousfield localization also in the context of [[enriched model category|enriched model categories]] is in

* [[Clark Barwick]], _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

Apparently an expanded version of this is

* [[Clark Barwick]], _On left and right model categories and left and right Bousfield localization_ ([pdf](http://www.math.harvard.edu/~clarkbar/complete.pdf))


## Discussion ##

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