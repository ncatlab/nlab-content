+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Infinity-limits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **pushout** is an ubiquitous construction in [[category theory]] providing a [[colimit]] for the diagram $\bullet\leftarrow\bullet\rightarrow\bullet$. It is dual to the notion of a [[pullback]].

## Pushouts in $Set$

In the category [[Set]] a 'pushout' is a quotient of the disjoint union of two sets.  Given a diagram of sets and functions like this:

\begin{center}
  \begin{tikzcd}
      & C \ar[ld, "f"'] \ar[rd, "g"] \\
    A &   & B
  \end{tikzcd}
\end{center}

the 'pushout' of this diagram is the set $X$ obtained by taking the disjoint union $A + B$ and identifying $a \in A$ with $b \in B$ if there exists $x \in C$ such that $f(x) = a$ and $g(x) = b$ (and all identifications that follow to keep [[equality]] an [[equivalence relation]]).

This construction comes up, for example, when $C$ is the intersection of the sets $A$ and $B$, and $f$ and $g$ are the obvious inclusions.  Then the pushout is just the union of $A$ and $B$.

Note that there are maps $i_A : A \to X$, $i_B : B \to X$ such that $i_A(a) = [a]$ and $i_B(b) = [b]$ respectively.  These maps make this square commute:

\begin{center}
  \begin{tikzcd}
                      & C \ar[ld, "f"'] \ar[rd, "g"] \\
    A \ar[rd, "i_A"'] &   & B \ar[ld, "i_B"] \\
                      & X
  \end{tikzcd}
\end{center}

In fact, the pushout is the [[universal property|universal]] solution to finding a [[commutative square]] like this.  In other words, given _any_ commutative square 

\begin{center}
    \begin{tikzcd}
                             & C \arrow[ld, "f"'] \arrow[rd, "g"] &                     \\
        A \arrow[rd, "j_A"'] &                                    & B \arrow[ld, "j_B"] \\
                             & Y                                  &                    
    \end{tikzcd}
\end{center}

there is a unique function $h: X \to Y$ such that 
$$ h i_A = j_A $$
and
$$ h i_B = j_B .$$
Since this universal property expresses the concept of pushout purely arrow-theoretically, we can formulate it in any category.  It is, in fact, a simple special case of a [[colimit]].  


## Definition

A **pushout** is a [[colimit]] of a [[diagram]] like this:

\begin{center}
    \begin{tikzcd}
          & c \arrow[ld, "f"'] \arrow[rd, "g"] &   \\
        a &                                    & b
    \end{tikzcd}
\end{center}

Such a diagram is called a [[span]].  If the colimit exists, we obtain a [[commutative square]]

\begin{center}
    \begin{tikzcd}
                             & c \arrow[ld, "f"'] \arrow[rd, "g"] &                     \\
        a \arrow[rd, "i_a"'] &                                    & b \arrow[ld, "i_b"] \\
                             & \chi                               &                    
    \end{tikzcd}
\end{center}

and the object $x$ is also called the **pushout**.  It has the universal property already described above in the special case of the category $Set$.

Other terms: $x$ is a __cofibred coproduct__ of $a$ and $b$, or (especially in [[algebraic categories]] when $f$ and $g$ are [[monomorphisms]]) a free product of $a$ and $b$ with $c$ __amalgamated__, or more simply an __amalgamation__ (or __amalgam__) of $a$ and $b$.

The concept of pushout is a special case of the notion of **[[cofiber coproduct|wide pushout]]** (compare [[wide pullback]]), where one takes the colimit of a diagram which consists of a set of arrows $\{f_i: c \to a_i\}_{i \in I}$. Thus an ordinary pushout is the case where $I$ has cardinality $2$. 

Note that the concept of pushout is dual to the concept of [[pullback]]: that is, a pushout in $C$ is the same as a pullback in $C^{op}$.

See [[pullback]] for more details.

## Properties

### In any category

+-- {: .num_prop #PushoutsAsCoequalizers}
###### Proposition
**(pushouts as coequalizers)

If [[coproducts]] exist in some [[category]], then the pushout

\begin{center}
    \begin{tikzcd}
        a \ar[r, "f"] \ar[d, "g"'] & b \ar[d] \\
        c \ar[r]                   & b \underset{a}{\sqcup} c    
    \end{tikzcd}
\end{center}

is equivalently the [[coequalizer]]

\begin{center}
  \begin{tikzcd}
     a 
     \ar[r, "i_1 \circ f", shift left] 
     \ar[r, "i_2 \circ g"', shift right] 
     & 
     b \sqcup  c 
     \arrow[r] 
     &[-35pt]
     b 
       \underset{a}{\sqcup} 
     c
  \end{tikzcd}
\end{center}

of the two morphisms induced by $f$ and $g$ into the [[coproduct]] of $b$ with $c$.

=--

+-- {: .num_prop #PushoutPreservesEpimorphisms}
###### Proposition
**(pushouts preserves epimorphisms and isomorphisms)

Pushouts preserve [[epimorphisms]] and [[isomorphisms]]:

If 

\begin{center}
    \begin{tikzcd}
        a \arrow[r, "f"] \arrow[d, "g"'] & b \arrow[d, "f_\ast g"] \\
        c \arrow[r]                      & d                      
    \end{tikzcd}
\end{center}

is a pushout square in some category then:

1. if $g$ is a [[epimorphism]] then $f_\ast g$ is an epimorphism;

1. if $g$ is an [[isomorphism]] then $f_\ast g$ is an isomorphism.

=--


+-- {: .num_prop}
###### Proposition
**([[pasting law for pushouts]])**

Consider a [[commuting diagram]] of the following shape in any category:


\begin{center}
    \begin{tikzcd}
        x \arrow[r] \arrow[d] & y \arrow[r] \arrow[d] & z \arrow[d] \\
        u \arrow[r]           & v \arrow[r]           & w          
    \end{tikzcd}
\end{center}

If the left square is a [[pushout]], then the total rectangle is a pushout if and only if the right square is a pushout.

=--

+-- {: .proof}
###### Proof
See the proof of the dual property for [[pullbacks]].
=--

+-- {: .num_prop}
###### Proposition

The converse implication does not hold: it may happen that the outer and the right square are pushouts, but not the left square. 

=--

+-- {: .proof}
###### Proof

See the proof of the dual proposition for [[pullbacks]].

=--


### In a quasitopos

+-- {: .num_prop #PushoutOfStrongMonomorphismInQuasitopos}
###### Proposition
**pushout of [[strong monomorphism]] in [[quasitopos]]**

Suppose that $(\mathrm{T},\mathcal{C})$ is either

* ([[monomorphism]],[[topos]]), or
* ([[strong monomorphism]],[[quasitopos]])

Suppose that 

\begin{center}
    \begin{tikzcd}
        {O_{0,1}} \arrow[r] \arrow[d, "m"'] & {O_{1,1}} \arrow[d, "h"] \\
        {O_{0,0}} \arrow[r]                 & {O_{1,0}}               
    \end{tikzcd}
\end{center}

is a [[commutative diagram]] in $\mathcal{C}$ such that 

* $m$ is $\mathrm{T}$ in $\mathcal{C}$
* the diagram is a pushout in $\mathcal{C}$


Then 

* $h$ is $\mathrm{T}$ in $\mathcal{C}$
* the diagram is a pullback in $\mathcal{C}$

=--

See at _[[quasitopos]]_ [this lemma](quasitopos#PushoutOfStrongMonos). Note that the result for quasitoposes immediately implies the result for toposes, since all monomorphisms $i: A \to B$ in a topos are [[regular monomorphism|regular]] ($i$ being the equalizer of the arrows $\chi_i, t \circ !: B \to \Omega$ in 

\begin{center}
    \begin{tikzcd}
                                               & 1 \arrow[d, "t"] \\
        B \arrow[ru, "!"] \arrow[r, "\chi_i"'] & \Omega          
    \end{tikzcd}
\end{center}

where $\chi_i$ is the classifying map of $i$) and therefore strong. 



## Examples

...

## Related entries

* [[amalgamation property]]

* [[wide pushout]]

* [[coequalizer]]

* [[colimit]]

* [[pullback]]

## References

Textbook accounts:

* [[Francis Borceux]], Section 2.5 in Vol. 1: *Basic Category Theory* of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))




[[!redirects pushout]]
[[!redirects pushouts]]
[[!redirects pushout diagram]]
[[!redirects pushout diagrams]]
[[!redirects cocartesian diagram]]
[[!redirects cocartesian diagrams]]
[[!redirects cocartesian square]]
[[!redirects cocartesian squares]]

[[!redirects cofibred coproduct]]
[[!redirects cofibred coproducts]]
[[!redirects cofibered coproduct]]
[[!redirects cofibered coproducts]]
[[!redirects cofiber coproduct]]
[[!redirects cofiber coproducts]]

[[!redirects amalgamated free product]]
[[!redirects amalgamated free products]]
[[!redirects amalgamated coproduct]]
[[!redirects amalgamated coproducts]]
[[!redirects amalgamation]]
[[!redirects amalgamations]]
[[!redirects amalgam]]
[[!redirects amalgams]]