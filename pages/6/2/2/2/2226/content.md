[[!redirects sign relations]]

* tic
{:toc}

A __sign relation__ is a special type of [[triadic relation]] that arises in the use of signs to connote meanings and denote objects.  If this sounds reminiscent of what we do in applying logic and reasoning to the world, actual and ideal, it is no accident.  Indeed, the polymathematician [[Charles Sanders Peirce]] famously defined _logic_ as "formal semiotic", that is, the formal theory of signs.

# History #

It is possible to trace the idea of a triadic sign relation back to hints in Plato and what we know of the Stoics, but one of the most detailed early formulations is found in this passage by Aristotle:

: Words spoken are symbols or signs $(\sigma\upsilon\mu\beta{o}\lambda\alpha)$ of affections or impressions $(\pi\alpha\theta\eta\mu\alpha\tau\alpha)$ of the soul $(\psi\upsilon\chi\eta)$;  written words are the signs of words spoken.  As writing, so also is speech not the same for all races of men.  But the mental affections themselves, of which these words are primarily signs $(\sigma\eta\mu\epsilon\iota\alpha)$, are the same for the whole of mankind, as are also the objects $(\pi\rho\alpha\gamma\mu\alpha\tau\alpha)$ of which those affections are representations or likenesses, images, copies $({o}\mu{o}\iota\omega\mu\alpha\tau\alpha)$.  (Aristotle, _De Interpretatione_, $1.16^{a}4$).

# Definition #

A definition of sign relations that is explicit enough to support the development of a formal theory was given by C.S. Peirce in the process of defining logic, and so it is informative to view it in that context.

: Logic will here be defined as _formal semiotic_.  A definition of a sign will be given which no more refers to human thought than does the definition of a line as the place which a particle occupies, part by part, during a lapse of time.  Namely, a sign is something, $A$, which brings something, $B$, its _interpretant_ sign determined or created by it, into the same sort of correspondence with something, $C$, its _object_, as that in which itself stands to $C$.  It is from this definition, together with a definition of "formal", that I deduce mathematically the principles of logic.  I also make a historical review of all the definitions and conceptions of logic, and show, not merely that my definition is no novelty, but that my non-psychological conception of logic has _virtually_ been quite generally held, though not generally recognized.  (Peirce, NEM 4, 20--21).

In the general discussion of diverse theories of signs, the question arises whether signhood is an absolute, essential, indelible, or _ontological_ property of a thing, or whether it is a relational, interpretive, and mutable role that a thing can be said to exercise only within a particular context of relationships.

Peirce's definition of a _sign_ defines it in relation to its _object_ and its _interpretant sign_, and thus it defines signhood in relative terms, by means of a predicate with three places.  In this definition, signhood is a role in a [[triadic relation]], a role that a thing fills in a given context of relationships --- it is not an _absolute_ or _non-relative_ property of a thing-in-itself, one that it possesses independently of all relationships to other things.

Some of the terms that Peirce uses in his definition of a sign may need to be elaborated for the contemporary reader.

* __Correspondence.__  The form of correspondence invoked in the above definition is what Peirce elsewhere calls a "triple correspondence", that is, just another way of referring to the whole triadic sign relation itself.  A sign relation, as a triadic relation, may involve various types of binary correspondences or dyadic relations, but it does not reduce to any combination of its dyadic aspects.  In particular, the triple correspondence that we find in sign relations should not be confused with the sort of "mirror image" correspondence between realities and representations that is debated in contemporary controversies about "correspondence theories of truth".

* __Determination.__  The concept of determination intended here is much more general than the concept we use in discussing strictly deterministic causal-temporal processes.  First of all, we are speaking of a _formal_ or _informational_ determination, as when we say "two points determine a line".  Causal and temporal determinations imply formal and informational determinations, but the converse does not always hold.  In addition, we are allowing here for what is called _determination in measure_, that is, an order of determinism that admits the full spectrum of more determined and less determined relationships.

* __Non-psychological.__  Peirce's "non-psychological conception of logic" must be distinguished from any variety of _anti-psychologism_.  He was quite interested in matters of psychology and had much to say about them.  But logic is a normative science while psychology is a descriptive science --- they are equipped with distinct sets of aims, methods, and rationales --- and thus the two sciences operate on different planes of study even when they have occasion to view the same data.

# Examples of sign relations #

Because the examples to follow have been artificially constructed to be as simple as possible, their detailed elaboration can run the risk of trivializing the whole theory of sign relations.  Despite their simplicity, however, these examples have subtleties of their own, and their careful treatment will serve to illustrate many important issues in the general theory of signs.

