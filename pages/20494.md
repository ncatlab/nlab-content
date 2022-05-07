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
C \ar[d, "t"'] \ar[r, "n"]\ar[dd, bend right, equals]& P \ar[d, "u"]  \\
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

1. A section $u:P\to B$, such that $m u = 1_P$.
2. Morphisms $r_1,\dots,r_k : B \to A$ and $s_1,\dots,s_k : B\to A$, for some $k\ge 1$, such that $p s_1 = 1_B$, $q s_i = q r_i$ for all $i$, $p r_i = p s_{i+1}$ for all $i\lt k$, and $p r_k = u m$.
3. Morphisms $t_1,\dots,t_{\ell+1} : C \to A$ and $v_1,\dots,v_{\ell} : C\to A$, for some $\ell \ge 0$, such that $q t_1 = 1_C$, $p t_i = p v_i$ for all $i\lt \ell$, $q v_i = q t_{i+1}$ for all $i\le \ell$, and $p t_{\ell+1} = s n$.

or the transpose thereof (i.e. interchanging $B$ with $C$ and so on).
\end{theorem}
\begin{proof}
For "if", suppose given a commutative square
\begin{center}\begin{tikzcd}
A \ar[r, "p"] \ar[d, "q"'] & B \ar[d, "b"] \\ C \ar[r, "c"'] & X.
\end{tikzcd}\end{center}
Since $m$ is a (split) epimorphism (by $s$), any factorization of this square through the given one will be unique, so it suffices to show that such a factorization exists.  Define $x = b u:P\to X$.  Then we have
$$ x m = b u m = b p r_k = c q r_k = c q s_k = b p s_k = b t r_{k-1} = \dots = b p s_1 = b $$
and
$$ x n = b s n = b p t_\ell = c q t_\ell = c q v_{\ell-1} = b p v_{\ell-1} = b p t_{\ell-1} = \dots = c q t_1 = c. $$
The transposed case is of course dual.

Conversely, suppose the given square is an absolute pushout.  Thus, in particular the induced square
\begin{center}\begin{tikzcd}
\hom(P,A) \ar[r, "p"] \ar[d, "q"'] & \hom(P,B) \ar[d, "m"] \\ \hom(P,C) \ar[r, "n"'] & \hom(P,P)
\end{tikzcd}\end{center}
is a pushout in $Set$.  Thus, in particular, the function $\hom(P,B)+\hom(P,C) \to \hom(P,P)$ is surjective, and thus for $1_P\in \hom(P,P)$ there must be either a $u:P\to B$ such that $m u = 1_P$ or a $u':P\to C$ such that $n u' = 1_P$.  WLOG assume the former.

Now the induced square
\begin{center}\begin{tikzcd}
\hom(B,A) \ar[r, "p"] \ar[d, "q"'] & \hom(B,B) \ar[d, "m"] \\ \hom(B,C) \ar[r, "n"'] & \hom(B,P)
\end{tikzcd}\end{center}
is also a pushout in $Set$.  We have two elements $1_B, u m \in \hom(B,B)$ that become equal in $\hom(B,P)$ (since $m 1_B = m = (1_P) m = m u m$), and in a pushout in $Set$ this means they must be related by a zigzag of elements of the vertex $\hom(B,A)$.  Unraveling this explicitly produces the morphisms $r_i,s_i$.

Similarly, from the induced square
\begin{center}\begin{tikzcd}
\hom(C,A) \ar[r, "p"] \ar[d, "q"'] & \hom(C,B) \ar[d, "m"] \\ \hom(C,C) \ar[r, "n"'] & \hom(C,P)
\end{tikzcd}\end{center}
and the elements $1_C\in\hom(C,C)$ and $s n \in \hom(C,B)$, we obtain the morphisms $t_i,v_i$.
\end{proof}

In particular, when $k=1$ and $\ell=0$, the above data reduces to

1. A section $u:P\to B$, such that $m u = 1_P$.
2. Morphisms $r,s : B \to A$ such that $p s = 1_B$, $q s = q r$, and $p r = u m$.
3. A morphism $t : C \to A$ such that $q t = 1_C$ and $p t = u n$.

This is precisely the data of the above-defined notion of split pushout, together with the additional morphism $r:B\to A$ such that $q r = q s$ and $p r = u m$.  However, given a split pushout as above we can define $r = t q s$ and check $q r = q t q s = q s$ and $p r = p t q s = u n q s = u m p s = u m$.  This gives another proof that any split pushout is an absolute pushout. 

## Examples

In their study of [[generalized Reedy categories]], Berger and Moerdijk introduce the notion of an [[Eilenberg-Zilber category]], one of the axioms of which demands that spans of split epimorphisms admit absolute pushouts. In practice, this seems to be the case because the pushout of these split epimorphisms is a split epimorphism as above, often with an additional section $v$ of $n$ satisfying the additional equation that $v m = q s$.


## References

The general characterization of absolute pushouts appears as Proposition 5.5 in:

* Robert Par&eacute;, Robert On absolute colimits. J. Algebra 19 (1971), 80–95. 

The Berger-Moerdijk definition of an Eilenberg-Zilber category appears in:

* {#BergerMoerdijk} [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_ (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 

