[[!redirects absolute pushouts]]

#Contents#
* table of contents
{:toc}

## Idea

An **absolute pushout** is a [[pushout]] which is [[preserved limit|preserved]] by any [[functor]] whatsoever.  In general this happens because the pushout is a pushout for purely "diagrammatic" reasons.  See [[absolute colimit]] for more.

## Definitions

+-- {: .num_defn #DefBasic}
###### Definition
A particular [[pushout]] [[diagram]] in a particular [[category]] $C$ is an **absolute pushout** if it is [[preserved limit|preserved]] by every [[functor]] with [[domain]] $C$.
=--

Equivalently, since the [[Yoneda embedding]] is the [[free cocompletion]] of $C$:

+-- {: .num_defn #DefYoneda}
###### Definition
A particular [[pushout]] diagram in a particular [[category]] $C$ is an **absolute pushout** if it is [[preserved limit|preserved]] by the [[Yoneda embedding]] $C \hookrightarrow [C^{op},Set]$.
=--

## Split pushouts

We propose the following notion of **split pushout**.

+-- {: .num_defn #DefSplitPushout}
###### Definition
A [[commutative diagram|commutative]] square 

\begin{center}\begin{tikzcd}
A \ar[r, "p"] \ar[d, "q"'] & B \ar[d, "m"] \\ C \ar[r, "n"'] & P
\end{tikzcd}\end{center}

defines a **split pushout** if there exist [[sections]] $p s = 1$, $q t = 1$, $m u = 1$
\begin{center}\begin{tikzcd}
A \ar[r, "p"'] \ar[d, "q"] & B \ar[d, "m"'] \ar[l, bend right, "s"'] \\ C \ar[r, "n"] \ar[u, bend left, "t"] & P \ar[u, bend right, "u"']
\end{tikzcd}\end{center}
so that $p t = u n$.
=--

## Split pushouts are absolute pushouts

+-- {: .num_prop }
###### Proposition
Split pushouts are absolute pushouts.
=--

+-- {: .proof}
###### Proof
Note that split pushouts are preserved by arbitrary functors, so it suffices to show that a split pushout is a pushout in the category in which it lives. To that end consider, a [[cone]] under the [[span]] $(p,q)$:
\begin{center}\begin{tikzcd}
A \ar[r, "p"] \ar[d, "q"'] & B \ar[d, "b"] \\ C \ar[r, "c"'] & X
\end{tikzcd}\end{center}
Upon composing with the sections to $q$ and $m$
\begin{center}\begin{tikzcd}
C \ar[d, "t"'] \ar[r, "p"]\ar[dd, bend right, equals]& P \ar[d, "u"]  \\
 A \ar[r, "p"] \ar[d, "q"'] & B \ar[d, "b"] \\ C \ar[r, "c"'] & X
\end{tikzcd}\end{center}
we see that $c$ factors through the claimed pushout $P$ as $c = (b  u) n$. We must verify that $b$ also factors as $b = (b  u)  m$. Since $p$ is an epimorphism, it suffices to prove that $b p = b u m p$, which follows easily:
$$ b p = c q = b u n q = b u m p.$$
This produces the desired factorization. Finally, since $m$ is an epimorphism, such factorizations are unique.
=--

Note the proof that a split pushout defines a pushout square in the category in which it lives did not require $p$ to be a _split_ epimorphism. However, arbitrary functors do not preserve epimorphisms. They do however preserve split epimorphisms, and thus the section guarantees that the image of $p$ will define an epimorphism in any category.

## General characterization

\begin{theorem}
A commutative square
\begin{center}\begin{tikzcd}
A \ar[r, "p"] \ar[d, "q"'] & B \ar[d, "m"] \\ C \ar[r, "n"'] & P
\end{tikzcd}\end{center}
is an absolute pushout if and only if either there exist

1. A section $s:P\to C$, such that $n s = 1_P$;
2. Morphisms $s_1,\dots,s_n : B \to A$ and $t_1,\dots,t_n : B\to A$, for some $n\ge 1$, such that $p s_1 = 1_C$, $p t_n = s n$, $q s_i = q t_i$, and $p t_i = p s_{i+1}$; and
3. Morphisms ...

or the transpose thereof (i.e. interchanging $B$ with $C$ and so on).
\end{theorem}

## Examples

In their study of [[generalized Reedy categories]], Berger and Moerdijk introduce the notion of an [[Eilenberg-Zilber category]], one of the axioms of which demands that spans of split epimorphisms admit absolute pushouts. In practice, this seems to be the case because the pushout of these split epimorphisms is a split epimorphism as above, often with an additional section $v$ of $n$ satisfying the additional equation that $v m = q s$.


## References

The Berger-Moerdijk definition of an Eilenberg-Zilber category appears in:

* {#BergerMoerdijk} [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_ (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 