Imagine a discussion between two people, $\mathrm{Ann}$ and $\mathrm{Bob}$, and attend only to that aspect of their interpretive practice that involves the use of the following nouns and pronouns:  $\backprime\backprime\mathrm{Ann}\prime\prime, \backprime\backprime\mathrm{Bob}\prime\prime, \backprime\backprime\mathrm{I}\prime\prime, \backprime\backprime\mathrm{you}\prime\prime$.

In this setting the _object domain_ is the set of two people, $\{ \mathrm{Ann}, \mathrm{Bob} \}$, while the _sign system_ or _syntactic domain_ is the set of four signs, $\{ \backprime\backprime\mathrm{Ann}\prime\prime, \backprime\backprime\mathrm{Bob}\prime\prime, \backprime\backprime\mathrm{I}\prime\prime, \backprime\backprime\mathrm{you}\prime\prime \}$.

In their use of this sign system, $\mathrm{Ann}$ and $\mathrm{Bob}$ are not only the passive objects of nominative and accusative references but also the active interpreters of the language they use.  The _system of interpretation_ associated with each language user can be represented in the form of a triadic relation called the _sign relation_ of that interpreter.

Understood in terms of its set-theoretic extension, a sign relation $L$ is a subset of a cartesian product $O \:\times\: S \:\times\: I$, where the sets $O, S, I$ are known respectively as the _object domain_, the _sign domain_, and the _interpretant domain_ of the sign relation $L \subseteq O \:\times\: S \:\times\: I$.

Broadly speaking, the three domains of a sign relation can be any sets whatsoever, but the kinds of sign relations that are typically contemplated in computational settings are usually constrained to having $I \subseteq S$.  In these situations interpretants are just special cases of signs, and this makes it convenient to lump signs and interpretants together into a single class called the _syntactic domain_.  In the forthcoming examples, $S$ and $I$ are identical as sets, so the same elements manifest themselves in two different roles of the sign relations in question.  When it is necessary to refer to the whole set of objects and signs in the union of the domains $O, S, I$ for a given sign relation $L$, one may refer to this set as the _world_ $W$ of $L$ and write $W = W_L = O \:\cup\: S \:\cup\: I$.

To facilitate an interest in the abstract structures of sign relations, and to keep the notations as brief as possible as the examples become more complicated, it serves to introduce the following general notations:

: $O$ = Object Domain
: $S$ = Sign Domain
: $I$ = Interpretant Domain

Introducing a few abbreviations for use in considering the present Example, we have the following data:

: $O \:=\: \{ \mathrm{Ann}, \mathrm{Bob} \} \:=\: \{ \mathrm{A}, \mathrm{B} \}$

: $S \:=\: \{ \backprime\backprime\mathrm{Ann}\prime\prime, \backprime\backprime\mathrm{Bob}\prime\prime, \backprime\backprime\mathrm{I}\prime\prime, \backprime\backprime\mathrm{you}\prime\prime \} \:=\: \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}$

: $I \:=\: \{ \backprime\backprime\mathrm{Ann}\prime\prime, \backprime\backprime\mathrm{Bob}\prime\prime, \backprime\backprime\mathrm{I}\prime\prime, \backprime\backprime\mathrm{you}\prime\prime \} \:=\: \{ \backprime\backprime\mathrm{A}\prime\prime, \backprime\backprime\mathrm{B}\prime\prime, \backprime\backprime\mathrm{i}\prime\prime, \backprime\backprime\mathrm{u}\prime\prime \}$

In the present Example, $S$ = $I$ = Syntactic Domain.

The next two Tables give the sign relations associated with the interpreters $\mathrm{A}$ and $\mathrm{B}$, respectively, putting them in the form of relational databases.  Thus, the rows of each Table list the ordered triples of the form $(o, s, i)$ that make up the corresponding sign relations, $L_\mathrm{A}, L_\mathrm{B} \subseteq O \:\times\: S \:\times\: I$.  It is often tempting to use the same names for objects and for relations involving these objects, but it is best to avoid this in a first approach, taking up the issues that this practice raises after the less problematic features of these relations have been treated.

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} L_\mathrm{A} = \text{Sign Relation of Interpreter A} \\
Object & Sign & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime  }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{3}} L_\mathrm{B} = \text{Sign Relation of Interpreter B} \\
Object & Sign & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime  }
}$$

These Tables codify a rudimentary level of interpretive practice for the agents $\mathrm{A}$ and $\mathrm{B}$, and provide a basis for formalizing the initial semantics that is appropriate to their common syntactic domain.  Each row of a Table names an object and two co-referent signs, making up an ordered triple of the form $(o, s, i)$ that is called an _elementary sign relation_, that is, one element of the relation's set-theoretic extension.

Already in this elementary context, there are several different meanings that might attach to the project of a _formal semiotics_, or a formal theory of meaning for signs.  In the process of discussing these alternatives, it is useful to introduce a few terms that are occasionally used in the philosophy of language to point out the needed distinctions.

