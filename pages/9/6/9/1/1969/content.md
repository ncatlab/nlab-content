
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

There are several ways to _model_ an [[(∞,1)-category]] $\mathbf{C}$ by an ordinary [[category]] $C$ equipped with some extra structure: for instance $C$ may be a [[category with weak equivalences]] or a [[model category]]. In all of these models, given two objects $X, Y \in C$, there is a way to construct an [[∞-groupoid]] $\mathbf{C}(X,Y)$ that is the correct [[hom-object]] of the [[(∞,1)-category]] $\mathbf{C}$ -- this is the _$(\infty,1)$-categorical hom-space_  modeled by $C$, often called the _derived hom space_  and then denoted $\mathbf{R}Hom(X,Y)$.

There are various equivalent explicit expressions for $\mathbf{R}Hom$. These are described and compared in the following.

+-- {: .query}
I don\'t like this term, (for reasons other than using the word 'categorical' ^_^).  Is there any hom-space that is *not* $(\infty,1)$-categorial?  It seems to me that if your hom-objects are spaces, then you\'re an $(\infty,1)$-category; and if you\'re an $(\infty,1)$-category, then your hom-objects could be any spaces.  So how about [[hom-space]]?  ---Toby

[[Urs Schreiber]]: I see your point. On the other hand probably few readers will expect behind a title "hom-space" more than a remark about the definition of a Top-enriched category. Here the point is the construction of these from 1-categorical data.

How can we say this better?

_Toby_:  Well, I also thought of 'hom-$\infty$-groupoid' and 'hom-simplicial set' (at which point the hyphen in 'hom-object' looks worse and worse), but these struck me as too specific, although they match what you\'re saying here.

[[Urs Schreiber]]: Choices like "hom-simplicial set" or similar still isn't good enough for what this entry is about, though: for instance in a simplicially enriched model category all hom-objects are of course "hom-simplicial sets", but the right "$(\infty,1)$-categori(c)al hom space" between two objects is the hom-simplicial set between a fibrant-cofibrant replacement of these two objects.

Other people would say "derived hom space". I reworded the above introduction and mention that term now.  

