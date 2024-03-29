# Initiality Project - Overview

This page is part of the [[Initiality Project]].

Here is a proposed slate of choices to make regarding type theories, presentations, definitions, and proof structure.  ("I" refers to [[Mike Shulman]].)  This is only a first proposal and may change; discussion is underway at the nForum [here](https://nforum.ncatlab.org/discussion/9160/initiality-project-plans/).

* table of contents
{: toc}

## The semantics
 {#Semantics}

Of the various ways to describe a [[categorical model of dependent types]], I suggest to use *categories with families*, presented in the style called by [[Steve Awodey|Awodey]] a [natural model](https://arxiv.org/abs/1406.3219), but fully algebraically.  That is, for us a category with families is a (small) [[category]] $C$ together with two [[presheaves]] $Tm,Ty \in [C^{op},Set]$ and a morphism $Tm \to Ty$ that is *algebraically representable* (or, one might say, "represented"): it is equipped with a *function* assigning to each morphism $A:y \Gamma \to Ty$, where $\Gamma\in C$ and $y$ denotes the [[Yoneda embedding]], an object $\Gamma.A\in C$ and a [[pullback square]]
$$\array{ y(\Gamma.A) & \to & Tm \\ \downarrow &&\downarrow \\ y\Gamma & \xrightarrow{A} & Ty. } $$

This is equivalent to the usual notion of category with families (and thereby also to the usual notion of "category with attributes", hence also to discrete or full split comprehension categories).  But, as noted by Awodey, focusing attention on $Tm$ and $Ty$ as objects of $[C^{op},Set]$ has the advantage that the additional structure corresponding to the rules of a type theory are also naturally formulated in $[C^{op},Set]$.  For instance, if $Ty^2$ denotes the domain of the local exponential $(Ty\times Ty \to Ty)^{(Tm\to Ty)}$, then the rules of $\Sigma$-formation and $\Pi$-formation correspond semantically to giving a morphism $Ty^2 \to Ty$.

Note also that $Ty^2$ can be described in the internal extensional type theory of $[C^{op},Set]$ by the context $(A:Ty, B:Tm(A) \to Ty)$; thus $[C^{op},Set]$ is a sort of "semantic [[logical framework]]" for structuring $C$.  My inclination right now is that while we can rely on this for intuition and explanation, we should also formulate all this structure precisely in traditional category-theoretic language, to avoid any appearance of circularity in our construction of categorical models of dependent type theory.

A *morphism of categories with families* is a functor $F:C\to D$ together with a commutative square in $[C^{op},Set]$:
$$\array{ Tm_C & \to & F^*(Tm_D) \\ \downarrow & & \downarrow \\ Ty_C & \to & F^*(Ty_D) }$$
which strictly respects the chosen pullback squares in an appropriate way.  This defines the category $CwF$ in which we hope to construct an initial object.


## The type theory

I suggest to start with a type theory containing only $\Pi$-types.  This seems the simplest situation where we will have to deal with all the basic issues.  We can then add additional structure as desired.

### Axioms

Note that this type theory is completely empty unless we also assert some axioms.  Ideally, I would like the "initiality theorem" to really be a "freeness theorem", saying that the syntactic category of a type theory with axioms is freely generated by those axioms.  Of course, particular axioms can just be added as rules to a theory, but such a general freeness theorem should be parametric over all possible axioms.

Since in a dependent type theory, each axiom can involve previous axioms in its type, it seems that the general semantic formulation will have to involve some kind of a "cell complex" in the category $CwF$.  However, we can leave this to the future for the moment and concentrate on the inductive clauses for interpreting the basic rules of $\Pi$-types.

### Raw syntax

I propose to use syntax with named variables, quotiented by $\alpha$-equivalence.  My reason is that our goal is expositional and sociological, and named variables keep the syntax as close as possible to what "users" of type theory are familiar with.  Since we are humans writing for humans to read, I don't want to deal explicitly with de Bruijn indices, and neither do I want to pretend that we are using de Bruijn indices when we aren't *really* using them.

If this proposal is adopted, then the raw terms for our simple type theory will be inductively generated by:

* Every variable $x$ is a term.
* If $A,B$ are terms and $x$ is a variable, then $\Pi(x:A) B$ is a term.
* If $A,B,M$ are terms and $x$ is a variable, then $\lambda(x:A.B)M$ is a term.
* If $A,B,M,N$ are terms and $x$ is a variable, then $App^{(x:A)B}(M,N)$ is a term.

We define $\alpha$-equivalence which renames bound variables as usual.  Note that the variable $x$ in $\Pi(x:A)B$ scopes only over $B$, in $\lambda(x:A.B)M$ it scopes only over $B$ and $M$, and in $App^{(x:A)B}(M,N)$ it scopes only over $B$.  Capture-avoiding substitution is likewise defined as usual.  Our partial interpretation will be defined recursively over the above inductive definition of terms, and proven to respect $\alpha$-equivalence.


### Bidirectionality

Following Streicher, all our terms are fully (or at least "sufficiently") annotated.  For instance, we write $App^{(x:A)B}(M,N)$ rather than just $App(M,N)$.  (It is, at best, unclear whether any less than fully annotated syntax can be used in an initiality theorem without preprocessing that is tantamount to annotating it.)

In particular, this means that given $\Gamma$ and $t$, if $\Gamma \vdash t:A$ can be derived for any value of $A$, then there is a canonical such $A$ that can be deduced syntactically, or *synthesized*, from $\Gamma$ and $t$.  For instance, if $App^{(x:A)B}(M,N)$ has any type, then it must have the type $B[N/x]$.  On the other hand, the conversion rule implies that $App^{(x:A)B}(M,N)$ must also have any type that is judgmentally *equal* to $B[N/x]$.

Type theorists have a standard technique for distinguishing these two situations, known as [[bidirectional typechecking]].  Instead of one judgment $\Gamma\vdash t:A$, we have two typing judgments:

* $\Gamma \vdash t \Rightarrow A$: in context $\Gamma$ the term $t$ *synthesizes* the type $A$.  Here $A$ is, if it exists, uniquely determined by $\Gamma$ and $t$: it is an "output" to their "inputs".
* $\Gamma \vdash t \Leftarrow A$: in context $\Gamma$ the term $t$ *checks against* the type $A$.  Here $\Gamma$, $t$, and $A$ are all "inputs" and the only "output" is the truth value of whether the typecheck is valid.

There are various advantages of bidirectional typechecking, including:

1. In at least some cases, it permits a formulation of type theory in which only normal forms exist.
1. In at least some cases, it allows omission of annotations, e.g. an un-annotated abstraction $\lambda x.M$ cannot synthesize a type, but it can check against a $\Pi$-type $\Pi(x:A) B$.
1. In at least some cases, it makes it easier to incorporate [[η-expansion]] into an equality-checking algorithm.
1. In at least some cases, it makes derivations of judgments unique, or at least canonical.
1. In at least some cases, it isolates the use of judgmental equality during typechecking in one particular "mode-switching" rule:
   $$ \frac{\Gamma \vdash t \Rightarrow A \qquad \Gamma \vdash A\equiv B}{\Gamma \vdash t \Leftarrow B} $$

(Experts, feel free to add more.)  It is unclear at present whether any of these advantages are relevant to categorical semantics, but by using a bidirectional framework we are better placed to take advantage of them if they do become relevant.  More importantly, it seems to me that the natural structure of the semantic interpretation, as suggested by [[Peter Lumsdaine]] (see below), matches the syntactic bidirectional picture quite closely, and it may be clarifying to make that analogy more precise.

Since all our terms are fully annotated, all of our formation, introduction, and elimination rules can synthesize their types.  However, their *premises* usually involve *checking* their subterms against appropriate types, so the above mode-switching rule gets applied a lot (it is the only way, in our system, to derive a checking judgment).  This might be an issue to want to optimize away in an implementation, but for our semantic purposes it seems irrelevant.

For instance, here are the formation, introduction, and elimination rules for $\Pi$-types:

$$
\frac{\Gamma \vdash A \, type \qquad \Gamma, x:A \vdash B\,type}{\Gamma \vdash \Pi(x:A) B \, type}
$$

$$
\frac{\Gamma \vdash A \, type \qquad \Gamma, x:A \vdash B\,type \qquad \Gamma \vdash M \Leftarrow \Pi(x:A) B \qquad \Gamma \vdash N \Leftarrow A}{\Gamma \vdash App^{(x:A)B}(M,N) \Rightarrow B[N/x]}
$$

$$
\frac{\Gamma \vdash A \, type \qquad \Gamma,x:A \vdash B \,type \qquad \Gamma,x:A \vdash M \Leftarrow B}{\Gamma \vdash \lambda(x:A.B)M \Rightarrow \Pi(x:A) B}
$$

(Note that the "is a type" judgment $\Gamma \vdash A\,type$ is not bidirectional.  With Russell universes we could consider making it so.)

The "hypothesis" rule is that a variable in the context synthesizes its assumed type:

$$\frac{(x:A) \in \Gamma}{\Gamma \vdash x \Rightarrow A.}$$

In implementations of bidirectional typechecking, the equality judgments $\Gamma \vdash s\equiv t : A$ and $\Gamma \vdash A \equiv B \, type$ are sometimes made bidirectional as well.  But at the moment, I don't think there will be is any benefit to us in doing likewise.  In particular, we would like our setup to be general enough to encompass type theories whose judgmental equality is "poorly behaved", e.g. undecidable, such as those with an [[extensional type theory|equality reflection rule]].  Thus the equality judgments should have primitive rules asserting reflexivity, symmetry, transitivity, and congruence properties.

Streicher also includes a basic judgment for equality of *contexts*.  Peter [suggests](https://nforum.ncatlab.org/discussion/8904/a-communal-proof-of-an-initiality-theorem/?Focus=71254#Comment_71254) that that isn't necessary, because

> any contexts that *would* be judgementally equal in the system with that judgement still end up canonically end up judgementally isomorphic, by the substitution that consists of not renaming variables.

I'm inclined to follow Peter's suggestion here, but am open to counterarguments.

Streicher also includes a number of explicit primitive rules involving things like validity of contexts and type-preservation by substitution.  I'm not sure whether these are necessary or not; it seems that maybe by presenting our type theories in "the usual way" we should always be able to ensure that substitution is admissible, even for type theories that are "ill-behaved" in other ways (such as equality reflection).  But maybe there are good reasons to include these rules explicitly?


## The proof

The following proposal for the inductive structure of the argument is based on Streicher's original approach, with a modification suggested by [Peter Lumsdaine](https://nforum.ncatlab.org/discussion/8904/a-communal-proof-of-an-initiality-theorem/?Focus=71254#Comment_71254), and further tweaks to incorporate bidirectionality and build in naturality using the natural-models technology.

### The partial interpretation

Given a finite set of variables $V = \{x_1,\dots,x_n\} \subseteq Var$, the *presheaf of environments* for $V$ is $Tm^V$.  We will define, by structural induction on any term $t$, and any any finite set $V$ of variables, the following partial morphisms of presheaves.

1. $\llbracket t \rrbracket ^V_{type} : Tm^V \rightharpoonup Ty$.
1. $\llbracket t \rrbracket ^V_{\Rightarrow} : Tm^V \rightharpoonup Tm$.
1. $\llbracket t \rrbracket ^V_{\Leftarrow} : Tm^V \times Ty \rightharpoonup Tm$ such that the composite $Tm^V \times Ty \rightharpoonup Tm \to Ty$ is the second projection.

In fact, the third of these is not actually inductive at all: it is simply a semantic counterpart of the bidirectional mode-switching judgment.  We define $\llbracket t \rrbracket ^V_{\Leftarrow}$ to be the domain restriction of
$$ Tm^V \times Ty \xrightarrow{pr_1} Tm^V \overset{\llbracket t \rrbracket ^V_{\Rightarrow}}{\rightharpoonup} Tm $$
to the equalizer of
$$ Tm^V \times Ty \xrightarrow{pr_1} Tm^V \overset{\llbracket t \rrbracket ^V_{\Rightarrow}}{\rightharpoonup} Tm \to Ty $$
and the restriction of the second projection $Tm^V \times Ty$ to its domain.

The other inductive clauses of the partial interpretation should precisely mirror the bidirectional rules of our type theory, using recursive calls to the above three operations as counterparts of the three syntactic judgments $\Gamma \vdash A\,type$, $\Gamma \vdash t\Rightarrow A$, and $\Gamma \vdash t\Leftarrow A$.  Note, though, that at this point this is only an analogy: we are simply inducting over the raw term structure of $t$, not making any actual reference to these judgments.

This suggestion incorporates the innovation proposed by [Peter](https://nforum.ncatlab.org/discussion/8904/a-communal-proof-of-an-initiality-theorem/?Focus=71254#Comment_71254) over Streicher's proof of taking the interpretation of the context $\Gamma$ as an *input* to the partial intepretation functions rather than an output (see in particular his point (7)).  The elements of the presheaf $Tm^V$ at some object $X\in C$ are what Peter calls "environments" for $t$.  Note that we do not require that $V$ contain all free variables occurring in $t$, but if it omits some then the partial interpretation morphisms should turn out to have empty domain.

I have also reformulated the interpretation function to "put naturality into the goals of the original induction" as suggested by Peter in his point (8), by directly defining partial morphisms in the "semantic logical framework" $[C^{op},Set]$.  This has the additional advantage that in writing down the inductive clauses we can refer directly to the natural-models formulation of the corresponding structure on $C$, as sketched [above](#Semantics).


### Totality of the interpretation

Although the partial interpretation functions sketched above incorporate a number of "tweaks" to make it more pleasing, in fact it was already the short part: Streicher does it in only 5 pages.  (His pages are very short, so this isn't actually very much, plus his type theory is more complicated.)  The long part is proving that these interpretation functions are total on derivable judgments; this takes Streicher 40 pages.

The outline should be the same as in Streicher's proof and Peter's proposal:

1. Prove by induction on raw terms that the partial interpretation functions take syntactic substitution (including weakening) to semantic substitution (restriction in the presheaves $Tm$ and $Ty$).  This takes Streicher 17 pages.

1. Prove by induction on derivations that the partial interpretation functions are total on derivable judgments.  This takes Streicher 20 pages.

### Loose ends

To complete the proof of initiality after this, it remains to:

1. Construct the term model.  This takes Streicher 12 pages.

1. Show that the above interpretation assembles into a morphism in $CwF$ from the term model to $C$.  As far as I can tell, Streicher doesn't actually do this, he just claims that it can be done.

1. Show that this morphism is unique.  Streicher doesn't actually do this either.

category: Initiality Project