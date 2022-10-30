<div class="rightHandSide toc">
[[!include type theory - contents]]
</div>
* table of contents
{:toc}

# Idea

Type theory is a branch of mathematical [[logic]] which studies elements of varying _types_, or _sorts_, rather than elements of a single fixed sort.  Type theory is distinguished particularly by the importance of [[context]] in the specification of terms and formulas, and has close links to the [[internal logic]] of categories.


# An introduction for category-theorists

One way to look at type theory, from the point of view of a category theorist, is as a _syntax for describing the construction of objects and morphisms in a category_.  This interpretation can be called *categorical semantics*.  Note that this type of semantics is only relevant to *extensional* type theory; see the section on intensional vs. extensional type theory below.  Even so, the description given here is a somewhat simplified one, which really only applies to type theories with a [[dependent sum]] operation, which allows us to reinterpret every [[context]] as a single type.


## Categorical semantics of type theory {#CategoricalSemantics}

Given a [[category]] $\mathcal{C}$, we may speak about its **categorical semantics** in terms of type theory. The [[syntax|syntactic]] constructs corresponding to [[object]]s and [[morphism]]s are called _types_ and _terms_, respectively. The types correspond to objects (with various subtleties), while the terms denote morphisms by using _variables_ to indicate domains.  


* In category theory a [[morphism]] $f$ in $\mathcal{C}$ with 
  [[domain]] $B$ and [[codomain]] $A$ 
  is in symbols

  $$  B \stackrel{f}{\to} A\,. $$ 

* In the categorical semantics of the category the same is
   a _term_ $f(x)$ of _type_ $A$ where $x$ is 
  a _free variable_ of _type_ $B$, which in symbols is given by

  $$ x\colon B \vdash f(x)\colon A\,. $$

We may think of the _free variables_ here as being placeholders for all the [[generalized element]]s $U \stackrel{x}{\to} B$ of $B$. Then the assertion $x\colon B \vdash f(x)\colon A$ indicates that with $B \stackrel{f}{\to} A$ given we may send $U \stackrel{x}{\to} B$ to the [[composition]] $(U \stackrel{x}{\to} B \stackrel{f}{\to}A ) = (U \stackrel{f(x)}{\to} A)$.

So the notation $x\colon B \vdash f(x)\colon A$ is a direct reflection of the description of the morphism $f$ under the [[Yoneda embedding]] $C \hookrightarrow Func(C^{op}, C)$. Since the Yoneda embedding is a [[full and faithful functor]], this is indeed an entirely equivalent characterization of the morphism $f$.

Generally, [[composition]] of morphisms in the category

$$
  C \stackrel{f}{\to} B \stackrel{g}{\to} A 
  \;\;
  =
  \;\; C \stackrel{g \circ f }{\to} A
$$

corresponds to _substitution_ in type theory of a term for a free variable: the morphisms $f$ and $g$ are interpreted as terms $f(x)$ and $g(y)$ of type $B$ and $A$ respectively, where $x$ and $y$ are variables of type $C$ and $B$ respectively. The composite morphism $g\circ f$ is the term $g(f(x))$ of type $A$ where $x$ is again a variable of type $C$.

In symbols this is written as:

$$ \frac { x\colon C \vdash f(x)\colon B \qquad y\colon B \vdash g(y)\colon A }
         { x\colon C \vdash g(f(x))\colon A } $$

Here the horizontal bar indicates that we have written down a _rule_, the rule that the judgement on the bottom is valid whenever the judgements on the top are valid.

What is an [[identity morphism]] $A \stackrel{f = Id_A}{\to} A$ in category theory is a term of the form $f(x) = x$ in type theory, a variable itself regarded as a term: $x$ is a term of type $A$ where $x$ is a variable of type $A$.

In symbols:

$$ \frac {}{ x\colon A \vdash x\colon A } $$

What sorts of syntactical constructions you allow on types and terms corresponds to the structure of the category $\mathcal{C}$ in which the [[semantics]] is intended to occur.  

