# Semi-left-exact reflections

* table of contents
{: toc}

## Idea

A **semi-left-exact reflection** (also called a *locally cartesian reflection*) is a [[reflector]] into a [[reflective subcategory]] that preserves some [[pullbacks]].  It fits into a hierarchy of left-exactness properties for reflectors:

$\;\;\;\;\;\;\;\;$
[left exact](reflective+subcategory#ExactReflectiveSubcategories) $\;\;\Rightarrow\;\;$
[[reflection with stable units|stable units]] 
$\;\;\Rightarrow\;\;$ 
**semi-left-exact** 
$\;\;\Rightarrow\;\;$ 
[[simple reflection|simple]]

In particular, semi-left-exactness is sufficient to imply that the corresponding [[reflective factorization system]] exists and can be constructed in one step, and that the reflective subcategory inherits [[local cartesian closure]] from the ambient category.

## Definitions

Let $C$ be a [[category]] with [[finite limits]], and $B\subseteq C$ a [[full subcategory|full]] [[reflective subcategory]] with reflector $L:C\to B$.  Let $E$ be the class of morphisms inverted by $L$, and let $M$ be the class of morphisms right orthogonal to $E$, i.e. $(E,M)$ is the associated [[reflective prefactorization system]].

The following is a combination of Theorems 4.1 and 4.3 from [CHK](#CHK) with Proposition 1.3 from [GK](#GK).

\begin{theorem}
  The following are equivalent:

  1. Every pullback of an $E$-morphism along an $M$-morphism is an $E$-morphism.
  2. Every pullback of an $E$-morphism along a morphism in $B$ is an $E$-morphism.
  3. Every pullback of a reflection unit $\eta_x : x \to L x$ along a morphism in $B$ is an $E$-morphism.
  4. $L$ preserves pullbacks along $M$-morphisms.
  5. $L$ preserves pullbacks along any morphism in $B$.
  6. If $f:x\to y$ is a morphism in $B$, then $f^* : C/y \to C/x$ preserves $E$-morphisms.
  7. (If $C$ is locally cartesian closed) If $f:x\to y$ is a morphism in $B$, then $f_* : C/x \to C/y$ maps $B/x$ into $B/y$.

  They all imply that $(E,M)$ is a factorization system and that the factorization of an arbitrary morphism $f:x\to y$ can be constructed as the following pullback:

  \begin{center}
    \begin{tikzcd}
      x \ar[dr] \ar[drr,"{\eta_x}"] \ar[ddr,"f"'] \ar[dr,"{\lambda_f}" description] \\
      & \bullet \ar[r,"g"'] \ar[d,"{\rho_f}"] & L x \ar[d,"L f"] \\
      & y \ar[r,"{\eta_y}"'] & L y
    \end{tikzcd}
  \end{center}
  If these conditions hold, we say that the reflector is **semi-left-exact**.
\end{theorem}
\begin{proof}
  Since all morphisms in $B$ are $M$-morphisms, (1)$\Rightarrow$(2) and (4)$\Rightarrow$(5), while (2)$\Rightarrow$(3) since the reflection units are in $E$.  And since $E$ consists of the $L$-inverted morphisms, (5)$\Rightarrow$(2) and (4)$\Rightarrow$(1).  And clearly (6)$\Rightarrow$(2); while for $f\in B$ the action of $f^*$ on a morphism in $C/y$ is the latter's pullback along a pullback of $f$, and any pullback of $f$ lies in $M$; thus (1)$\Rightarrow$(6).  So to complete the equivalence of (1)-(6) it will suffice to show that (3) implies (4).

  First we prove that (3) implies the factorization exists.  For in the diagram above $g$ is a pullback of the unit $y\to L y$ along the morphism $L x \to L y$ in $B$, hence $g\in E$; so by 2-out-of-3 $\lambda_f\in E$, while $\rho_f\in M$ since $M$ is closed under pullback and $L f \in M$.

  Now this construction implies that if $f\in M$ then $\lambda_f$ is invertible, hence the naturality square for $\eta$ at $f$ is a pullback.  Now if we want to pull back some $h:c\to k$ along an $M$-morphism $f:a\to k$, we can paste two pullback squares to obtain a large pullback rectangle:

\begin{center}
  \begin{tikzcd}
    d \ar[r] \ar[d] & a \ar[d,"f"] \ar[r,"{\eta_a}"] & L a \ar[d,"{L f}"]\\
    c \ar[r,"h"'] & k \ar[r,"{\eta_k}"'] & L k.
  \end{tikzcd}
\end{center}

  Since $\eta_k \circ h = L h \circ \eta_c$ by naturality, we can now factor this pullback rectangle through the pullback of $f$ along $L h$:

\begin{center}
  \begin{tikzcd}
    d \ar[r,dashed] \ar[d] & e \ar[r] \ar[d] & L a \ar[d,"{L f}"]\\
    c \ar[r,"{\eta_c}"'] & L c \ar[r,"{L h}"'] & L k
  \end{tikzcd}
\end{center}

  so that the left-hand square is also a pullback.  But this is a pullback of the reflection unit $\eta_c$ along the map $e\to L c$ that lies in $B$ (since $B$ is closed under pullbacks).  Thus by (3) the map $d \to e$ lies in $E$, and hence exhibits $e$ as $L d$.  The right-hand pullback square above is then $L$ applied to the given pullback square, so that $L$ indeed preserves this pullback, i.e. (4) holds.

  Finally, if $C$ is locally cartesian closed, then (6) implies (7) by adjointness, while (7) implies (5) in the form $L/x \circ f^* \cong L/y \circ f^*$ by passage to right-adjoint mates.
\end{proof}

Of course, if $L$ preserves all pullbacks (i.e. it is [[left exact reflection|left exact]]), then it is semi-left-exact.  The statement about the existence of the reflective factorization system implies that any semi-left-exact reflection is [[simple reflection|simple]].

\begin{remark}
  Note that for any $x\in C$, the functor $L/x\colon C/x \to B/L x$ has a right adjoint given by pullback along $\eta_x : x \to L x$.  Condition (3) above then says that the counit of this adjunction is an isomorphism, which is to say that this right adjoint is fully faithful.  In this form, semi-left-exactness is equivalent to (a particular case of) the notion of *admissible* reflection in [[categorical Galois theory]].
\end{remark}

## Related pages

* [[semi-left-exact left Bousfield localization]]

## References

* {#CHK} Cassidy and H&#233;bert and [[Max Kelly|Kelly]], "Reflective subcategories, localizations, and factorization systems".  *J. Austral. Math Soc. (Series A)* 38 (1985), 287--329 ([pdf](http://journals.cambridge.org/download.php?file=%2FJAZ%2FJAZ1_38_03%2FS1446788700023624a.pdf&code=5796045be8904c5183c2e95bce65491e))

* {#GK} [[David Gepner]] and [[Joachim Kock]], *Univalence in locally cartesian closed categories*, [arxiv:1208.1749](https://arxiv.org/abs/1208.1749)

[[!redirects semi-left-exact reflection]]
[[!redirects semi-left-exact reflections]]
[[!redirects semi left exact reflection]]
[[!redirects semi left exact reflections]]
[[!redirects semi left-exact reflection]]
[[!redirects semi left-exact reflections]]
[[!redirects semi-left exact reflection]]
[[!redirects semi-left exact reflections]]

[[!redirects semi-left-exact reflector]]
[[!redirects semi-left-exact reflectors]]
[[!redirects semi left exact reflector]]
[[!redirects semi left exact reflectors]]
[[!redirects semi left-exact reflector]]
[[!redirects semi left-exact reflectors]]
[[!redirects semi-left exact reflector]]
[[!redirects semi-left exact reflectors]]

[[!redirects semi-left-exact reflective subcategory]]
[[!redirects semi-left-exact reflective subcategories]]
[[!redirects semi left exact reflective subcategory]]
[[!redirects semi left exact reflective subcategories]]
[[!redirects semi left-exact reflective subcategory]]
[[!redirects semi left-exact reflective subcategories]]
[[!redirects semi-left exact reflective subcategory]]
[[!redirects semi-left exact reflective subcategories]]

[[!redirects semi-left-exact localization]]
[[!redirects semi-left-exact localizations]]
[[!redirects semi left exact localization]]
[[!redirects semi left exact localizations]]
[[!redirects semi left-exact localization]]
[[!redirects semi left-exact localizations]]
[[!redirects semi-left exact localization]]
[[!redirects semi-left exact localizations]]

[[!redirects semi-left-exact localisation]]
[[!redirects semi-left-exact localisations]]
[[!redirects semi left exact localisation]]
[[!redirects semi left exact localisations]]
[[!redirects semi left-exact localisation]]
[[!redirects semi left-exact localisations]]
[[!redirects semi-left exact localisation]]
[[!redirects semi-left exact localisations]]

[[!redirects locally cartesian reflection]]
[[!redirects locally cartesian reflections]]

[[!redirects locally cartesian reflector]]
[[!redirects locally cartesian reflectors]]

[[!redirects locally cartesian localization]]
[[!redirects locally cartesian localizations]]

[[!redirects locally cartesian localisation]]
[[!redirects locally cartesian localisations]]