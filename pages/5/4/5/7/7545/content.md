
# Absolute differential forms
* table of contents
{: toc}

## Idea

It\'s well known that one can integrate a [[differential form]] on an [[orientation|oriented]] [[submanifold]].  Less well known (but also true), one can integrate a [[differential pseudoform]] on an [[pseudoriented]] (transversely oriented) submanifold.  But in classical differential geometry, one also sees forms that can be integrated on *unoriented* submanifolds.

I call these _absolute_ forms.  The term 'absolute' suggests a lack of additional required structure, in this case some sort of orientation on the domain of integration.  It also suggests [[absolute value]], since many of the examples from classical differential geometry involve absolute values.  Indeed, we can define the absolute value of a form or a pseudoform to be an absolute form, although not every absolute form arises in this way.

The main theorem of absolute forms is that, if $\omega$ is a (pseudo)-$p$-form and $R$ is a (pseudo)-oriented $p$-dimensional submanifold, then
$$ {\left| \int_R \omega \right|} \leq \int_{|R|} {|\omega|} ,$$
where ${|\omega|}$ is an absolute $p$-form (the absolute value of $\omega$), $|{R}|$ is simply $R$ with its (pseudo)-orientation ignored, and the absolute value on the left is the ordinary absolute value of scalars.  This theorem also applies if we start with an absolute $p$-form $\omega$, (although in that case $R$ starts out unoriented and so is the same as ${|R|}$).  If $R$ is a [[de Rham cohomology|de Rham]] chain (a formal [[linear combination]] of appropriately oriented submanifolds), we also take absolute values of the formal coefficients in ${|R|}$.  (This operation does not respect the usual notion of equality of chains, but the theorem is true all the same.)


## Definitions

Let $X$ be a [[differentiable manifold]] (or similar sort of space), and let $p$ be a [[natural number]] (typically $0 \leq p \leq n$, where $n$ is the [[dimension]] of $X$).  Recall that an (exterior differential) __$p$-[[exterior differential form|form]]__ $\omega$ on $X$ is a [[function]] that assigns a [[real number]] (or whatever is the relevant sort of scalar) $\omega_c(v_1,\ldots,v_p)$ to a point $c$ in $X$ and a $p$-[[tuple]] $(v_1,\ldots,v_p)$ of [[tangent vectors]] at $c$, [[multilinear map|multilinearly]] and [[alternating form|alternating]] in the $v_i$.  Similarly, a __$p$-[[pseudoform]]__ $\omega$ on $X$ is a function that assigns a scalar $\omega_c^o(v_1,\ldots,v_p)$ to a point $c$ in $X$, a local [[orientation]] $o$ at $c$, and a $p$-tuple $(v_1,\ldots,v_p)$ of tangent vectors at $c$, multilinearly and alternating in the $v_i$ and reversing sign under a reversal of $o$.

+-- {: .num_defn}
###### Definition

An __absolute $p$-form__ $\omega$ on $X$ is a function that assigns a scalar $\omega_c(v_1,\ldots,v_p)$ to a point $c$ in $X$ and a $p$-[[tuple]] $(v_1,\ldots,v_p)$ of [[tangent vectors]] at $c$ and that satisfies the following conditions:

1.  Fixing $c$, $\omega_c({-})$ shall be [[uniformly continuous map|uniformly continuous]].

2.  The $p$-tuple $(v_1,\ldots,v_p)$ shall be [[linearly independent subset|linearly independent]] if $\omega_c(v_1,\ldots,v_p) \ne 0$.  Thus, although $\omega_c$ is not linear, we may still call it [[alternating form|alternating]]; however (as a consequence of 3), it is actually [[symmetric function|symmetric]].

3.  Fix a $p$-dimensional subspace $S$ of the tangent space at $c$ and an orientation $o$ of $S$.  Now given a linearly independent $p$-tuple $(v_1,\ldots,v_p)$ from $S$ (that is a [[basis]] of $S$), let $\omega_c(v_1,\ldots,v_p)_S^o$ be $\pm\omega_c(v_1,\ldots,v_p)$ according to whether the orientation of $S$ induced by the $v_i$ matches $o$, and extend this by continuity to all $p$-tuples from $S$ (which extension must be unique and exists by 1&2).  The resulting function $\omega_c({-})_S^o$ shall be [[multilinear map|multilinear]] (and so also alternating, by 2).
=--

The multilinearity condition here is rather weaker than for a (pseudo)-form, since it applies only within a $p$-dimensional subspace.  Shifting one vector even slightly outside of $S$ loses all connection provided by multilinearity, which is why we need a continuity condition; continuity holds for (pseudo)-forms automatically.

An absolute $p$-form $\omega$ is __[[continuous map|continuous]]__ if it is jointly continuous in all of its data ($c$ as well as the $v_i$).  Since the domain of the function $\omega$ is a manifold (a [[vector bundle]] over $X$, although $\omega$ is not a map of vector bundles), we can even discuss [[differentiable map|differentiability]], [[smooth map|smoothness]], and even [[analytic map|analyticity]] of $\omega$ when $X$ has the relevant structure.