For example, if our semantic categories have binary [[product]]s, then the syntax of the type theory includes a _type constructor_ $\times$ allowing us to build a new type $A\times B$ from two given types $A$ and $B$.  It will also have _term constructors_ allowing us to build, for example, a term $\langle a,b\rangle$ of type $A\times B$ from any given terms $a$ of type $A$ and $b$ of type $B$.  Note the great advantage of the type-theoretic formalism: the notation (and thought process) can be very set-theoretic, but because the terms $a$ and $b$ can denote morphisms with arbitrary domain (by choosing their free variables appropriately), we are really describing the full universal property of a cartesian product.

An important extension of type theory involves _dependent_ types: types which are a "function" of the _elements_ of some other type.  For instance, the type $D(m)$ of "days of the month" is a function of the element $m$ of the type $M$ of months, since different months have different allowable collections of days.  Syntactically, in addition to the existence of dependent types, one often allows constructions on them such as _dependent sums_ $\Sigma_{x:A} B(x)$ (regarded as the "type of pairs" $(x,y)$ such that $x\in A$ and $y\in B(x)$) and _[[dependent product]]s_ $\Pi_{x:A} B(x)$ (regarded as the "type of functions" $f$ such that for any $x\in A$, we have $f(x)\in B(x)$).  Semantically, a type $B(x)$ depending on an element $x$ of type $A$ is represented by a morphism $B\to A$, thought of as an $A$-indexed family of objects; each $B(x)$ is supposed to be the fiber over $x$.  Then dependent sum and product are interpreted by the left and right adjoints to the [[pullback]] functors $f^*:E/Y\to E/X$ along a morphism $f:X\to Y$; the left adjoint always exists, while the right adjoint exists in any [[locally cartesian closed category]].


## Categorical semantics of logic in type theory

How does type theory relate to logic?  Well, _[[propositional logic]]_ is just the type theory whose semantic categories are _posets_.  In this case, the types $P,Q,\dots$ are usually called _propositions_, and the existence of a (necessarily unique) term of type $Q$, having a free variable of type $P$, is just the assertion that $P\le Q$ (or, in more logical language, "$P$ implies $Q$").  The type constructor for binary products is usually written $\wedge$ and called "and," the type constructor for binary coproducts is usually written $\vee$ and called "or," and so on.  The term constructors are generally called _inference rules_, since they allow us to infer new theorems from old ones.

Now, it turns out that there are (at least) two ways to reconcile propositional logic (the type theory of posets) with type theory of more general categories, producing [[predicate logic]].

### Logic over type theory

In the first approach, which can be described as _typed predicate logic_ or _logic over type theory_, we keep the propositions separate from the types.  (Since, as we have seen, propositional logic is a specific kind of type theory, this means we really have two interacting type theories.  However, in this case we generally reserve "type" for the second kind of type as distinguished from the "propositions.")

In this case, the syntax has collections of types and terms, together with constructors, and also rules for forming propositions out of types and terms, and inference rules for forming implications between propositions.  The types and terms form the underlying type theory of the logic, and the propositions 'depend' on these.  For instance, given two terms $x,y$ of type $A$, we can often form a proposition $x=y$ which asserts that $x$ and $y$ are equal.  Other important "proposition constructors" are the _quantifiers_ $\exists x$ and $\forall x$, where $x$ is a variable associated to a type (not a proposition).  This can concisely be formalized as a [[pure type system]] with one sort for types and another sort for propositions, such that propositions are allowed to depend on types, but not conversely.

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

### Propositions as types

The second approach to reconciling type theory with logic
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
the dependent type constructors $\Sigma$ and $\Pi$.

In this case, the semantics involved is the more general _codomain fibration_ $p:C^\to\to C$, whose fibres are the [[slice categories]] $C/A$.  If we want to take the point of view of "proof irrelevance," meaning that we only care whether something is true rather than how many proofs it has, then we can think of the semantics as living in the "poset reflections" $pos(C/A)$ of these slice categories (in which all parallel morphisms are identified).  Note also that the $pos(C/A)$ is equivalent to the poset of subobjects of $A$ in the [[free exact completion]] of $C$, so this can also be regarded as doing "logic over type theory" with semantics valued in free exact completions.


## Syntactic categories and free models

There are two equivalent ways to describe formally the semantics of a given type theory (possibly with logic) in a category.  Essentially, the idea is that there is an [[adjunction]]

