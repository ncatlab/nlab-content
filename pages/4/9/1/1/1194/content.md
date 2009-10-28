* table of contents
{:toc}

# Idea

Type theory is a branch of mathematical [[logic]] which studies elements of varying _types_, or _sorts_, rather than elements of a single fixed sort.  Type theory is distinguished particularly by the importance of [[context]] in the specification of terms and formulas, and has close links to the [[internal logic]] of categories.

# An introduction for category-theorists

One way to look at type theory, from the point of view of a category theorist, is as a _syntax for describing the construction of objects and morphisms in a category_.  This interpretation can be called *categorical semantics*.

## Categorical semantics of type theory

The [[syntax|syntactic]] constructs corresponding to objects and morphisms are called _types_ and _terms_, respectively.  The types correspond to objects (with various subtleties), while the terms denote morphisms by using _variables_ to indicate domains.  For example, given terms $f(x)$ and $g(y)$ with one free variable each, representing morphisms $[f]$ and $[g]$, the term $g(f(x))$ represents the morphism $[g]\circ [f]$.

What sorts of syntactical constructions you allow on types and terms corresponds to the structure of the category in which the [[semantics]] is intended to occur.  For example, if our semantic categories have binary products, then the syntax of the type theory includes a _type constructor_ $\times$ allowing us to build a new type $A\times B$ from two given types $A$ and $B$.  It will also have _term constructors_ allowing us to build, for example, a term $\langle a,b\rangle$ of type $A\times B$ from any given terms $a$ of type $A$ and $b$ of type $B$.  Note the great advantage of the type-theoretic formalism: the notation (and thought process) can be very set-theoretic, but because the terms $a$ and $b$ can denote morphisms with arbitrary domain (by choosing their free variables appropriately), we are really describing the full universal property of a cartesian product.

An important extension of type theory involves _dependent_ types: types which are a "function" of the _elements_ of some other type.  For instance, the type $D(m)$ of "days of the month" is a function of the element $m$ of the type $M$ of months, since different months have different allowable collections of days.  Syntactically, in addition to the existence of dependent types, one often allows constructions on them such as _dependent sums_ $\Sigma_{x:A} B(x)$ (regarded as the "type of pairs" $(x,y)$ such that $x\in A$ and $y\in B(x)$) and _dependent products_ $\Pi_{x:A} B(x)$ (regarded as the "type of functions" $f$ such that for any $x\in A$, we have $f(x)\in B(x)$).  Semantically, a type $B(x)$ depending on an element $x$ of type $A$ is represented by a morphism $B\to A$, thought of as an $A$-indexed family of objects; each $B(x)$ is supposed to be the fiber over $x$.  Then dependent sum and product are interpreted by the left and right adjoints to the [[pullback]] functors $f^*:E/Y\to E/X$ along a morphism $f:X\to Y$; the left adjoint always exists, while the right adjoint exists in any [[locally cartesian closed category]].

## Categorical semantics of logic in type theory

How does type theory relate to logic?  Well, _propositional logic_ is just the type theory whose semantic categories are _posets_.  In this case, the types $P,Q,\dots$ are usually called _propositions_, and the existence of a (necessarily unique) term of type $Q$, having a free variable of type $P$, is just the assertion that $P\le Q$ (or, in more logical language, "$P$ implies $Q$").  The type constructor for binary products is usually written $\wedge$ and called "and," the type constructor for binary coproducts is usually written $\vee$ and called "or," and so on.  The term constructors are generally called _inference rules_, since they allow us to infer new theorems from old ones.

Now, it turns out that there are (at least) two ways to reconcile logic (the type theory of posets) with type theory of more general categories.  In the first approach, which can be described as _typed predicate logic_ or _logic over type theory_, we keep the propositions separate from the types.  (Since, as we have seen, propositional logic is a specific kind of type theory, this means we really have two interacting type theories.  However, in this case we generally reserve "type" for the second kind of type as distinguished from the "propositions.")

