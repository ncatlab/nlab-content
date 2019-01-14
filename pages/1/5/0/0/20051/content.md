# Semi-left-exact reflections

* table of contents
{: toc}

## Idea

A **semi-left-exact reflection** is a [[reflector]] into a [[reflective subcategory]] that preserves some [[pullbacks]].  It fits into a hierarchy of left-exactness properties for reflectors:

\begin{center}
  [[left exact reflection|left exact]] $\Rightarrow$ [[reflection with stable units|stable units]] $\Rightarrow$ **semi-left-exact** $\Rightarrow$ [[simple reflection|simple]]
\end{center}

In particular, semi-left-exactness is sufficient to imply that the corresponding [[reflective factorization system]] exists and can be constructed in one step, and that the reflective subcategory inherits [[local cartesian closure]] from the ambient category.

## Definitions

Let $C$ be a [[category]] with [[finite limits]], and $B\subseteq C$ a [[full subcategory|full]] [[reflective subcategory]] with reflector $L:C\to B$.  Let $E$ be the class of morphisms inverted by $L$, and let $M$ be the class of morphisms right orthogonal to $E$, i.e. $(E,M)$ is the associated [[reflective prefactorization system]].

The following is a combination of Theorems 4.1 and 4.3 from [CHK](#CHK) with Proposition 1.3 from [GK](#GK).

\begin{theorem}
  The following are equivalent:

  1. Every pullback of an $E$-morphism along an $M$-morphism is an $E$-morphism.
  2. $L$ preserves pullbacks along $M$-morphisms.
  3. $L$ preserves pullbacks along any morphism in $B$.
  4. If $f:x\to y$ is a morphism in $B$, then $f^* : C/y \to C/x$ preserves $E$-morphisms.
  5. (If $C$ is locally cartesian closed) If $f:x\to y$ is a morphism in $B$, then $f_* : C/x \to C/y$ maps $B/x$ into $B/y$.

  They all imply that $(E,M)$ is a factorization system and that the factorization of an arbitrary morphism $f:x\to y$ can be constructed as the following pullback:

(error)

  If these conditions hold, we say that the reflector is **semi-left-exact**.
\end{theorem}
\begin{proof}
  Since all morphisms in $B$ are $M$-morphisms, (2) implies (3).  Now given (3), the functor $f^*$ commutes with localization $L/x : C/x \to B/x$ and $L/y : C/y \to B/y$, so if $e\in E$ is inverted by the latter then $f^*(e)$ is inverted by the former; thus (4) holds.  On the other hand, $f^*(e)$ is also the pullback of $e$ along a pullback of $f$, and since the latter is an $M$-morphism, (1) also implies (4).

  Now assuming (4), in the diagram above $g$ must be an $E$-morphism, hence by 2-out-of-3 so is $\lambda_f$, while $\rho_f\in M$ since $M$ is closed under pullback and $L f \in M$; thus the factorization exists.

  It now follows that if $f\in M$ to start with, then $\lambda_f$ must be an isomorphism, hence the naturality square for $\eta$ at $f$ is a pullback.  Now the pullback pasting law combined with (4) implies (1) and (2).

  Finally, if $C$ is locally cartesian closed, then (4) implies (5) by adjointness, while (5) implies (3) in the form $L/x \circ f^* \cong L/y \circ f^*$ by passage to right-adjoint mates.
\end{proof}

Of course, if $L$ preserves all pullbacks (i.e. it is [[left exact reflection|left exact]]), then it is semi-left-exact.  The statement about the existence of the reflective factorization system implies that any semi-left-exact reflection is [[simple reflection|simple]].

## Properties

Semi-left-exactness of a reflection $\ell$ of $C$ into $B\subseteq C$ is also equivalent to saying that for any $x\in C$, the right adjoint of the induced functor $\ell\colon C/x \to B/\ell(x)$ (which is given by pullback along $\eta_x$) is fully faithful.  In this form it is equivalent to (a particular case of) the notion of *admissible* reflection in [[categorical Galois theory]].

+--{: .query}
[[Mike Shulman]]: I no longer see why that's true.  Full-faithfulness of the right adjoint says that $E$-morphisms are preserved by pullback along morphisms in $B$, but that seems weaker than any of the above characterizations.
=--


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
