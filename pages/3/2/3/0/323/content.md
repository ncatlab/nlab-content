
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In the [[category]] [[Set]] a 'pullback' is a [[subset]] of the [[cartesian product]] of two [[sets]].  Given a [[diagram]] of [[sets]] and [[functions]] like this:

\begin{center}
  \begin{tikzcd}
    A \ar[rd, "f"'] &   & B \ar[ld, "g"] \\
                    & C
  \end{tikzcd}
\end{center}

the 'pullback' of this diagram is the [[subset]] $X \subseteq A \times B$ consisting of pairs $(a,b)$ such that the [[equation]] $f(a) = g(b)$ holds.  

A pullback is therefore the [[categorical semantics]] of an _[[equation]]_.

This construction comes up, for example, when $A$ and $B$ are [[fiber bundles]] over $C$: then $X$ as defined above is the [[product]] of $A$ and $B$ in the category of fiber bundles over $C$.  For this reason, a pullback is sometimes called a __fibered product__ (or _fiber product_ or _fibre product_).

In this case, the fiber of $A \times_C B$ over a [[generalized element|(generalized)]] element $x$ of $C$ is the ordinary [[product]] of the fibers of $A$ and $B$ over $x$.  In other words, the fiber product is the product taken fiber-wise.  Of course, the fiber of $A$ at the generalized element $x\colon I \to C$ is itself a fibre product $I \times_C A$; the terminology depends on your point of view.

Note that there are maps $p_A\colon X \to A$, $p_B\colon X \to B$ sending any $(a,b) \in X$ to $a$ and $b$, respectively.  These maps make this [[commuting diagram|square commute]]:

\begin{center}
  \begin{tikzcd}
                    & X \ar[ld, "p_A"'] \ar[rd, "p_B"] \\
    A \ar[rd, "f"'] &   & B \ar[ld, "g"]               \\
                    & C
  \end{tikzcd}
\end{center}

In fact, the pullback is the [[universal property|universal]] solution to finding a commutative square like this.  In other words, given _any_ [[commutative diagram|commutative square]] 

\begin{center}
  \begin{tikzcd}
                    & Y \ar[ld, "q_A"'] \ar[rd, "q_B"] \\
    A \ar[rd, "f"'] &   & B \ar[ld, "g"]               \\
                    & C
  \end{tikzcd}
\end{center}

there is a unique function $h\colon Y \to X$ such that 

$$ p_A h = q_A $$

and

$$ p_B h = q_B\,.$$

Since this universal property expresses the concept of pullback purely arrow-theoretically, we can formulate it in any category.  It is, in fact, a simple special case of a [[limit]].


## Definition

### In category theory

####As a limit

A **pullback** is a [[limit]] of a [[diagram]] like this:

\begin{center}
  \begin{tikzcd}
    a \ar[rd, "f"'] &   & b \ar[ld, "g"] \\
                    & c
  \end{tikzcd}
\end{center}

Such a diagram is also called a **pullback diagram** or a [[cospan]].  If the [[limit]] exists, we obtain a commutative square

\begin{center}
  \begin{tikzcd}
                    & x \ar[ld, "p_a"'] \ar[rd, "p_b"] \\
    a \ar[rd, "f"'] &   & b \ar[ld, "g"]               \\
                    & c
  \end{tikzcd}
\end{center}

and [[generalized the|the]] object $x$ is also called the **pullback**. It is well defined up to unique [[isomorphism]]. It has the universal property already described above in the special case of the category $Set$.

The last commutative square above is called a __pullback square__.

The concept of pullback is dual to the concept of [[pushout]]: that is, a pullback in $C$ is the same as a pushout in the [[opposite category]] $C^{op}$.

####Nuts and bolts

Let $\mathcal{C}$ be a category, with $f\colon a\to c$ and $g\colon b\to c$ coterminal arrows in $\mathcal{C}$ as below

\begin{center}
  \begin{tikzcd}
    a \ar[rd, "f"'] &   & b \ar[ld, "g"] \\
                    & c
  \end{tikzcd}
\end{center}

A **pullback** of $f$ and $g$ consists of an object $x$ together with arrows $p_a\colon x\to a$ and $p_b\colon x\to b$ such that the following diagram commutes universally

\begin{center}
  \begin{tikzcd}
                    & x \ar[ld, "p_a"'] \ar[rd, "p_b"] \\
    a \ar[rd, "f"'] &   & b \ar[ld, "g"]               \\
                    & c
  \end{tikzcd}
\end{center}

This means that for any other object $x'$ with arrows $p'_a\colon x'\to a$ and $p'_b\colon x'\to b$ such that 

\begin{center}
  \begin{tikzcd}
                    & x' \ar[ld, "p'_a"'] \ar[rd, "p'_b"] \\
    a \ar[rd, "f"'] &   & b \ar[ld, "g"]               \\
                    & c
  \end{tikzcd}
\end{center}

commutes, there exists a unique arrow $u\colon x'\to x$ such that

\begin{center}
  \begin{tikzcd}
                    & x' \ar[ld, "p'_a"'] \ar[rd, "p'_b"] \ar[d, "u", dotted] \\
    a & x \ar[l, "p_a"'] \ar[r, "p_b"]  & b               \\
  \end{tikzcd}
\end{center}

commutes.

### In type theory

In [[type theory]] a [[pullback]] $P$ in

\begin{center}
  \begin{tikzcd}
    P \ar[r] \ar[d] & A \ar[d, "f"] \\
    B \ar[r, "g"']  & C
  \end{tikzcd}
\end{center}

is given by the [[dependent sum]] over the [[dependent type|dependent]] [[equality type]]

$$
  P = \sum_{a\colon A} \sum_{b\colon B} (f(a) = g(b))
  \,.
$$



## Properties

+-- {: .num_prop #PullbacksAsEqualizers}
###### Proposition
**(pullbacks as equalizers)

If [[product]]s exist in $C$, then the pullback

\begin{center}
  \begin{tikzcd}
    a \times_c b \ar[r] \ar[d] & a \ar[d, "f"] \\
    b \ar[r, "g"']             & c
  \end{tikzcd}
\end{center}

is equivalently the [[equalizer]]

\begin{center}
  \begin{tikzcd}
    a \times_c b \ar[r] & a \times b \ar[r, shift left, "fp_1"] \ar[r, shift right, "gp_2"'] & c
  \end{tikzcd}
\end{center}

of the two morphisms induced by $f$ and $g$ out of the [[product]] of $a$ with $b$.

=--

As a consequence of the above, any category with binary products and equalizers has pullbacks.  Conversely any category with binary products and pullbacks has equalizers: the equalizer of $f,g:A \to B$ is the pullback of $(1,f) \maps A \to A \times B$ and $(1,g) \maps A \to A \times B$.

+-- {: .num_prop #PullbackPreservesMonomorphisms}
###### Proposition
**(pullbacks preserve monomorphisms and isomorphisms)

Pullbacks preserve [[monomorphisms]] and [[isomorphisms]]:

If 

\begin{center}
  \begin{tikzcd}
    a \ar[r] \ar[d, "f^\ast g"'] & b \ar[d, "g"] \\
    c \ar[r, "f"']               & d
  \end{tikzcd}
\end{center}

is a pullback square in some category then:

1. if $g$ is a [[monomorphism]] then $f^\ast g$ is a monomorphism;

1. if $g$ is an [[isomorphism]] then $f^\ast g$ is an isomorphism.

On the other hand that $f^\ast g$ is a monomorphism does not imply that $g$ is a monomorphism.

=--


+-- {: .num_prop}
###### Proposition
**([[pasting law for pullbacks]])**

In any category consider a diagram of the form

\begin{center}
  \begin{tikzcd}
    a \ar[r] \ar[d] & b \ar[r] \ar[d] & c \ar[d] \\
    d \ar[r]        & e \ar[r]        & f
  \end{tikzcd}
\end{center}

There are three commuting squares: the two inner ones and the outer one.

Suppose the right-hand inner square is a pullback, then: 

The square on the left is a pullback if and only if the outer square is.

=--

+-- {: .proof}
###### Proof

Pasting a morphism $x \to a$ with the outer square gives rise to a commuting square over the (composite) bottom and right edges of the diagram.  The square over the cospan in the left-hand inner square arising from $x \to a$ includes a morphism into $b$, which if $b$ is a pullback induces the same commuting square over $d \to e \to f$ and $c \to d$.  So one square is universal iff the other is.
=--


+-- {: .num_prop}
###### Proposition

The converse implication does not hold: it may happen that the outer and the left square are pullbacks, but not the right square. 

=--

+-- {: .proof}
###### Proof

For instance let $i\colon a \to b$ be a [[split monomorphism]] with [[retract]] $p\colon b \to a$ and consider

\begin{center}
  \begin{tikzcd}
    a \ar[r, "="] \ar[d, "="'] & a \ar[r, "="] \ar[d, "i"] & a \ar[d, "="] \\
    a \ar[r, "i"']             & b \ar[r, "p"']            & a
  \end{tikzcd}
\end{center}

Then the left square and  the outer rectangle are pullbacks but the right square cannot be a pullback unless $i$ was already an [[isomorphism]].

=--

+-- {: .num_remark }
###### Remark

On the other hand, in the [[(∞,1)-category]] of [[∞-groupoids]], there is a sort of "partial converse"; see [[homotopy pullback#HomotopyFiberCharacterization]].

=--

### Saturation

The [[saturated class of limits|saturation]] of the class of pullbacks is the class of limits over categories $C$ whose groupoid reflection $\Pi_1(C)$ is trivial and such that $C$ is [[L-finite category|L-finite]].

### Pullback functor
{#PullbackFunctor}

If $f\colon X \to Y$ is a [[morphism]] in a [[category]] $C$ with pullbacks, there is an induced pullback [[functor]] $f^*\colon C/Y \to C/X$, sometimes also called [[base change]].

## Related concepts

[[!include notions of pullback -- contents]]

## References

Textbook account:

* [[Francis Borceux]], Section 2.5 in Vol. 1: *Basic Category Theory* of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

See also:

* [[Joyal|André Joyal]], _[[joyalscatlab:Cartesian squares]]_

In view of more general [[finite limits]] and [[L-finite limits]]:

* [[Robert Paré]], *Simply connected limits*.  Can. J. Math., Vol. XLH, No. 4, 1990, pp. 731-746, [CMS](http://math.ca/10.4153/CJM-1990-038-6)



[[!redirects pullbacks]]
[[!redirects pullback square]]
[[!redirects pullback diagram]]
[[!redirects pullback squares]]
[[!redirects pullback diagrams]]
[[!redirects cartesian square]]
[[!redirects cartesian diagram]]
[[!redirects cartesian squares]]
[[!redirects cartesian diagrams]]
[[!redirects fiber product]]
[[!redirects fiber products]]
[[!redirects fibre product]]
[[!redirects fibre products]]
[[!redirects fibered product]]
[[!redirects fibered products]]
[[!redirects fibred product]]
[[!redirects fibred products]]