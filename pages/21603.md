
#Contents#
* table of contents
{:toc}

## Idea

The [[CompLF v1|rules of CompLF]] have been designed so that [[structural rules]] (e.g. weakening and substitution) are admissible, and the remaining rules can be expressed as higher-order abstract syntax (HOAS) axioms in [[logical frameworks]] like [[LF]] or [[Isabelle]]/Pure. (Except the variable rule, which isn't needed in HOAS form.) This is a significant (but superficial) difference from Nuprl. Two major interesting things happen with this HOAS formulation of CompLF.

First, the HOAS formulation highlights a connection between dependent type systems and partial logic. The connection is there for all dependent type systems formulated as deductive systems with judgments on raw terms, but Nuprl-like systems make more use of the connection than most.

Second, although the rules are not algorithmic, there is implicit propagation of type validity facts in the semantics, which is analogous to the type propagation of a dependent type checker. The primitive typing judgment form ($a \Vdash A$) outputs validity of the type ($A\,type$). But using the inversion rules, it's possible to derive rules for a defined typing judgment form that inputs type validity. This will hopefully be useful for verifying a bidirectional proof checker for CompLF and similar systems.

## Second-order formulation of rules

This section repeats some of the rules of v1 in HOAS style, since variables and substitution (of terms) are technically expressed differently. Most rules that don't add variables to the context are skipped, since there's no guesswork in translating these.

As usual, translating into HOAS lands in the second-order fragment. There's a pretty standard notation for rules of this fragment.

### Miscellaneous

$$\frac{a \Vdash A}{A\,type}$$

### Equality

$$\begin{gathered}
\frac{a \Vdash A}{q \Vdash p1 = p2 \in (a = a \in A)} \\
\\
\frac{p \Vdash a = a' \in A}{a \Vdash A} \\
\\
\frac{p \Vdash a = a' \in A \qquad
x \Vdash A \vdash C[x]\,type \qquad
c \Vdash C[a]}
{c \Vdash C[a']}
\end{gathered}$$

### Identity

$$\frac{p \Vdash t \equiv t' \qquad c \Vdash C[t]}{c \Vdash C[t']}$$

### Functions

$$\begin{gathered}
\frac{A\,type \qquad x \Vdash A \vdash B[x]\,type}{\Pi x:A.B[x]\,type} \\
\\
\frac{\Pi x:A.B[x]\,type}{A\,type} \\
\\
\frac{\Pi x:A.B[x]\,type \qquad a \Vdash A}{B[a]\,type} \\
\\
\\
\frac{f \Vdash \Pi x:A.B[x] \qquad a \Vdash A}{f\,a \Vdash B[a]} \\
\\
\frac{A\,type \qquad
x \Vdash A \vdash p[x] \Vdash f\,x = f'\,x \in B[x]}
{q \Vdash f = f' \in \Pi x:A.B[x]}
\end{gathered}$$

### Intersection

$$\begin{gathered}
\frac{b \Vdash \cap x:A.B[x] \qquad a \Vdash A}{b \Vdash B[a]} \\
\\
\frac{A\,type \qquad
x \Vdash A \vdash p[x] \Vdash b = b' \in B[x]}
{q \Vdash b = b' \in \cap x:A.B[x]}
\end{gathered}$$

### Subset

$$\begin{gathered}
\frac{x \Vdash A \vdash B[x]\,type \qquad
a \Vdash A \qquad b \Vdash B[a]}
{a \Vdash \{x:A | B[x]\}} \\
\\
\frac{a \Vdash \{x:A | B[x]\} \qquad
x \Vdash A,y \Vdash B[x] \vdash c[x] \Vdash C[x]}
{c[a] \Vdash C[a]}
\end{gathered}$$

### Computations

$$\begin{gathered}
\frac{x \Vdash Comp \vdash b[x] \Vdash Comp}{\lambda x.b[x] \Vdash Comp} \\
\\
\frac{\begin{array}{l}
a \Vdash A \qquad
y \Vdash A \vdash C[y]\,type \\
x \Vdash Comp,x' \Vdash Comp,h \Vdash x = x' \in A \vdash
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
x1 \Vdash Comp,x2 \Vdash Comp \vdash R[x1,x2]\,type \\
y1 \Vdash Comp,y2 \Vdash Comp \vdash s[y1,y2] \Vdash R[y1,y2] \supset R[y2,y1] \\
y1 \Vdash Comp,y2 \Vdash Comp,y3 \Vdash Comp \vdash t[y1,y2,y3] \Vdash R[y1,y2] \supset R[y2,y3] \supset R[y1,y3]
\end{array}}
{\{x1 = x2 | R[x1,x2]\}\,type} \\
\\
\frac{\begin{array}{l}
p \Vdash t1 = t2 \in \{x1 = x2 | R[x1,x2]\} \\
R[t1,t2]\,type \\
h \Vdash R[t1,t2] \vdash c \Vdash C
\end{array}}
{c \Vdash C}
\end{gathered}$$

### Natural Numbers

$$\frac{\begin{array}{l}
n \Vdash Nat \qquad
x \Vdash Nat \vdash C[x]\,type \\
c \Vdash C[zro] \\
x \Vdash Nat,h \Vdash C[x] \vdash c \Vdash C[suc(x)]
\end{array}}
{c \Vdash C[n]}$$

## Judgment-level reasoning

There's another way to write the HOAS formulation of rules, which is perhaps not as pretty, but makes the utility of the HOAS formulation more clear: The judgment forms are atomic relation symbols in a predicate logic, and the rules are axioms.

Here's just one example, since the translation from the above "second-order" notation is completely systematic (FIXME: No it's not. You need to infer where to put quantifiers!):

$natElim\,:\,\forall n,c,C.(n \Vdash Nat) \Rightarrow
(\forall x.(x \Vdash Nat) \Rightarrow (C(x)\,type)) \Rightarrow$  
$\qquad (c \Vdash C(zro)) \Rightarrow
((x \Vdash Nat) \Rightarrow (h \Vdash C(x)) \Rightarrow (c \Vdash C(suc(x)))) \Rightarrow$  
$\qquad (c \Vdash C(n))$