In this case, the syntax has collections of types and terms, together with constructors, and also rules for forming propositions out of types and terms, and inference rules for forming implications between propositions.  The types and terms form the underlying type theory of the logic, and the propositions 'depend' on these.  For instance, given two terms $x,y$ of type $A$, we can often form a proposition $x=y$ which asserts that $x$ and $y$ are equal.  Other important "proposition constructors" are the _quantifiers_ $\exists x$ and $\forall x$, where $x$ is a variable associated to a type (not a proposition).

The natural home for the semantics of typed predicate logic turns out to be an _indexed poset_: a category $C$ together with a functor $P:C^{op}\to Pos$.  This is often described equivalently as a category $E$ of propositions that is [[Grothendieck fibration|fibred over]] the category $C$ of terms, and whose fibers are posets.  (Thus, an alternative way of thinking of propositional logic is as the 'logic' of a poset fibred over the trivial one-object category, which corresponds to the fact that the propositions do not contain or depend on typed terms.)  The ordinary type theory happens in $C$ as described above, and a proposition $\phi$ with a free variable $x$ of type $A$ is interpreted by an element $[\phi]$ of the poset $P(A)$ (the fiber over $A$).  The prototypical indexed poset is $P:Set^{op}\to Pos$ sending each set to the poset of its [[subset]]s, with an evident generalization to [[subobject]]s in any category; thus we think of $[\phi]$ as "the set of all $x\in A$ such that $\phi(x)$ is true." Another way of describing this setup is as the _subobject fibration_ $cod:Sub(C)\to C$.

Just as the allowed constructions on types are reflected in
the structure of the semantic category, the allowed
constructions on propositions here are reflected in the
structure of the semantic posets $P(A)$.  For instance, if
we allow conjunction $\wedge$ of propositions, then each
$P(A)$ must be a meet-[[semilattice]].  The action of the
functor $P$ on morphisms, usually written $f^*:P(Y)\to
P(X)$, is used to model the substitution of the term
represented by $f$ for the variable of a proposition,
multiple variables and substitutions being interpreted by
means of finite products, as in [[Lawvere theory|Lawvere
theories]].  In that case, the functor $\pi^*:P(X)\to
P(X\times Y)$ interprets the adding of an unused variable
to a context.  The left and right [[adjoint
functor|adjoints]] to $f^*$, when they exist, describe the
semantics of the two quantifiers; thus we write them as
$\exists_f \dashv f^* \dashv \forall_f$.  The functors
$\exists_\pi$ and $\forall_\pi$ interpret the traditional
existential and universal quantifiers.

The [[internal logic]] of various sorts of categories are most naturally regarded as the typed predicate logic associated to the "poset of subobjects" functor $Sub:C^{op}\to Pos$, and the requisite levels of structure on $C$ induce the required semantic structure on both $C$ and $Sub$.  For instance, if $C$ is [[regular category|regular]], then each $Sub(X)$ is a meet-semilattice and the adjoints $\exists_f$ exist, while if $C$ is a [[Heyting category]], then each $Sub(X)$ is a [[Heyting algebra]] and both adjoints $\exists_f$ and $\forall_f$ exist.  However, not all indexed posets in which one wants to apply type theory are constructed from subobjects  in some category; see for instance [[tripos]].

The _second_ approach to reconciling type theory with logic
is to blur the distinction between types and propositions;
this is called the "[[propositions as types]]" paradigm.
Instead of requiring that a proposition $\phi$ be
interpreted as merely true or false (that is, a [[truth
value]] or equivalently a [[subsingleton]]), we allow it to
be interpreted by any set (that is, any object of the
semantic category).  One way to think of this is that
$[\phi]$ is the set of _proofs_, or _reasons_, why $\phi$
is true; it is [[inhabited set|inhabited]] iff $\phi$ is
true, but a true statement may have many distinct proofs
(although, for technical reasons, this is not the case in
naive categorical models of [[classical logic]]).  Thus,
for instance, instead of asserting that $\phi\Rightarrow
\psi$, we consider the _type_ $\phi \to \psi$ of all proofs
that $\phi$ implies $\psi$, which is inhabited just when
$\phi$ actually does imply $\psi$.  Similarly, the
quantifiers $\exists$ and $\forall$ become identified with
the dependent type constructors $\Sigma$ and $\Pi$.  In
this case, the semantics involved is the more general
_codomain fibration_ $p:C^\to\to C$, whose fibres are the [[slice category|slice categories]] $C/A$.

