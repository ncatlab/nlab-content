
#Contents#
* table of contents
{:toc}

## Idea

The [[CompLF v1|rules of CompLF]] have been designed so that [[structural rules]] (e.g. weakening and substitution) are admissible, and the remaining rules can be expressed as higher-order abstract syntax (HOAS) axioms in [[logical frameworks]] like [[LF]] or [[Isabelle]]/Pure. (Except the variable rule, which isn't needed in HOAS form.) This is a significant (but superficial) difference from Nuprl. Two major interesting things happen with this HOAS formulation of CompLF.

First, the HOAS formulation highlights a connection between dependent type systems and partial logic. The connection is there for all dependent type systems formulated as deductive systems with judgments on raw terms, but Nuprl-like systems make more use of the connection than most.

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

So in the HOAS formulation of rules, the judgment forms are atomic relation symbols in a predicate logic, and the rules are axioms. Note that $C$ in this example rule is a *function* in the HOAS formulation. But it's a function of the metalanguage, not of the object language. When rules quantify over functions, that's second-order quantification.

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

## Judgment-level reasoning

Reasoning at the judgment level using this metalanguage is not as convenient as having a type checker for terms, or even as convenient as having a Nuprl-like proof refiner that extracts the realizers. But it's very straightforward and expressive. It can be used to prove derived rules, and other facts about derivability that aren't of the form to be rules. For example, you can show that adding a certain new rule would allow deriving a contradiction.

Many unusual phenomena of Nuprl-like systems become clearer when analyzed in terms of judgment-level reasoning.

### Vs reasoning about Reflected Judgments

In Nuprl-like systems, the semantic judgments are reflected internally as squashed types, and can be reasoned about using propositions-as-types. The metalanguage gives us a way to reason about formal judgments. Aside from the ability to reason about "large" judgment forms like type validity, is this judgment-level reasoning actually different from internal reasoning? It turns out it is.

For example, consider the metalanguage formula:

$$\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$$

The puzzle is to find, assuming ($A\,type$) and ($B\,type$), a type that's provably inhabited if and only if that formula is derivable. In more detail, we want some metalanguage function $R$ such that:

$$\forall A,B.(A\,type) \Rightarrow (B\,type) \Rightarrow
((\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)) \Leftrightarrow (\exists p.p \Vdash R(A,B)))$$

A couple of perhaps-plausible-looking solutions for $R(A,B)$ are ($\Pi t:Comp.(t \in A) \to (t \in B)$) and ($\Pi t:\top.(t \in A) \to (t \in B)$). But both of these are wrong. The first is too weak (you get left-to-right only) and the second is not even a type (which makes existence of an element too strong).

The metalanguage formula we're trying to represent turns out to be asserting that $A$ is a subtype of $B$, since it can be read as a special case of the subsumption rule:

$$\frac{t \Vdash A}{t \Vdash B}$$

So we can take $R(A,B)$ to be ($A \lt\!\!:\;B$). In fact, the first wrong answer is what we called "inclusion" ($\subseteq$).

#### Open vs "Closed Terms"

So how come ($\forall t.(t \Vdash A) \Rightarrow (t \Vdash B)$) and ($\Pi t:Comp.(t \in A) \to (t \in B)$) don't correspond? I mean, the intuitive reason is that subtyping is not just member inclusion, it must also preserve equations. But what is the formal reason? We have the fact that

$$\forall p.(a \Vdash A) \Leftrightarrow (p \Vdash a \in A)$$

so the difference between ($\Vdash$) and ($\in$) is not the mismatch. The mismatch turns out to be the quantifiers used.

#### Strong vs Weak Negation

FIXME: Move to a different section:

But we could also use ($\Pi a:A.a \in B$). There's something sneaky about this solution though: it fails to satisfy an additional requirement that you usually want, namely:

$$\forall A,B.(A\,type) \Rightarrow (B\,type) \Rightarrow (R(A,B)\,type)$$

So it's inhabited exactly when it should be, but it's not a type as often as it could be!
