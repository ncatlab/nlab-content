
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

Quotient type may be constructed as [[higher inductive types]]. See [here](higher+inductive+type#QuotientsOfSets)

### From univalence
 {#FromUnivalence}

Quotient types are implied by adding [[univalence]] to [[Martin-Löf type theory]], see the references [below](#FromUnivalence).

More in detail, a sufficient set of hypothesis that imply the existence of quotient types is this:

* ambient [[dependent product types]] [[dependent sum types]] and [[identity types]];
* availability of [[propositional truncation]];
* existence of a univalent family $U$;
* every [[h-prop]] is equivalent to some type in $U$.

In terms of [[categorical semantics]] in fibration categories, this comes about as follows:

In fibration categories where every map is a fibration, "hprop" means
"[[subobject]]", propositional truncation becomes a stable [[image]]
factorisation, and from a univalent universe $U$ containing all hprops,
we can construct a [[subobject classifier]] as 

$$
  \underset{x \colon U}{\sum} isProp(x)
  \,.
$$

(For the subobject classification u.m.p., existence comes from "every
hprop is equivalent to some type in $U$", and uniqueness comes from
univalence of $U$.)  So in this setting, the HoTT argument just becomes
the usual construction of [[exact quotients]] from a subobject classifier
in a [[regular category|regular]] [[locally cartesian closed category]].

One thing to be careful about, in the fibration category setting, is
that "equivalences" as defined in type theory correspond not generally
to the original equivalences, but to the right homotopy equivalences,
which of course may be different.  This is why e.g. Mike Shulman's def
of "type-theoretic fibration category" doesn't include a class of
equivalences as separate data, but takes them to be the right homot
equivs.  So for the type-theoretic arguments to apply, "univalent
fibration" should be defined using right homot equivs.

## Related concepts

* [[setoid]]

* [[quotient]]

* [[quotient space]]

* [[quotient stack]]

## References

### From univalence
 {#FromUnivalence}

The argument that adding [[univalence]] (plus universe resizing) to [[Martin-Löf type theory]] implies the existence of quotient types is attributed to Voevodsky in places like here: [pdf, slides 41 & 61](http://benedikt-ahrens.de/talks/IRIT_slides.pdf).
  
Voevodsky's own account of this seems to be entirely in his Coq-code repository here:

* [[Vladimir Voevodsky]], _Equivalence classes with respect to a given relation_,
[here](https://github.com/vladimirias/Foundations/blob/df19211f602ab71ee44f0ae4de2a19170c5b9e4d/hlevel2/hSet.v#L466), _Set quotients of types_, 
[here](https://github.com/vladimirias/Foundations/blob/df19211f602ab71ee44f0ae4de2a19170c5b9e4d/hlevel2/hSet.v#L555)

A more readable version of this is in section 6.10 of 

* _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Def. 6.10.5 there is the definition of the quotients.  This uses
truncation, for which something like univalence and resizing is
necessary and univalence and truncation is sufficient for. 
Then theorem 6.10.6 right below that definition checks that these
quotient do indeed behave like quotients should, and this is where
univalence proper comes in.

This discussion of quotients from univalence in the HoTT book
originally comes from 

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_,
([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

The relevant section there is 2.4 "Voevodsky's impredicative
quotients", see def. 2.24 and the lines right below.

[[!redirects quotient type]]
[[!redirects quotient types]]