## Syntactic categories and free models

(to be written; for now see [[context]] and [[internal logic]]).


# Type-theoretical foundations

From a [[foundations|foundational]] point of view, type theory can also be regarded as the language in which mathematics is written.  This has several aspects, notably *syntax* (the language) and *semantics* (what it means).

## Syntax of type-theoretical foundations

At the most basic level, what we do when we do mathematics is *manipulate symbols according to specified rules*.  Just as in chess the rules state that a knight moves like *so* and not like *so*, in mathematics the rules state that a quantifier can be eliminated like *so* and not like *so*.  The actual rules of the game of mathematics are extremely complicated, but the idea of foundations is to derive them from a much simpler list of fundamental rules.  Type theory says that these fundamental rules are a *calculus of terms*, and that each term comes equipped with a *type*.  Thus, the rules define one or more *types*, and one of the judgments one can make (that is, one of the "moves" of the game) is of the form "$t$ is a well-formed term of type $A$," usually written as $t:A$.

In this way we can build many different "type theories".  Most familiar type theories include a special type called $Prop$ of "propositions", and a special type of judgment which asserts that a given proposition (i.e. a term of type $Prop$) is "true."  We generally also include "logical inference" rules for constructing complex propositions (e.g. if $\varphi:Prop$ then $(\forall x:A. \varphi) :Prop$) and deducing the truth of propositions (e.g. if $\varphi$ and $\psi$ then also $\varphi\wedge\psi$).  We may also include "axioms", i.e. propositions $\varphi$ such that the judgment "$\varphi$ is true" can be made unconditionally.  For example, in Peano arithmetic, there are two types $N$ and $Prop$, a constant term $0:N$, a rule that if $n:N$ then $s(n):N$, a rule that if $n:N$ and $m:N$ then $(n=m):Prop$, the usual rules of logical inference, and various axioms.

