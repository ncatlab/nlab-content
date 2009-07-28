# Idea #

Given a [[Reedy category]] $R$ and a [[model category]] $C$ the **Reedy model structure** is a [[model category]] structure on the [[functor category]] $[R,C] = Func(R,C)$.

If $C^\circ$ denotes the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ then the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by the Reedy model structure on $Func(R,C)$ should be the [[(∞,1)-category of (∞,1)-functors]] $Func_\infty(R,C^\circ)$.


#Definition#

+-- {: .num_theorem #model}
###### Theorem
If $R$ is a [[Reedy category]] and $C$ is a [[model category]], then there is a canonical induced [[model category|model structure]] on the [[functor category]] $C^R$ in which the weak equivalences are the objectwise weak equivalences in $C$.
=--

The basic idea is as follows.  Given a diagram $X:R\to M$ and an object $r\in R$, define its **latching object** to be
$$ L_r X = \colim_{s \overset{+}{\to} r} X_s$$
where the colimit is over the full subcategory of $R_+/r$ containing all objects except the identity $1_r$.  Dually, define its **matching object** to be
$$ M_r X = \lim_{r \overset{-}{\to} s} X_s$$
where the limit is over the full subcategory of $r/R_-$ containing all objects except $1_r$.  There are evident canonical, and natural, morphisms
$$L_r X\to X_r \to M_r X.$$
Note that $L_0 X = 0$ is the initial object and $M_0 X$ is the terminal object, since there are no objects of degree $\lt 0$.

In the case $R=\Delta^{op}$, the latching object $L_n X$ can be thought of as the object of _degenerate_ $n$-simplices sitting inside the object $X_n$ of all $n$-simplices.  When $R=\alpha$ is an ordinal, then $L_{n+1} X = X_n$ and $M_n X = 1$, and dually for $R=\alpha^{op}$.

We now define a morphism $f:X\to Y$ in $M^R$ to be a cofibration or trivial cofibration if for all $r$, the map
$$L_r Y \sqcup_{L_r X} X_r \to Y_r$$
is a cofibration or trivial cofibration in $M$, respectively, and to be a fibration or trivial fibration if for all $r$, the map
$$ X_r \to M_r X \times_{M_r Y} Y_r$$
is a fibration or trivial fibration in $M$, respectively.  Define $f$ to be a weak equivalence if each $f_r$ is a weak equivalence in $M$.

One then verifies that this defines a model structure; the details can be found in (for instance) Hovey and Hirschhorn's books.  In particular, to factor a morphism $f:X\to Y$ in either of the two necessary ways, we construct the factorization $f_r = g_r h_r$ inductively on $r$, by factoring the induced morphism
$$ L_r Z \sqcup_{L_r X} X_r \to M_r Z \times_{M_r Y} Y_r$$
in the appropriate way in $M$.


# Remarks

* Any Reedy cofibration or fibration is, in particular, an objectwise one, but the converse does not generally hold.

* An object $X$ is Reedy cofibrant if and only if each map $L_r X \to X_r$ is a cofibration in $M$.  In particular, this implies that each $X_r$ is cofibrant in $M$.

* For some $M$, $M^R$ also admits a [[projective model structure|projective]] or [[injective model structure|injective]] model structures.  For instance for $M = $ [[SSet]] this is the [[global model structure on simplicial presheaves]]. 

  In general the Reedy structure will not be the same as either, but will be a kind of mixture of both. If $R = R_+$ then the Reedy model structure coincides with the [[injective model structure]], if $R = R_-$ it coincides with the [[projective model structure]].

  For a detailed comparison of Reedy and global projective/injective model structures see around example A.2.9.22 in [[Higher Topos Theory|HTT]].


* In addition to its existing for all $C$, another advantage of the Reedy structure is the explicit nature of its cofibrations, fibrations, and factorizations.

* If $R$ admits more than one structure of Reedy category, then $C^R$ will have more than one Reedy model structure.  For instance, if $R = (\cdot\to\cdot)$ is the walking arrow, then we can regard it as either the ordinal $2$ or its opposite $2^{op}$, resulting in two different Reedy model structures on $C^2$.

* For a general Reedy category $R$, the diagonal functor $C\to C^R$ need not be either a right or a left [[Quillen adjunction|Quillen functor]] (although, of course, it has left and right adjoints given by colimits and limits over $R$).  One can, however, characterize those Reedy categories for which one or the other is the case, and in this case one can construct [[homotopy limit|homotopy limits]] and colimits using the derived functors of these Quillen adjunctions.