# Dyadic aspects of sign relations #

For an arbitrary 3-adic relation $L \subseteq X \:\times\: Y \:\times\: Z = X_1 \:\times\: X_2 \:\times\: X_3$, there are six 2-adic (or 2-ary) relations that are obtained by projecting $L$ on one of the planes of the $X Y Z$-space $X \:\times\: Y \:\times\: Z$.  Various notations for these projections are defined by the following sequence of equations:

$$\array{\arrayopts{\colalign{left}}
L_{X Y} & = & proj_{X Y} L & = & L_{12} & = & proj_{12} L & = &
\{ (x, y) \in X \:\times\: Y : (x, y, z) \in L \: (\exists z \in Z) \} \\
L_{X Z} & = & proj_{X Z} L & = & L_{13} & = & proj_{13} L & = &
\{ (x, z) \in X \:\times\: Z : (x, y, z) \in L \: (\exists y \in Y) \} \\
L_{Y X} & = & proj_{Y X} L & = & L_{21} & = & proj_{21} L & = &
\{ (y, x) \in Y \:\times\: X : (x, y, z) \in L \: (\exists z \in Z) \} \\
L_{Y Z} & = & proj_{Y Z} L & = & L_{23} & = & proj_{23} L & = &
\{ (y, z) \in Y \:\times\: Z : (x, y, z) \in L \: (\exists x \in X) \} \\
L_{Z X} & = & proj_{Z X} L & = & L_{31} & = & proj_{31} L & = &
\{ (z, x) \in Z \:\times\: X : (x, y, z) \in L \: (\exists y \in Y) \} \\
L_{Z Y} & = & proj_{Z Y} L & = & L_{32} & = & proj_{32} L & = &
\{ (z, y) \in Z \:\times\: Y : (x, y, z) \in L \: (\exists x \in X) \} }$$

By way of unpacking the set-theoretic notation, here is what the first definition says in ordinary language.  The 2-adic relation that results from the projection of $L$ on the $X Y$-plane $X \:\times\: Y$ is written as $L_{X Y}$, $proj_{X Y} L$, $L_{12}$, or $proj_{12} L$, and it is defined as the set of ordered pairs $(x, y)$ in $X \:\times\: Y$ such that $(x, y, z)$ is in $L$ for some $z$ in $Z$.

## Denotation ##

One aspect of a sign's complete meaning is concerned with the reference that a sign has to its objects, which objects are collectively known as the _denotation_ of the sign.  Denotative references fall within the projection of the sign relation on the plane that is spanned by its object domain and its sign domain.

Given a sign relation $L \subseteq O \:\times\: S \:\times\: I$, the projections $L_{O S} \subseteq O \:\times\: S$ and $L_{S O} \subseteq S \:\times\: O$ form a converse pair of 2-adic relations, either of which tells us all there is to know about the relationship between objects and signs in $L$.  Without loss of hay in either bale, the _denotative component_ of $L$ is defined and notated as follows:

$$\array{
\mathop{Den} (L) & \text{:=} & L_{O S} & = & \mathop{proj}_{O S} L
& = &
\{ (o, s) \in O \:\times\: S : (o, s, i) \in L \: (\exists i \in I) \}
}$$

Looking to the denotative aspects of $L_\mathrm{A}$ and $L_\mathrm{B}$, various rows of the above Tables specify, for example, that $\mathrm{A}$ uses $\backprime\backprime\mathrm{i}\prime\prime$ to denote $\mathrm{A}$ and $\backprime\backprime\mathrm{u}\prime\prime$ to denote $\mathrm{B}$, whereas $\mathrm{B}$ uses $\backprime\backprime\mathrm{i}\prime\prime$ to denote $\mathrm{B}$ and $\backprime\backprime\mathrm{u}\prime\prime$ to denote $\mathrm{A}$.  All of these denotative references are summed up in the projections on the $O S$-plane, as shown in the following Tables:

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Den} L_\mathrm{A} = \mathop{proj}_{O S} L_\mathrm{A} \\
Object & Sign \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime  }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Den} L_\mathrm{B} = \mathop{proj}_{O S} L_\mathrm{B} \\
Object & Sign \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime  }
}$$

## Connotation ##

Another aspect of meaning concerns the connection that a sign has to its interpretants within a given sign relation.  As before, this type of connection can be vacuous, singular, or plural in its collection of terminal points, and it can be formalized as the 2-adic relation that is obtained as a planar projection of the 3-adic sign relation in question.

The connection that a sign makes to its interpretant is here referred to as its _connotation_.  In the full theory of sign relations, this aspect of meaning includes the links that a sign has to affects, concepts, ideas, impressions, intentions, and the whole realm of an agent's mental states and allied activities, broadly encompassing intellectual associations, emotional impressions, motivational impulses, and real conduct.  Taken at the full, in the natural setting of semiotic phenomena, this complex system of references is unlikely ever to find itself mapped in much detail, much less completely formalized, but the tangible warp of its accumulated mass is commonly alluded to as the connotative import of language.