An absolute $0$-form is the same thing as a $0$-form.  An absolute $n$-form on an $n$-dimensional manifold $X$ is essentially the same thing as an $n$-pseudoform; with the notation from condition 3, the only possibility for $S$ is the entire tangent space $T_c{X}$, and we have
$$ \tilde\omega_c^o(v_1,\ldots,v_n) = \omega_c(v_1,\ldots,v_n)_{T_c{X}}^o $$
to relate the $n$-pseudoform $\tilde{\omega}$ to the absolute $n$-form $\omega$.  Finally, the only absolute $p$-form for $p \gt n$ is $0$.

At a point $c$, an absolute $p$-form $\omega$ is:

* __indefinite__ if $\omega_c(v_1,\ldots,v_p) \gt 0$ for some (necessarily [[linearly independent subset|linearly independent]]) $p$-tuple of vectors and $\omega_c(v_1,\ldots,v_p) \lt 0$ for some $p$-tuple,

* __semidefinite__ if not indefinite,

* __definite__ (and hence semidefinite) if $\omega_c(v_1,\ldots,v_p) \ne 0$ for every independent $p$-tuple of vectors at $c$,

* __positive__ (and hence semidefinite) if $\omega_c(v_1,\ldots,v_p) \geq 0$ for every $p$-tuple of vectors (it is enough when they are independent),

* __negative__ (and hence semidefinite) if $\omega_c(v_1,\ldots,v_p) \leq 0$ for every (independent) $p$-tuple of vectors.

All these are at a point $c$; $\omega$ satisfies the condition tout court if it holds for all $c$.

Given an absolute $p$-form $\omega$, its __[[absolute value]]__ ${|\omega|}$ is a positive semidefinite absolute $p$-form:
$$ {|\omega|}_c(v_1,\ldots,v_p) \coloneqq {|\omega_c(v_1,\ldots,v_p)|} .$$
If we start with a $p$-form $\omega$, then the same definition defines a positive absolute $p$-form ${|\omega|}$.  If we start with a $p$-pseudoform $\omega$, then essentially the same definition still works; we use either orientation to evaluate $\omega$ with the same result.  Note that ${|\omega|}$ is continuous if $\omega$ is.  However, we may *not* conclude that ${|\omega|}$ is differentiable just because $\omega$ is differentiable (or even analytic).  On the other hand, ${|\omega|}$ inherits differentiability properties from $\omega$ wherever $\omega \ne 0$.  (Even then, however, we cannot inherit analyticity, except in $1$ dimension.)

Given two absolute $p$-forms $\omega$ and $\eta$, their __sum__ $\omega + \eta$ is an absolute $p$-form:
$$ (\omega + \eta)_c(v_1,\ldots,v_p) \coloneqq \omega_c(v_1,\ldots,v_p) + \eta_c(v_1,\ldots,v_p) .$$
Given an absolute $p$-form $\omega$ and a scalar field $f$, their __product__ $f \omega$ is an absolute $p$-form:
$$ (f \omega)_c(v_1,\ldots,v_p) \coloneqq f(c) \omega_c(v_1,\ldots,v_p) .$$
In this way, the space of absolute $p$-forms is a [[module]] over the [[associative algebra|algebra]] of scalar fields and the space of [[sections]] of a [[vector bundle]].  For now, we decline to define products of absolute forms of aribtrary rank.

Given an absolute $p$-form $\omega$ on $X$, a manifold $U$, and a [[continuously differentiable map]] $R\colon U \to X$, the __pullback__ $R^*\omega$ is an absolute $p$-form on $U$:
$$ (R^*\omega)_c(v_1,\ldots,v_p) \coloneqq \omega_{R(c)}(R_*v_1,\ldots,R_*v_p) .$$
Here, $R_*v_i$ is the [[pushforward]] of $v_i$ under $R$.  Note that $R^*\omega$ is continuous if $\omega$ is; we can also pull back differentiability and analyticity properties that $\omega$ and $R$ both have.

Given a continuous absolute $p$-form $\omega$ on $X$, a $p$-dimensional manifold $U$, and a continuously differentiable map $R\colon U \to X$, the __integral__ $\int_R \omega$ is a scalar:
$$ \int_R \omega \coloneqq \int_U R^*\omega .$$
On the right-hand side, $R^*\omega$ is a continuous absolute $p$-form on $U$, but since $U$ is $p$-dimensional, this is essentially the same as a continuous $p$-pseudoform on $U$, and we already know how to integrate this (see [[integration of differential forms]]).


## Examples

Examples of absolute forms from classical differential geometry include:

*  Absolute $0$-forms are the same as ordinary $0$-forms.

*  Absolute $n$-forms on an $n$-[[dimensional]] manifold are the same as $n$-pseudoforms (and hence the same as [[absolutely continuous measure|absolutely continuous]] [[Radon measures]]).

*  In [[complex analysis]], ${|\mathrm{d}z|}$ is an absolute $1$-form sometimes used in [[contour integration]].  This literally is the absolute value of the differential of the identity map $z$.

