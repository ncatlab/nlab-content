
#Contents#
* table of contents
{:toc}

## Idea

This is the definition of the original [[CompLF]] formal system, version zero, without as much English getting in the way.

## Syntax

### Term grammar

The main [[syntax|syntactic]] class is [[terms]]. [[type|Type]] expressions are terms. There are also [[variables]] and [[contexts]].

variables ($x$, $y$, ...)` ::= `(Written as usual. Complain if you can't tell them apart from metavariables.)

terms ($t$, $a$, $b$, $f$, $T$, $A$, $B$, $R$, ...)` ::=`

* $x \qquad$ (variable reference)
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

"$A$ is a refinement/[[subquotient]] of $B$.":

$A \sqsubseteq B\;\coloneqq\;A \subseteq B \wedge B \prec A$

#### Computations

The Church booleans:

$tru\;\coloneqq\;\lambda t.\lambda f.t$

$fls\;\coloneqq\;\lambda t.\lambda f.f$

#### Type constructors

$\top\;\coloneqq\;tru = tru \in Bool$

$\bot\;\coloneqq\;tru = fls \in Bool$

"Squash" of $A$:

$\lfloor A \rfloor\;\coloneqq\;\{\underline{\;}:\top | A\}$

## Rules {#Rules}

### Type Formation

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
{\Gamma \vdash \cap x:A.B\,type} \\
\\
\frac{}{\Gamma \vdash Comp\,type} \\
\\
\frac{\Gamma \vdash A\,type \qquad \Gamma,x:A \vdash B\,type}
{\Gamma \vdash \{x:A | B\}\,type} \\
\\
\frac{\begin{array}{l}\Gamma,x1:Comp,x2:Comp \vdash R\,type \\
\Gamma,y1:Comp,y2:Comp \vdash s \Vdash R[y1,y2/x1,x2] \to R[y2,y1/x1,x2] \\
\Gamma,y1:Comp,y2:Comp,y3:Comp \vdash t \Vdash R[y1,y2/x1,x2] \to R[y2,y3/x1,x2] \to R[y1,y3/x1,x2]\end{array}}
{\Gamma \vdash \{x1 = x2 | R\}\,type} \\
\\
\frac{}{\Gamma \vdash Bool\,type}
\end{gathered}$$

### Miscellaneous

$$\begin{gathered}
\frac{x:T \in \Gamma}{\Gamma \vdash x \Vdash T} \\
\\
\frac{A \equiv_\beta B \qquad \Gamma \vdash B\,type \qquad
\Gamma \vdash t \Vdash A}
{\Gamma \vdash t \Vdash B} \\
\\
\frac{t \equiv_\beta t' \qquad \Gamma \vdash t \Vdash T}
{\Gamma \vdash t' \Vdash T} \\
\\
\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash A \prec A} \\
\\
\frac{\Gamma \vdash A\,type}{\Gamma \vdash p \Vdash Comp \prec A}
\end{gathered}$$

### Equality

$$\begin{gathered}
\frac{\Gamma \vdash t \Vdash T}{\Gamma \vdash p \Vdash t = t \in T} \\
\\
\frac{\Gamma \vdash p \Vdash t1 = t2 \in T}{\Gamma \vdash t1 \Vdash T} \\
\\
\frac{\Gamma \vdash p \Vdash t1 = t2 \in T}{\Gamma \vdash t2 \Vdash T} \\
\\
\frac{\Gamma,x:A \vdash B\,type \qquad
\Gamma \vdash p \Vdash a1 = a2 \in A \qquad
\Gamma \vdash b \Vdash B[a1/x]}
{\Gamma \vdash b \Vdash B[a2/x]} \\
\\
\frac{\Gamma \vdash t \Vdash T}
{\Gamma \vdash q \Vdash p1 = p2 \in (t = t \in T)}
\end{gathered}$$

### Functions

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

### Intersection

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

$$\begin{gathered}
\frac{}{\Gamma \vdash tru \Vdash Bool} \qquad
\frac{}{\Gamma \vdash fls \Vdash Bool} \\
\\
\frac{\Gamma \vdash b \Vdash Bool}{\Gamma \vdash b \Vdash Comp} \\
\\
\frac{\Gamma,x:Bool \vdash C\,type \qquad
\Gamma \vdash c \Vdash C[tru/x] \qquad
\Gamma \vdash c \Vdash C[fls/x] \qquad
\Gamma \vdash b \Vdash Bool}
{\Gamma \vdash c \Vdash C[b/x]} \\
\\
\frac{\Gamma \vdash T\,type \qquad
\Gamma \vdash p \Vdash \bot}
{\Gamma \vdash t \Vdash T}
\end{gathered}$$