$$ type theories \quad \underoverset{Sem}{Syn}{\rightleftarrows} \quad categories $$

in which

* the right adjoint $Sem$ (semantics) assigns to a category its [[internal logic|internal type theory]] whose types and terms (and propositions, if present) are the objects and morphisms (and subobjects) of the category, while 

* the left adjoint $Syn$ (syntax) builds the [[syntactic category]] of a type theory, whose objects, morphisms, and subobjects are the types, terms, and propositions of the type theory.

Thus, if $T$ is a type theory and $C$ a category with corresponding structure, it is equivalent to give a structure-preserving functor $Syn(T) \to C$, or to give a translation of type theories $T\to Sem(C)$.  Either one is called a "model" of $T$ in $C$.  For more details on the construction of $Syn$, see [[context]], and for more details on $Sem$, see [[internal logic]].

By the way, it should be noted that there are various technical difficulties in making this precise.  For instance, categories of any sort form a 2-category (or something more, if they are higher categories themselves), so we have to make type theories into a 2-category as well.  Also, there is a bit of a mismatch in that *substitution* in type theory is usually "implicit," which implies that it is strictly associative, but the corresponding categorical operation of [[pullback]] is not generally strictly associative.  For this reason, various people have defined technical intermediaries between type theories and categories, which mostly boil down to a category equipped with a [[split fibration]] replacing its [[codomain fibration]].  These go by names like *comprehension category*, *category with attributes*, or *contextual category*.


# Syntax of type theory {#Syntax}

It's hard to give a universal definition of "a type theory," but the following very general setup covers most cases.  Note that in general, the following definitions are mutually [[recursion|recursive]].

* A **typing declaration** is something of the form $t:A$.  We say that $t$ is a **term** (of type $A$) and that $A$ is the **type**.  In some type theories, there is a fixed collection of allowable types, while in others the types are themselves terms belonging to some other type (often called $Type$).

* A **[[context]]** is a list of typing declarations, in which each term is a fresh variable (i.e. one not occurring to the left of its typing declaration).  If the list of types is not fixed, then one requires that each type occurring in a context be well-formed relative to the sub-context appearing to its left.  In other words, for $\Gamma, x:A$ to be a valid context, the judgment (see below) $\Gamma \vdash A:Type$ must be derivable.

* A **judgment** is something of the form $\Gamma \vdash \mathcal{J}$, where $\Gamma$ is a valid context.  Different type theories allow different things in the place of $\mathcal{J}$, but the most common are *typing declarations* and *equalities* between terms of the same type.  For example, the judgment
  $$ x:N, y:N \vdash x+y :N $$
  asserts that any two natural numbers have a sum, which is also a natural number.  Similarly, 
  $$ x:N, y:N, z:N \vdash (x+y)+z = x+(y+z) :N $$
  asserts that natural number addition is associative.

* A **rule** asserts that if some given list of judgments are valid, then so is another one of a specified form derived from them.  Of course, to be interesting such rules must contain "meta-variables" which range over contexts, types, or terms.  Rules are generally written in the following form:
  $$ \frac{\Gamma_1 \vdash t_1:A_1 \qquad \dots \qquad \Gamma_n \vdash t_n:A_n}{\Delta \vdash s:B}. $$
  This is to be read as a rule asserting that if $\Gamma_1 \vdash t_1:A_1$  through $\Gamma_n \vdash t_n:A_n$ are valid judgments, then so is $\Delta \vdash s:B$.

A given type theory is determined by its collections of types, judgments, and rules.  Rules can of course be classified in various ways; here are some of the most common.

## Structural rules

Structural rules say essentially that variables can be substituted, reordered, and ignored in appropriate ways.  For instance, there is an "exchange" structural rule:
$$ \frac{ \Gamma, x:A, y:B, \Delta \vdash ?}{ \Gamma, y:B, x:A, \Delta \vdash ?}.$$
which asserts that variables in the context can be reordered.  (In the presence of dependent types, there is a restriction here that $B$ cannot depend on $x$.)

Some type theories, such as those related to [[linear logic]], omit some of the structural rules, but most of the time the structural rules are taken for granted.

## Type-forming rules

