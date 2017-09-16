# Idea

A _Reedy category_ is a category $R$ equipped with a structure enabling the inductive construction of diagrams and natural transformations of shape $R$.  

The most important consequence of a Reedy structure on $R$ is the existence of a [[model category|model structure]] on the [[functor category]] $M^R$ whenever $M$ is a model category (no extra hypotheses on $M$ are required): the 

* [[Reedy model structure]] .

# Definition

A **Reedy category** is a [[category]] $R$ equipped with two [[wide subcategory|lluf subcategories]] $R_+$ and $R_-$ and a [[function]] $d:ob(R) \to \alpha$ called _degree_, where $\alpha$ is an [[ordinal number]], such that:

* Every nonidentity morphism in $R_+$ raises degree,
* Every nonidentity morphism in $R_-$ lowers degree, and
* Every morphism $f$ in $R$ factors uniquely as a map in $R_-$ followed by a map in $R_+$.


# Examples

* Any ordinal $\alpha$, considered as a [[poset]] and hence a category, is a Reedy category with $\alpha_+=\alpha$, $\alpha_-$ the [[discrete category]] on $ob(\alpha)$, and $d$ the identity.

* The [[opposite category|opposite]] of any Reedy category is a Reedy category; simply exchange $R_+$ and $R_-$.

* The prototypical examples of Reedy categories are the [[simplex category]] $\Delta$ and its opposite $\Delta^{op}$.  More generally, for any [[simplicial set]] $X$, its [[category of simplices]] $\Delta/X$ is a Reedy category.


# Model structures

See [[Reedy model structure]] for more.

+-- {: .num_theorem #model}
###### Theorem
If $R$ is a Reedy category and $M$ is a model category, then there is a canonical induced model structure on $M^R$ in which the weak equivalences are objectwise.
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




# Generalization

One problem with the notion of Reedy category is that it is [[evil]]: it is not invariant under [[equivalence of categories]].  It's not hard to see that any Reedy category is necessarily skeletal.  In fact, it's even worse: no Reedy category can have _any_ nonidentity isomorphisms!  This is problematic for many $\Delta$-like categories such as the [[category of cycles]], Segal's category $\Gamma$, the [[tree category]] $\Omega$, and so on.

The following generalization of the notion of Reedy category, due to Ieke Moerdijk and Clemens Berger, avoids these problems and maintains the truth of Theorem \ref{model} above.  Define a **generalized Reedy category** to be a category $R$ with the same structure $R_+$, $R_-$, and $d$ as before, but now such that

* every non-isomorphism in $R_+$ raises degree,
* every non-isomorphism in $R_-$ lowers degree,
* every morphism $f$ factors as a map in $R_-$ followed by a map in $R_+$, uniquely up to isomorphism, and
* If $f\in R_-$ and $\theta$ is an isomorphism such that $\theta f = f$, then $\theta = 1$ (isomorphisms see the maps in $R_-$ as [[epimorphism|epis]]).

The last condition is not self-dual, but has an obvious dual version.