Now if we want a foundation for *all* of mathematics, of course we need a more powerful theory than these.  But ZFC can also be stated in this style: it has two types $Set$ and $Prop$, rules saying that if $x:Set$ and $y:Set$ then $(x=y):Prop$ and $(x\in y):Prop$, the usual rules of logical inference and a [collection of axioms](http://ncatlab.org/nlab/show/ZFC).  The same with [ETCS](http://ncatlab.org/nlab/show/ETCS), which it is convenient to write with three types $Set$, $Function$, and $Prop$.  Especially when we intend a theory like ZFC or ETCS as a foundation for all of mathematics, it is convenient to call the type-theoretic language in which these theories are written the "meta-language" or "meta-theory," while ZFC/ETCS is the "object language" or "object theory."

Things then get a bit confusing because there are various ways to augment type theories.  It's common to include *type constructors*, which allow us to form new types such as $A\times B$ out of types $A$ and $B$.  Then we need an additional judgment $T:Type$, so that such a type-constructor is a rule saying that (for example) if $A:Type$ and $B:Type$ then $(A\times B):Type$.  We can also have type-constructors which take *terms* as input, in addition to types; these are called *dependent types*.  When we include exponential or dependent-product types, the complexity and power of the type-theoretic meta-language begins to approach that of the object languages ZFC and ETCS, enabling it itself to serve as a foundation for mathematics.  That is, instead of defining a group to be a set equipped with (among other things) a function $G\times G\to G$, we could interpret a group as a *type* $G$ equipped with (among other things) a *term* $m(x,y):G$ with free variables $x:G$ and $y:G$.  Or, which amounts to the same thing, we could change our terminology so that what we have been calling "types" are instead called "sets."  It is then natural to say that a type theory (especially one with many type-constructors) is itself the object-theory in a meta-meta-theory having meta-types (or "kinds") such as $Type$, $Term$, and $Judgment$.

Thus, words like "type" and "set" and "class" are really quite fungible.  This sort of level-switch is especially important when we want to study the mathematics *of* type theory, i.e. the mathematical theory of manipulating symbols according to the rules of type theory, analogous to the mathematical theory of moving pieces around on a chessboard according to the usual rules.  When we study type theory in this way, we are *doing* mathematics, just like when we're doing group theory or ring theory or whatever.  It's just that our objects of study are called "types", "terms", and so on.  However, what we do in this mathematical theory *can*, like any other area of mathematics, be formalized in any particular chosen foundation, be it ZFC or ETCS or a type theory at a higher level.  Now the type theory is itself the "object-theory" and ZFC is the "meta-theory"!

## Semantics of type-theoretical foundations

Now, intuitively, we generally think of a type $A$ as denoting some "collection" of "things", and a term $t:A$ as indicating a "particular one" of those things.  In order for this to make sense, the type theory has to exist in some metatheory (which might or might not be formalized) having a notion of "set" to specify the relevant "collections of things".  In particular, there must be a set of types, and for each type there is a set of terms which can be judged to be of that type.  The judgment rules for propositions then become the study of formal logic; we say that a proposition is "provable" or is a "theorem" if it can be judged to be true.

Now, a *model* of this theory assigns a set $[A]$ (in the meta-theoretic sense) to every type $A$ and a function of appropriate arity to every term, in a way so that the rules and axioms are satisfied.  Thus, for instance, a model of Peano arithmetic consists of a set $[N]$, an element $[0]\in [N]$, a function $[s]\colon [N]\to[N]$, and so on.  Likewise, a model of the type theory of ZFC (here the levels get confusing) consists of a set $[Set]$, a function $[{\in}]\colon [Set]\times [Set] \to [Prop]$, and so on.

One can then prove, under certain hypotheses, various things about the relationship between syntax and semantics, such as:

* The *Soundness Theorem*: if $\varphi$ is a proposition which is provable from the axioms of a theory, then the corresponding statement $[\varphi]$ in any model is actually true (in the sense of the metatheory).  Equivalently, if a theory has at least one model, then it doesn't prove a contradiction.
* The *Completeness Theorem*: if $[\varphi]$ is true in every model of a theory, then $\varphi$ is provable in that theory.  Equivalently, if a theory doesn't prove a contradiction, then it has at least one model.
* The (first) *Incompleteness Theorem*: if a theory doesn't prove a contradiction, then there exist statements $\varphi$ such that neither $\varphi$ nor $\not\varphi$ is provable in the theory.
* Corollary to the completeness and incompleteness theorems: if a theory doesn't prove a contradiction, then it has more than one model.

The "certain hypotheses" is where we get into the difference between *first-order* and *higher-order*.  We say that a type theory is *higher-order* if it involves type constructors such as function-types $B^A$ (intended to represent the "type of all functions $A\to B$") or power-types $P A$ (intended to represent the "type of all subtypes of $A$).  Otherwise it is *first-order*.  (We have to deal with $Prop$ specially in first-order logic.  If we actually have a type $Prop$, then the theory should be higher-order, since $Prop \cong P 1$; thus in first-order logic we take $Prop$ to be a "kind" on the same level as $Type$, which doesn't participate in type operations.)  We say "second-order" if we never iterate the power-type operation.

+-- {: .query}
I don\'t buy your argument that $Prop$ must be treated specially; perhaps I don\'t understand what you\'re saying, but I\'ll pretend that I do.  First, I don\'t see the relevance of your premise, that $Prop$ makes things higher-order because it is a power type.  You might as well say that $1$ makes things higher-order because $1 \cong P 0$.  What really makes things higher order is the ability to form *arbitrary* power types or function types, not the existence of one or two special cases.  And second, I don\'t agree with the conclusion, that $Prop$ can\'t participate in type operations.  It\'s true that many type theories *do* treat $Prop$ specially and forbid its participation in type operations, but allowing it to participate in first-order type operations like $\times$ and $+$ is not going to make things higher order.  Conversely, $Prop \cong 1 + 1$ in some type theories, in which case you can hardly stop it from participating in type operations!  ---Toby
=--

The Soundness Theorem is true for all theories,  but *the Completeness Theorem is true only for first-order theories*.  The Incompleteness Theorem as stated above is true for higher-order theories, but the corollary fails since the completeness theorem does.  In particular, a higher-order theory can sometimes be *categorical* in the logician's sense: having exactly one model (at least, up to isomorphism).  The second-order version of Peano Arithmetic has this property.  (At this level, there is little fundamental difference between first-order and higher-order theories; they each have advantages and disadvantages.  However, when we move up to the metalevel and talk about the term calculus itself, we always get a first-order theory.  This is why some people believe that first-order logic is the only truly "foundational" logic.)

## Term models

One usually proves the Completeness Theorem by building a "tautological" model out of the theory itself.  That is, for each type $A$ we simply take the set $[A]$ to be the set of terms of type $A$ with no free variables (or "ground terms").  However, without modification, this naive idea fails for two reasons.

First of all, there might not be enough ground terms.  Some of the axioms of the theory might assert that there exists something with some property, without there being a corresponding term constructor actually producing something with that property.  This is obviously the case for the usual version of ZFC, which has no term constructors at all (hence no ground terms at all!) but lots of axioms that assert the existence of things.  This problem is easily remedied, however, by introducing new constant terms or term constructors into the language.

The second problem is that we may not know how to define all the necessary relations on the ground terms in order to have a model.  Suppose, for instance, we have a couple of ground terms $t_1$ and $t_2$ in some augmented version of ZFC; how can we tell whether $t_1\in t_2$ should hold in our tautological model?  Certainly if the axioms of the theory imply $t_1\in t_2$, then it should hold, and if they imply $t_1\notin t_2$, then it shouldn't, but they might not imply either one.  The usual way to remedy this is to enumerate all such statements and one by one decide arbitrarily whether to make them true or false in the model we're constructing.

This works, but the model we get (though small, even countable, and concrete) isn't really *canonical*; we had to make a bunch of arbitrary choices.  In the case of Peano Arithmetic, we can avoid introducing new constant terms and obtain a model which is "canonical" and in fact the "smallest" in some sense: it consists of the terms $s(s(\dots(s(0))\dots))$, which can of course be identified with "the" natural numbers in the meta-theory.  But this doesn't work for most other theories.  Suppose, for instance, that we augment ZF with term constructors for all of its existence axioms.  Let $\varphi$ be a sentence independent of ZF; then our term-constructor for the axiom of separation gives us a term $\{\emptyset | \varphi\}$.  Does the relation $\emptyset \in \{\emptyset | \varphi\}$ hold in the term model?  We have to make an arbitrary choice.

The slicker categorial approach described above using categories of [[contexts]] does produce a really canonical model, but only with an expanded notion of "model": instead of each $[A]$ being a set, we take it to be an object of some fixed category $\mathcal{S}$ with enough structure.  We can then build a much more "tautological" model because we have the freedom to build the category $\mathcal{S}$ along with the model.  In the resulting model, the true statements are *precisely* the statements provable in the theory, and it's even initial among all models of the theory in the appropriate sort of category.


# Type theory versus set theory

Blog discussions about the difference between type theory and set theory:

* [one](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c026984)
* [two](http://golem.ph.utexas.edu/category/2009/10/syntax_semantics_and_structura.html#c028459)


# Formal definitions

(It might be nice to actually *define* a type theory, at least in some easy restricted case.)


[[!redirects dependent type theory]]
[[!redirects type theories]]