Most of the most interesting rules involve forming new types.  For instance, we may want to assert that if $A$ and $B$ are types then so is $A\times B$.  It may not appear that we have a kind of judgment meaning "$A$ is a type," but we can solve this by treating every *type* as being itself also a *term* of a type such as $Type$ (which is sometimes written $*$).  Thus, for instance, the product-forming rule is written
$$\frac{\Gamma\vdash A:Type \qquad \Gamma \vdash B:Type}{\Gamma \vdash A\times B:Type}.$$
It then comes with attendant rules for forming terms of type $A\times B$, such as:
$$\frac{\Gamma\vdash A:Type \qquad \Gamma \vdash B:Type}{\Gamma, x:A, y:B \vdash \langle x,y\rangle : A\times B}$$
and for extracting the original terms out, such as
$$\frac{\Gamma\vdash A:Type \qquad \Gamma \vdash B:Type}{\Gamma, t:A\times B \vdash \pi_1(t):A} \qquad
\frac{\Gamma\vdash A:Type \qquad \Gamma \vdash B:Type}{\Gamma, t:A\times B \vdash \pi_2(t):B}
$$
and the obvious rules saying that $\pi_1\langle x,y\rangle = x$ and $\pi_2\langle x,y\rangle = y$ and $\langle \pi_1(t), \pi_2(t)\rangle = t$.

## Universes

Of course, this begs the question---what is the type of $Type$?  We don't strictly need it to have one---nothing says that everything has to be a term of some type.  But it is also sometimes convenient to write $Type = Type_0$ and introduce a hierarchy of additional "universes," so that $Type_0 : Type_1$, $Type_1:Type_2$, and so on.  A technique called "universe polymorphism" means that usually we can forget about the indices and just treat "$Type$" as a single entity to which everything belongs, unless we do perverse things to try to get paradoxes.

## Dependent types

As suggested above, we can have types which depend on terms, and type constructors which apply to these.  For instance, we can have a rule of dependent product formation:
$$\frac{\Gamma, x:A \vdash B(x):Type}{\Gamma \vdash \Pi_{x:A} B(x) : Type}
$$
Note that in the case when $B$ is independent of $x$, this includes a "function type" $A\to B$.  Similarly, we have dependent sums $\Sigma_{x:A} B(x):Type$, which in the non-dependent case include ordinary products $A\times B$.

## Propositions

As mentioned above, one way to deal with logic over type theory is to represent a proposition simply by a type, regarded as the type of all its proofs, or of all reasons why it is true.  A different way is to introduce a separate type $Prop$, perhaps living at the same "level" as $Type$, and allow propositions to depend on types, in the same way that types depend on types.  The same sorts of type constructors, but acting on propositions, then implement the logical connectives and quantifiers.  For instance, the analogue of dependent product formation becomes a rule of universal quantification:
$$\frac{\Gamma, x:A \vdash B(x):Prop}{\Gamma \vdash \forall_{x:A} B(x) : Prop}
$$
and similarly $\Sigma$ becomes $\exists$.

In either case, asserting that a proposition is "true" is the same as asserting that it is [[inhabited type|inhabited]], i.e. exhibiting a term of that type.  Thus, we don't need to introduce a new kind of judgment for logic; we can continue to use the same sorts of judgments of the form "$t$ is a term of type $A$," only now $A$ can be a proposition and $t$ a proof or reason why $A$ is true.  In particular, the *axioms* of a logical theory can also be formulated as term-forming rules.

## Additional dependencies

It is also possible to have types depending on propositions, propositions depending on propositions, kinds depending on types, etc. etc.  See, for instance, [[pure type system|pure type systems]] and the [[calculus of constructions]].


# Type-theoretical foundations

From a [[foundations|foundational]] point of view, type theory can also be regarded as the language in which mathematics is written.  This has several aspects, notably *syntax* (the language) and *semantics* (what it means).

## Syntax of type-theoretical foundations

At the most basic level, what we do when we do mathematics is *manipulate symbols according to specified rules*.  Just as in chess the rules state that a knight moves like *so* and not like *so*, in mathematics the rules state that a quantifier can be eliminated like *so* and not like *so*.  The actual rules of the game of mathematics are extremely complicated, but the idea of foundations is to derive them from a much simpler list of fundamental rules.  Type theory says that these fundamental rules are a *calculus of terms*, and that each term comes equipped with a *type*.  Thus, the rules define one or more *types*, and one of the judgments one can make (that is, one of the "moves" of the game) is of the form "$t$ is a well-formed term of type $A$.  This corresponds to the syntax described above.