*  More generally, the [[arclength]] element $\mathrm{d}s = {\|\mathrm{d}\mathbf{x}\|}$ on a [[Riemannian manifold]] is an absolute $1$-form.  Neither $\mathrm{d}s$ nor (in general) $\mathrm{d}\mathbf{x}$ is actually the differential of anything, but $\mathrm{d}\mathbf{x}$ is the canonical [[tangent vector|vector]]-valued $1$-form (which, on an [[affine space]], really is the differential of the [[identity map]] $\mathbf{x}$), and we really can use the metric to take the norm of such a form to get an absolute $1$-form.

*  Similarly, the [[surface area]] element $\mathrm{d}S$ on a Riemannian manifold is an absolute $2$-form, and we can continue into higher dimensions (although the classical [[volume element]] $\mathrm{d}V$ in $\mathbb{R}^3$ is already covered as a $3$-pseudoform).  In principle, we ought to be able to write down expression for $\mathrm{d}S$ etc in terms of $\mathrm{d}s$, although so far the only thing that I know how to do is $\mathrm{d}S = {\|{\mathrm{d}\mathbf{x} \hat\times \mathrm{d}\mathbf{x}}\|} / 2$, where $\hat\times$ indicates a wedge product of vector-valued forms whose vectors are multiplied by the [[cross product]]. (This can be generalized to any finite-dimensional area in any finite-dimensional Riemannian manifold; in particular, $\mathrm{d}V = {|{\mathrm{d}\mathbf{x} \hat\cdot \mathrm{d}\mathbf{x} \hat\times \mathrm{d}\mathbf{x}}|} / 6$.)

+-- {: .num_remark}
The reason that $\mathrm{d}s$ determines $\mathrm{d}S$ is that lengths determine areas, as through Heron\'s Formula.  However, our usual ways of deriving one form from another (thinking of them, at a given point, as maps from lists of vectors to numbers) involve only rerranging (permuting, duplicating, and contracting) the inputs and applying operations to the outputs.  But this cannot be sufficient; knowing only the lengths of two vectors $v$ and $w$ (which vectors are the inputs to $\mathrm{d}S$, and which lengths are the outputs of $\mathrm{d}s$ at those inputs) does not tell you the area of the parallelogram that they span (which is the output of $\mathrm{d}S$).  You also need the length of $v - w$ (or of $v + w$).  So while we can express $\mathrm{d}S_c$ ($\mathrm{d}S$ at a point $c$) as $(v, w \mapsto 2 H(\mathrm{d}s(v), \mathrm{d}s(w), \mathrm{d}s(v - w))$ (where $H$ is the Heron function, the real-valued function of three real variables that takes the lengths of the three sides of a triangle and returns its area), or equivalently as $(v, w \mapsto 2 H({\|v\|}, {\|w\|}, {\|{v - w}\|}))$, we cannot express $\mathrm{d}S$ with a formula anything along the lines of ${\|{\mathrm{d}\mathbf{x} \hat\times \mathrm{d}\mathbf{x}}\|} / 2$ using $\mathrm{d}s$ directly instead of $\mathrm{d}\mathbf{x}$.  (And so you may as well describe $\mathrm{d}S_c$ as $(v, w \mapsto {\|{v \times w}\|})$ instead.)
=--


## Related concepts

* exterior [[differential forms]] and [[pseudoforms]] (the more well-known variations);

* [[cojet differential forms]] (and [[cogerm differential forms]] more generally) generalize both exterior and absolute $1$-forms and pseudo-$1$-forms;

* [[coflare differential form]]s are a common generalization of exterior forms, absolute forms, and cojet forms (although not all cogerm forms).


## References

Near the end of a Usenet post from 2002, we see a definition of $\int_R {|\omega|}$ for $\omega$ a (pseudo)-$p$-form and $R$ a $p$-dimensional submanifold, but without a broader context for ${|\omega|}$ itself:

* [[Toby Bartels]] and Ralph Hartley; [Densitized Pseudo Twisted Forms](https://groups.google.com/group/sci.physics.research/msg/424da828e75b6b90?dmode=source)
  {#Usenet}

Apparently absolute $p$-forms (at least if continuous) are the same as even $p$-[[densities]] as defined by Gelfand; see this MathOverflow answer:

* Juan Carlos &#193;lvarez Paiva; answer to [Why do I need densities in order to integrate on a non-orientable manifold?](http://mathoverflow.net/questions/90455/why-do-i-need-densities-in-order-to-integrate-on-a-non-orientable-manifold/90714#90714).
  {#MathOverflow}


[[!redirects absolute differential form]]
[[!redirects absolute differential forms]]
[[!redirects absolute form]]
[[!redirects absolute forms]]
[[!redirects differential absolute form]]
[[!redirects differential absolute forms]]

[[!redirects absolute value of a form]]
[[!redirects absolute value of a differential form]]
[[!redirects absolute value of a pseudoform]]
[[!redirects absolute value of a pseudo-form]]
