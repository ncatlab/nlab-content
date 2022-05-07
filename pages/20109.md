# Homotopy factorization systems

* table of contents
{: toc}

## Idea

A **homotopy factorization system** in a [[model category]] is a presentation of an [[orthogonal factorization system in an (∞,1)-category|orthogonal factorization system]] in its [[simplicial localization|underlying]] [[(∞,1)-category]].

## The enriched case

### Definition

Let $V$ be a [[monoidal model category]] (with cofibrant unit object) and $M$ a $V$-[[enriched model category]].  In the case $V =$ [[SSet]], the following definition is found in [Bousfield, section 6](#Bousfield).

\begin{definition}
  A **homotopy factorization system** in $M$ is a pair $(L,R)$ of classes of maps such that:

  1. Every map in $L$ is a cofibration, and every map in $R$ is a fibration.
  2. If $i:A\to B$ is in $L$ and $p:X\to Y$ is in $R$, then the induced [[pullback power]]
     $$ [i,p] : [B,X] \to [A,X] \times_{[A,Y]} [B,Y] $$
     is an acyclic fibration in $V$.
  3. Every morphism in $M$ factors as a map in $L$ followed by a map in $R$.
  4. $L$ and $R$ are closed under [[retracts]].

\end{definition}

### Remarks

It follows that $(L,R)$ is in fact a [[weak factorization system]].  For on the one hand; the underlying-set functor $V(I,-) : V\to Set$ takes acyclic fibrations to surjections since $I$ is cofibrant; thus $(L,R)$ have the lifting property.  And on the other hand, if $i$ has the left lifting property against $R$, then factoring it and applying the retract argument implies $i\in L$, and dually.

Note that $[i,p]$ is automatically a fibration, since $i$ is a cofibration and $p$ a fibration; thus the content of assertion (2) is that this map is a weak equivalence.  If $A$ (hence also $B$) is cofibrant and $Y$ (hence also $X$) is fibrant, then the pullback $[A,X] \times_{[A,Y]} [B,Y]$ is pullback of two fibrations between fibrant objects and thus a [[homotopy pullback]]; thus in this case the condition is equivalent to asking that the square
\begin{center}
  \begin{tikzcd}
    {}[B,X] \ar[r] \ar[d] & {}[A,X] \ar[d]\\
    {}[B,Y] \ar[r] & {}[A,Y]
  \end{tikzcd}
\end{center}
is a homotopy pullback square.  If $V$ is [[right proper]], then the condition for the pullback to be a homotopy pullback can be weakened to "$A$ (hence also $B$) is cofibrant OR $Y$ (hence also $X$) is fibrant", and thus becomes automatic if either all objects of $M$ are fibrant or all objects of $M$ are cofibrant.


## The unenriched case

### Definition

A hierarchy of notions of "homotopy factorization system" for unenriched model categories can be found in [Joyal, Appendix F](#Joyal).  Let $M$ be a model category and $(L,R)$ a pair of classes of maps.  Write $C$ for the class of cofibrations, $F$ for the class of fibrations, $M_{c}$ for the subcategory of cofibrant objects, $M_f$ for the subcategory of fibrant objects, $M_{c f}$ for the subcategory of fibrant and cofibrant objects, $C_{c f}$ for the class of cofibrations between fibrant and cofibrant objects, etc.

\begin{definition}
  
* $(L,R)$ is a **weak homotopy factorization system** if
  1. $L$ and $R$ are closed under weak equivalence in the [[arrow category]] $M^\to$, and
  2. $(L\cap C_{c f}, R\cap F_{c f})$ is a [[weak factorization system]] in $M_{c f}$.
* $(L,R)$ is a **homotopy factorization system** if it is a weak homotopy factorization system and in addition
  1. If $f\in L$ and $g f\in L$, then $g\in L$.
  2. If $g\in R$ and $g f\in R$, then $f\in R$.
* $(L,R)$ is a **strong homotopy factorization system** if it is a homotopy factorization system and in addition
  1. $(L\cap C, R\cap F)$ is a weak factorization system in $M$.

\end{definition}

## Relation between definitions

The relation between the enriched and unenriched notions is unclear to the author of this page, but here are some things that can be said.

\begin{proposition}
  Suppose either every object of $M$ is fibrant and cofibrant, or $V$ is right proper and either every object of $M$ is fibrant or every object of $M$ is cofibrant.  Then given an enriched hfs, by closing $L$ and $R$ under weak equivalence in $M^\to$ we obtain an unenriched weak hfs $(L',R')$.
\end{proposition}
\begin{proof}
  Since $(L,R)$ is a wfs, to show that $(L',R')$ is an unenriched weak hfs, it suffices to show that $L'\cap C_{c f} = L \cap C_{c f}$ and dually.  Note that any morphism in $C_{c f}$ is both cofibrant and fibrant in the Reedy model structure on $M^\to$; hence if two such morphisms are weakly equivalent in $M^\to$, there is a single weak equivalence relating them.  But the property of being a homotopy pullback square is preserved under weak equivalence; and under the given hypotheses, as remarked above, the homotopy lifting property can be expressed in terms of such a square, and is thus preserved by weak equivalences between cofibrations.  The proof for $R$ is dual (using the other Reedy model structure).
\end{proof}

It is unclear whether or under what conditions this weak hfs is a hfs or a strong hfs.

In the converse direction, the following are proven by [Joyal](#Joyal):

* An unenriched weak hfs $(L,R)$ is determined by $(L\cap C_{c f}, R\cap F_{c f})$ (called its **center**).
* If $(L,R)$ is an unenriched weak hfs, then $L\cap C_C$ has the left lifting property against $R\cap F_f$.
* If $(L,R)$ is an unenriched weak hfs, then every morphism from a cofibrant object to a fibrant one factors as a map in $L\cap C_c$ followed by one in $R\cap F_f$.

\begin{proposition}
  If $(L,R))$ is an unenriched weak hfs, the following are equivalent:

  1. If $f\in L$ and $g f\in L$, then $g\in L$.
  2. If $g\in R$ and $g f\in R$, then $f\in R$.
  3. The codiagonal of any map in $L\cap C_c$ belongs to $L$.
  4. The diagonal of any map in $R\cap F_f$ belongs to $R$.
  5. if $f\in L\cap C_{c f}$ and $g f \in L\cap C_{c f}$ and $g\in C$, then $g\in L$.
  6. if $g\in R\cap F_{c f}$ and $g f \in R\cap F_{c f}$ and $f\in F$, then $f\in R$.

\end{proposition}

The closure under diagonals and codiagonals suggests that some kind of homotopy orthogonality should exist, using [[simplicial resolutions]] rather than enrichment.

## References

* {#Bousfield} [[A. K. Bousfield]], *Constructions of factorization systems in categories*, Journal of Pure and Applied Algebra 9 (1977) 207-220, [pdf](http://web.math.rochester.edu/people/faculty/doug/otherpapers/Bousfield_Fact.pdf)

* {#Joyal} [[Andre Joyal]], *Notes on quasi-categories*, [pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf)

[[!redirects homotopy factorization system]]
[[!redirects homotopy factorization systems]]
[[!redirects weak homotopy factorization system]]
[[!redirects weak homotopy factorization systems]]
[[!redirects strong homotopy factorization system]]
[[!redirects strong homotopy factorization systems]]
[[!redirects homotopy factorization system in a model category]]
[[!redirects homotopy factorization systems in a model category]]
[[!redirects factorization system in a model category]]
[[!redirects factorization systems in a model category]]
[[!redirects orthogonal factorization system in a model category]]
[[!redirects orthogonal factorization systems in a model category]]