_Toby_:  I could go for [[derived hom-space]] (with or without hyphen, although we\'ve been using hyphens here for some reason).  That clarifies that it\'s not the na&#239;ve hom-space but doesn\'t imply that it\'s the $\infty$-categorification of a $1$-categorial hom-space.

_Urs_: At least "derived hom-space" has the advantage that it follows wide-spread practice. However, to me this wide-spread practice looks like a bad practice: the term "derived" is used widely but inconsistently and unsystematically. And it carries with it the historical baggage of its origin as a procedure whose conceptual meaning wasn't understood. "Derived" essentially just indicates: "there is some procedure that gives us this construction from given data", never mind if we know what the procedure actually means. Today we know what it actually means: it is all about constructing $(\infty,1)$-categories. I feel on the $n$Lab we should play Bourbaki and implement good terminology from the point of view of higher category theory.

=--


## Interrelation between the different constructions ##

For $(C,W \subset Mor(C))$ a [[category with weak equivalences]], Dwyer-Kan [[simplicial localization]] produces an [[SSet]]-[[enriched category]] as follows

For $X,Y \in Obj(C)$ and for $n \in \mathbb{N}$ define a category $w Mor_C^n(X,Y)$ 

* whose objects are zig-zags of morphisms in $C$ of length $n$

  $$
    X = X_0 \leftarrow X_1 \to X_2 \leftarrow \cdots \to X_{n-1} \leftarrow X_n = Y
  $$

  such that each morphism going to the left, $X_{2k}\leftarrow X_{2k +1}$, is a [[weak equivalence]], an element in $W$.

* morphisms between such objects $(X,X_i,Y) \to (X',X'_i,Y')$ are collections of weak equivalences $(X_i \to X'_i)$ for all $0 \lt i \lt n $ such that all triangles and squares commute.

Write $N(wMor_C^n(X,Y))$ for the [[nerve]] of this category, a [[simplicial set]].

Then the [[simplicial localization|hammock localization]] $L^H C$ of $C$ is the [[simplicially enriched category]] with objects those of $C$ and [[hom-object]]s given by the [[colimit]] over the length of these hammock hom-categories

$$
  L^H C(X,Y) = colim_n N(wMor_C^n(X,Y))
  \,.
$$

The [[Kan fibrant replacement]] of this simplicial set is the hom-space between $X$ and $Y$ of the $(\infty,1)$-category modeled by $(C,W)$.

If the structure of a category with weak equivalences is enhanced to that of a [[model category]], then there are several other ways to construct hom-simplicial sets. The following diagram shows how all these different ways are related and equivalent to the Dwyer-Kan cnstruction $L^H C(X,Y)$ -- while being usually way more tractable.

Suppose now that $Q : C \to C$ is a [[cofibrant replacement functor]] and $R : C \to C$ a [[fibrant replacement functor]], $\Gamma^\bullet : C \to (cC)_c$ a [[cosimplicial resolution functor]] and $\Lambda_\bullet : C \to (sC)_f$ a [[simplicial resolution functor]] in the [[model category]] $C$.


+-- {: .un_theorem }
###### Theorem (Dwyer--Kan)

There are natural weak equivalences between the following equivalent realizations of this [[SSet]] [[hom-object]]:

$$
  \array{
    Mor_C(\Gamma^\bullet X, R Y)
    &&&&
    Mor_C(Q X, \Lambda_\bullet Y)
    \\
    & \searrow^\simeq && {}^\simeq \swarrow
    \\
    &&
    diag Mor_C(\Gamma^\bullet X, \Lambda_\bullet Y)
    \\
    &&
    \uparrow^\simeq
    \\
    &&
    hocolim_{p,q \in \Delta^{op} \times \Delta^{op}}
    Mor_C(\Gamma^p X, \Lambda_q Y)
    \\
    &&\downarrow^\simeq
    \\
    &&N wMor_C^3(X,Y)
    \\
    &&\downarrow^\simeq
    \\
    &&Mor_{L^H C}(X,Y)
  }
  \,.
$$

=--

## Details ##

### Enriched homs between cofibrant/fibrant objects ###

We describe here in more detail properties of [[hom-object]]s in a [[simplicial model category]] for the case that the domain objects are cofibrant and the codomain objects are fibrant.

The crucial axiom used for this is the axiom of an [[enriched model category]] $C$ which says that 

* the [[copower|tensor operation]]

  $$
    \cdot : C \times SSet \to C
  $$

  is a [[Quillen bifunctor]];

* or equivalently that for $X \to Y$ a cofibration 
  and $A \to B$ a fibration the induced morphism

  $$
    C(Y, A) \to C(X,A) \times_{C(X,B)} C(Y,B)
  $$

  is a fibration, which is acyclic if either 
  $X \to Y$ or $A \to B$ is.

First of all the first statement directly implies that for $\emptyset \in C$ the [[initial object]] and $A \in C$ any object, the simplicial set $C(\emptyset,A) = {*}$ is the terminal simplicial set, because for any simplicial set $S$

$$
  \begin{aligned}
    SSet(S,C(\emptyset, A))
    & =  Hom_C(\emptyset \cdot S, A)
    \\
    & = Hom_C(colim_{\emptyset} \cdot S, A)
    \\
    & = Hom_C(\emptyset, A)
    \\
    &= {*}
  \end{aligned}
  \,,
$$

where we use that the [[copower|tensor]] [[Quillen bifunctor]] is required to respect [[colimit]]s and that the empty colimit is the [[initial object]]. (All equality signs here denote [[isomorphism]]s, to distinguish them from weak equivalences.)

Similarly one has for all $X$ that $C(X,{*}) = {*}$.

Using this, the second equivalent form of the enrichment axiom has as a special case the following statement.

+-- {: .un_lemma }
###### Lemma

In a [[simplicial model category]] $C$, for $X \in C$ cofibrant and $A \in C$ fibrant, the [[simplicial set]] $C(X,A)$ is a [[Kan complex]].

=--

+-- {: .proof}
###### Proof

We apply the [[enriched model category]] axiom to the cofibration $\emptyset \to X$ and the fibration $A \to {*}$ to obtain a fibration

$$
  C(X,A) \to C(\emptyset, A) \times_{C(\emptyset,{*})} C(X,{*})  
  \,.
$$

The right hand is the [[pullback]] of the terminal simplicial set ${*} = \Delta^0$ to itself, hence is itself the point. So we have a fibration $ C(X,A) \to {*}$
and $C(X,A)$ is a fibrant object in the standard [[model structure on simplicial sets]], hence a [[Kan complex]].
.
=--


+-- {: .un_lemma }
###### Lemma

In a [[simplicial model category]] $C$, for $X \in C$ cofibrant and $f : A \to B$ a fibration, the morphism of [[simplicial set]]s $C(X,f) : C(X,A) \to C(X,B)$ is a [[Kan fibration]] that is a [[weak homotopy equivalence]] if $f$ is acyclic.

Dually, for $i : X \to Y$ a cofibration and $A$ fibrant, the morphism $C(i,A) : C(X,A) \to C(Y,A)$ is a cofibration of simplicial sets.

=--

+-- {: .proof}
###### Proof

This is as before. Explicity, consider the first case, the second one is the formal dual of that:

We enter the enrichment axiom with the morphisms $\emptyset \to X$ and $A \to B$ and find for the required [[pullback]] that

$$
  C(\emptyset,A) \times_{C(\emptyset, B)} C(X,B)
  =
  {*} \times_{*} C(X,B)
  =
  C(X,B)
$$

and hence that $C(X,A) \to C(X,B)$ is, indeed, a fibration, which is acyclic if $A \to B$ is.

=--


+-- {: .un_proposition }
###### Proposition

Let $C$ be a [[simplicial model category]]. 

Then for $X$ a cofibant object and 

$$
   f : A \stackrel{\simeq}{\to}  B
$$

a weak equivalence between fibrant objects, the [[enriched functor|enriched]] [[hom-object|hom-functor]]

$$
  C(X,f) : C(X,A) \to C(X,B)
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.

Similarly, for $A$ a fibrant object and $j : X \stackrel{\simeq}{\to} Y$ a weak equivalence between cofibrant objects, the morphism

$$
  C(j,A) : C(X,A) \to C(Y,A)
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.


=--


+-- {: .proof}
###### Proof

The second case is formally dual to the first, so we restrict attention to the first one.

By the above, the axioms of an [[enriched model category]] ensure that the above statement is true when $f$ is in addition a fibration. So we reduce the situation to that case.

This is possible because both $A$ and $B$ are assumed to be fibrant. This allows to apply the _factorization lemma_ that is described in great detail at [[category of fibrant objects]]. By this lemma, for every morphism $f : A \to B$ between fibrant objects there is a commutative diagram

$$
  \array{
    && \mathbf{E}_f B
    \\
    & {}^{\mathllap{\in fib \cap W}}\swarrow && \searrow^{\mathrlap{\in fib}}
    \\
    A &&\stackrel{\simeq}{\to}&& B
  }
$$

Since $f$ is assumed a weak equivalence it follows by [[category with weak equivalences|2-out-of-3]] that $\mathbf{E}_f B$ is also a weak equivalence. 

Therefore by the above properties of simpliciall enriched categories we obtain a [[span]] of acyclic fibrations of [[Kan complex]]es

$$
  C(X,A) \stackrel{\simeq}{\leftarrow}
  C(X, \mathbf{E}_f B)
  \stackrel{\simeq}{\to} 
  C(X,B)
  \,.
$$

By the [[Whitehead theorem]] every weak equivalence of Kan complexes is a [[homotopy equivalence]], hence there is a weak equivalence

$$
  C(X,A) \stackrel{\simeq}{\to} C(X,\mathbf{E}_f B) \stackrel{\simeq}{\to} C(X,B)
$$

that is homotopic to our $C(X,f)$. Therefore this is also a weak equivalence.

=--




## References ##

A useful quick review of the interrelation of the various constructions of derived hom spaces is page 14, 15 of

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

where the above diagram is taken from.

The definition in terms of simplicial and fibrant/cofibrant resolutions is described in detail in sections 16, 17 of

* Hirschhorn, _Model categories and their localization_ .


[[!redirects (∞,1)-categorical hom-space]]
[[!redirects (infinity,1)-categorical hom space]]
[[!redirects (∞,1)-categorical hom space]]
[[!redirects (infinity,1)-categorial hom-space]]
[[!redirects (∞,1)-categorial hom-space]]
[[!redirects (infinity,1)-categorial hom space]]
[[!redirects (∞,1)-categorial hom space]]