
#Contents#
* table of contents
{:toc}

## Idea

This article documents the differences between versions [[CompLF v0|zero]] and [[CompLF v1|one]] of [[CompLF]]. It also provides pointers to explanations of some of the theory that enables some of these differences, which is perhaps surprisingly (disappointingly?) subtle and deep. It gets into the connection between meaning explanations and partial logic, and the practical advantage of intensionality at the judgment level of dependent type theory.

## Admissibility vs Soundness

One of the most important differences between v0 and v1 is that many of the rules that are merely *admissible* in v0 are actually primitive or *derivable* in v1. In this regard, v1 is closer to Nuprl, and does not continue v0's "experiment" with admissible rules [[CompLF#AdmissSem|discussed previously]].

The most conspicuous changes are the addition of some new rules in v1: the "sanity" or "presuppositionality" rule, and "inversion" rules for the type formation rules. Sanity is this one:

$$\frac{\Gamma \vdash a \Vdash A}{\Gamma \vdash A\,type}$$

There are (unfortunately) many inversion rules, but they all have the effect of saying merely that most of the type formation rules are invertible. For example, here are the inversions of $\Pi$ formation:

$$\begin{gathered}
\frac{\Gamma \vdash \Pi x:A.B\,type}{\Gamma \vdash A\,type} \\
\\
\frac{\Gamma \vdash \Pi x:A.B\,type \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash B[a/x]\,type}
\end{gathered}$$

Note that there's a substitution baked into the $\Pi$ codomain rule. This is because substitution is still an admissible rule. Not baking in a substitution here would probably mess that up.

Less conspicuous, but just as important, are other changes throughout the rules of v0 that are possible because we no longer have to prove sanity and inversion by induction on formal derivations. Indeed, having sanity and inversion as primitive has the effect that many other rules become stronger: If you can derive $a \Vdash A$, then you also know that $A$ and many of its subexpressions are all valid types. In v0, this was by carefully designing the rules so that all those extra consequences were already derivable. In v1, it's actually revealing additional facts about the interpretation of the judgments. (Examples below.)

Due to the use of PER semantics, to make the inversion rules sound, semantic equality of types is now intensional, like in Nuprl (and intensional type theory!), and unlike in v0. (TODO: Write an explanation of this.) As for sanity, that was actually sound all along, but including it as a primitive rule would ruin admissibility of inversion, were that not also primitive.

Here is a list of changes to existing rules of v0 that are possible because sanity and inversion are primitive:

* The direct computation rule, which lets you beta convert in a type, (and which previously used the auxiliary judgment ($\equiv_\beta$) but now uses ($\longrightarrow_\beta$), which is discussed [separately](#BetaConv)) no longer requires the new type to be proven valid as an extra premise. Indeed, the new type *must* be valid, since it's semantically the same as the old one, which is valid by assumption.

* As a consequence of the previous, the other old direct computation rule, which lets you beta convert in the subject, has become redundant and has been removed. To derive it, just switch the judgment to express membership with the equality type, use direct computation in that type, and switch back.

* The "select right" rule of equality, which goes from ($a = a' \in A$) to ($a' \Vdash A$) has become redundant and has been removed. Prove symmetry in the usual way, and combine with select left. (Maybe it was already redundant before, who knows?)

* The subset elimination rule had a premise in v0 showing that the motive is a valid type family. In v1, this premise is removed. Semantically, it's redundant because it follows from the typing premise for the sole case (and the additional free variable constraint).

* Similarly, the PER elimination rule had the motive validity premise removed.

* Yet another, the $Bool$ elimination rule had the motive validity premise removed. This one is a bit more interesting, because this rule has *two* cases, which only show validity of a substitution instance of the motive. Luckily, a family over the booleans only *has* two substitution instances, semantically.

* As a consequence of the previous, the rule saying booleans are computations has become redundant and has been removed. It follows from case analysis on the boolean, and the fact that both canonical booleans are obviously computations, by the computation formation rules. The reason this argument didn't work in v0 is that you'd have trouble showing the motive is valid.

* Another consequence of the strengthened $Bool$ elimination which is perhaps much more surprising: The $\bot$ elimination rule, which effectively said that the two booleans aren't equal, has become redundant and has been removed. Like in type theory with universes, you can prove this by interpreting the booleans as true and false *types*. Why this is possible without universes is [[just kidding|explained elsewhere]], but it boils down to types syntactically being terms, having primitive sanity and inversion, and the strengthened $Bool$ elimination rule. (TODO: Explain this elsewhere!) (As icing on the cake, the derived $\bot$ elimination rule doesn't need a motive validity premise either. But this seems to require [identity](#IdType), a different v1 addition.)

## Relaxed Equality

Another important change is the new equality formation rule. Here is the v0 rule:

$$\frac{\Gamma \vdash p \Vdash A \prec C \qquad
\Gamma \vdash q \Vdash B \prec C \qquad
\Gamma \vdash a \Vdash A \qquad \Gamma \vdash b \Vdash B}
{\Gamma \vdash a = b \in C\,type}$$

Here is the v1 rule:

$$\frac{\Gamma \vdash a1 \Vdash Relax(A) \qquad \Gamma \vdash a2 \Vdash Relax(A)}
{\Gamma \vdash a1 = a2 \in A\,type}$$

The new rule uses the new type constructor $Relax$, instead of the defined notion of respect ($\prec$). Since respect is defined in terms of equality, respect-based equality was a rather annoying circularity in the rules, which made the soundness proof a nuisance. But that is *not* the main improvement. One could just make respect into a primitive type constructor to avoid the circularity.

The real improvement is that "relaxed equality" avoids the implicit quantification over types in the v0 formation rule. Notice that the v0 rule involves the types $A$ and $B$ which are not mentioned in the conclusion. Because of this, it was not clear at all how to give a strong inversion rule for equality formation. With relaxed equality, the inversion rules are rather obvious.

Despite this major organizational improvement, the relaxed equality formation rule is saying essentially the same thing as the respect-based equality rule. This is because of a lovely property of $Relax$: ($A \lt\!\!:\;Relax(B)$) if and only if ($A \prec B$). So some miscellaneous v0 rules about respect:

$$\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash A \prec A}
\qquad
\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash Comp \prec A}$$

are replaced by v1 rules about $Relax$:

$$\frac{\Gamma \vdash a \Vdash A}{\Gamma \vdash a \Vdash Relax(A)}
\qquad
\frac{\Gamma \vdash A\,type \qquad \Gamma \vdash t \Vdash Comp}
{\Gamma \vdash t \Vdash Relax(A)}$$

This allows the bootstrapping of general reasoning about respect to proceed in essentially the same way.

### Greatest type respected

To understand how $Relax$ avoids quantification in the equality formation rule, it's helpful to note that $Relax(A)$ is the greatest type (ordered by subtyping) that's respected by $A$. This is a corollary of that lovely subtyping characterization of $Relax$. So starting from the v0 rule, to know that $a$ and $b$ are elements of *some* types $A$ and $B$ that are respected by $C$, it's necessary and sufficient to check that $a$ and $b$ are elements of $Relax(C)$.

### Greatest partition that's a superset

There's another way to think about $Relax$. ($Comp \prec A$) is saying that any type $A$ is a [[subquotient]] of $Comp$. A subquotient can be decomposed as a subset followed by a quotient, or as a quotient followed by a subset. So what happens if you decompose some arbitrary type $A$ in these ways?

It turns out there's a unique subset of $Comp$ of which $A$ is a quotient. It's ($Comp \cap A$), the type of computations that are also elements of $A$.

It turns out that the other decomposition is *not* unique. But $Relax(A)$ is the greatest (ordered by subtyping) quotient of $Comp$ of which $A$ is a subset.

Now here's the cool part: Nuprl uses an equality formation rule that essentially uses the type ($A \cup Comp$) in place of our $Relax(A)$. (Except Nuprl calls it $Base$ instead of $Comp$.) And *that* type is the *least* quotient of $Comp$ of which $A$ is a subset!

Indeed, ($A \cup Comp$) can be understood as the type you get from $A$ by adding all computations, that *aren't* elements of $A$, as additional elements. Meanwhile, $Relax(A)$ instead adds *at most one* additional element, which is implemented by all computations that aren't elements of $A$. That is, ($A \cup Comp$) and $Relax(A)$ both add all the remaining computations, but ($A \cup Comp$) uses the finest possible equality, while $Relax(A)$ uses the coarsest.

### Kleene equality

Thinking of $Relax$ as adding at most one garbage element gives yet another way to think about it. The additional element can be regarded as an undefined element. It's the element of $Relax(A)$ whose realizers fail to denote an element of the desired type $A$. So $Relax$ is sort of like a lifted domain, and equality in a lifted domain is [[Kleene equality]]. Indeed, this gives the actual PER of $Relax$ used in the semantics:

$(a = a' \in Relax(A))\;\coloneqq\;(a \in A \vee a' \in A) \to (a = a' \in A)$

From that definition, the general intro and elim rules for the $Relax$ type constructor should be relatively clear.

What this means for the equality type is that while it's *strict* equality, when regarded as a relation on partial elements, it's *non-strict* when regarded as a type-valued operation. That is, ($a = a' \in A$) might be a valid type even if $a$ and/or $a'$ are not elements of $A$ (non-strict), but it cannot be *true* unless both $a$ and $a'$ are elements of $A$ (strict).

Meanwhile, ($a = a' \in Relax(A)$) is non-strict in both senses, in terms of potential elements of $A$. But for elements of $Relax(A)$, it's strict in both senses. If ($a = a' \in Relax(A)$) is a valid type, then $a$ and $a'$ are elements of $Relax(Relax(A))$. But that means they're elements of $Relax(A)$, because $Relax$ is idempotent. (You can't add computations to a type that already has all of them.)

All of this is provable internally, using the rules for $Relax$ and equality.

## Shortcut Beta Conversion {#BetaConv}

To take a break from the big, important changes, here's a minor, unimportant one. In v0, beta conversion was formulated as a judgment form ($\equiv_\beta$) which was defined to be the congruence closure of beta reduction. It turns out that that's kind of a minor nuisance to spell out in a HOAS presentation of the rules. But because $\lambda$ is the only binding form in the syntax, there's a shortcut for getting full congruence. (In general, this shortcut does not avoid congruence rules for binding forms.)

In v1, "partially-compatible beta reduction" ($\longrightarrow_\beta$) has only two congruence rules: one for $\lambda$, and one for the argument of an application. Plus it's not reflexive, symmetric, or transitive. But because the v1 direct computation rules explicitly allow reduction in either direction, and can implicitly be applied repeatedly, this is enough.

Obviously, consecutive applications of the direct computation rules allow rewriting with the reflexive, symmetric, transitive closure (equivalence closure) of ($\longrightarrow_\beta$). Let's call that ($\leftrightarrow_\beta$). It turns out to be the same as ($\equiv_\beta$).

What we seem to be missing is most of the congruence rules. But we have a trick: if ($a \leftrightarrow_\beta a'$), then

$b[a/x] \longleftarrow_\beta
(\lambda x.b)\,a \leftrightarrow_\beta
(\lambda x.b)\,a' \longrightarrow_\beta
b[a'/x]$

by application argument congruence (extended to the equivalence closure) and the beta rule.

So ($b[a/x] \leftrightarrow_\beta b[a'/x]$). This lets us rewrite in any context *if* the hole does not appear under binders, *or* the thing we're rewriting at least does not mention a bound variable. This actually seems to cover nearly all the cases of rewriting in practice, and then you don't even need to bother with congruence rules, which is nice.

But for the proof, what we need is that it means we effectively have congruence rules for all non-binding forms. And we really have the $\lambda$ congruence rule for the only binding form in the language. So we effectively have all the congruence rules.

## Let-Comp

Measured by utility, the most important change has got to be the addition of the "letcomp" rule:

$$\frac{\begin{array}{l}\Gamma \vdash a \Vdash A \qquad
\Gamma,y:A \vdash C\,type \\
\Gamma,x:Comp,x':Comp,h:(x = x' \in A) \vdash
p \Vdash c[x/y] = c'[x'/y] \in C[x/y] \\
x,x',h \notin FV(c,c')\end{array}}
{\Gamma \vdash q \Vdash c[a/y] = c'[a/y] \in C[a/y]}$$

In v0, quotienting was almost completely broken. It was [[CompLF#PERtheory|explained]] how it was *supposed* to work, with parenthetical remarks that it didn't yet seem to work. In v1, letcomp is what makes it work.

Another solution presumably would've been to add a stronger elimination rule to PER comprehension. But this would not be taking full advantage of PER semantics, where quotienting is intuitively part of the very meaning of the judgments, and all types are implicitly subquotients.

Letcomp is a subquotient elimination rule, formulated to work on an arbitrary type by regarding it as a subquotient of $Comp$. The name "letcomp" is based on the observation that it binds an element as a general pair of related computations.

Letcomp can also be understood as internalizing the meaning of the semantic hypothetical judgment form:

$(x:A \gg c = c' \in C)\;\leftrightarrow\;((A\,type) \to ((x:A \gg C\,type) \wedge \forall a,a'.(a = a' \in A) \to (c[a/x] = c'[a'/x] \in C[a/x])))$

With this grand purpose as an attempt to complete the internalization of the PER semantics, it may not be surprising that letcomp is very useful for deriving rules for type constructors defined by PER comprehension. But it's not perfect. Rules that involve metavariables without an associated typing premise tend to cause trouble. Alas, it seems very difficult to do much about that. ("Pullback" types à la [Melliès & Zeilberger](#MZFuncRefine) might address the most serious gaps.) Notice however that intrinsic dependent type systems would not need rules with metavariables without typing premises. So the ability to derive type constructors and their rules seems quite substantial already.

There was actually an early version of letcomp for v0. But the soundness of letcomp was not established until after changing the semantics to support primitive inversions.

## Natural Numbers Type

CompLF v1 adds a type $Nat$ of [[Dana Scott|Scott]]-encoded natural numbers. The Scott nats themselves are not new, of course. What's new is having them collected into an inductive type, which actually gives CompLF some serious proof-theoretic strength. It's expected to have the same strength as (first-order) [[Peano arithmetic]], but the upper bound has not been checked.

The motive premise cannot be avoided in the $Nat$ elimination rule. One probable reason is that that would be too strong, since it would allow type-level recursion. But another reason has to do with technical details of PER semantics. (TODO: Explain.) Nuprl's version of induction actually *does* avoid the motive premise. (Nuprl's logic is much stronger than Peano arithmetic, by the way.) For some, this was a major advantage of Nuprl, since it's a way to get nontrivial proofs of termination for recursive functions. But CompLF must pursue alternatives. (TODO: Explain!)

## Identity Types {#IdType}

TODO

## Miscellaneous

Certain rules in v0 (equality formation and PER formation) used non-dependent function types ($\to$) to express implications. In v1, non-dependent family intersection types ($\supset$) is used (in relax introduction and PER formation) instead. In some cases, the propositions involved are guaranteed to be proof-irrelevant, so it doesn't matter. In PER formation, there's no guarantee that $R$ is proof-irrelevant, but there's no good reason for the user to use a proof-relevant relation, since the proof is ignored. In both versions of PER formation, you can run into trouble trying to use a proof-relevant relation. (So the change doesn't help or hurt.)

In v0, there was a reflexivity rule for equality, in addition to the uniqueness and selectivity rules. That was redundant. So now reflexivity is derived from uniqueness and select left.

There's been some reordering of rules, premises, and renaming of metavariables.

## References

* {#MZFuncRefine} Paul-André Melliès, Noam Zeilberger, _Functors are Type Refinement Systems_, POPL 2015 ([pdf](https://www.irif.fr/~mellies/papers/functors-are-type-refinement-systems.pdf))