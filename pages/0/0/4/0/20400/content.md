
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Proto CLF is a work-in-progress [[proof assistant]] design combining ideas from [[Nuprl]], [[LF]], and [[decidability|undecidable type checking]]. "CLF" abbreviates "Computational Logical Framework". So far, it's just Matt Oliveri's unpublished plans and metatheory development, but information may appear here.

### Motive

The motivation for CLF is to try and combine the convenience of [[type theory|type systems]] with the flexibility of [[certified programming|program verification]], and make the resulting style of correct program construction applicable to mathematics in a general way.

In most typed computational languages—even those with rather strong type systems, like the [[dependent type theory|dependent type systems]] of [[Coq]] and [[Agda]]—there is a distinction between types and program specifications. A specification should

* constrain the computational behavior of conforming [[terms]], and
* not constrain the way this behavior is implemented.

[[type|Types]] typically constrain both behavior and implementation. Intuitively, this is because types are typically implemented using elaborate [[syntax]] checks, so they constrain behavior *by* constraining implementation.

A *program logic* provides predicates and proof rules about programs, and this provides an adequate approach to specification and verification of computational behavior. The requirement to satisfy a predicate doesn't constrain the way a program is implemented because the syntax rules for forming a program don't take into account any predicates the programmer may hope the program to satisfy. This is the sense in which program verification is more flexible than syntactic typing.

Using [[propositions as types]], many dependent type systems support specifications, in addition to types. But with the restriction to syntactic type checking, types and specifications remain distinct notions in practice.

By taking types to denote (certain) [[PER]]s on terms, Nuprl provides an [[intrinsic and extrinsic views of typing|extrinsic]] notion of type that subsumes program specifications. So Nuprl has a type system, and its types provide the flexibility of program verification; but it seems that Nuprl doesn't provide the convenience of a type system with a type checking algorithm.

From a naive perspective, it can't be done. Type checking Nuprl would be undecidable, but more importantly, it would require automatically coming up with proofs of true mathematical statements, and there's no good way to do that.

But that just means there needs to be additional machinery for formal proofs and practical proof checking. The question is then whether the formal proof machinery is as convenient, for developing correct programs, as type checking. The answer, for Nuprl's proof system, is supposedly "no". CLF will try to do better, by checking proof terms in a manner similar to dependent type checking.

### Method