If we include enough type constructors, then we can use type theory as a foundation for much of mathematics.  Instead of building mathematical objects out of [[sets]] as in foundational set theories such as [[ZFC]] or [[ETCS]], we build mathematical objects out of types.  The presence of dependent types, with sums and products, is usually quite convenient for this purpose.  That is, instead of defining a group to be a set equipped with (among other things) a function $G\times G\to G$, we could interpret a group as a *type* $G$ equipped with (among other things) a *term* $m(x,y):G$ with free variables $x:G$ and $y:G$.

## Type theory versus set theory

Alternately, we could change our terminology so that what we have been calling "types" are instead called "sets."  However, in order for this to accord with the common usages of "set", we need to include enough type constructors that our types can mimic the behavior of sets, and in particular be "extensional" and have "quotient types."  See the section on "Extensional vs Intensional" type theory, below.

On the other hand, type theory is, among other things, a convenient language for formulating first-order logical theories, and among these theories are foundational set theories such as [[ZFC]] and [[ETCS]].  For instance, ZFC has two types $Set$ and $Prop$, proposition-forming rules saying that if $x:Set$ and $y:Set$ then $(x=y):Prop$ and $(x\in y):Prop$, the usual rules of logical inference and a [[ZFC|collection of axioms]].  The same with [[ETCS]], which it is convenient to write with three types $Set$, $Function$, and $Prop$.

Especially when we intend a theory like ZFC or ETCS as a foundation for all of mathematics, it is convenient to call the type-theoretic language in which these theories are written the "meta-language" or "meta-theory," while ZFC/ETCS is the "object language" or "object theory."  On the other hand, for a more complex and powerful type theory with many type-constructors, which is suitable to serve as a foundation for mathematics itself, it is natural to say that this type theory is *itself* the *object-theory* in a meta-theory having meta-types such as $Type$, $Term$, and $Judgment$.

Thus, words like "type" and "set" and "class" are really quite fungible.  This sort of level-switch is especially important when we want to study the mathematics *of* type theory, i.e. the mathematical theory of manipulating symbols according to the rules of type theory, analogous to the mathematical theory of moving pieces around on a chessboard according to the usual rules.  When we study type theory in this way, we are *doing* mathematics, just like when we're doing group theory or ring theory or whatever.  It's just that our objects of study are called "types", "terms", and so on.  However, what we do in this mathematical theory *can*, like any other area of mathematics, be formalized in any particular chosen foundation, be it ZFC or ETCS or a type theory at a higher level.  Now the type theory is itself the "object-theory" and ZFC is the "meta-theory"!

Here are some blog discussions about the difference between type theory and set theory:

