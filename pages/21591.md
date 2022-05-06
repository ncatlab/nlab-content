
#Contents#
* table of contents
{:toc}

## Idea

This is the definition of the formal system [[CompLF]], version 1. Actually, there were several versions between [[CompLF v0|zero]] and one, but you're not missing anything interesting.

## Syntax

### Term grammar

The main [[syntax|syntactic]] class is [[terms]]. [[type|Type]] expressions are terms. There are also [[variables]] and [[contexts]].

variables ($x$, $y$, ...)` ::= `(Written as usual. Complain if you can't tell them apart from metavariables.)

terms ($t$, $a$, $b$, $f$, $T$, $A$, $B$, $R$, ...)` ::=`

* $x \qquad$ (variable reference)
* $\lambda x.b \qquad$ (lambda abstraction)
* $f\,a \qquad$ (application)

* $t \equiv t' \qquad$ (identity type) (computational equivalence)
* $a = b \in C \qquad$ (equality type)
* $Relax(A) \qquad$ ("relax" type)
* $\Pi x:A.B \qquad$ (dependent function type)
* $\cap x:A.B \qquad$ (family intersection type)
* $\{x:A | B\} \qquad$ (subset/separation type)
* $Comp \qquad$ (type of computations ([[realizers]]))
* $Bool \qquad$ (type of "booleans") (two-element type)
* $\{x = y | R\} \qquad$ ([[PER]] comprehension type)
* $Nat \qquad$ (type of natural numbers)

contexts ($\Gamma$, ...)` ::= `$\cdot$` | `$\Gamma,x:T$

As usual, the rules may make liberal use of informal list operations to work with contexts.

### Abbreviations

#### Semantic Judgment Forms {#SemJudg}

$a \in A\;\coloneqq\;a = a \in A$

$A \to B\;\coloneqq\;\Pi \underline{\;}:A.B$

$A \supset B\;\coloneqq\;\cap \underline{\;}:A.B$

$A \wedge B\;\coloneqq\;\{\underline{\;}:A | B\}$

#### Computations

The [[Alonzo Church|Church]] booleans:

$tru\;\coloneqq\;\lambda t.\lambda f.t$

$fls\;\coloneqq\;\lambda t.\lambda f.f$

[[Dana Scott|Scott]] nats:

$zro\;\coloneqq\;\lambda z.\lambda s.z$

$suc(n)\;\coloneqq\;\lambda z.\lambda s.s\,n$

#### Type Constructors

The type constructors given in the grammar above that have subexpressions are actually abbreviations for applied constants. For example:

$\Pi x:A.B\;\coloneqq\;KPi\,A\,(\lambda x.B)$

In particular, $\lambda$ is the only real binding form of the language.

$\top\;\coloneqq\;tru = tru \in Bool$

$\bot\;\coloneqq\;tru = fls \in Bool$

### Judgment forms

$a \longrightarrow_\beta b \qquad$ (beta "reduction")

$\Gamma \vdash T\,type \qquad$ (type validity)

$\Gamma \vdash t \Vdash T \qquad$ (element in a type) (realizer of a type)

## Rules {#Rules}

### Partially-Compatible Reduction

$$\begin{gathered}
\frac{}{(\lambda x.b)\,a \longrightarrow_\beta b[a/x]} \\
\\
\frac{b \longrightarrow_\beta b'}
{\lambda x.b \longrightarrow_\beta \lambda x.b'} \\
\\
\frac{a \longrightarrow_\beta a'}
{f\,a \longrightarrow_\beta f\,a'}
\end{gathered}$$

### Miscellaneous

$$\begin{gathered}
\frac{x:T \in \Gamma}{\Gamma \vdash x \Vdash T} \\
\\
\\
\frac{A \longrightarrow_\beta B \qquad \Gamma \vdash t \Vdash A}
{\Gamma \vdash t \Vdash B} \\
\\
\frac{B \longrightarrow_\beta A \qquad \Gamma \vdash t \Vdash A}
{\Gamma \vdash t \Vdash B} \\
\\
\\
\frac{\Gamma \vdash a \Vdash A}{\Gamma \vdash A\,type}
\end{gathered}$$

### Relax

$$\begin{gathered}
\frac{\Gamma \vdash A\,type}{\Gamma \vdash Relax(A)\,type} \\
\\
\frac{\Gamma \vdash Relax(A)\,type}{\Gamma \vdash A\,type} \\
\\
\\
\frac{\Gamma \vdash a \Vdash A}{\Gamma \vdash a \Vdash Relax(A)} \\
\\
\frac{\Gamma \vdash A\,type \qquad \Gamma \vdash t \Vdash Comp}
{\Gamma \vdash t \Vdash Relax(A)} \\
\\
\\
\frac{\begin{array}{l}\Gamma \vdash a' \Vdash Comp \\
\Gamma \vdash p1 \Vdash (a \in A) \supset (a = a' \in A) \\
\Gamma \vdash p2 \Vdash (a' \in A) \supset (a = a' \in A)\end{array}}
{\Gamma \vdash q \Vdash a = a' \in Relax(A)} \\
\\
\frac{\Gamma \vdash a \Vdash A \qquad \Gamma \vdash p \Vdash a = a' \in Relax(A)}
{\Gamma \vdash q \Vdash a = a' \in A}
\end{gathered}$$

### Equality

$$\begin{gathered}
\frac{\Gamma \vdash a1 \Vdash Relax(A) \qquad \Gamma \vdash a2 \Vdash Relax(A)}
{\Gamma \vdash a1 = a2 \in A\,type} \\
\\
\frac{\Gamma \vdash a1 = a2 \in A\,type}{\Gamma \vdash a1 \Vdash Relax(A)} \qquad
\frac{\Gamma \vdash a1 = a2 \in A\,type}{\Gamma \vdash a2 \Vdash Relax(A)} \\
\\
\\
\frac{\Gamma \vdash a \Vdash A}
{\Gamma \vdash q \Vdash p1 = p2 \in (a = a \in A)} \\
\\
\frac{\Gamma \vdash p \Vdash a = a' \in A}{\Gamma \vdash a \Vdash A} \\
\\
\frac{\Gamma \vdash p \Vdash a = a' \in A \qquad
\Gamma,x:A \vdash C\,type \qquad
\Gamma \vdash c \Vdash C[a/x]}
{\Gamma \vdash c \Vdash C[a'/x]}
\end{gathered}$$

### Identity

$$\begin{gathered}
\frac{\Gamma \vdash t1 \Vdash Comp \qquad \Gamma \vdash t2 \Vdash Comp}
{\Gamma \vdash t1 \equiv t2\,type} \\
\\
\\
\frac{}{\Gamma \vdash q \Vdash p1 = p2 \in (t \equiv t)} \\
\\
\frac{\Gamma \vdash p \Vdash t \equiv t' \qquad \Gamma \vdash c \Vdash C[t/x]}
{\Gamma \vdash c \Vdash C[t'/x]}
\end{gathered}$$

### Functions

$$\begin{gathered}
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \Pi x:A.B\,type} \\
\\
\frac{\Gamma \vdash \Pi x:A.B\,type}{\Gamma \vdash A\,type} \\
\\
\frac{\Gamma \vdash \Pi x:A.B\,type \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash B[a/x]\,type} \\
\\
\\
\frac{\Gamma \vdash f \Vdash \Pi x:A.B \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash f\,a \Vdash B[a/x]} \\
\\
\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash p \Vdash f\,x = f'\,x \in B \qquad
x \notin FV(f,f')}
{\Gamma \vdash q \Vdash f = f' \in \Pi x:A.B}
\end{gathered}$$

### Intersection

$$\begin{gathered}
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \cap x:A.B\,type} \\
\\
\frac{\Gamma \vdash \cap x:A.B\,type}{\Gamma \vdash A\,type} \\
\\
\frac{\Gamma \vdash \cap x:A.B\,type \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash B[a/x]\,type} \\
\\
\\
\frac{\Gamma \vdash b \Vdash \cap x:A.B \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash b \Vdash B[a/x]} \\
\\
\frac{\Gamma \vdash A\,type \qquad
\Gamma,x:A \vdash p \Vdash b = b' \in B \qquad
x \notin FV(b,b')}
{\Gamma \vdash q \Vdash b = b' \in \cap x:A.B}
\end{gathered}$$

### Subset

$$\begin{gathered}
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \{x:A | B\}\,type} \\
\\
\frac{\Gamma \vdash \{x:A | B\}\,type}{\Gamma \vdash A\,type} \\
\\
\frac{\Gamma \vdash \{x:A | B\}\,type \qquad \Gamma \vdash a \Vdash A}
{\Gamma \vdash B[a/x]\,type} \\
\\
\\
\frac{\Gamma,x:A \vdash B\,type \qquad
\Gamma \vdash a \Vdash A \qquad \Gamma \vdash b \Vdash B[a/x]}
{\Gamma \vdash a \Vdash \{x:A | B\}} \\
\\
\frac{\Gamma \vdash a \Vdash \{x:A | B\} \qquad
\Gamma,x:A,y:B \vdash c \Vdash C \qquad y \notin FV(c,C)}
{\Gamma \vdash c[a/x] \Vdash C[a/x]}
\end{gathered}$$

### Computations

$$\begin{gathered}
\frac{}{\Gamma \vdash Comp\,type} \\
\\
\\
\frac{\Gamma,x:Comp \vdash b \Vdash Comp}{\Gamma \vdash \lambda x.b \Vdash Comp} \\
\\
\frac{\Gamma \vdash f \Vdash Comp \qquad \Gamma \vdash a \Vdash Comp}
{\Gamma \vdash f\,a \Vdash Comp} \\
\\
\\
\frac{\begin{array}{l}\Gamma \vdash a \Vdash A \qquad
\Gamma,y:A \vdash C\,type \\
\Gamma,x:Comp,x':Comp,h:(x = x' \in A) \vdash
p \Vdash c[x/y] = c'[x'/y] \in C[x/y] \\
x,x',h \notin FV(c,c')\end{array}}
{\Gamma \vdash q \Vdash c[a/y] = c'[a/y] \in C[a/y]}
\end{gathered}$$

### Booleans

$$\begin{gathered}
\frac{}{\Gamma \vdash Bool\,type} \\
\\
\frac{}{\Gamma \vdash tru \Vdash Bool} \qquad
\frac{}{\Gamma \vdash fls \Vdash Bool} \\
\\
\frac{\Gamma \vdash b \Vdash Bool \qquad
\Gamma \vdash c \Vdash C[tru/x] \qquad
\Gamma \vdash c \Vdash C[fls/x]}
{\Gamma \vdash c \Vdash C[b/x]}
\end{gathered}$$

### PER

$$\begin{gathered}
\frac{\begin{array}{l}\Gamma,x1:Comp,x2:Comp \vdash R\,type \\
\Gamma,y1:Comp,y2:Comp \vdash s \Vdash R[y1,y2/x1,x2] \supset R[y2,y1/x1,x2] \\
\Gamma,y1:Comp,y2:Comp,y3:Comp \vdash t \Vdash R[y1,y2/x1,x2] \supset R[y2,y3/x1,x2] \supset R[y1,y3/x1,x2]\end{array}}
{\Gamma \vdash \{x1 = x2 | R\}\,type} \\
\\
\\
\frac{\Gamma \vdash \{x1 = x2 | R\}\,type \qquad
\Gamma \vdash t2 \Vdash Comp \qquad
\Gamma \vdash p \Vdash R[t1,t2/x1,x2]}
{\Gamma \vdash q \Vdash t1 = t2 \in \{x1 = x2 | R\}} \\
\\
\frac{\begin{array}{l}
\Gamma \vdash p \Vdash t1 = t2 \in \{x1 = x2 | R\} \\
\Gamma \vdash R[t1,t2/x1,x2]\,type \\
\Gamma,h:R[t1,t2/x1,x2] \vdash c \Vdash C \qquad h \notin FV(c,C)
\end{array}}
{\Gamma \vdash c \Vdash C}
\end{gathered}$$

### Natural Numbers

$$\begin{gathered}
\frac{}{\Gamma \vdash Nat\,type} \\
\\
\\
\frac{}{\Gamma \vdash zro \Vdash Nat} \\
\\
\frac{\Gamma \vdash n \Vdash Nat}{\Gamma \vdash suc(n) \Vdash Nat} \\
\\
\\
\frac{\Gamma \vdash n \Vdash Nat}{\Gamma \vdash n \Vdash Comp} \\
\\
\frac{\begin{array}{l}
\Gamma \vdash n \Vdash Nat \qquad
\Gamma,x:Nat \vdash C\,type \\
\Gamma \vdash c \Vdash C[zro/x] \\
\Gamma,x:Nat,h:C \vdash c \Vdash C[suc(x)/x]
\end{array}}
{\Gamma \vdash c \Vdash C[n/x]}
\end{gathered}$$
