# Idea

Type theory is a branch of mathematical [[logic]] which studies elements of varying _types_, or _sorts_, rather than elements of a single fixed sort.  Type theory is distinguished particularly by the importance of [[context]] in the specification of terms and formulas, and has close links to the [[internal logic]] of categories.

# An introduction for category-theorists

One way to look at type theory, from the point of view of a category theorist, is as a _syntax for describing the construction of objects and morphisms in a category_.  The [[syntax|syntactic]] constructs corresponding to objects and morphisms are called _types_ and _terms_, respectively.  The types correspond to objects (with various subtleties), while the terms denote morphisms by using _variables_ to indicate domains.  For example, given terms $f(x)$ and $g(y)$ with one free variable each, representing morphisms $[f]$ and $[g]$, the term $g(f(x))$ represents the morphism $[g]\circ [f]$.

What sorts of syntactical constructions you allow on types and terms corresponds to the structure of the category in which the [[semantics]] is intended to occur.  For example, if our semantic categories have binary products, then the syntax of the type theory includes a _type constructor_ $\times$ allowing us to build a new type $A\times B$ from two given types $A$ and $B$.  It will also have _term constructors_ allowing us to build, for example, a term $\langle a,b\rangle$ of type $A\times B$ from any given terms $a$ of type $A$ and $b$ of type $B$.  Note the great advantage of the type-theoretic formalism: the notation (and thought process) can be very set-theoretic, but because the terms $a$ and $b$ can denote morphisms with arbitrary domain (by choosing their free variables appropriately), we are really describing the full universal property of a cartesian product.

An important extension of type theory involves _dependent_ types: types which are a "function" of the _elements_ of some other type.  For instance, the type $D(m)$ of "days of the month" is a function of the element $m$ of the type $M$ of months, since different months have different allowable collections of days.  Syntactically, in addition to the existence of dependent types, one often allows constructions on them such as _dependent sums_ $\Sigma_{x:A} B(x)$ (regarded as the "type of pairs" $(x,y)$ such that $x\in A$ and $y\in B(x)$) and _dependent products_ $\Pi_{x:A} B(x)$ (regarded as the "type of functions" $f$ such that for any $x\in A$, we have $f(x)\in B(x)$).  Semantically, a type $B(x)$ depending on an element $x$ of type $A$ is represented by a morphism $B\to A$, thought of as an $A$-indexed family of objects; each $B(x)$ is supposed to be the fiber over $x$.  Then dependent sum and product are interpreted by the left and right adjoints to the [[pullback]] functors $f^*:E/Y\to E/X$ along a morphism $f:X\to Y$; the left adjoint always exists, while the right adjoint exists in any [[locally cartesian closed category]].

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
this is called the "propositions as types" paradigm.
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

[[!redirects dependent type theory]]
[[!redirects type theories]]