* [one](http://golem.ph.utexas.edu/category/2009/09/towards_a_computeraided_system.html#c026984)
* [two](http://golem.ph.utexas.edu/category/2009/10/syntax_semantics_and_structura.html#c028459)


## Semantics of type-theoretical foundations

Now, intuitively, we generally think of a type $A$ as denoting some "collection" of "things", and a term $t:A$ as indicating a "particular one" of those things.  In order for this to make sense, the type theory has to exist in some metatheory (which might or might not be formalized) having a notion of "set" to specify the relevant "collections of things".  In particular, there must be a set of types, and for each type there is a set of terms which can be judged to be of that type.  The judgment rules for propositions then become the study of formal logic; we say that a proposition is "provable" or is a "theorem" if it can be judged to be true.

Now, a *model* of this theory (in the category of sets) assigns a set $[A]$ (in the meta-theoretic sense) to every type $A$ and a function of appropriate arity to every term, in a way so that the rules and axioms are satisfied.  Thus, for instance, a model of Peano arithmetic consists of a set $[N]$, an element $[0]\in [N]$, a function $[s]\colon [N]\to[N]$, and so on.  Likewise, a model of the type theory of ZFC (here the levels get confusing) consists of a set $[Set]$, a function $[{\in}]\colon [Set]\times [Set] \to [Prop]$, and so on.

One can then prove, under certain hypotheses, various things about the relationship between syntax and semantics, such as:

* The *Soundness Theorem*: if $\varphi$ is a proposition which is provable from the axioms of a theory, then the corresponding statement $[\varphi]$ in any model is actually true (in the sense of the metatheory).  Equivalently, if a theory has at least one model, then it doesn't prove a contradiction.
* The *Completeness Theorem*: if $[\varphi]$ is true in every model of a theory, then $\varphi$ is provable in that theory.  Equivalently, if a theory doesn't prove a contradiction, then it has at least one model.
* The (first) *Incompleteness Theorem*: if a theory doesn't prove a contradiction, then there exist statements $\varphi$ such that neither $\varphi$ nor $\not\varphi$ is provable in the theory.
* Corollary to the completeness and incompleteness theorems: if a theory doesn't prove a contradiction, then it has more than one model.

The "certain hypotheses" is where we get into the difference between *first-order* and *higher-order*.  We say that a type theory is *higher-order* if it involves type constructors such as function-types $B^A$ (intended to represent the "type of all functions $A\to B$") or power-types $P A$ (intended to represent the "type of all subtypes of $A$).  Otherwise it is *first-order*.  (We have to deal with $Prop$ specially in first-order logic.  If we actually have a type $Prop$, then the theory should be higher-order, since $Prop \cong P 1$; thus in first-order logic we take $Prop$ to be a "kind" on the same level as $Type$, which doesn't participate in type operations.)  We say "second-order" if we never iterate the power-type operation.

+-- {: .query}
I don\'t buy your argument that $Prop$ must be treated specially; perhaps I don\'t understand what you\'re saying, but I\'ll pretend that I do.  First, I don\'t see the relevance of your premise, that $Prop$ makes things higher-order because it is a power type.  You might as well say that $1$ makes things higher-order because $1 \cong P 0$.  What really makes things higher order is the ability to form *arbitrary* power types or function types, not the existence of one or two special cases.  And second, I don\'t agree with the conclusion, that $Prop$ can\'t participate in type operations.  It\'s true that many type theories *do* treat $Prop$ specially and forbid its participation in type operations, but allowing it to participate in first-order type operations like $\times$ and $+$ is not going to make things higher order.  Conversely, $Prop \cong 1 + 1$ in some type theories, in which case you can hardly stop it from participating in type operations!  ---Toby

[[Mike Shulman]]: This seems to be basically a dispute about the meaning of "higher-order"?  To me, for something to be first-order, it should be interpretable in a [[Heyting category]], which does not necessarily have a [[subobject classifier]] (though it does, as you point out, have a power object for $0$).  I also expect that the presence of $Prop$ as a type is sufficient to make the Completeness Theorem fail, as described in the next paragraph.  Probably "participate in type operations" is the wrong claim to be making, rather the claim should be something along the lines of $Prop$ being a kind, rather than a type, i.e. we don't have $Prop:Type$, or at least not $Prop:Type_0$.
=--

The Soundness Theorem is true for all theories, but *the Completeness Theorem is true only for first-order theories*.  The Incompleteness Theorem as stated above is true for higher-order theories, but the corollary fails since the completeness theorem does.  In particular, a higher-order theory can sometimes be *categorical* in the logician's sense: having exactly one model (at least, up to isomorphism).  The second-order version of Peano Arithmetic has this property.  (At this level, there is little fundamental difference between first-order and higher-order theories; they each have advantages and disadvantages.  However, when we move up to the metalevel and talk about the term calculus itself, we always get a first-order theory.  This is why some people believe that first-order logic is the only truly "foundational" logic.)

## Term models

One usually proves the Completeness Theorem by building a "tautological" model out of the theory itself.  That is, for each type $A$ we simply take the set $[A]$ to be the set of terms of type $A$ with no free variables (or "ground terms").  However, without modification, this naive idea fails for two reasons.

First of all, there might not be enough ground terms.  Some of the axioms of the theory might assert that there exists something with some property, without there being a corresponding term constructor actually producing something with that property.  This is obviously the case for the usual version of ZFC, which has no term constructors at all (hence no ground terms at all!) but lots of axioms that assert the existence of things.  This problem is easily remedied, however, by introducing new constant terms or term constructors into the language.

The second problem is that we may not know how to define all the necessary relations on the ground terms in order to have a model.  Suppose, for instance, we have a couple of ground terms $t_1$ and $t_2$ in some augmented version of ZFC; how can we tell whether $t_1\in t_2$ should hold in our tautological model?  Certainly if the axioms of the theory imply $t_1\in t_2$, then it should hold, and if they imply $t_1\notin t_2$, then it shouldn't, but they might not imply either one.  The usual way to remedy this is to enumerate all such statements and one by one decide arbitrarily whether to make them true or false in the model we're constructing.

This works, but the model we get (though small, even countable, and concrete) isn't really *canonical*; we had to make a bunch of arbitrary choices.  In the case of Peano Arithmetic, we can avoid introducing new constant terms and obtain a model which is "canonical" and in fact the "smallest" in some sense: it consists of the terms $s(s(\dots(s(0))\dots))$, which can of course be identified with "the" natural numbers in the meta-theory.  But this doesn't work for most other theories.  Suppose, for instance, that we augment ZF with term constructors for all of its existence axioms.  Let $\varphi$ be a sentence independent of ZF; then our term-constructor for the axiom of separation gives us a term $\{\emptyset | \varphi\}$.  Does the relation $\emptyset \in \{\emptyset | \varphi\}$ hold in the term model?  We have to make an arbitrary choice.

(It *is* true that any *given* model of ZF contains a [[minimal model of ZF|minimal model]], i.e. a smallest [[transitive set]] which is a model of ZF.  However, different models of ZF have different minimal models, and the construction of the minimal model is not "syntactic" in this sense.)

The slicker categorial approach described above using categories of [[contexts]] does produce a really canonical model, but only with an expanded notion of "model": instead of each $[A]$ being a set, we take it to be an object of some fixed category $\mathcal{S}$ with enough structure.  We can then build a much more "tautological" model because we have the freedom to build the category $\mathcal{S}$ along with the model.  In the resulting model, the true statements are *precisely* the statements provable in the theory, and it's even initial among all models of the theory in the appropriate sort of category.


# Extensional vs Intensional

There is an important distinction between *extensional* type theories and *intensional* ones.  The meanings of these words is probably clearest when dealing with function types, such as an exponential $Y^X$, but also arises in respect to quotient types and identity types.

## Extensional and intensional function types

A function type $Y^X$ is said to be **extensional** if whenever $f,g\colon X\to Y$ are functions such that $f(x)=g(x)$ for all $x\in X$, then in fact $f=g$ as elements of $Y^X$.  This clearly corresponds to the modeling of function types by [[function sets]] in the set-theoretic semantics, or more generally by [[exponential objects]] in the categorical semantics discussed above.  The uniqueness clause of the defining assertion of an exponential object, i.e. that any map $Z\times X\to Y$ factors through a *unique* map $Z\to Y^X$, precisely models this "extensionality" property.  Thus, the standard categorical semantics is most closely allied to type theories which have such an "extensionality" axiom.

By contrast, suppose that $X$ and $Y$ are interpreted by data types in some programming language, and $Y^X$ is interpreted by some type of computable functions from $Y^X$.  Of course, many differently coded functions can have the same "extensional behavior," i.e. the same output for any given input, but we may still want to distinguish between these functions because they may not share other properties (such as running time or complexity).  Thus, this type $Y^X$ is not extensional---equality of functions, as elements of $Y^X$, is "implementation-sensitive," a finer measure than mere equality on all inputs.  We say instead that these function types are **intensional**.

In type theory, extensional function-types generally come with both a "$\beta$-rule," which specifies the computational behavior of a $\lambda$-abstraction (i.e. $(\lambda x. t)(y) = t[y/x]$), and an "$\eta$-rule," which specifies that a $\lambda$-abstraction is determined by its behavior (i.e. $f = (\lambda x. f(x))$).  In the categorical semantics, the first specifies the existence of factorizations, while the second requires them to be unique.  In intensional type theory, we generally keep the $\beta$-rule (it is certainly natural from a computational standpoint) but discard the $\eta$-rule.  Thus, one natural sort of semantics for intensional type theory is valued in a category with "weak exponentials," i.e. objects which satisfy the existence but not uniqueness property of an exponential (and similarly for dependent type theory with $\Pi$-types and weak [[dependent product]]s).

## Quotient types and exact completion

Intensional type theory is also popular among adherents of [[constructive mathematics]] and especially [[predicative mathematics]], because of its computational content.  [[Per Martin-Lof|Per Martin-Löf]]'s original [[dependent type theory]] is often presented from this perspective.

When viewing intensional type theory as a foundation for mathematics (rather than, say, a syntax for reasoning about computer programs), it is natural to view the types as representing [[presets]], rather than sets.  This is in line with the classical constructivist viewpoint that "a set is defined by a collection of things together with an equality relation."  Note that in intensional type theory, the "equality" between terms is free to be the "syntactic" equality, which is entirely computable and preserved by everything in sight.  In particular, if we adopt the viewpoint of [[propositions as types]], then "the axiom of choice is trivially valid" for functions between types (i.e. presets) since to assert that something exists is to give an element of a sum type, which is exactly to give a witness and thereby a way to choose such a thing.

If we then define "sets" to be types equipped with equality relations (sometimes called [[setoids]]), then the sets will have more familiar properties, such as existence of extensional exponentials (obtained by equipping the intensional exponentials with an extensional equality relation), as well as the existence of [[quotient sets]].  (The existence of quotient types is often assumed in extensional type theory, but not in intensional type theory.)  In categorical terms, the [[syntactic category]] of an intensional type theory has only weak exponentials (resp. dependent products), but that is sufficient to ensure that its [[free exact completion]] has actual exponentials (resp. dependent products).  Note also that free exact completions always also validate [[COSHEP]], since every object of the starting category (here the category of types) is projective.  This matches the above observations about the axiom of choice.

## Identity types

+-- {: .query}
Quick comment:  Even in internal type theory, one needs identity types to validate COSHEP.  Type theory without identity types is very strange (the category of contexts may not have all pullbacks, and not every morphism need be a display morphism).

[[Mike Shulman]]: I'm not sure that that's so strange.  At least, not to the type theorists.  (-:  Categorically, I think of display maps as being fibrations in some model-category-type structure, which makes sense to me, although in semantics valued in an honest higher-category I would expect every morphism to be equivalent to a display morphism.

Actually, don't you need *extensional* identity types in order to get all pullbacks and make every morphism display?  I think intensional identity types just mean that you can factor every morphism through a display morphism which is "equivalent" in some sense, i.e. you have the [[identity type weak factorization system]].

And I didn't know that about COSHEP, why is that?  Isn't it true that all types are projective, at least in the propositions-as-types logic, since to assert that something exists is to give a construction of it?  Or are you saying that you need identity types in order to even construct the category of setoids, since you need the category of types to have at least weak finite limits?

_Toby_:  I mean that you need identity types in order to have the free functor from presets to sets that allows every type (preset) to be interpreted as a set.  So every set is a quotient (in a sense) of a preset, and every preset is projective (in a sense), but it\'s not a projective *set*.  We merely have that the free set on that preset is projective *if* it exists.

I really meant to work out a clean example of such a type theory on [my personal web](tobybartels:HomePage), but I never did (so you don\'t need to look there).

PS:  You\'re right about the display maps; that part\'s not so strange.  Maybe it\'s not strange at all, but Martin-L&#246;f (at least) considers identity types indispensible (and they are, in his framework, for $W$-types to work).
=--

(to be written...)

## Higher-categorical semantics

(to be written...)

# Particular type theories

The following particular type theories are important enough to (potentially) have pages of their own.

* [[simple type theory]]
* [[simply typed lambda calculus]]
* [[Martin-Lof dependent type theory|Martin-Löf dependent type theory]]
* [[pure type system]]
* the [[calculus of constructions]]
* the [[internal logic]] of various kinds of categories, including the [[Mitchell-Benabou language]] of an [[elementary topos]]
* the [[internal logic of a 2-topos]]
* the [[internal logic of an (∞,1)-topos]]


[[!redirects dependent type theory]]
[[!redirects dependent type theories]]
[[!redirects type theories]]
