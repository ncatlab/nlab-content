
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[type theory]] the kind of [[type]] corresponding in [[categorical semantics]] to a [[quotient object]] / [[coequalizer]].


## Properties

### From higher inductive types

Quotient type may be constructed as [[higher inductive types]]. See [here](higher+inductive+type#QuotientsOfSets).

#### History and effectiveness

This notion of quotient type predates the general notion of higher inductive type, however; it appears already in [Martin Hofmann's thesis](#HofmannThesis).

Hofmann works in a theory that includes a [[type of propositions]] $Prop$ that may be assumed to satisfy [[proof irrelevance]] --- for instance, it might be the universe of [[h-propositions]] --- and considers the *effectiveness* of quotient types only for quotients of Prop-valued [[equivalence relations]].  This corresponds to the correct categorical notion of effectiveness (see [[Barr-exact category]]) and (as Hofmann noted) is provable in the presence of [[propositional extensionality]] (which in turn follows from the [[univalence axiom]]).

However, before the introduction of homotopy type theory and the realization of the importance of homotopy levels such as [[h-propositions]], some authors considered also quotients of arbitrary $Type$-valued "equivalence relations" (i.e. [[setoids]]).  [Maietti](#Maietti99) shows, by adapting [Diaconescu's argument](/nlab/show/excluded+middle#RelationToTheAxiomOfChoice), that "effectiveness" for quotients of this sort of "equivalence relation" implies the law of [[excluded middle]].


### From univalence
 {#FromUnivalence}

Quotient types are implied by adding [[univalence]] to [[Martin-Löf type theory]]. We indicate how this works:

A sufficient set of hypothesis that imply the existence of quotient types is this:

* ambient [[dependent product types]] [[dependent sum types]] and [[identity types]];
* availability of [[propositional truncation]];
* existence of a univalent family $U$;
* every [[h-prop]] is equivalent to some type in $U$.

In terms of [[categorical semantics]] in [[fibration categories]], this comes about as follows:

In [[fibration categories]] where every map is a fibration, "hprop" means
"[[subobject]]", propositional truncation becomes a stable [[image]]
factorisation, and from a univalent universe $U$ containing all hprops,
we can construct a [[subobject classifier]] as 

$$
  \underset{x \colon U}{\sum} isProp(x)
  \,.
$$

(For the subobject classification axioms: existence comes from "every
hprop is equivalent to some type in $U$", and uniqueness comes from
univalence of $U$.)  

So in this setting, the HoTT argument just becomes the usual construction (due to [Par&#233; 74](#Pare), see for instance [MacLane-Moerdijk 92, IV.5](#MacLaneMoerdijk92)) of exact quotients from a [[subobject classifier]] in a [[regular category|regular]] [[locally cartesian closed category]]. For more on this see at _[quotient object -- in toposes](quotient+object#InToposes)_.

One thing to be careful about, in the [[fibration category]] setting, is
that "equivalences" as defined in type theory correspond not generally
to the original equivalences, but to the right homotopy equivalences,
which of course may be different.  This is why e.g. Mike Shulman's def
of "type-theoretic fibration category" doesn't include a class of
equivalences as separate data, but takes them to be the right homot
equivs.  So for the type-theoretic arguments to apply, "univalent
fibration" should be defined using right homot equivs.

## Related concepts

* [[setoid]]/[[Bishop set]]

* [[quotient]]

* [[quotient space]]

* [[quotient stack]]

## References

On the convoluted history of the notion of quotient types, from [[setoids]]/[[Bishop sets]] to [[higher inductive types]] and in [[univalent foundations of mathematics]]:

* Nuo Li, *Quotient Types in Type Theory*, Nottingham (2014) &lbrack;[pdf](https://eprints.nottingham.ac.uk/28941/1/Nuo%20Li%27s_Thesis.pdf), [oai:eprints.nottingham.ac.uk:28941](https://core.ac.uk/display/33573841), [[Li-QuotientTypes.pdf:file]]&rbrack;

* {#Murray22} [[Zachary Murray]], §4.3.2 in: *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;



### As a higher inductive type

As [[higher inductive types]]:

* {#HofmannThesis} [[Martin Hofmann]], p. 111 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;


* {#Maietti99} [[Maria Emilia Maietti]], *About effective quotients in constructive type theory*, in "Types for proofs and programs" (1999)

* [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Gabe Dijkstra]], [[Nicolai Kraus]], [[Fredrik Forsberg]], *Quotient inductive-inductive types*, Foundations of Software Science and Computation Structures (FoSSaCS 2018), Lecture Notes in Computer Science **10803** (2018) &lbrack;[doi:10.1007/978-3-319-89366-2_16](https://doi.org/10.1007/978-3-319-89366-2_16), [arXiv:1612.02346](https://arxiv.org/abs/1612.02346)&rbrack;

### From univalence
 {#FromUnivalenceReferences}

The argument that adding [[univalence]] (plus universe resizing) to [[Martin-Löf type theory]] implies the existence of quotient types is attributed to Voevodsky in places like here: [pdf, slides 41 & 61](http://benediktahrens.net/talks/IRIT_slides.pdf).
  
Voevodsky's own account of this seems to be entirely in his Coq-code repository here:

* [[Vladimir Voevodsky]], _Equivalence classes with respect to a given relation_,
[here](https://github.com/vladimirias/Foundations/blob/df19211f602ab71ee44f0ae4de2a19170c5b9e4d/hlevel2/hSet.v#L466), _Set quotients of types_, 
[here](https://github.com/vladimirias/Foundations/blob/df19211f602ab71ee44f0ae4de2a19170c5b9e4d/hlevel2/hSet.v#L555)

A more readable version of this is in section 6.10 of 

* _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Def. 6.10.5 there is the definition of the quotients.  This uses truncation, for which something like univalence and resizing is necessary and univalence and truncation is sufficient. 
Then theorem 6.10.6 right below that definition checks that these quotient do indeed behave like quotients should, and this is where univalence proper comes in.

This discussion of quotients from univalence in the HoTT book
originally comes from 

* [[Egbert Rijke]], [[Bas Spitters]], *Sets in homotopy type theory*, Mathematical Structures in Computer Science **25**  5 "From type theory and homotopy theory to Univalent Foundations of Mathematics" (2015) 1172-1202 
&lbrack;[doi:10.1017/S0960129514000553](https://doi.org/10.1017/S0960129514000553), [arXiv:1305.3835](http://arxiv.org/abs/1305.3835)&rbrack;

The relevant section there is 2.4 "Voevodsky's impredicative
quotients", see def. 2.24 and the lines right below.



The [[categorical semantics]]-version of the argument for colimits from a [[subobject classifier]] in an [[elementary topos]] is due to

* {#Pare74} [[Robert Paré]], _Colimits in Topoi_, Bull. AMS 80 (1974) pp.556-661. ([pdf](http://www.ams.org/journals/bull/1974-80-03/S0002-9904-1974-13497-X/S0002-9904-1974-13497-X.pdf))

reviewed for instance in

* {#MacLaneMoerdijk92} [[Saunders MacLane]], [[Ieke Moerdijk]], section IV.5 of _[[Sheaves in Geometry and Logic]] &#8211; A first introduction to topos theory_, Springer Verlag, 1992

A more elementary discussion is in 

* [[Todd Trimble]], _[[toddtrimble:An elementary approach to elementary topos theory]]_

[[!redirects quotient type]]
[[!redirects quotient types]]