CLF is planned to combine a semantics similar to that of Nuprl with a language of proof terms similar to that of [Cedille](https://cedille.github.io/). (Cedille is actually the latest in a series of dependent type systems (co)designed by Aaron Stump in which the meaning of equality pertains to realizers, not proof terms.)

The terms that the CLF type system is about are called "[[realizers]]". (Since its Nuprl-inspired PER semantics is a term realizability model.) The proof terms would be an *additional* class of terms. In the case of "obviously-well-typed" programs, the tree structures of the realizers and proof terms should be nearly isomorphic, so the system will resemble a typical syntactic type checker. In general, proof terms have additional information not present in realizers. This is the information that is needed for proof/type checking, but is not part of the computational content of the witness/element.

CLF types only depend on realizers, never proof terms. So to handle proof checking rules analogous to certain rules of dependent type systems, a realizer needs to be extracted from a proof on the fly. (Nuprl works around such rules, since it doesn't extract realizers on the fly.) This seems to be essentially the problem of dependent proof refinement discussed in [Algebraic Foundations of Proof Refinement](#SterlingHarperRefinement). An analogue of on-the-fly realizer extraction is used by Cedille too, and is called "erasure".

### Intended Style

The primitives of CLF will probably be pretty low-level, and will rely on some "bootstrapping" up to the usual principles of type theory. (Some of this can be seen already, in the discussion of the rules below.) This bootstrapping will rely in crucial ways on the realizers being fundamentally untyped.

However, once the bootstrapping is taken care of, the intent is that the main way of using CLF will be a lot like other dependently-typed proof assistants: Constructions will be thought of as elements of types, and the type system will guide the details of constructing elements.

Given the goal of a system that feels typed, it may seem weird to explicitly base it on untyped realizers. The reason goes back to the flexibility of specifications, compared to purely syntactic typing. It should *always* be possible to construct elements in such a way that the computational content is well-implemented. But it seems that syntactic dependent typing requires ever more tricks to be added to the language in order to express elements using terms that are efficient.

Rather than having to change the language, CLF provides the option of reasoning about assignment of types to untyped realizers to *prove* the missing type theoretic principles. Of course, reasoning about type assignment can also be used, to taste, even when not strictly necessary. In general, there's a spectrum of styles for using an extrinsic type theory, based on how much of the well-typedness of a construction is true by construction, versus proven afterward. Correctness by construction makes the development feel more intrinsic, but this difference in style is not a commitment: the extrinsic perspective applies to everything.

### CLF as a Metalogic

The above considerations motivate a whole class of type system implementations that combine Nuprl-style semantics with a Cedille-like proof term checker. But what about [[category|categories]]?

To justify the proof rules, systems like Nuprl, Cedille, and CLF are based on term realizability models. But it's not currently clear to what extent this approach is compatible with the [[relation between type theory and category theory|categorical semantics of type theory]].

The specifics of CLF are motivated by the insight (of Matt Oliveri, but strongly inspired by [Andromeda](http://www.andromeda-prover.org/)) that [[extensional type theory|extensional type theories]] (with equality reflection) promise to make great logical frameworks. Although categorical semantics for "structural" fragments of Nuprl-style systems may be feasible and useful, CLF sidesteps the whole issue by being a metalogic for reasoning about formal systems.

The idea is that by regarding CLF as a metalogic, its possible lack of categorical semantics is irrelevant because the object logic can be chosen so as to reason about the desired semantics. CLF as a metalogic is a way to try to make the (hypothesized) technical advantages of a Nuprl-Cedille-like approach applicable to any type theory.

Some discussion is needed to explain what makes extensional type theory good for logical frameworks, what that has to do with metalogics, and what makes CLF a good metalogic. [Later](#CLFasLF).

First, what follows is a draft version of the formal system that will be used in prototype CLF. These rules are non-algorithmic rules pertaining only to types and realizers; the details of the proof system are not designed yet. (And they won't be until some issues are addressed in the semantics and rule set.)

## Syntax

### Term grammar

The main [[syntax|syntactic]] class is [[terms]]. [[type|Type]] expressions are terms. There are also [[variables]] and [[contexts]].

variables ($x$, $y$, ...)` ::= `(Written as usual. Complain if you can't tell them apart from metavariables.)

terms ($t$, $a$, $b$, $f$, $T$, $A$, $B$, $R$, ...)` ::=`

* $\lambda x.b \qquad$ (lambda abstraction)
* $f\,a \qquad$ (application)

* $a = b \in C \qquad$ (equality type)
* $\Pi x:A.B \qquad$ (dependent function type)
* $\cap x:A.B \qquad$ (family intersection type)
* $Comp \qquad$ (type of computations ([[realizers]]))
* $\{x:A | B\} \qquad$ (subset/separation type)
* $\{x = y | R\} \qquad$ ([[PER]] comprehension type)
* $Bool \qquad$ (type of "booleans") (two-element type)

To be added: an infinite type.

contexts ($\Gamma$, ...)` ::= `$\cdot$` | `$\Gamma,x:T$

As usual, the rules may make liberal use of informal list operations to work with contexts.

### Judgment forms

$a \equiv_\beta b \qquad$ (beta conversion)

The only [[beta reduction]] is $(\lambda x.b)\,a \longrightarrow_\beta b[a/x]$. Conversion is the congruence closure.

The other [[judgment]] forms will be defined [[induction|inductively]] by the rules below. They are:

$\Gamma \vdash T\,type \qquad$ (type validity)

$\Gamma \vdash t \Vdash T \qquad$ (element in a type) (realizer of a type)

Note that in [[Nuprl]], the ($\Gamma \vdash t \Vdash T$) form is written ($\Gamma \vdash T\;\lfloor ext t \rfloor$). The "extract" part is computed from a derivation, so the user thinks of the judgment as stating that the type is [[inhabited type|inhabited]].

In the rules below, however, no attention is paid to what can be metatheoretically computed with terms or derivations. That is (important) future work.

($\Gamma \vdash t \Vdash T$) is used instead of ($\Gamma \vdash t\,:\,T$) in order to avoid the misinterpretation of this judgment form as [[intrinsic and extrinsic views of typing|intrinsic typing]] of terms. Note the contrast with variables, which *are* intrinsically typed.

The ($t\,:\,T$) form can be translated to this system as either ($t \Vdash T$) or ($? \Vdash t \in T$). The latter uses the abbreviation "$\in$" defined below, and the abuse of meta-notation that we don't care what goes in the "$?$". With ($t \Vdash T$), we think of $t$ as resulting from the proof of $T$. With ($? \Vdash t \in T$), we think of the "*semantic judgment*" ($t \in T$) as a goal to prove internally. The rules ensure that these two ways of expressing an element of a type are interderivable. From this point on, ($\Gamma \vdash ? \Vdash T$) will be written as just ($\Gamma \vdash T$), although it remains informal.

### Abbreviations

#### Semantic Judgment Forms {#SemJudg}

$a \in A\;\coloneqq\;a = a \in A$

$A \to B\;\coloneqq\;\Pi \underline{\;}:A.B$

$A \wedge B\;\coloneqq\;\{\underline{\;}:A | B\}$

"$A$ equality is respected in $B$.":

$A \prec B\;\coloneqq\;\Pi t:Comp.\Pi t':Comp.
(t \in B)\to(t = t' \in A)\to(t = t' \in B)$

"$A$ members are included in $B$.":

$A \subseteq B\;\coloneqq\;\Pi t:Comp.(t \in A)\to(t \in B)$

"$A$ is a subtype of $B$.":

$A \lt\!\!:\;B\;\coloneqq\;(\lambda x.x) \in (A \to B)$

Note: ($A \lt\!\!:\;B$) ought to be logically equivalent to ($A \subseteq B \wedge A \prec B$), using the rules. And also to ($\Pi t:Comp.\Pi t':Comp.(t = t' \in A)\to(t = t' \in B)$). So semantically, thinking of types as PERs, subtypes are subrelations.

"$A$ is a refinement/[[subquotient]] of $B$.":

$A \sqsubseteq B\;\coloneqq\;A \subseteq B \wedge B \prec A$

Note the reversal of $\prec$ in $\sqsubseteq$, compared to $\lt\!\!:$. As relations on types, $\subseteq$, $\lt\!\!:$, and $\sqsubseteq$ ought to be preorders. $\prec$ is not transitive.

#### Computations

The Church booleans:

$tru\;\coloneqq\;\lambda t.\lambda f.t$

$fls\;\coloneqq\;\lambda t.\lambda f.f$

#### Type constructors

$\top\;\coloneqq\;tru = tru \in Bool$

$\bottom\;\coloneqq\;tru = fls \in Bool$

"Squash" of $A$:

$\lfloor A \rfloor\;\coloneqq\;\{\underline{\;}:\top | A\}$

## Rules

These rules are not the final rules that are planned to be implemented in CLF. The major differences planned for the final rules from those here are:

* Use roughly Nuprl-style hidden assumptions, but with unhiding handled automatically.
* Have an additional judgment form for goals whose realizer is ignored/arbitrary, which interacts with unhiding.
* Add formal proof terms.

The expectation and hope is that the result will look fairly similar to algorithmic elaboration-style type checking rules. These rules will be the primitive tactics, and type checking will thus be a special case of running tactic trees.

### Type Formation

We have a strong equality formation rule, inspired by the medium-strength rule from [Anand & Rahli](#AnandRahliITP14), which is also stronger than the usual one. Here is respect-based equality formation:

$$\begin{gathered}
\frac{\Gamma \vdash p \Vdash A \prec C \qquad
\Gamma \vdash q \Vdash B \prec C \qquad
\Gamma \vdash a \Vdash A \qquad \Gamma \vdash b \Vdash B}
{\Gamma \vdash a = b \in C\,type} \\
\\
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \Pi x:A.B\,type} \\
\\
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \cap x:A.B\,type}
\end{gathered}$$

The $Comp$ type, which is called $Base$ in Nuprl:

$$\begin{gathered}
\frac{}{\Gamma \vdash Comp\,type} \\
\\
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \{x:A | B\}\,type}
\end{gathered}$$

The PER comprehension type was originally conceived by Stuart Allen, and then forgotten and subsequently [reintroduced](#PERTypes14). However, I think Nuprl had already had $Base$, subsets, and quotients, which make it definable. The real innovation is how PER comprehension and the strengthened equality formation rule interact to allow internal, logical-relations-style type definitions. We only allow forming a PER type from a pseudo-PER, rather than implicitly taking the symmetric transitive closure of any family:

$$\begin{gathered}
\frac{\begin{array}{l}\Gamma,x1:Comp,x2:Comp \vdash R\,type \\
\Gamma,y1:Comp,y2:Comp \vdash s \Vdash R[y1,y2/x1,x2] \to R[y2,y1/x1,x2] \\
\Gamma,y1:Comp,y2:Comp,y3:Comp \vdash t \Vdash R[y1,y2/x1,x2] \to R[y2,y3/x1,x2] \to R[y1,y3/x1,x2]\end{array}}
{\Gamma \vdash \{x1 = x2 | R\}\,type} \\
\\
\frac{}{\Gamma \vdash Bool\,type}
\end{gathered}$$

### Miscellaneous

$$\frac{x:T \in \Gamma}{\Gamma \vdash x \Vdash T}$$

The untyped beta conversion rules have the same role as Nuprl's direct computation rules:

$$\begin{gathered}
\frac{A \equiv_\beta B \qquad \Gamma \vdash B\,type \qquad
\Gamma \vdash t \Vdash A}
{\Gamma \vdash t \Vdash B} \\
\\
\frac{t \equiv_\beta t' \qquad \Gamma \vdash t \Vdash T}
{\Gamma \vdash t' \Vdash T}
\end{gathered}$$

Every type respects itself, and $Comp$. (Yes, you can use any term you like as the proof.):

$$\begin{gathered}
\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash A \prec A} \\
\\
\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash Comp \prec A}
\end{gathered}$$

### Equality

A reflexivity rule, but any term can be the proof:

$$\frac{\Gamma \vdash t \Vdash T}{\Gamma \vdash p \Vdash t = t \in T}$$

Terms participating in equality are elements. Normally this would only be admissible, but in CLF, it comes in handy to make it into "selectivity" rules:

$$\begin{gathered}
\frac{\Gamma \vdash p \Vdash t1 = t2 \in T}{\Gamma \vdash t1 \Vdash T} \\
\\
\frac{\Gamma \vdash p \Vdash t1 = t2 \in T}{\Gamma \vdash t2 \Vdash T}
\end{gathered}$$

Note that the above equality rules make ($\Gamma \vdash t \Vdash T$) and ($\Gamma \vdash t \in T$) interderivable, as promised.

We use a "subsumptive" rewrite rule as equality elimination. "Subsumptive" refers to the property that the proof of the type we rewrite in is unaffected. The terminology "subsumptive" for this is new to CLF, although this is effectively the same equality elimination rule as in Nuprl. The terminology comes from "subsumptive" vs "coercive" implementations of subtyping. Note that formally, CLF has no typed judgmental equality. Semantically, it's an [[extensional type theory]], but the semantic equality judgment is implemented as the equality type. This is sound due to equality reflection. So this rule is semantically a consequence of equality reflection, equality substitution, and (typed) conversion. As with equality reflection, the proof of equality is irrelevant:

$$\frac{\Gamma,x:A \vdash B\,type \qquad
\Gamma \vdash p \Vdash a1 = a2 \in A \qquad
\Gamma \vdash b \Vdash B[a1/x]}
{\Gamma \vdash b \Vdash B[a2/x]}$$

Any two terms are equal as the (consequently unique) proof of a true equality:

$$\frac{\Gamma \vdash t \Vdash T}
{\Gamma \vdash q \Vdash p1 = p2 \in (t = t \in T)}$$

That means $\top$ too, which is thus the maximum PER, ordered by subtyping. (Well, just as soon as we make $tru$ an element of $Bool$.)

### Functions

We have the standard application rule, and a variant of function extensionality:

$$\begin{gathered}
\frac{\Gamma \vdash f \Vdash \Pi x:A.B \qquad
\Gamma \vdash a \Vdash A}
{\Gamma \vdash f\,a \Vdash B[a/x]} \\
\\
\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash p \Vdash f\,x = f'\,x \in B \qquad
x \notin FV(f,f')}
{\Gamma \vdash q \Vdash f = f' \in \Pi x:A.B}
\end{gathered}$$

Unconventionally, we consider function extensionality to be the $\Pi$ intro rule, and derive the fact that lambdas implement functions.

### Intersection

Elements of a family intersection are like elements of a $\Pi$ type, except you don't have to apply them. An intersection element is *already* an element of all instances of the family. So the rules for family intersection are analogous to the rules for $\Pi$:

$$\begin{gathered}
\frac{\Gamma \vdash b \Vdash \cap x:A.B \qquad
\Gamma \vdash a \Vdash A}
{\Gamma \vdash b \Vdash B[a/x]} \\
\\
\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash p \Vdash b = b' \in B \qquad
x \notin FV(b,b')}
{\Gamma \vdash q \Vdash b = b' \in \cap x:A.B}
\end{gathered}$$

### Computation Formation

$$\begin{gathered}
\frac{\Gamma,x:Comp \vdash b \Vdash Comp}{\Gamma \vdash \lambda x.b \Vdash Comp} \\
\\
\frac{\Gamma \vdash f \Vdash Comp \qquad \Gamma \vdash a \Vdash Comp}
{\Gamma \vdash f\,a \Vdash Comp}
\end{gathered}$$

### Subset

The subset type resembles an existential quantifier. In the elimination rule, the proof part must be computationally irrelevant, since an element of a subset does not include the proof. Nuprl handles this with a hidden assumption, which is the practical way to do it. But it's also sound to just stick in a free variable side condition.

$$\begin{gathered}
\frac{\Gamma,x:A \vdash B\,type \qquad
\Gamma \vdash a \Vdash A \qquad \Gamma \vdash b \Vdash B[a/x]}
{\Gamma \vdash a \Vdash \{x:A | B\}} \\
\\
\frac{\Gamma,z:\{x:A | B\} \vdash C\,type \qquad
\Gamma,x:A,y:B \vdash c \Vdash C[x/z] \qquad y \notin FV(c) \qquad
\Gamma \vdash a \Vdash \{x:A | B\}}
{\Gamma \vdash c[a/x] \Vdash C[a/z]}
\end{gathered}$$

### PER

The rules for PER comprehension are made simpler by the fact that we required $R$ to be a pseudo-PER in the formation rule. The idea is that ($(t1 = t2 \in \{x1 = x2 | R\;x1\;x2\}) \leftrightarrow \lfloor R\;t1\;t2 \rfloor$), using the squash type constructor defined above. So comprehension and equality are almost inverse; you just lose the computational content of the equivalence proof.

$$\begin{gathered}
\frac{\Gamma \vdash \{x1 = x2 | R\}\,type \qquad
\Gamma \vdash t2 \Vdash Comp \qquad
\Gamma \vdash p \Vdash R[t1,t2/x1,x2]}
{\Gamma \vdash q \Vdash t1 = t2 \in \{x1 = x2 | R\}} \\
\\
\frac{\begin{array}{l}
\Gamma \vdash C\,type \qquad
\Gamma \vdash R[t1,t2/x1,x2]\,type \\
\Gamma \vdash p \Vdash t1 = t2 \in \{x1 = x2 | R\} \\
\Gamma,z:R[t1,t2/x1,x2] \vdash c \Vdash C \qquad z \notin FV(c)
\end{array}}
{\Gamma \vdash c \Vdash C}
\end{gathered}$$

### Booleans

$$\frac{}{\Gamma \vdash tru \Vdash Bool} \qquad
\frac{}{\Gamma \vdash fls \Vdash Bool}$$

Exercise: Does the following rule express ($Bool \subseteq Comp$), ($Bool \lt\!\!:\;Comp$), or ($Bool \sqsubseteq Comp$)?

$$\frac{\Gamma \vdash b \Vdash Bool}{\Gamma \vdash b \Vdash Comp}$$

Our elimination rule is intuitively characterizing $Bool$ as the least type containing $tru$ and $fls$. The usual elimination rule is derived; it's derivable because Church booleans actually work.

$$\frac{\Gamma,x:Bool \vdash C\,type \qquad
\Gamma \vdash c \Vdash C[tru/x] \qquad
\Gamma \vdash c \Vdash C[fls/x] \qquad
\Gamma \vdash b \Vdash Bool}
{\Gamma \vdash c \Vdash C[b/x]}$$

An [[ex falso quodlibet]] rule, which is technically about booleans, because of how we defined $\bottom$. Note that this makes $\bottom$ the minimum PER, ordered by inclusion, subtyping, or refinement.

$$\frac{\Gamma \vdash T\,type \qquad
\Gamma \vdash p \Vdash \bottom}
{\Gamma \vdash t \Vdash T}$$

## Admissible rules

### Structural rules

The structural rules of weakening and substitution are admissible. "Strengthening" is not. Nonadmissibility of strengthening means: just because a variable isn't free in the conclusion doesn't mean the derivation isn't using it. This is typical of extensional type theory. Typically it's considered all the fault of equality reflection, which may be technically true for some systems. But Nuprl turned this apparent bug into a feature: subsets and intersections provide flexible control over which proofs make it into the computational content, and which are merely establishing external facts. Computational irrelevance is implemented by literally omitting the irrelevant proofs from terms. This leads to the lack of strengthening, and to undecidable type checking. The restriction imposed by equality reflection is that equality proofs never have computational content.

CLF follows Nuprl in trying to give the user maximum control over the terms used to represent elements. The hope is that with care, this can allow significantly greater convenience and performance than with decidable dependent type systems, which are committed to retaining enough annotations to effectively reject ill-typed terms.

### Sanity and Inversion

You'd think a statement should make sense before you try to prove it. And likewise, that a type should be valid before you try to construct an element. But in practice, it also works to consider a typed construction as providing evidence that the type makes sense. Specifically, the only way to derive ($\Gamma \vdash t \Vdash T$) is if you could also derive ($\Gamma \vdash T\,type$). That's a "sanity check" admissible rule. It's *probably* admissible for the judgments defined by the rules above.

Also, since the only way to derive type validity in this system (not using the sanity admissible rule) is to use a type former, a derivation of type validity implies that there are derivations of validity for the subexpressions of the type expression. These are "inversion" admissible rules.

### Admissible Rules vs PER Semantics {#AdmissSem}

For full Nuprl, it seems practically impossible to prove admissibility of sanity or inversion, if they're not just included among the primitive rules. But they *can* be included among the primitive rules, because they're true in the semantics. Due to the way hypothetical judgments are defined, making the inversion rules true requires making type equality intensional.

The above rules are the result of an experiment to reason about formal derivability in a Nuprl-style system. In the PER semantics that the above rules were based on, type equality is extensional. So the basic rules directly satisfied were more complicated, since they needed extra premises that inversion would've made redundant. The above rules are actually admissible rules relative to those basic rules. Sanity and inversion are "probably" admissible for the above rules because what's actually known is that they're admissible for the basic rules; they were in fact used to prove the above rules.

So the experiment was partially successful, but I (Matt Oliveri) don't recommend the approach. It cannot be easily adapted to handle universes, and some of the rules above still have type validity premises that a fully semantic approach could avoid.

It may seem weird that Nuprl is based on a particular PER semantics, if you think of it as a mathematical model. But if you think of it as a proof theoretic technique that reasons about realizability instead of formal derivability, perhaps it's more palatable.

Thinking that way, all the consequences of the PER semantics are like admissible rules, and can be added to the formal system if they're useful. But it still seems like a good idea to try and find a stable formal system with enough rules that incompleteness is not a problem in practice.

This raises questions though: If the formal rules of a Nuprl-style system are considered admissible, what defines the system? What are the mathematical models of Nuprl-style systems? If they're considered unnatural, should Nuprl-style systems be modified?

In my (Matt Oliveri's) opinion, Nuprl-style systems are potentially relevant and useful to mathematics, but it's not currently clear exactly how that might work.

### Loose ends

Now that we've covered the issue that the distinction between derivable and admissible doesn't really matter for this system, we can get to explaining particular aspects that may seem to be in particular need of an explanation.

#### Equality uses respect which uses equality

The equality formation rule refers to the respect ("$\prec$") relation. The latter is not primitive, it's defined in terms of equality. Is that OK? Yes: Because of the rule that all types respect $Comp$, we get enough instances of equality formation to prove:

$$\frac{\Gamma \vdash A\,type \qquad \Gamma \vdash B\,type}
{\Gamma \vdash A \prec B\;type}$$

If it still seems suspiciously circular, rest assured that in the semantics, respecting computational equivalence is more basic than anything in the type system. The rule about respecting $Comp$ just exposes the fact internally.

Because every type respects itself, we get all the instances of equality formation from Martin-Löf type theory. Equality types beyond that are for reasoning about membership.

#### Usual Pi-intro rule

Taking function extensionality to be $\Pi$ intro seems odd. Not only is it not about lambdas, it's not apparently about elements at all; just equality. That's (one place) where the selectivity rules are handy. The function extensionality rule is strong enough to combine with selectivity (and reflexivity) to derive elements of function type. A term is a function when you can apply it to an argument to get a result:

$$\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash f\,x \Vdash B \qquad x \notin FV(f)}
{\Gamma \vdash f \Vdash \Pi x:A.B}$$

Proving that lambdas are functions additionally uses beta conversion. Lambdas are functions, not by fiat, but because they produce results when applied.

Note that not all functions are denoted by lambdas. At the very least, the empty function is denoted by any term you like. That is, a function type with empty domain has the same PER as $\top$. However, any function is equal to a lambda, when considered only as a function. Formally, we have

$$\Gamma,f:\Pi x:A.B \vdash f = (\lambda x.f\,x) \in \Pi x:A.B$$

but not

$$\Gamma,f:Comp,Hf:f \in \Pi x:A.B \vdash f = (\lambda x.f\,x) \in Comp$$

.

#### Congruence rules

With such a small set of type constructors, it may be hard to tell, but congruence rules are rarely needed as primitives. Beta conversion was already defined as an untyped congruence closure, and for typed equality, the subsumptive rewrite rule does most of the work of congruence rules. The extensionality rules for $\Pi$ and $\cap$ are needed to help with binders and (our ersatz) hidden assumptions. That may turn out to handle everything, with this judgmental setup.

## Semantic Judgmental Reflection

### Equality reflection

With many type theories $T$, it's cumbersome but straightforward to define collections of the formal derivations of $T$ as type families in $T$. This provides a form of *syntactic* reflection of a system's judgments within itself. [[provability logic|There]] [[modal type theory|are]] [[higher-order abstract syntax|ways]] of making syntactic reflection more convenient and/or powerful.

But Nuprl-style systems provide a quite different kind of judgmental reflection that we'll call "*semantic* judgmental reflection", or just "judgmental reflection" for short. The original example of judgmental reflection, and the basis of the name, is the equality reflection rule of extensional type theory (ETT), which makes the "identity" type family a reflection of the meaning of the element equality judgment of the same system. In a sense, this is still the only judgmental reflection principle in Nuprl-style systems. (But the type family is called "equality".) The difference is in the interpretation of the equality judgment.

There are two styles of interpretation for ETT: [[intrinsic and extrinsic views of typing|intrinsic and extrinsic]]. Extrinsic is the original, since an example is Martin-Löf's [[meaning explanation]], which was the original justification for equality reflection. Intrinsic seems to have become the default one. It's the style considered in [Martin Hofmann's thesis](#HofmannThesis), for example. But Nuprl and CLF commit to the extrinsic style.

An irony is that by considering terms extrinsically typed, you consider them intrinsically meaningful. In Nuprl and CLF, following Martin-Löf, terms have an intrinsic computational meaning. The role of the Nuprl-style type system is to reason about that. (Remember: this can all be considered a [substitute for admissible rules](#AdmissSem)! ...Probably.)

There is actually no interpretation necessary, for terms in general. The type system can be layered over the terms as they are, making use of an operational model of their computational meaning. (A denotational semantics would probably work too.) The details need not concern us here, but some things are important:

* Computational meaning pertains principally to closed terms, because free variables don't compute; they're just placeholders.
* Some closed terms are designated as types, and denote PERs on closed terms.
* For closed terms and types, the equality judgment form ($t = t' \in T$) just accesses the PER of the type.
* For closed terms and types, the judgment of being an element of a type ($t \in T$) is a special case of equality.
* It's the judgments about closed terms that are reflected as closed types; judgments about open terms are not involved.

All of these points are important to the design of a Nuprl-style system. But the one that seems to distinguish the approach from intrinsic typing is that being an element is a special case of equality. In the intrinsic approach, equality is only meaningful when applied to two terms known to have the same type. So being an element must be somehow prior to equality. But with the judgment of being an element as a special case of equality, it's simultaneous.

A lot of the power of judgmental reflection is that it *can* be understood as reasoning about the computational content of the language as it actually is. But since it's probably not *necessary* to interpret Nuprl-style systems as being about their own syntax, we should speak of "computations", not "closed terms". In CLF, however they're interpreted, computations are axiomatized as the elements of $Comp$. (And actually, it may be that types need not be computations.) Types are PERs on $Comp$, and are accessed by the equality judgment form, which is reflected by the equality type constructor. So you use equality types to reason about equality in types, and also membership of computations in types.

So then what's with all this respect ("$\prec$") stuff in the equality formation rule? If terms have an intrinsic computational meaning, and equality reasons about it, shouldn't the rule be just:

$$\frac{\Gamma \vdash T\,type}{\Gamma \vdash t1 = t2 \in T\,type}$$

?

No, that doesn't work. The extra complexity has to do with making the axiomatization work for open terms. Consider the type $I\;\coloneqq\;\{x = y | x \in Bool \wedge y \in Bool\}$. Then $tru = fls \in I$. But then consider ($x:I \vdash tru = x \in Bool\,type$). The simple formation rule would derive it, but it doesn't make sense, because ($tru = tru \in Bool$) and ($tru = fls \in Bool$) are different types, although $tru$ and $fls$ are the same $I$. The problem is that equality of types and elements is generally different from equality of computations, and we want well-typed open terms to respect equality of elements. The respect-based equality formation rule doesn't derive the bad type family because you'd need to find some type $T$ such that ($x:I \vdash x \Vdash T$) and ($T \prec Bool$). But if ($x:I \vdash x \Vdash T$), then $T$ considers $tru$ and $fls$ equal, while if ($T \prec Bool$), then it doesn't. That variables and other open terms cannot generally be treated as computations is the sense in which variables are intrinsically typed: although elements are all realized by computations, an arbitrary element generally cannot be used as a computation, so reasoning about membership is constrained.

### Other semantic judgments

Based on the ability to reason about membership, in addition to equality, other types can be defined that seem like semantic judgments. For example, $\prec$, $\subseteq$, $\lt\!\!:$, and $\sqsubseteq$ were [defined above](#SemJudg). But what kinds of things are these semantic judgments in general?

A lenient answer is that semantic judgments are type (families) $J$ such that ($\lfloor J \rfloor \to J$) is inhabited. That is, the squash-stable types. All such types are isomorphic to equality types, and are the regular subobjects, if you consider a Nuprl-style system as a category. (In a [[relation between type theory and category theory#DependentTypeTheory|manner analogous to ETT]], using inhabitedness of equality types to determine equality of morphisms.)

A stricter definition of semantic judgments is that they are type (families) $J$ such that ($\lfloor J \rfloor \lt\!\!:\;J$). Types formed with equality, squash itself, $\prec$, $\subseteq$, $\lt\!\!:$, and $\sqsubseteq$ are always judgments in this strict sense. These types are extensionally equal to equality types (for example, this one: $(\lambda x.x) \in J$) in the following sense:

$$A \approx B\;\coloneqq\;A \lt\!\!:\;B \wedge B \lt\!\!:\;A$$

This definition of extensional equality is motivated by the "subsumption" (derived) rule:

$$\frac{\Gamma \vdash t \Vdash A \qquad
\Gamma \vdash A \lt\!\!:\;B}
{\Gamma \vdash t \Vdash B}$$

So $\approx$ gives us subsumptions in both directions. Extensionally equal types denote the same PER.

Thus, the semantic judgments in the strict sense are regular subobjects defined in a convenient way so that they're inhabited if and only if they're basically $\top$. $\approx$ is itself a semantic judgment. Also:

$$(A \approx B) \approx (A \sqsubseteq B \wedge B \sqsubseteq A)$$

However, ($A \subseteq B \wedge B \subseteq A$) is generally weaker. For example, $\top$ and $Comp$ have the same members (computations) but are not extensionally equal, or even isomorphic.

## PER theory

## More admissible/derived rules

### Fun with subsets

### Bool eliminations

Combining ($Bool \lt\!\!:\;\Comp$) with the above elimination rule for $Bool$, you get this alternative elimination rule, where the motive is a family on $Comp$:

$$\frac{\Gamma,x:Comp \vdash C\,type \qquad
\Gamma \vdash c \Vdash C[tru/x] \qquad
\Gamma \vdash c \Vdash C[fls/x] \qquad
\Gamma \vdash b \Vdash Bool}
{\Gamma \vdash c \Vdash C[b/x]}$$

Curiously, you can go in the other direction too, and get both of the original rules from this one.

To get the usual elimination rule, prove that Church booleans are self-eliminating functions:

$$\frac{\Gamma,x:Bool \vdash C\,type \qquad
\Gamma \vdash b \Vdash Bool}
{\Gamma \vdash b \Vdash C[tru/x] \to C[fls/x] \to C[b/x]}$$

This is reasoning about membership, so we really do want to know that $Bool$s are $Comp$s. The usual elimination rule then just applies $b$ at that function type.

In Nuprl, it's often possible to get induction rules without a premise showing that the motive is a valid family. The idea is that for sufficiently concrete types, validity of the motive can be proven pointwise, and moreover the cases of this proof are actually implied by the cases of the main induction.

In the current CLF rules though, it doesn't seem possible to derive such rules. Also, including such strengthened induction rules as primitive doesn't seem compatible with the [current hybrid approach](#AdmissSem) based on admissible formal rules: the sanity check would require an unusual type validity rule, which would ruin the inversion lemma. Basically the Nuprl-style justification for omitting the motive premise is "too semantic" for the current hybrid approach.

### Subtyping (Conjectural)

## CLF and Logical Frameworks {#CLFasLF}

(Sorry, nothing here yet.)

### LF= {#LFEq}

### LF Signatures as Inductive-Inductive Families

### Bishop-style Quotients

## References

* {#AnandRahliITP14} Abhishek Anand, Vincent Rahli, _Towards a Formally Verified Proof Assistant_, Interactive Theorem Proving (ITP) 2014 ([project web](http://www.nuprl.org/html/Nuprl2Coq/), [paper web](http://www.nuprl.org/KB/show.php?ID=726), [pdf](http://www.nuprl.org/documents/Anand/TowardsAFormallyVerifiedProofAssistant.pdf))

* {#PERTypes14} Abhishek Anand, Mark Bickford, [[Robert Constable|Robert L. Constable]], Vincent Rahli, _A Type Theory with Partial Equivalence Relations as Types_, Types for Proofs and Programs (TYPES) 2014 ([slides](https://vrahli.github.io/articles/slides-per-types.pdf), [web](http://www.nuprl.org/KB/show.php?ID=722), [pdf](http://www.nuprl.org/documents/Anand/ATypeTheoryWithPartialEquivalenceRelationsAsTypes.pdf))

* {#HofmannThesis} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. dissertation, University of Edinburgh (1995). ([link](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/))

* {#SterlingHarperRefinement} [[Jonathan Sterling]], [[Robert Harper]], _Algebraic Foundations of Proof Refinement_, 2017 ([arXiv](https://arxiv.org/abs/1703.05215))