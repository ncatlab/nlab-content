
# Proper classes
* table of contents
{: toc}

## Idea

A _proper class_ is a [[set]] that is too big to be a set.  Exactly what this means depends on the [[foundations]] of mathematics, but something must be said about it to study [[large category|large categories]].


## Definitions

There are several ways to deal with this and define a proper class.

A __proper class__ is a [[large category|large]] [[discrete category]].  But since a large category is usually defined as having a proper class of objects, this just moves the bubble under the wallpaper to 'large category' and something must be applied there.

A __proper class__ is a collection that can be put in [[bijection]] with the class of all [[ordinal number|ordinals]], $Ord$.  But this requires the [[global axiom of choice]] to be correct.

A __proper class__ is a class that is not a [[set]].  So now we have to define 'class'.

A __proper class__ is a class whose cardinality is not the [[cardinal number]] of any set.  This is a  version of the previous definition not violating the [[principle of equivalence]]; however, in some foundations these are actually equivalent (using the [[axiom of replacement]]).

A __class__ is a collection of [[sets]].  Here the bubble is moved to 'collection', but we will be able to pop that bubble below.  Also we might want to allow the members of a proper class to be other than sets (such as [[structured sets]]); certainly it is true, however, that a __pure class__ is a collection of [[pure sets]].

A __class__ is a formula in the language of [[set theory]] for a [[truth value]], equipped with a specified [[free variable]] for a set.  This is a formalisation of the previous definition, but it must be interpreted metamathematically: a __formula for a class__ in a given [[context]] $\Gamma$ is a formula for a truth value in the extension of $\Gamma$ by one more free variable for a set.

A __class__ may even be an undefined concept; the real definition is to define a __[[set]]__ as a class that is itself a member of some class.  With appropriate axioms, this is equivalent to the previous definition (and conservative over set theory without classes), but it\'s also possible to apply stronger axioms here; this choice is the difference between $BNG$ and $MK$ as extensions of [[ZFC]].

A __class__ is a [[subset]] of a [[Grothendieck universe]] $U$, while a ([[small category|small]]) __set__ is merely an element of $U$.  This gives a relative notion, depending on $U$.  As stated here, we get a concept of class like that of the strong theory $MK$; to be more like $BNG$ (and therefore conservative over set theory without an axiom of universes) we should define a __class__ to be a subset of $U$ that is definable in the language of set theory.


## Usage

A __[[large category]]__ is a [[category]] whose class of [[morphisms]] is a proper class.  It is sufficient that the class of [[objects]] be a proper class, which is also necessary if the category is [[locally small category|locally small]].

Category theorists care about proper classes because many examples of categories in practice (such as [[Set]], to begin with!) are large.


## Category of classes

The [[category of classes]] is closed under all large [[limits]]
and [[small colimits]].
See the linked article for more information and precise definitions.

The [[category]] of classes $Class$ is a [[large category]] that is not [[locally small]].
It admits all [[colimits]], understood in the following sense.

First, given a class $I$, we define an $I$-indexed family of classes
as a map of classes $f:T\to I$.
The preimage $f^{-1}(\{i\})$ is precisely the class with index $i$.
Such families can be pulled back along maps of classes $J\to I$ and pushed forward along maps $I\to J$.

Next, given a category $I$ (not necessarily locally small),
we define an $I$-indexed diagram of classes
as a pair $(o:T_O\to Ob(I),m:T_M\to Mor(I))$ of indexed families of classes
that satisfies the obvious reformulation of conditions in the definition of a [[functor]].

We now claim that an arbitrary $I$-indexed diagram of classes admits a [[colimit]].

First, the standard reduction of $I$-indexed [[colimits]]
to a [[coequalizer]] of a pair of arrows between coproducts indexed by $Mor(I)$ and $Ob(I)$
still works in this context since class-indexed families of classes can be pulled back
along source and target maps $Mor(I)\to Ob(I)$.

Secondly, class-indexed coproducts of classes can be computed simply by taking
the total class of the corresponding class-indexed family of classes.

Thirdly, [[coequalizers]] of classes exist by [[Scott's trick]].
Observe that given a pair of arrows $f,g:X\to Y$ between classes,
we can define an [[equivalence relation]] on $Y$
by saying that $y~y'$ if there is a map $h:[0,n]\to Y$
such that $h(0)=y$, $h(n)=y'$
and for any $i\in[0,n)$ there is $x\in X$ such that $h(i)=f(x)$ and $h(i+1)=g(x)$
or $h(i)=g(x)$ and $h(i+1)=f(x)$.
The quotient of $Y$ by this equivalence relation exists by [[Scott's trick]]
and is precisely the desired coequalizer.

If one is working in the category of (definable) classes for [[ZF]] or [[ZFC]], or the category of classes of [[NBG]], then all finite _external_ diagrams $D\to Class$ have colimits.
The reduction to a coequaliser of a pair of finite coproducts works as per usual.
_Finite_ coproducts exist as one can use finite disjunctions of the defining formulas (in ZF(C)) or Class Separation (in NBG) to define a new class.
Coequalisers then exist by the above argument, as [[Scott's trick]] is available due to the class $V$ of sets having well-founded stratifications by sets (for instance the von Neumann [[cumulative hierarchy]] $V = \bigcup_{\alpha\in ORD} V_\alpha$).

Just as an [[elementary topos]] is an axiomatization of basic properties of the category [[Set]], a [[category with class structure]] is an axiomatization of basic properties of the category $Class$.  See also [[algebraic set theory]].

## References

A paper detailing one approach to the technical side of how classes appear in [[category theory]] (namely using [[Grothendieck universes]]) is

* {#Levy18} Paul Blain Levy, _Formulating Categorical Concepts using Classes_ (arXiv:[1801.08528](https://arxiv.org/abs/1801.08528))

[[!redirects class]]
[[!redirects classes]]
[[!redirects proper class]]
[[!redirects proper classes]]
