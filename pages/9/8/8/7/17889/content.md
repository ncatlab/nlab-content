\tableofcontents

(This is a stub)

\section{Idea}

Subtractive logic is an extension of (propositional or first order) intuitionistic logic  with a new connective, subtraction, dual to implication, such that each sentence $A$ have a "dual" $\overline{A}$ verifying $A \vdash_{\text{SL}} B$ if and only if $\overline{B} \vdash_{\text{SL}} \overline{A}$. Propositional subtractive logic is a conservative extension over propositional intuitionistic logic, but it is not the case for the first order case.

\section{Syntax}

In the following and to the rest of the articles, uppercases letters $A, B, C, D$ will denote sentences.

We start with (a slightly modified) [[Gerhard Gentzen|Gentzen's]] LJ [[sequent calculus]], whose rules are as follow:

Axioms:

$$
    \frac{}{A \vdash_{\text{SL}} A} \; \text{ax} \qquad
    \frac{}{\bot \vdash_{\text{SL}} A}\;\text{ax} \qquad
    \frac{}{A \vdash_{\text{SL}} \top}\; \text{ax}
$$

Cut:

$$\frac{A \vdash_{\text{SL}} C \quad C \vdash_{\text{SL}} B}{A \vdash_{\text{SL}} B} \; \text{cut}$$

Rules of conjonctions:

$$
    \frac{}{A \wedge B \vdash_{\text{SL}} A} \;\text{elim-}\wedge_1 \qquad
    \frac{}{A \wedge B \vdash_{\text{SL}} B} \;\text{elim-}\wedge_2 \qquad
    \frac{A \vdash_{\text{SL}} B \quad A \vdash_{\text{SL}} C}{A \vdash_{\text{SL}} B \wedge C} \;\text{intro-}\wedge
$$

Rules of disjonctions:

$$
    \frac{}{A \vdash_{\text{SL}} A \vee B} \;\text{intro-}\vee_1 \qquad
    \frac{}{B \vdash_{\text{SL}} A \vee B} \;\text{intro-}\vee_2 \qquad
    \frac{A \vdash_{\text{SL}} C \quad B \vdash_{\text{SL}} C}{A \vee B \vdash_{\text{SL}} C} \;\text{elim-}\vee
$$

\begin{remark}
    Rules for conjonctions and disjonctions are eerily similar, in particular if $A$ and $B$ are composed only of conjonctions, disjonctions and variables, noting by $\overline{A}$ and $\overline{B}$ the same formulas but replacing each conjonctions by disjonctions and disjonctions by conjonctions simultaneously, then $A \vdash_{\text{SL}} B$ if and only if $\overline{B} \vdash_{\text{SL}} \overline{A}$. That is what we mean by saying that conjonctions and disjonctions are dual. In the same vein, top and bottom are duals.
\end{remark}

Rules of implications:

$$
    \frac{}{(A \implies B) \wedge A \vdash_{\text{SL}} B}\;\text{elim-}\implies \qquad
    \frac{A \wedge B \vdash_{\text{SL}} C}{A \vdash_{\text{SL}} B \implies C}\;\text{intro-}\implies
$$

This rule usually do not have a dual in intuitionistic logic, but we'll just create one written $A - B$, rules of subtractions:

$$
    \frac{}{B \vdash_{\text{SL}} (A \implies B) \vee A}\;\text{elim-}\text{sub} \qquad
    \frac{C \vdash_{\text{SL}} A \vee B}{B - C\vdash_{\text{SL}} A}\;\text{intro-}\text{sub}
$$

Giving the syntax of propositional subtractive logic, to make it first order, it suffice to add the existential operator and its dual, the forall operator (where $x$ does not occur free in $C$):

$$
    \frac{A \vdash_{\text{SL}} C}{\exists x.A \vdash_{\text{SL}} C}\;\text{elim-}\exists \qquad
    \frac{A \vdash_{\text{SL}} B[t/x]}{A \vdash_{\text{SL}} \exists x. B}\;\text{intro-}\exists
$$

and

$$
    \frac{C \vdash_{\text{SL}} A}{C \vdash_{\text{SL}} \forall x. A}\;\text{intro-}\forall \qquad
    \frac{B[t/x] \vdash_{\text{SL}} A}{\forall x. B \vdash_{\text{SL}} A}\;\text{elim-}\forall
$$

\begin{definition}
    \label{dual}
    The dual of a sentence $A$ is another sentence $\overline{A}$ defined by structural induction on the syntax of the sentence by $ 
        \begin{cases}
            A & \,\text{if}\, A \,\text{is a variable}\\
            \bot & \,\text{if}\, A = \top \\
            \top & \,\text{if}\, A = \bot \\
            \overline{C} \vee \overline{B} & \,\text{if}\, A = B \wedge C \\
            \overline{C} \wedge \overline{B} & \,\text{if}\, A = B \vee C \\
            \overline{C} \implies \overline{B} & \,\text{if}\, A = B - C \\
            \overline{C} - \overline{B} & \,\text{if}\, A = B \implies C \\
            \exists x. \overline{B} & \,\text{if}\, A = \forall x. B\\
            \forall x. \overline{B} & \,\text{if}\, A = \exists x. B
            \end{itemize}
        \end{cases}
    $
\end{definition}

\section{Relation to other logics}

(this is a stub)

TODO: bi-interpretation with classical logic, what $A - B$ becomes when there's the law of excluded middle, conservation over propositional intuitionistic logic but not over first order one.

\section{Models and semantics}

(this is a stub)

TODO: bi-topologies (where closed sets are also a topology) as models, category semantics of bi-cartesian closed categories, kripke semantics

\section{Related concepts}

* [[continuation semantics]]

\section{References:}

* [[Tristan Crolard]], [_Subtractive logic_](http://www.sciencedirect.com/science/article/pii/S0304397599001243),  Theoretical Computer Science, 254, Issues 1&#8211;2, 6 March 2001, Pages 151-185