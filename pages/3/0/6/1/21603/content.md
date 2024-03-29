
#Contents#
* table of contents
{:toc}

## Idea

The [[CompLF v1|rules of CompLF]] have been designed so that [[structural rules]] (e.g. weakening and substitution) are admissible, and the remaining rules can be expressed as higher-order abstract syntax (HOAS) axioms in [[logical frameworks]] like [[LF]] or [[Isabelle]]/Pure. (Except the variable rule, which isn't needed in HOAS form.) This is a significant (but superficial) difference from Nuprl. Two major interesting things happen with this HOAS formulation of CompLF.

First, the HOAS formulation highlights a connection between dependent type systems and partial logic. The connection is there for all dependent type systems formulated as deductive systems with judgments on raw terms (untyped [[abstract syntax]] trees), but Nuprl-like systems make more use of the connection than most.

Second, although the rules are not algorithmic, there is implicit propagation of type validity facts in the semantics, which is analogous to the type propagation of a dependent type checker. The primitive typing judgment form ($a \Vdash A$) outputs validity of the type ($A\,type$). But using the inversion rules, it's possible to derive rules for a defined typing judgment form that inputs type validity. This will hopefully be useful for verifying a bidirectional proof checker for CompLF and similar systems.

## Second-order formulation of rules

This section repeats some of the rules of v1 in HOAS style, since variables and substitution (of terms) are technically expressed differently. For convenience, here is the $Nat$ elimination rule from [[CompLF v1|v1]]:

$$\frac{\begin{array}{l}
\Gamma \vdash n \Vdash Nat \qquad
\Gamma,x:Nat \vdash C\,type \\
\Gamma \vdash c \Vdash C[zro/x] \\
\Gamma,x:Nat,h:C \vdash c \Vdash C[suc(x)/x]
\end{array}}
{\Gamma \vdash c \Vdash C[n/x]}$$

And here it is in a traditional HOAS form:

$natElim\,:\,\forall n,c,C.(n \Vdash Nat) \Rightarrow
(\forall x.(x \Vdash Nat) \Rightarrow (C(x)\,type)) \Rightarrow$  
$\qquad (c \Vdash C(zro)) \Rightarrow
(\forall x,h.(x \Vdash Nat) \Rightarrow (h \Vdash C(x)) \Rightarrow (c \Vdash C(suc(x)))) \Rightarrow$  
$\qquad (c \Vdash C(n))$

So in the HOAS formulation of rules, the judgment forms are atomic relation symbols in a predicate logic, and the rules are axioms. Note that $C$ in this example rule is a *function* in the HOAS formulation. But it's a function of the logical framework, not of the object language. When rules quantify over functions, that's second-order quantification.

Translating ordinary rules into HOAS lands in a second-order fragment. There's a somewhat standard notation for rules of this fragment, which leaves the quantifiers implicit, and more resembles ordinary rules. (Meta)variables "declared" to the left of a turnstile in a "premise" are quantified just in that premise; the rest are quantified at the outside of the rule. Note that all the premise-local quantifiers only quantify over terms, which is first-order. Here is $natElim$ in this "second-order" notation:

$$\frac{\begin{array}{l}
n \Vdash Nat \qquad
x:Nat \vdash C[x]\,type \\
c \Vdash C[zro] \\
x:Nat,h:C[x] \vdash c \Vdash C[suc(x)]
\end{array}}
{c \Vdash C[n]}$$

Much nicer, right? Note that the variable declarations effect both a quantifier and a typing hypothesis. So the special status of typing judgments working like context entries is built into the notation.

The rest of the rules we repeat in HOAS form will be given now in this second-order notation. Many rules will not be repeated because there's no guesswork in translating them.

### Miscellaneous

$$\frac{a \Vdash A}{A\,type}$$

### Equality

$$\begin{gathered}
\frac{a \Vdash A}{q \Vdash p1 = p2 \in (a = a \in A)} \\
\\
\frac{p \Vdash a = a' \in A}{a \Vdash A} \\
\\
\frac{p \Vdash a = a' \in A \qquad
x:A \vdash C[x]\,type \qquad
c \Vdash C[a]}
{c \Vdash C[a']}
\end{gathered}$$

### Identity

$$\frac{p \Vdash t \equiv t' \qquad c \Vdash C[t]}{c \Vdash C[t']}$$

### Functions

$$\begin{gathered}
\frac{A\,type \qquad x:A \vdash B[x]\,type}{\Pi x:A.B[x]\,type} \\
\\
\frac{\Pi x:A.B[x]\,type}{A\,type} \\
\\
\frac{\Pi x:A.B[x]\,type \qquad a \Vdash A}{B[a]\,type} \\
\\
\\
\frac{f \Vdash \Pi x:A.B[x] \qquad a \Vdash A}{f\,a \Vdash B[a]} \\
\\
\frac{A\,type \qquad
x:A \vdash p[x] \Vdash f\,x = f'\,x \in B[x]}
{q \Vdash f = f' \in \Pi x:A.B[x]}
\end{gathered}$$

### Intersection

$$\begin{gathered}
\frac{b \Vdash \cap x:A.B[x] \qquad a \Vdash A}{b \Vdash B[a]} \\
\\
\frac{A\,type \qquad
x:A \vdash p[x] \Vdash b = b' \in B[x]}
{q \Vdash b = b' \in \cap x:A.B[x]}
\end{gathered}$$

### Subset

$$\begin{gathered}
\frac{x:A \vdash B[x]\,type \qquad
a \Vdash A \qquad b \Vdash B[a]}
{a \Vdash \{x:A | B[x]\}} \\
\\
\frac{a \Vdash \{x:A | B[x]\} \qquad
x:A,y:B[x] \vdash c[x] \Vdash C[x]}
{c[a] \Vdash C[a]}
\end{gathered}$$

### Computations

$$\begin{gathered}
\frac{x:Comp \vdash b[x] \Vdash Comp}{\lambda x.b[x] \Vdash Comp} \\
\\
\frac{\begin{array}{l}
a \Vdash A \qquad
y:A \vdash C[y]\,type \\
x:Comp,x':Comp,h:(x = x' \in A) \vdash
p[x,x',h] \Vdash c[x] = c'[x'] \in C[x]
\end{array}}
{q \Vdash c[a] = c'[a] \in C[a]}
\end{gathered}$$

### Booleans

$$\frac{b \Vdash Bool \qquad
c \Vdash C[tru] \qquad
c \Vdash C[fls]}
{c \Vdash C[b]}$$

### PER

$$\begin{gathered}
\frac{\begin{array}{l}
x1:Comp,x2:Comp \vdash R[x1,x2]\,type \\
y1:Comp,y2:Comp \vdash s[y1,y2] \Vdash R[y1,y2] \supset R[y2,y1] \\
y1:Comp,y2:Comp,y3:Comp \vdash t[y1,y2,y3] \Vdash R[y1,y2] \supset R[y2,y3] \supset R[y1,y3]
\end{array}}
{\{x1 = x2 | R[x1,x2]\}\,type} \\
\\
\frac{\begin{array}{l}
p \Vdash t1 = t2 \in \{x1 = x2 | R[x1,x2]\} \\
R[t1,t2]\,type \\
h:R[t1,t2] \vdash c \Vdash C
\end{array}}
{c \Vdash C}
\end{gathered}$$

## Judgment-level reasoning {#JudgReason}

Reasoning at the judgment level using this logical framework is not as convenient as having a type checker for terms, or even as convenient as having a Nuprl-like proof refiner that extracts the realizers. But it's very straightforward and expressive. It can be used to prove derived rules, and other facts about derivability that aren't of the form to be rules. For example, you can show that adding a certain new rule would allow deriving a contradiction.

Many unusual phenomena of Nuprl-like systems become clearer when analyzed in terms of judgment-level reasoning.

### Vs reasoning about Reflected Judgments

In Nuprl-like systems, the semantic judgments are reflected internally as squashed types, and can be reasoned about using propositions-as-types. The logical framework gives us a way to reason about formal judgments. Aside from the ability to reason about "large" judgment forms like type validity, is this judgment-level reasoning actually different from internal reasoning? It turns out it is.

For example, consider the framework formula:

$$\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$$

The puzzle is to find, assuming ($A\,type$) and ($B\,type$), a type that's provably inhabited if and only if that formula is derivable. In more detail, we want some framework function $R$ such that:

$$\forall A,B.(A\,type) \Rightarrow (B\,type) \Rightarrow
((\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)) \Leftrightarrow (\exists p.p \Vdash R(A,B)))$$

A couple of perhaps-plausible-looking solutions for $R(A,B)$ are ($\Pi t:Comp.(t \in A) \to (t \in B)$) and ($\Pi t:\top.(t \in A) \to (t \in B)$). But both of these are wrong. The first is too weak (you get left-to-right only) and the second is not even a type (which makes existence of an element too strong).

The framework formula we're trying to represent turns out to be asserting that $A$ is a subtype of $B$, since it can be read as a special case of the subsumption rule:

$$\frac{t \Vdash A}{t \Vdash B}$$

So we can take $R(A,B)$ to be ($A \lt\!\!:\;B$). In fact, the first wrong answer is what we called "inclusion" ($\subseteq$).

#### Open vs "Closed Terms"

So how come ($\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$) and ($\Pi t:Comp.(t \in A) \to (t \in B)$) don't correspond? I mean, the intuitive reason is that subtyping is not just member inclusion, it must also preserve equations. But what is the formal reason? We have the fact that

$$\forall p.(a \Vdash A) \Leftrightarrow (p \Vdash a \in A)$$

so the difference between ($\Vdash$) and ($\in$) is not the mismatch. The mismatch turns out to be the quantifiers used.

It turns out ($\Pi t:Comp.(t \in A) \to (t \in B)$) is inhabited if and only if ($\forall t.(t \Vdash Comp) \Rightarrow (t \Vdash A) \Rightarrow (t \Vdash B)$). So there's an extra ($t \Vdash Comp$) requirement making inclusion weaker than subtyping.

If you think about how adequacy of a HOAS representation works, the logical framework quantifiers over terms are quantifying over *open* terms, specifically. Meanwhile the object language quantifiers range over the elements of a type, and in the PER semantics, elements of types are represented by *closed* terms. The open terms behave differently because PER semantics also enforces respect for typed equality, and in the formal system, this requirement is implicit.

But equality at the $Comp$ type is just computational equivalence, which is respected by all the semantic judgments. So when dealing with computations, the implicit respect requirements are vacuous, and the framework reasoning about arbitrary open terms closely resembles semantic reasoning about arbitrary closed terms. This might be part of the reason why $Comp$ is sometimes glossed as the type of all closed terms, although this technically doesn't make sense. (Semantically, many types contain all the closed terms, while syntactically, no type can rule out variables.)

Another reason for the intuition that $Comp$ is the type of closed terms is that there's an admissible rule saying that any closed term has type $Comp$. (This rule cannot be represented in HOAS style without some modal trick. The proof is by structural induction on the term, and uses the appropriate computation formation rule in each case. The motive needs to be generalized in order to handle binding forms.)

Returning to the issue of subtyping vs inclusion, one could think of inclusion as the closed special case of subtyping. It's only because of the restriction to $Comp$ that the ($(t \in A) \to (t \in B)$) part corresponds to ($(t \Vdash A) \Rightarrow (t \Vdash B)$), as explained in the next section.

#### Presuppositions

So if quantifying over $Comp$ adds an undesired ($t \Vdash Comp$) requirement, quantifying over $\top$ seems closer, since the requirement ($t \Vdash \top$) is trivial. But in general, ($\Pi t:D.(t \in A) \to (t \in B)$) corresponds to ($\forall t.(t \Vdash D) \Rightarrow ((t \in A)\,type \wedge ((t \Vdash A) \Rightarrow (t \Vdash B)))$). With ($t \Vdash Comp$), ($(t \in A)\,type$) is derivable, but in general, its derivability depends on $t$ and $A$.

So since ($t \Vdash \top$) is trivial, ($\Pi t:\top.(t \in A) \to (t \in B)$) corresponds to just ($\forall t.(t \in A)\,type \wedge ((t \Vdash A) \Rightarrow (t \Vdash B))$), but the ($\forall t.(t \in A)\,type$) part is too strong. Due to relaxed equality, it's saying that $Relax(A)$ is basically the same as $\top$, which is usually not so.

The root of the problem is that ($f \Vdash \Pi x:A.B[x]$) is not interderivable with ($x:A \vdash f\,x \Vdash B[x]$) in general, but rather ($(A\,type) \wedge (x:A \vdash f\,x \Vdash B[x])$). From the perspective of [[intrinsic and extrinsic views of typing|intrinsic typing]], it doesn't make sense to regard ($A\,type$) as part of the *truth* of ($f \Vdash \Pi x:A.B[x]$). Instead, it's a "presupposition": something that has to be true for ($f \Vdash \Pi x:A.B[x]$) to even *make sense*.

The full presupposition of ($f \Vdash \Pi x:A.B[x]$) is ($(\Pi x:A.B[x])\,type$). That ($f \Vdash \Pi x:A.B[x]$) is interderivable with ($(A\,type) \wedge (x:A \vdash f\,x \Vdash B[x])$), and not ($(\Pi x:A.B[x])\,type \wedge (x:A \vdash f\,x \Vdash B[x])$), ($(\Pi x:A.B[x])\,type \Rightarrow (x:A \vdash f\,x \Vdash B[x])$), or something even weirder, is due to the "presupposition policy" the judgment forms are using. (Is there a better term for this?) (Technically, ($(\Pi x:A.B[x])\,type \wedge (x:A \vdash f\,x \Vdash B[x])$) is also interderivable, but it redundantly checks ($x:A \vdash B[x]\,type$).)

As a practical matter, presuppositions don't validate themselves, so a proof assistant needs some policy on when/how they get validated. In Nuprl-like systems, the presuppositions are all instances of the type validity judgment. Although they generally cannot be checked automatically, as mentioned in the [idea section](#idea), propagation of type validity resembles type propagation in a type checker.

Validity/definedness of type expressions is propagated differently than elements of the types are. Various formation and inversion rules for type constructors, combined with various typing judgment forms, yield various styles of type (validity) propagation, and provide a policy for handling presuppositions. This is a running theme of this page.

A related approach to presupposition policy comes from *partial logics*: logics in which formulas may not be meaningful propositions, in the sense that they fail to denote a truth value. The case in type theory is the possibility of type expressions that are not valid, in that they don't denote a semantic type. But classical partial logics provide a different perspective on non-denoting formulas, which avoids having any primitive validity judgment. This is discussed in [later sections](#PartLogic).

If the presuppositions can be checked automatically (as in most dependent type checkers), the presupposition policy is not so visible to the user, but it's still there. When trying to represent judgment-level assertions as types though, the details of the presupposition policy become important.

Getting back to ($\Pi t:\top.(t \in A) \to (t \in B)$) failing to correspond to ($\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$), the problem is that the forms of implication generally don't correspond, due to the implicit requirement to check that the type-level implication is a valid type. Assuming a *type* incurs an obligation to show that the expression is in fact a type, while assuming a *judgment* has no implicit obligation.

#### Type Expressions differing only in their Presuppositions {#DiffPresup}

It looks like the type-level assumption ($(t \in A) \to ...$) is not going to work. Let's take a closer look at what the solution ($A \lt\!\!:\;B$) is doing instead. Subtyping was defined as:

$A \lt\!\!:\;B\;\coloneqq\;(\lambda x.x) \in (A \to B)$

Using the computation formation rules, we have ($\lambda x.x \Vdash Comp$). By assumption, we have ($A\,type$) and ($B\,type$), so by $\Pi$ formation, we have ($(A \to B)\,type$). Finally, equality formation gives us ($(\lambda x.x) \in (A \to B)$).

That this sort of representation is a type at all is actually the clever part. Using the representation of ($t \Vdash T$) as ($t \in T$), and the rules for functions, it's now straightforward that ($A \lt\!\!:\;B$) represents ($\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$).

But it seems like there's a less tricky solution: ($\Pi a:A.a \in B$). Both ($A \lt\!\!:\;B$) and this assume $A$ itself, rather than ($t \in A$). And that *is* the way you're supposed to do it in type theory, after all. The standard wisdom is that typing judgments are not something you can assume. We have just covered in detail *why* that is still the case with Nuprl-like extensions.

($\Pi a:A.a \in B$) does technically solve the problem: if ($A\,type$) and ($B\,type$), then

$\forall p.(\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)) \Leftrightarrow (p \Vdash \Pi a:A.a \in B)$

This implies that ($\Pi a:A.a \in B$) is inhabited when it should be, and is squashed, moreover. There's something disappointing about this solution though: while ($A \lt\!\!:\;B$) is a type whenever $A$ and $B$ are, validity of ($\Pi a:A.a \in B$) entails that ($a:A \vdash a \Vdash Relax(B)$). In other words, that $A$ equality is respected in $B$. This should only be a *consequence* of subtyping, not a *presupposition* of it.

Specifically,

* $(A \lt\!\!:\;B)\,type \Leftrightarrow (A\,type \wedge (\underline{\;}:A \vdash B\,type))$ and
* $(\Pi a:A.a \in B)\,type \Leftrightarrow (A\,type \wedge (a:A \vdash a \Vdash Relax(B)))$.

So these semantic judgments are true at the same time, but have different presuppositions. For the problem of representing semantic judgments as types, it seems that the moral of the story is to close off a term as much as possible before reasoning about membership, if you want to avoid presuppositions.

#### Related Pairs of Computations

There is actually another solution though: the big-hammer approach of reasoning about pairs of computations: ($\Pi t:Comp.\Pi t':Comp.(t = t' \in A) \to (t = t' \in B)$). This representation makes it explicit that subtyping implies respect for equality. Thanks in part to the let-comp rule, this type is completely equivalent to ($A \lt\!\!:\;B$): the presuppositions are the same, and they have the same PER.

#### Lessons

The puzzle of representing the subtyping judgment as a type operation has been chosen because the discussion of solutions, plausible false solutions, and partial solutions touches upon many important issues of judgment-level reasoning. Here is a summary of important lessons we tried to convey:

* The judgment forms that have interesting presuppositions are the *semantic* judgment forms, which are implemented as *type* operations.
* The presupposition(s) of a semantic judgment represented as a type are simply the things you need to show in order to show that the type is valid.
* The formal judgment forms don't have interesting presuppositions; only that the expressions involved are syntactically well-formed, which can be checked while parsing.
* Type-level implication ($A \to B$) and judgment-level implication ($X \Rightarrow Y$) are not the same, even when the types $A$ and $B$ represent the corresponding judgments $X$ and $Y$, because of presuppositions.
* Two type expressions can have the same meaning in case they're both meaningful, but differ in their presuppositions, the conditions under which they're meaningful.
* Respect for typed equality is automatically enforced by "open" reasoning about arbitrary elements, but can/must be done manually when doing "closed" reasoning about computations.

All but the last point also apply—via propositions-as-types—to a style of partial logic that [[Peter Aczel]] called "Frege structures". Partial logic, Frege structures, and the connection to Nuprl-like systems are discussed [below](#PartLogic).

The last point—about respect for equality, except when dealing with elements of a particular type—seems very peculiar to PER semantics. You don't need PER semantics to get those other "Frege phenomena", and you don't need PER semantics to get implicit respect for extensional equality, but the way they interact in PER semantics is quite extraordinary.

### "Non-negatable" Types {#NonNegate}

We have [seen](#DiffPresup) that just because a judgment form is representable as a type operation doesn't mean that that type operation gets you a valid type in all the situations you might want. In the most extreme case of this, the type is only meaningful when it's true. In other words, the type presupposes itself. Karl Crary [called](#KCThesis) these types "non-negatable", since they're intuitively either true or nonsense, never false. Assuming a non-negatable type with a type-level implication is guaranteed to be useless, since you must prove it in order to safely assume it.

#### Membership in a Type (Formerly)

Crary's main example of a non-negatable type was membership ($a \in A$). Membership is not non-negatable in Nuprl anymore, since Nuprl switched to a more liberal equality. It's also not non-negatable in CompLF, which uses relaxed equality. Membership is still "harder to negate" than one might like, as we saw.

But in Martin-Löf type theory, and earlier versions of Nuprl, the equality semantic judgment/type ($a1 = a2 \in A$) presupposes ($a1 \in A$) and ($a2 \in A$). Since the membership *type* ($a \in A$) is an abbreviation for equality ($a = a \in A$), it presupposed itself. (With membership non-negatable, Crary added subtyping as a primitive type constructor, or else it would've been non-negatable as well.)

#### Type Validity {#TpOK}

There is another semantic judgment which is still non-negatable: type validity. It's kind of a weird trick that this judgment is representable as a type. (Coincidentally, Crary noticed the trick, and used it, arguing that it was more convenient than membership in an arbitrary universe.) It sounds like there'd be a size paradox, right? Well that's why there's probably nothing that can be done about the non-negatability.

So what's the big trick? Basically, to use almost any trivially true proposition that mentions the type. We'll use:

$TpOK(A)\;\coloneqq\;A \supset \top$

The trick is that it's only "trivially true" when it's a valid type, which requires that $A$ is a valid type. So it's either true or nonsense; it's non-negatable. We have:

$\forall p.(A\,type) \Leftrightarrow (p \Vdash TpOK(A))$

The right-to-left direction crucially relies on the sanity rule ($(a \Vdash A) \Rightarrow (A\,type)$) and an inversion rule.

#### Membership in a Type (Sometimes)

Although membership is not *always* non-negatable anymore, because ($a \in A$) presupposes ($a \Vdash Relax(A)$), it's still non-negatable whenever $A$ and $Relax(A)$ are the same. This is precisely when $A$ is a quotient of $Comp$. (And in that case, Nuprl's ($A \cup Comp$) would be the same as well, so Nuprl's membership would also be non-negatable.)

### Combined Truth {#CombTruth}

Hopefully, the [representability of type validity](#TpOK) shows better what's "really" going on with representability of judgment forms. When truth of a squashed type is used at the judgment level, it's not just the intuitive truth—which *presupposes* validity—that's being used; it's some "combined truth", which *implies* validity, via the sanity rule.

When assuming the truth of a type using type-level implication, you assume the usual truth, and presuppositions are accumulated. But when assuming the truth of a type using judgment-level implication, you assume combined truth. Keep in mind that the derivation rules themselves are all assertions of judgment-level implications, and are thus working with combined truth.

So technically, combined truth comes from the ($a \Vdash A$) formal judgment form, when we only really care about whether $A$ is inhabited. In general, ($a \Vdash A$) says that $A$ is a type, and $a$ is an element of it. Meanwhile the type ($a \in A$) intuitively says that $a$ is an element of $A$, *presupposing* ($a \Vdash Relax(A)$). Since the latter *implies* that $Relax(A)$—and therefore $A$—are types, ($a \in A$) indirectly presupposes that $A$ is a type. Combined truth of ($a \in A$) combines its intuitive truth with its presuppositions, and thus ends up the same as ($a \Vdash A$).

As for $TpOK(A)$, the intuitive truth is vacuous, and the presupposition is basically just that $A$ is a type, so the combined truth of $TpOK(A)$ says that $A$ is a type.

#### Elimination into Combined Truth {#CombElim}

Some of the elimination rules do not have a premise requiring that the elimination motive be a valid type family. The substitution instance of the motive appearing in the conclusion still must be a valid type, due to combined truth. But the validity of that substitution instance follows from the validity of substitution instances obtained from the premises.

This is the case for identity elimination (rewrite), subset elimination, $Bool$ elimination, and PER comprehension elimination. Although they're ostensibly not eliminating anything, the direct computation rules are similar in that they can be used to rewrite with beta conversion in any typing goal.

Because combined truth allows many semantic judgment forms—even [type validity](#TpOK)—to be represented as typing judgments, these "combined elimination" principles are stronger than they may look.

A common problem with the representation of judgment forms as type operations is the reliance on combined truth, which means that presuppositions are carrying some or all of the weight, but they don't get propagated in the same way as ordinary truth.

If an elimination rule requires a premise showing that the motive is a valid type family, the presupposition part of combined truth effectively has to be shown prior to the application of the rule. In other words, such ordinary elimination rules help to conclude ordinary truth only. But with a combined elimination rule, there is no motive validity premise, so the rule helps to conclude the combined truth of the motive.

Here are some consequences of combined elimination on represented judgments:

* You can beta convert in the subject of a typing judgment, not just the type.
* You can beta convert in a type validity judgment.
* Same goes for rewriting with an identity.
* You can branch on a boolean in a valid type.

That last one—type-level branching—is provided by the following derived rule:

$$\frac{b \Vdash Bool \qquad T\,type \qquad F\,type}{(b\,T\,F)\,type}$$

This is shown by eliminating $b$ with the motive ($C[x] \coloneqq TpOK(x\,T\,F)$). Since type validity is non-negatable, we would not be able to show this motive to be valid except by proving each case. But proving each case is exactly why we want to use $Bool$ elimination in the first place! So without the combined elimination, we'd be in an infinite regress. As for proving each case, it goes by beta reducing the applied Church boolean, yielding one of the premises.

### Identity {#IdType}

($t1 = t2 \in Comp$) intuitively says that $t1$ and $t2$ are computationally equivalent. But it presupposes that $t1$ and $t2$ are computations, so the combined truth is that $t1$ and $t2$ are the same computation.

The identity type ($t1 \equiv t2$) also says that $t1$ and $t2$ are computationally equivalent, but the presupposition has been weakened, so that combined truth does *not* imply that $t1$ and $t2$ are computations.

Because computational equivalence does not respect typed equality, except for the $Comp$ type (and its subtypes), ($t1 \equiv t2$) is not generally a type unless $t1$ and $t2$ are computations. That is, it's only a type family over a pair of computations. But surprisingly, some instances of identity are valid types although $t1$ and $t2$ are not computations. In particular, if the terms $t1$ and $t2$ are computationally equivalent, ($t1 \equiv t2$) is (combined) true.

That identity is often not known to be a type doesn't get in the way of assuming it with *judgment-level* implication. For example, you can prove derived rules showing that identity is symmetric and transitive. Indeed, identity is in some sense the "real" equality of judgment-level reasoning: it's intuitively a relation on *terms*, not elements of a type; it's an equivalence relation; and it rewrites in any open type expression, not just valid type families.

(TODO: Explain how many presuppositions arise from intensional type equality, and that equality of identity types is extensional, making them valid when they're pointwise true. Maybe on another page.)

## Checking Mode {#CheckingMode}

The sanity rule says that the usual formal typing judgment ($a \Vdash A$) implies type validity ($A\,type$). This is analogous to the *admissible* sanity rule of unidirectional typing rules:

$$\frac{\Gamma\,ctx \qquad \Gamma \vdash a\,:\,A}{\Gamma \vdash A\,type}$$

In a unidirectional type checker, type validity being a conclusion of sanity goes well with the type expression itself being an output of the type checker. In a [[bidirectional typechecking|bidirectional type checker]], there are two modes: "synthesizing mode" inputs a term and (if it succeeds) outputs a type it has, and "checking mode" inputs a term and a type, and checks the term against the type.

Although CompLF's primitive rules are not algorithmic, we can think of the typing judgment ($a \Vdash A$) as corresponding to the synthesizing mode of bidirectional typing, due to the sanity rule. This section defines another formal judgment form (logical framework predicate) to correspond to the checking mode, and derives rules that propagate type validity bidirectionally.

### Basics

Here is the defined judgment:

$A \ni a\;\coloneqq\;(A\,type) \Rightarrow (a \Vdash A)$

The intuition is that a derivation of ($a \Vdash A$) includes a derivation of ($A\,type$), which is accessed using the sanity rule. So any rule that concludes with a judgment of form ($a \Vdash A$) is effectively outputting a derivation of type validity as well as typing.

By defining ($A \ni a$) as an implication assuming type validity, a rule that concludes with a judgment of that form will be implicitly taking the type validity judgment as an extra premise, and inputting a derivation of it. (Intuitively, ($A \ni a$) inputs *and* outputs type validity, but it doesn't matter because ($X \Rightarrow (X \wedge Y)$) is equivalent to ($X \Rightarrow Y$).)

So synthesizing mode ($a \Vdash A$) outputs type validity, while checking mode ($A \ni a$) inputs it. We can immediately derive the rules that change direction:

$$\frac{a \Vdash A}{A \ni a} \qquad
\frac{A\,type \qquad A \ni a}{a \Vdash A}$$

The rule on the left has type validity coming in from both directions. For algorithmic rules, the types themselves would be coming in, and they would need to be compared. The rule here would just mean to check that they're syntactically equal, and an algorithm for dependent type checking would usually do something much smarter. But since these rules are not algorithmic, we just do the stupid thing for illustration purposes.

The rule on the right explicitly takes type validity, and propagates it out in both directions. In algorithmic rules, the type itself would need to be given to the rule via a type annotation on the term in the conclusion.

Here's a more interesting direction change rule using subsumption:

$$\frac{t \Vdash A \qquad A \lt\!\!:\;B \ni p}{B \ni t}$$

Deriving this rule, we receive the validity of $A$ from the first premise, and the validity of $B$ from the conclusion, form the validity of ($A \lt\!\!:\;B$) in order to use the second premise, which lets us change $t$ from an $A$ to a $B$.

### Functions

With a unidirectional type checker (that does not use nonlocal inference), lambdas need a type annotation for the function domain. This corresponds to the type validity premise in the (derived) lambda rule of CompLF:

$$\frac{A\,type \qquad x:A \vdash b[x] \Vdash B[x]}{\lambda x.b[x] \Vdash \Pi x:A.B[x]}$$

As with bidirectional type checking, we can avoid this by making the rule checking mode:

$$\frac{x:A \vdash B[x] \ni b[x]}{\Pi x:A.B[x] \ni \lambda x.b[x]}$$

Note that ($x:A \vdash B[x] \ni b[x]$) is notation for ($\forall x.(x \Vdash A) \Rightarrow (B(x) \ni b(x))$). That is, context entries are always synthesizing mode in our notation.

The unidirectional rule for function application receives two candidates for the domain of the function: one from the function itself, one from the argument. So it needs to compare them. The bidirectional rule eliminates (or at least postpones) this check by using checking mode on the argument. We can derive an analogous rule for CompLF:

$$\frac{f \Vdash \Pi x:A.B[x] \qquad A \ni a}{f\,a \Vdash B[a]}$$

(TODO: Put up more rules)

### Caveat

When reasoning at the judgment level, the bidirectional rules don't actually seem to make most things easier, and they make many things less convenient. There are now two judgment forms for typing, making rules incompatible without manually switching directions. Avoiding type validity premises is *usually* not that helpful because those premises are usually easy, so it's easier to just follow your nose through them than cleverly avoid them. Since a main point of judgment-level reasoning is to derive new rules, sticking to a bidirectional style tends to multiply the number of derived rules you want, creating extra work.

It seems like a better idea to postpone a serious attempt at a bidirectional rule set until you have an actual algorithm in mind. At that point, the defined checking mode judgment might make it much easier to prove sound those bidirectional rules you will actually use.

Sometimes though, even for judgment-level reasoning, bidirectional rules can avoid a large number of very silly subgoals, like when introducing an element of a deeply nested type. In this case, the unidirectional rules would make you prove many copies of the same type validity goals, and bidirectional rules are the perfect plumbing.

## Strengthening Type Validity {#StrTpV}

Most of the primitive type constructors have inversions for their formation rules. When deriving rules for a new "type constructor" defined using PER comprehension, an extra trick or two are needed to get the inversion rules you want.

The reason why inversion rules are usually desirable when deriving a type constructor is that the elimination rules typically need to know that the subexpressions of the type being eliminated are well-typed. (Type subexpressions are valid; element subexpressions have the appropriate type.) These facts are proven when forming the type, so it's only fair to be able to get back what you've paid for. Otherwise they would need to be proven again whenever applying an elimination rule. (This is assuming the derived rules are for the primitive typing judgment, where the introduction rules establish type validity. For [checking mode](#CheckingMode) rules you would expect introduction rules to avoid that, but this also requires inversion rules.)

The PER comprehension type constructor itself does not have any formation inversion rules. Partially this is because a later version of CompLF may strengthen the introduction rules in a way that's incompatible with the obvious inversion rule. But mostly it's because the inversion rule wouldn't really help. It's easier and more flexible to add your own type validity conditions than to take whatever falls out of the PER comprehension.

For example, suppose we're deriving $\Sigma$ types. We should start with the PER for a $\Sigma$ type:

$\Sigma' x:A.B[x]\;\coloneqq\;\{p = p' | \exists a,a',b,b':Comp.a = a' \in A \wedge b = b' \in B[a] \wedge p \equiv \lang a,b \rang \wedge p' \equiv \lang a',b' \rang\}$

Where $\exists$ is defined as a squashed subset, and $\lang a,b \rang$ is some encoding of ordered pairs, suppose.

We could try to derive the inversion rules

$$\frac{\Sigma' x:A.B[x]\,type}{A\,type} \qquad
\frac{\Sigma' x:A.B[x]\,type \qquad a \Vdash A}{B[a]\,type}$$

for $\Sigma'$ somehow by pulling things out of that (relatively) complicated PER comprehension. But it's easier to just define another type operation ($\Sigma x:A.B[x]$) to be just like ($\Sigma' x:A.B[x]$), but only a valid type if ($\Pi x:A.B[x]$) is. (The choice of $\Pi$ over the other type constructors with the same validity conditions is arbitrary.)

### Type Validity {#TpV}

We can define a utility type constructor to add a type validity condition to another type, while leaving its PER unmodified:

$TpV(A | B)\;\coloneqq\;TpOK(B) \supset A$

Intuitively, we want some kind of validity-level conjunction, so it's unintuitive that this definition uses implication (non-dependent intersection). But for validity, type-level implication *is* actually a conjunction. (That's another way to see why type-level implications mess up reasoning about combined truth.)

If we used

$TpV(A | B)\;\coloneqq\;\{\underline{\;}:A | TpOK(B)\} \qquad (wrong)$

it would only add the validity condition ($\underline{\;}:A \vdash B\,type$). And if we used

$TpV(A | B)\;\coloneqq\;TpOK(B) \wedge A \qquad (wrong)$

it would squash $A$, so the PER would generally not be the same. ($TpOK(B) \supset A$) is not the only way to do it, but it seems like a good way to do it.

Here are the derived rules for $TpV$:

$$\begin{gathered}
\frac{A\,type \qquad B\,type}{TpV(A | B)\,type} \\
\\
\frac{TpV(A | B)\,type}{A\,type} \qquad
\frac{TpV(A | B)\,type}{B\,type} \\
\\
\\
\frac{B\,type \qquad a \Vdash A}{a \Vdash TpV(A | B)} \\
\\
\frac{a \Vdash TpV(A | B)}{a \Vdash A}
\end{gathered}$$

With $TpV$, we can complete the definition of $\Sigma$ types as suggested above:

$\Sigma x:A.B[x]\;\coloneqq\;TpV(\Sigma' x:A.B[x]\;|\;\Pi x:A.B[x])$

Combining the inversion rules for $TpV$ and $\Pi$, we get the desired inversion rules for $\Sigma$. Inversion rules for $\Sigma'$ are not needed at all. In general, there seems to be no use for inversion rules for PER comprehension.

### Custom Presuppositions

It would not be dependent type theory if types depended only on types. In the primitive type constructors, aside from the trick of [type-level branching](#CombElim), the only dependency comes from the equality types. But for the equality type to be valid, the terms only need to be elements of $Relax(A)$ for the appropriate $A$. When types depend on elements, we might want type validity to require well-typedness of the terms. And who knows, we might also want all sorts of other requirements for validity of a derived type constructor. What kinds of requirements can be added to type validity?

Because type validity is a judgment form without any term witness, the most we could hope to pack into type validity is mere inhabitedness of a type. And it turns out we can indeed do that. We would like to add inhabitedness of a type as a condition to type validity in the same way that $TpV$ added a type validity condition. It suffices to define a type constructor $PreSup(P)$ whose validity coincides with combined truth of $P$, and then add that to an existing type with $TpV$.

$PreSup(P)$ is a non-negatable version of $\lfloor P \rfloor$. It should validate the following rules:

$$\begin{gathered}
\frac{p \Vdash P}{q \Vdash PreSup(P)} \\
\\
\frac{PreSup(P)\,type}{p \Vdash \lfloor P \rfloor}
\end{gathered}$$

It would be pretty straightforward to just add a primitive type constructor to do this. And it's really just a lucky break that we don't have to.

[Recall](#DiffPresup) that there's a "bad" definition of subtyping as ($\Pi a:A.a \in B$). Well actually we'll use ($\cap a:A.a \in B$), which is just as bad. It's bad as a definition of subtyping because it has the excessively strong presupposition that ($A \prec B$). Due to the inversion rules and the rules for $Relax$, we can actually *use* this presupposition if we know the bad subtyping is a valid type. This seems to be the most interesting fact we can get out of the primitive inversion rules, so we should encode inhabitedness of a type in terms of respect for equality.

We can define a type constructor for "Diaconescu booleans" that quotients $Bool$ down to a singleton if and only if some type $P$ is inhabited. In the [[Diaconescu-Goodman-Myhill theorem]], these conditionally quotiented booleans are used to encode a proposition as an equation.

$DiaBool(P)\;\coloneqq\;TpV(\{b1 = b2 | b1 = b2 \in Bool \vee (P \wedge b1 \in Bool \wedge b2 \in Bool)\} | P)$

Our $DiaBool$-ical trick is that ($DiaBool(\top) \prec DiaBool(P)$) if and only if $\lfloor P \rfloor$. So we define $PreSup$ as:

$PreSup(P)\;\coloneqq\;\cap b:DiaBool(\top).b \in DiaBool(P)$

This definition was motivated by getting respect to mean the right thing, but as it turns out, subtyping and respect coincide for instances of $DiaBool$. (Since they all have the same computations, namely the booleans.) So $PreSup(P)$ is non-negatable, and satisfies the rules above.

As an (admittedly pretty boring) application of $PreSup$, we can define a "Martin-Löf" equality type constructor that's like relaxed equality, but is only meaningful on elements of the indicated type:

$a1 =_A a2\;\coloneqq\;TpV(a1 = a2 \in A\;|\;PreSup(a1 \in A \wedge a2 \in A))$

## Partial Logic {#PartLogic}

This section sketches the connection between dependent type theory and partial logic. The idea of the connection is that both styles of system handle presuppositions in essentially the same way.

### Frege Structures

In [a paper](#KahleFSU) about adding universes to Frege structures, Reinhard Kahle presents Frege structures formulated as "a truth theory over applicative theories". That is, a logic for reasoning about [[combinatory logic|combinators]], plus a truth predicate. (Supposedly, Frege structures were not originally formulated that way.)

This formulation based on a truth predicate is a close analogue of the formulation of CompLF in a HOAS logical framework.

* The formulas of the applicative language for Frege structures correspond to the logical framework formulas for CompLF.

* The terms of the applicative language correspond to the terms of CompLF. Additionally, both term languages present an untyped computation system.

* Classical propositions represented as computations in Frege structures correspond to types represented as computations in CompLF.

* The truth predicate ($T$) of this "truth theory" formulation expresses what we called [combined truth](#CombTruth). It thus corresponds (modulo propositions-as-types) to the typing judgment form ($\Vdash$) of CompLF. Rather than have a primitive "is a proposition" predicate, the truth theory uses ($P(x)\;\coloneqq\;T(x) \vee T(\dot{\not} x)$), which works in part due to classical logic. This corresponds to the type validity judgment form.

Kahle's paper is very much about the representability of formulas as propositions in Frege structures, which corresponds to the representability of framework formulas as squashed types in CompLF [discussed above](#JudgReason). With Frege structures, there's a strong metatheorem about representability. Kahle calls it "Proposition 5". This allows representing any formula with only positive occurrences of $T$. By adding universes to Frege structures, Kahle allows for negative occurrences of restricted versions of combined truth.

(It seems that there's nothing as strong as Proposition 5 available for CompLF. For example, there doesn't seem to be a way to express disjunction of combined truth in CompLF. The disjunction available in CompLF is only a type when both disjuncts are. Frege structures have a "parallel or" that's (combined) true when either disjunct is.)

Since proposition validity ($P(x)\;\coloneqq\;T(x) \vee T(\dot{\not} x)$) uses only positive occurrences of $T$, it's representable. Namely, ($T(\dot{\not}(\dot{\not} x \dot{\wedge} x)) \leftrightarrow (T(x) \vee T(\dot{\not} x))$). So with appropriate definitions of disjunction and implication for classical logic, the representation could also be ($x \dot{\vee} \dot{\not} x$) or ($x \dot{\to} x$). So the idea is essentially the same as representing [type validity](#TpOK) as a type in CompLF: use some tautology that mentions the thing that should be valid. (Our particular definition, ($A \supset \top$) could be imitated in Frege structures as ($x \dot{\to} (x \dot{=} x)$), but this *doesn't* work, because it's always true, due to the parallel behavior of Frege structures connectives, rather than the short-circuiting behavior of CompLF type constructors. Clearly not *all* tautologies do the trick.)

In Frege structures, too, proposition validity is [non-negatable](#NonNegate). With the truth predicate, this can be expressed quite clearly as $\not T(\dot{\not}(x \dot{\to} x))$. In Frege structures terminology, this is saying that ($x \dot{\to} x$) is "not false". It's either "true" (combined true) or not a proposition.

So intuitively, the problem with representing negative occurrences of $T$ without stratification is that that would entail assuming proposition validity in a proposition. But you can't, since proposition validity is non-negatable.

TODO: Relation to synthesis and checking modes?  
tl;dw  
Synthesis: $T(x)$  
Checking: $\not T(\dot{\not} x)$

### Fitch-Scott Partial Logic {#FSLogic}

[[Dana Scott]] wrote [a note](#ScottComb) in which he sketched a system very similar to Frege structures. This was prior to [[Peter Aczel]]’s paper that coined "Frege structures". Scott attributes key ideas of the system to Fitch, who worked on foundational logics based on combinators.

For anyone trying to learn about Frege structures on the internet, it seems like many of the papers about it are paywalled. Scott's note and [Kahle's paper](#KahleFSU) are a couple of (currently, Aug 2020) open access sources. Kahle cited Aczel on Frege structures, and didn't give much explanation of the basics. Hopefully that was done by Aczel, but that paper is paywalled.

Scott's note seems like a good explanation of the main ideas of Frege structures, since his system is so similar. We covered Kahle's version first because—if not for the above discussion of the approach using a formal truth predicate—Frege structures might seem quite distant from Nuprl-like systems, other than a basis on the untyped lambda calculus.

#### Paradox and Partiality

Scott explains how—due to the way the system combines untyped lambda calculus and logical operations—there *would* be an inconsistency due to the [[liar paradox|liar]]/[[Russell's paradox|Russell]] paradox, except that the formula which seems to contradict itself turns out to be neither true nor false. In the terminology of Frege structures, it's not a proposition. (For CompLF, it can similarly be shown that something looking like a self-contradicting type is not a type. Formalizing this requires the logical framework, since [type validity is non-negatable](#TpOK).)

But Scott's system doesn't have the distinct notions of first-order formula vs proposition from Kahle's truth theory formulation of Frege structures. In Scott's terminology, the formulas are apparently just the terms that one is treating as formulas, by regarding them as possibly having a truth value. Because some formulas cannot have a truth value ("truth-value gaps"), the system is regarded as a partial logic: some formulas fail to denote a truth value.

Scott analyzes this partial logic as a three-valued logic, with an undefined "value" below the usual values true and false. The significance of ordering undefined below true and false (like in the flat domain of partial booleans) is that the connectives need to be monotone. (And quantifiers too, which work like infinitary connectives.)

Scott gives three-valued truth tables for the connectives. We have come a long way from type theory, with its typing and type validity judgments, but hopefully the connection is still in sight: the possibility of a formula being undefined corresponds to the possibility of raw type expressions for which type validity is not derivable. Truth tables for type constructors seems like too much to ask for, but truth tables for partial logic still shows the issue of presuppositions in a new light.

#### Squadge

There's an unusual primitive connective in Scott's system, which is not in Kahle's formulation of Frege structures: a "squadge" connective, which "gives the common part of the *and* and the *or*." That is, it has the same value as conjunction and disjunction, when they agree, and is otherwise undefined. In case that does not seem like an intuitive definition, it also has the same value as its inputs, when they agree, and is otherwise undefined. Squadge is supposedly necessary, in the purely propositional part of partial logic, for defining all the monotone connectives. It plays a role analogous to CompLF's $TpV$ and $PreSup$, allowing the user to [strategically make formulas undefined](#StrTpV). But with an undefined formula already available due to the liar/Russell paradox, squadge turns out to be redundant, at least semantically:

$r\;\coloneqq\;\lambda x.~(x\,x)$  
$*\;\coloneqq\;r\,r$  
$PreSup(\phi)\;\coloneqq\;\phi \vee *$

$PropOK(\phi)\;\coloneqq\;\phi \to \phi$  
$PropV(\phi | \psi)\;\coloneqq\;(PropOK(\psi) \to \phi) \wedge PropOK(\psi)$

$\phi\,squadge\,\psi\;\coloneqq\;PropV(\phi | PreSup(\phi \leftrightarrow \psi))$

By defining squadge in terms of $PropV$ and $PreSup$, which work like (the classical special cases of) the CompLF counterparts, it's clear that CompLF also has squadge. But CompLF doesn't have the parallel versions of conjunction, disjunction, or the quantifiers, that Frege structures do! Meanwhile Frege structures *can* define (the classical special cases of) CompLF's connectives. That is, short-circuiting conjunction and implication, and strict disjunction and quantifiers.

#### Partial Sequent Calculus

Scott gives a proof system for his partial logic: a modified sequent calculus where each side of the turnstile is a set of *terms*. These terms are treated like formulas in that the derivation rules use connectives and quantifiers on them. So the situation is analogous to that of a deductive system for dependent type theory, based on raw terms: certain terms in the rules are treated like types. Just as dependent typing rules need to cope with types that are not valid though, the sequent calculus for partial logic needs to cope with truth-value gaps. The particulars of the rules for partial sequent calculus are quite different from dependent typing rules, though.

#### Recursive Classes

Scott sketches a representability metatheorem similar to Kahle's Proposition 5, but more exciting: by combining a [[fixed-point combinator]] with the quantifiers and connectives, the system can represent recursive first-order predicates in which the recurrences are positive. Implicitly, the predicate can also use combined truth positively, because this just means using some term as a formula.

The predicates obtained in this way are usually non-negatable. The fact that you can meaningfully prove them tends to rely on the non-strictness of connectives and quantifiers, to avoid infinite descent down a recursion that doesn't terminate. (Branching on the argument would allow guiding the recursion to a base case, to get proofs. But this would not arise from a plain first-order definition. Also, the pure untyped lambda calculus doesn't provide a way to branch on arbitrary objects. Moreover, even if the recursion terminates, this does not help if you can't prove it, which would usually require induction, and Scott's system has no such principle.)

Due to being non-negatable, these recursive predicates are more like defined judgment forms than types, in CompLF terminology. Or you could think of them as proper classes. But the properness is certainly not about cardinality.

The use of general recursion to define non-negatable semantic judgment forms seems like it should work in CompLF too, but as with Proposition 5, you don't get as strong a result due to the lack of parallel connectives. But in the first place, it's not clear that these non-negatable recursive definitions are actually good for much, since you can't reason about them by induction. Any sort of useful interaction with other parts of the system would probably need to be arranged very cleverly.

#### Dependent Types

Scott encodes types as what Kahle called propositional functions: functions whose applications always have a truth value. These collect into a class, $V$, expressing that something is a propositional function. $V$ itself is not a type, but is closed under the construction of $\Pi$ and $\Sigma$ types, which Scott defines with the now-usual logical predicates clauses (except using classical logic to write the usual implication as disjunction). He shows some good derived rules for $\Pi$.

Encoding dependent type systems into Frege structures and [[explicit mathematics]] became a research topic later on. It doesn't seem to have led to a nice [[proof assistant]] for working with dependently typed constructions, though.

Finally, Scott sketches a sort of universe hierarchy, based on stratifying the classes of true/false objects. This is somewhat like the universes of Kahle, but sounds more like the "truth levels" of Cantini that Kahle cites.

#### What about Kripke?

At the same time as Scott's note, [Kripke came out with](#KripkeTruth) a "theory of truth" very much like Fitch's idea to use partial logic to avoid paradox. Kripke followed the style of Tarski's notion of truth predicate, rather than use combinators or lambda calculus. Formulas can be Gödel numbered in first-order arithmetic, and this numbering allows formulating Tarski's T-schema, saying that any formula is logically equivalent to the truth predicate applied to the Gödel number of the formula.

Just as Fitch-Scott logic and Frege structures allow defining recursive formulas using the untyped lambda calculus/combinators, Kripke's theory allows them by combining the truth predicate with [quining][]. You might say Frege structures provide [[type of types#RussellStyle|Russell-style]] recursive formulas while Kripke's theory provides [[type of types#TarskiStyle|Tarski-style]] recursive formulas. Either way, you can formulate "This sentence is false.", and the liar paradox is avoided by not assigning that formula a truth value.

[quining]: https://en.wikipedia.org/wiki/Quine_(computing)

Kripke's theory provides the full T-schema in the setting of partial logic. There's also a "closed off" version that totalizes the logic by mapping undefined to false at the end. This version resembles Kahle's truth theory, and has a restricted T-schema.

### Free Logic

Free logic is logic in which terms need not denote elements of types (logical sorts). Free logics seem to be essentially the same idea as logics of partial terms. The term "free logic" is nice since it's shorter than "logic of partial terms". "Partial logic" would be nice, but that seems to be taken to mean logic of partial *formulas*, as discussed [above](#FSLogic).

There is a [SEP article](#SEPLogicFree) about free logic. Its emphasis is on a free version of untyped classical first-order logic, so for us, that means it has one type, and the well-defined terms denote elements of that type. The article refers to the type as the quantification domain, and thinks of its elements ("members") as the "existing things". The article speaks of whether terms denote some existing thing, rather than whether they are well-defined. So the article's "existence" predicate is often called a "definedness" predicate elsewhere. This may be a difference for philosophical purposes, but for mathematical and metatheoretical purposes, they seem the same.

In CompLF, the quantifiers (like family intersection and subset, but of course also $\Pi$ and $\Sigma$) have types as the quantification domains. Functions (elements of $\Pi$ types) also have types as their domains. So the form of CompLF statement corresponding to existence/definedness of $t$ should be ($t \in T$). Or is it ($t \Vdash T$)? Or ($T \ni t$)? So you see, there are extra complications, due to having multiple types, the distinction between propositions and judgments, and the fact that type expressions themselves may be undefined. Also, with the HOAS logical framework, we also have the framework-level quantifiers, which do not involve types. We will see that all of these things are somewhat related to ideas in free logic.

#### Negative, Positive, Neutral

The SEP article identifies three "general approaches" to the semantics of free logic: In "negative" semantics, atomic formulas are necessarily false when applied to a non-denoting term. In "positive" semantics, the only requirement is that existence applied to a non-denoting term is false. (Of course, since existence is required to indicate which terms have a denotation.) In "neutral" semantics, atomic formulas, except for existence, necessarily lack a truth value when applied to a non-denoting term.

So technically, the positive approach is the most general, since all approaches require the same behavior of the existence predicate, and otherwise, the positive approach has no requirements. Meanwhile, assuming there's at least one atomic predicate other than existence with at least one argument, the negative and neutral approaches are mutually exclusive. Actually, maybe the positive approach was intended to rule out truth value gaps. In that case it would not be more general than neutral. (And none of these approaches would explain CompLF.) But if we consider each argument of each atomic predicate individually, we can consider whether it's behaving like the negative approach, neutral approach, or neither.

In the presence of truth value gaps, there are two interpretations of the negative approach to an argument: One is that if the argument is undefined, the predicate must be false. The other is that if the argument is undefined, the predicate must not be true. The first interpretation does not seem to show up anywhere in CompLF, but the second interpretation of the negative approach shows up in the equality predicate: If ($t = t' \in T$) is true, then $t$ and $t'$ must denote elements of $T$. (So if $t$ or $t'$ fail to denote, the equation cannot be (combined) true.) So the negative approach in this interpretation corresponds to strictness principles for atomic predicates: a predicate is true only if an argument is defined.

The neutral approach *also* shows up in the equality predicate, provided we regard a term as having a truth value if and only if it denotes a type: If ($t = t' \in T$) is a type, then $t$ and $t'$ must denote elements of $Relax(T)$ (which entails also that $T$ is a type). So if $t$, $t'$, or $T$ fail to denote, the equation has no truth value. So the neutral approach corresponds to inversion principles for atomic type constructors.

The identity type constructor ($\equiv$) has neither strictness nor inversion principles, so I suppose we could consider it to be following the positive approach.

#### Outer Domain

The positive approach to the semantics of free logic often makes use of an "outer domain". This domain is not (necessarily) quantified over, but it's used as the codomain of the term interpretation function. Atomic predicates are then interpreted simply as relations on the outer domain.

In the semantics of CompLF, the outer domain is the set of terms, considered up to computational equivalence. So the "interpretation" of terms is just a quotient projection. (Types are subquotients of this outer domain, not subsets, and the PER semantics that's used to handle this causes phenomena that seem to have no analogue in free logic. For example, not everything is a $Comp$, even though $Comp$ is the internalization of the outer domain.)

Relations on the outer domain are used as the interpretations of judgment forms. So in general, they correspond to predicates in the positive approach. They can be made more negative using conjunction. Provided they're representable as type operations, they can be made more neutral using $TpV$ and $PreSup$. (See [above](#StrTpV).)

#### Quantification over Outer Domain

TODO

TODO?: Kahle's $T$ according to free logic.

## References

* {#ScottComb} [[Dana Scott]], _Combinators and Classes_, Lambda Calculus and Computer Science Theory (LCCST) 1975 ([web](https://www.researchgate.net/publication/221200880_Combinators_and_classes))

* {#KCThesis} Karl Crary, _Type-Theoretic Methodology for Practical Programming Languages_, 1998 PhD thesis ([web](http://www.nuprl.org/KB/show.php?ShowPub=Cra98), [pdf](http://www.nuprl.org/documents/Crary/Thesis-TypeTheoretic.pdf))

* {#KahleFSU} Reinhard Kahle, _Universes over Frege Structures_, Annals of Pure and Applied Logic (2003) ([web](https://www.sciencedirect.com/science/article/pii/S0168007202000404))

* {#SEPLogicFree} John Nolt, _Free Logic_, Stanford Encyclopedia of Philosophy (SEP) Fall 2018 ([web](https://plato.stanford.edu/archives/fall2018/entries/logic-free/))

* {#KripkeTruth} Saul Kripke, _Outline of a Theory of Truth_, Journal of Philosophy (1975)