Formally speaking, however, the connotative aspect of meaning presents no additional difficulty.  The connotative aspect of a sign relation $L$ is given by its projections $\mathop{proj}_{S I} L$ and $\mathop{proj}_{I S} L$ on the plane of signs and interpretants.  Adopting the first orientation, the _connotative component_ of $L$ is defined and notated as follows:

$$\array{
\mathop{Con} (L) & \text{:=} & L_{S I} & = & \mathop{proj}_{S I} L
& = &
\{ (s, i) \in S \:\times\: I : (o, s, i) \in L \: (\exists o \in O) \}
}$$

All of these connotative references are summed up in the projections on the $S I$-plane, as shown in the following Tables:

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Con} L_\mathrm{A} = \mathop{proj}_{S I} L_\mathrm{A} \\
Sign & Interpretant \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime  }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Con} L_\mathrm{B} = \mathop{proj}_{S I} L_\mathrm{B} \\
Sign & Interpretant \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{A}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{A}\prime\prime \\
\backprime\backprime\mathrm{u}\prime\prime & \backprime\backprime\mathrm{u}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{B}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{B}\prime\prime \\
\backprime\backprime\mathrm{i}\prime\prime & \backprime\backprime\mathrm{i}\prime\prime  }
}$$

## Ennotation ##

The aspect of a sign's meaning that arises from the 2-adic relation of its objects to its interpretants has no standard name.  If an interpretant is considered to be a sign in its own right, then its independent reference to an object can be taken as belonging to another moment of denotation, but this neglects the mediational character of the whole transaction in which this occurs.  Denotation and connotation have to do with 2-adic relations in which the sign plays an active role, but here we have to consider a 2-adic relation between objects and interpretants that is mediated by the sign from an off-stage position, as it were.  As a relation between objects and interpretants that is mediated by a sign, this aspect of meaning may be referred to as the _ennotation_ of a sign, and the 2-adic relation that forms the _ennotative component_ of a sign relation $L$ may be notated as $\mathop{Enn} (L)$.

The ennotative component of meaning for a sign relation $L$ is captured by its projection on the plane of the object and interpretant domains, defined and notated as follows:

$$\array{
\mathop{Enn} (L) & \text{:=} & L_{O I} & = & \mathop{proj}_{O I} L
& = &
\{ (o, i) \in O \:\times\: I : (o, s, i) \in L \: (\exists s \in S) \}
}$$

As it happens, the sign relations $L_\mathrm{A}$ and $L_\mathrm{B}$ are fully symmetric with respect to exchanging signs and interpretants, so all the data of $\mathop{proj}_{OS} L_\mathrm{A}$ is echoed unchanged in $\mathop{proj}_{OI} L_\mathrm{A}$ and all the data of $\mathop{proj}_{OS} L_\mathrm{B}$ is echoed unchanged in $\mathop{proj}_{OI} L_\mathrm{B}$, as shown in the following Tables:

$$\array{
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Enn} L_\mathrm{A} = \mathop{proj}_{O I} L_\mathrm{A} \\
Object & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{i}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{u}\prime\prime  }
&
\array{\arrayopts{\frame{solid}\rowlines{solid solid none}}
\cellopts{\colspan{2}} \mathop{Enn} L_\mathrm{B} = \mathop{proj}_{O I} L_\mathrm{B} \\
Object & Interpretant \\
\mathrm{A} & \backprime\backprime\mathrm{A}\prime\prime \\
\mathrm{A} & \backprime\backprime\mathrm{u}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{B}\prime\prime \\
\mathrm{B} & \backprime\backprime\mathrm{i}\prime\prime  }
}$$

# Semiotic equivalence relations #

* See [[semiotic equivalence relation]].

# References and further reading #

* Aristotle, "On Interpretation", Harold P. Cooke (trans.), in _Aristotle_ (vol. 1), Harvard University Press, Cambridge, MA, 1938.

* Peirce, C.S., _The New Elements of Mathematics by Charles S. Peirce_, 4 volumes in 5, Carolyn Eisele (ed.), Mouton Publishers, The Hague, Netherlands, 1976.  Humanities Press, Atlantic Highlands, NJ, 1976.  Cited as (NEM volume, page).

# External links #

* [Sign Relation @ MyWikiBiz](http://mywikibiz.com/Sign_relation)

* [Sign Relation @ PlanetMath](http://planetmath.org/encyclopedia/SignRelation.html)

* [Semiotic Equivalence Relation @ PlanetMath](http://planetmath.org/encyclopedia/SemioticEquivalenceRelation.html)
