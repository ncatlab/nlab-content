
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

Proto CLF is a work-in-progress [[proof assistant]] design combining ideas from [[Nuprl]], [[LF]], and [[decidability|undecidable type checking]] based on subsumptive [[equality types]]. "CLF" abbreviates "Computational Logical Framework". So far, it's just Matt Oliveri's unpublished metatheory development, but information may appear here.

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

($\Gamma \vdash t\,:\,T$) is not used in order to avoid the misinterpretation of this judgment form as [[intrinsic and extrinsic views of typing|intrinsic typing]] of terms. Note the contrast with variables, which *are* intrinsically typed.

The ($t\,:\,T$) form can be translated to this system as either ($t \Vdash T$) or ($? \Vdash t \in T$). The latter uses the abbreviation "$\in$" defined below, and the abuse of meta-notation that we don't care what goes in the "$?$". With ($t \Vdash T$), we think of $t$ as resulting from the proof of $T$. With ($? \Vdash t \in T$), we think of the "*semantic judgment*" ($t \in T$) as a goal to prove internally. The rules ensure that these two ways of expressing an element of a type are interderivable. From this point on, ($\Gamma \vdash ? \Vdash T$) will be written as just ($\Gamma \vdash T$), although it remains informal.

### Abbreviations

#### Semantic Judgment Forms

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

"$A$ is a refinement/subquotient of $B$.":

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

$\{A\}\;\coloneqq\;\{\underline{\;}:\top | A\}$

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

The rules for PER comprehension are made simpler by the fact that we required $R$ to be a pseudo-PER in the formation rule. The idea is that ($(t1 = t2 \in \{x1 = x2 | R\;x1\;x2\}) \leftrightarrow \{R\;t1\;t2\}$), using the squash type constructor defined above. So comprehension and equality are almost inverse; you just lose the computational content of the equivalence proof.

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

The structural rules of weakening and substitution are admissible. "Strengthening" is not. Nonadmissibility of strengthening means: just because a variable isn't free in the conclusion doesn't mean the derivation isn't using it. This is typical of "extensional type theory". Typically it's considered all the fault of equality reflection, which may be technically true for some systems. But Nuprl turned this apparent bug into a feature: subsets and intersections provide flexible control over which proofs make it into the computational content, and which are merely establishing external facts. Computational irrelevance is implemented by literally omitting the irrelevant proofs from terms. This leads to the lack of strengthening, and to undecidable type checking. The restriction imposed by equality reflection is that equality proofs never have computational content.

CLF follows Nuprl in trying to give the user maximum control over the terms used to represent elements. The hope is that with care, this can allow significantly greater convenience and performance than with decidable dependent type systems, which are committed to retaining enough annotations to effectively reject ill-typed terms.

### Sanity and Inversion

You'd think a statement should make sense before you try to prove it. And likewise, that a type should be valid before you try to construct an element. But in practice, it also works to consider a typed construction as providing evidence that the type makes sense. Specifically, the only way to derive ($\Gamma \vdash t \Vdash T$) is if you could also derive ($\Gamma \vdash T\,type$). That's a "sanity check" admissible rule. It's *probably* admissible for the judgments defined by the rules above.

Also, since the only way to derive type validity in this system (not using the sanity admissible rule) is to use a type former, a derivation of type validity implies that there are derivations of validity for the subexpressions of the type expression. These are "inversion" admissible rules.

### Admissible Rules vs PER Semantics

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

The equality formation rule refers to the respect ("$\prec$") relation. The latter is not primitive, it's defined in terms of equality. Is that OK? Yes: because of the rule that all types respect $Comp$, we get enough instances of equality formation to prove:

$$\frac{\Gamma \vdash A\,type \qquad \Gamma \vdash B\,type}
{\Gamma \vdash A \prec B\;type}$$

If it still seems suspiciously circular, rest assured that in the semantics, respecting computational equivalence is more basic than anything in the type system. The rule about respecting $Comp$ just exposes the fact internally.

Because every type respects itself, we get all the instances of equality formation from Martin-Löf type theory. Equality types beyond that are for reasoning about membership.

#### Usual Pi-intro rule

Taking function extensionality to be $\Pi$ intro seems odd. Not only is it not about lambdas, it's not apparently about elements at all; just equality. That's (one place) where the selectivity rules are handy. The function extensionality rule is strong enough to combine with selectivity (and reflexivity) to derive elements of function type. A term is a function when you can apply it to an argument to get a result:

$$\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash f\,x \Vdash B \qquad x \notin FV(f)}
{\Gamma \vdash f \Vdash \Pi x:A.B}$$

Proving that lambdas are functions additionally uses beta conversion. Lambdas are functions, not by fiat, but because they produce results when applied. Note that not all functions are lambdas. At the very least, the empty function is denoted by any term you like. That is, a function type with empty domain has the same PER as $\top$.

#### Congruence rules

With such a small set of type constructors, it may be hard to tell, but congruence rules are rarely needed as primitives. Beta conversion was already defined as an untyped congruence closure, and for typed equality, the subsumptive rewrite rule does most of the work of congruence rules. The extensionality rules for $\Pi$ and $\cap$ are needed to help with binders and (our ersatz) hidden assumptions. That may turn out to handle everything, with this judgmental setup.

## Semantic Judgmental Reflection

## PER theory

## More admissible rules

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

### Subtyping (Conjectural)

## References

* {#AnandRahliITP14} Abhishek Anand, Vincent Rahli, _Towards a Formally Verified Proof Assistant_, Interactive Theorem Proving (ITP) 2014 ([project web](http://www.nuprl.org/html/Nuprl2Coq/), [paper web](http://www.nuprl.org/KB/show.php?ID=726), [pdf](http://www.nuprl.org/documents/Anand/TowardsAFormallyVerifiedProofAssistant.pdf))

* {#PERTypes14} Abhishek Anand, Mark Bickford, Robert L. Constable, Vincent Rahli, _A Type Theory with Partial Equivalence Relations as Types_, Types for Proofs and Programs (TYPES) 2014 ([slides](https://vrahli.github.io/articles/slides-per-types.pdf), [web](http://www.nuprl.org/KB/show.php?ID=722), [pdf](http://www.nuprl.org/documents/Anand/ATypeTheoryWithPartialEquivalenceRelationsAsTypes.pdf))