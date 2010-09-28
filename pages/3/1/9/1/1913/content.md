# Differential forms
* tic
{:toc}

## Idea

A differential form is a geometrical object on a [[manifold]] that can be integrated. A differential form $\omega$ is a [[section]] of the [[exterior algebra]] $\Lambda^* T^* X$ of a [[cotangent bundle]], which makes sense in many contexts (e.g. [[manifolds]], [[algebraic varieties]], [[analytic space]]s, ...). 


## Abstract version

Before turning to the usual version in differential geometry, we examine the above requirement through [[general abstract nonsense]].

One way to exhibit this statement nicely is:
+-- {: .standout}
A differential $n$-form on $X$ is a smooth $n$-[[n-functor|functor]] $P_n(X) \to \mathbf{B}^n \mathbb{R}$ from the [[path n-groupoid]] of $X$ to the $n$-fold [[delooping]] of the additive [[Lie group]] of real numbers.
=--
+-- {: .query}
Urs, do you know where the need for orientation comes in here?  I don\'t follow it in enough detail to see, although I intend to read Moerdijk--Reyes.  ---Toby

[[Eric]]: I'm probably confused, but if $\sigma_n$ is a morphism in $P_n(X)$, then (unless $X$ is a [[directed space]]), the opposite $\sigma_n^{-1}$ is also in $P_n(X)$ and I think $\omega(\sigma_n) = -\omega(\sigma_n^{-1})$.

_Toby_:  Between Eric\'s comment here and Urs\'s at [[latest changes]], I\'m happy to remove this query box.

[[Eric]]: I think it is a good question. Maybe we should keep the query box here until the answer is incorporated in the page.

[[Urs Schreiber]]: here is my reply, that I originally posted at [[latest changes]]. I'll try to eventually work this into the main text of the entry

The orientation of the diffential form corresponds to the inherent orientation of [[k-morphism]]s: as we identify the differential form with a smooth functor on the [[path n-groupoid]], that [[path n-groupoid]] necessarily has _oriented_ $k$-volumes as its [[k-morphism]]s, simply because these $k$-morphisms need to come with information about their (higher categorical) source and target.

To get pseudo-differential forms that may be integrated also over non-oriented and possibly non-orientable manifolds one needs to consider parallel transport functors not with coefficients in just $\mathbf{B}^n \mathbb{R}$ coming from the [[crossed complex]] 
     
$$
   (\mathbb{R} \to {*} \to \cdots \to {*})
$$

but the more refined crossed complex

$$
  (\mathbb{R} \to {*} \to \cdots \to \mathbb{Z}_2)
$$

where the $\mathbb{Z}_2$-factor acts by sign reversal on $\mathbb{R}$ (one can also use $U(1)$ instead of $\mathbb{R}$, this way $[P_n(-), \mathbf{B}^n U(1)]$ becomes the [[Deligne cohomology|Deligne complex]] and knows not just about differential forms but about $U(1)$ $n-1$-gerbes with connection even).

A little bit of discussion of this unoriented case is currently at [[orientifold]]. There for the case $n=2$.
=--

Note that an $n$-morphism in $P_n(X)$ is an oriented $n$-dimensional submanifold of $X$.

Such a functor (as described in more detail at [[connection on a bundle]]) assigns a real number to each parametrised $n$-dimensional cube of $X$, that is a subspace by a smooth map $\Sigma : [0,1]^n \to X$.  If the differential form that this $n$-functor defines is denoted $\omega \in \Omega^n(X)$, then this real number is denoted by the [[integration|integral]]
$$
  \int_{[0,1]^n} \Sigma^* \omega
  \,.
$$

This integral in turn encodes the $n$-functoriality of the $n$-functor: it effectively says that
* if we decompose the standard $n$-cube $[0,1]^n$ into $N^n$ little subcubes $(C_k)_{k\in \mathbb{N}^n}$  for $N \in \mathbb{N}$
* and apply the $n$-functor to each of these to obtain a result (a real number) to be denoted $\omega(C_k)$;
* then by $n$-functoriality the result of the application of the functor to the full $\Sigma$ is the composition of all the $\omega(C_k)$ in $\mathbb{R}$. i.e. their sum
  $$
    \int_{[0,1]^n} \Sigma^* \omega
    =
    \sum_k \omega(C_k)
    \,.
  $$

Since one can let $N$ increase arbitrarily in this prescription -- $N \to \infty$ -- it follows that the value of the functor on $\Sigma$ is already determined by all its values on all "infinitesimal $n$-cubes" in some sense. 

+--{.query}
[[Eric]]: This is neat and goes toward answering my query about an "arrow theoretic" presentation on [[measure space]].
=--

The notion of **differential form** is the one that makes this precise: a differential form is a rule for assigning to each "infinitesimal $n$-cube" a number.

There are in turn different ways to make that last statement precise: 

* In [[differential geometry]] an "infinitesimal $n$-cube" is modeled by an $n$-tuple of [[tangent bundle|tangent vectors]] and a differential form is a fiberwise linear map from the $n$-fold exterior power of the [[tangent bundle]] to the real numbers, as given below.

* In [[synthetic differential geometry]] the statement is in essence the same one, but the difference is that there the notion of "infinitesimal $n$-cube" has a concrete meaning on the same footing of other $n$-cubes. If $D^n$ denotes the abstract infinitesimal $n$-cube in this context, then the mapping space $X^{D^n}$ of morphisms from $D^n\to X$ is the $n$-fold [[tangent bundle]] of $X$ and a differential form is precisely nothing but a morphism
  $$
    \omega : X^{D^n} \times D^n \to \mathbb{R}
  $$ 
  (where $\mathbb{R}$ is now the synthetic differential version of the real numbers) subject to three constraints. (These constraints can be seen as the infinitesimal analog of the $n$-functoriality discussed above).

  This is described in detail in section 4 of 

  * Moerdijk-Reyes, [[Models for Smooth Infinitesimal Analysis]]

  For more on this see [[differential forms in synthetic differential geometry]].


## Examples

Just to reassure everybody that we\'re still talking about the same thing:

In local coordinates, a differential form can be expressed in terms of the coordinate variables and their derivatives; a typical $2$-form in coordinates $(x,y,z)$ might be
$$ x^2 y\, \mathrm{d}x \wedge \mathrm{d}y + 3 \sin x\, \mathrm{d}x \wedge \mathrm{d}z - (x + 4 y)\, \mathrm{d}x \wedge \mathrm{d}z .$$
In classical differential geometry, expressions like this (but usually written without the '$\wedge$') showed up naturally as integrands; then people began to see them as objects in their own right.

However, differential forms do not need to be expressed in local coordinates; we can say that $\omega$ and $\eta$ are differential forms and get
$$ \mathrm{d}\omega \wedge \eta ,$$
for example, as a new differential form.


## Definitions

Given a differentiable [[manifold]] $X$, or even a [[generalized smooth space]] $X$ for which this definition makes sense, a __differential form__ on $X$ is a [[section]] of the [[exterior algebra]] of the [[cotangent bundle]] over $X$; sometimes one refers to an __exterior differential form__ to be more precise.  One often requires differential forms to be smooth, or at least continuous, but we will state this explicitly when we want it.  A __differential $p$-form__ on $X$ is a section of the $p$th [[exterior power]] of the cotangent bundle; the [[natural number]] $p \geq 0$ is the __rank__ of the form.  A general differential form is a $p$-indexed [[sequence]] of differential $p$-forms of which all but finitely many are zero; on a finite-dimensional manifold, this latter condition is automatic.


The _space_ $C^\infty\Omega^*(X)$ of *smooth* forms on $X$ may also be defined as the [[universal differential envelope]] of the space $C^\infty\Omega^0(X)$ of smooth functions on $X$ (which are the same as the smooth $0$-forms as defined above); more concretely:

It is generated by the smooth functions and three operations:

*  an associative binary operation of addition generalising the usual addition of functions,
*  an associative binary operation $\wedge$ (the __exterior product__ or __wedge product__) generalising the usual multiplication of functions,
*  a unary operation $\mathrm{d}$ (the __exterior derivative__, or __differential__);

subject to these identities:

*  addition makes $C^\infty\Omega^*(X)$ into an [[abelian monoid]],
*  both $\mathrm{d}$ and $\wedge$ distribute over addition,
*  $\mathrm{d}\mathrm{d}f = 0$,
*  $\mathrm{d}f \wedge \mathrm{d}f = 0$,
*  $\mathrm{d}(f \wedge \eta) = \mathrm{d}f \wedge \eta + f \wedge \mathrm{d}\eta$,
*  $\mathrm{d}(\mathrm{d}f \wedge \eta) + \mathrm{d}f \wedge \mathrm{d}\eta = 0$,

in which $f$ is a smooth function and $\eta$ is an arbitrary smooth form.  (Note that one often drops the '$\wedge$' after a $0$-form; thus, $f \eta = f \wedge \eta$.  There is hardly any ambiguity if one drops the '$\wedge$' entirely, but it\'s traditional.)

Although not directly stated, it can be proved that addition makes $C^\infty\Omega^*(X)$ into an [[abelian group]]; in fact, it is a [[module]] of the [[commutative ring]] of smooth functions on $X$.  This is further a [[graded module]], graded by the [[natural numbers]], with the elements of grade $p$ being the $p$-forms defined earlier; the space of these is $C^\infty\Omega^p(X)$.  If $\omega$ is a $p$-form and $\eta$ is a $q$-form, we have:

*  $\mathrm{d}\omega$ is a $(p+1)$-form,
*  $\omega \wedge \eta$ is a $(p+q)$-form.

The law
$$\mathrm{d}\mathrm{d}\eta = 0$$
holds for any form $\eta$, but the other laws become more complicated; if $\omega$ is a $p$-form and $\eta$ is a $q$-form, then we get

*  $\omega \wedge \omega = 0$ if $p$ is odd,
*  $\omega \wedge \eta = (-1)^{pq}\, \eta \wedge \omega$,
*  $\mathrm{d}(\omega \wedge \eta) = \mathrm{d}\omega \wedge \eta + (-1)^p\, \omega \wedge \mathrm{d}\eta$.

That is, $C^\infty\Omega^*(X)$ is a [[skew-commutative algebra]] over the ring of smooth functions, equipped with a [[derivation]] $\mathrm{d}$ of degree $1$.  In fact, the description above in terms of generators and relations makes it the [[free functor|free]] skew-commutative algebra over that ring equipped with such a derivation.  (Or if it doesn\'t, then it\'s because I left something out of that description.)

More general forms (in $\Omega^*(X)$) can be recovered as sums of terms, each of which is the wedge product of a function and a smooth form.  (This can also be seen as a special case of a vector-valued form as below.)  One can still define the exterior derivative of a $C^1$ (once continuously differentiable) form; in general, the differential of a $C^k$ form is a $C^{k-1}$ form.  If $X$ is not a smooth manifold but only $C^k$ for some $1 \leq k \lt \infty$, then one has to take more care here, but the definition of the skew-commutative algebra of $C^k$ differential forms can still be made to work.


Given local coordinates $(x^1, \ldots, x^n)$ on a patch $U$ in an $n$-dimensional manifold $X$, any differential form $\eta$ on $U$ can be expressed uniquely as a sum of $2^n$ terms
$$ \eta = \sum_I \eta_I \wedge \mathrm{d}x^I ,$$
where $I$ runs over *increasing* [[lists]] of indices from $(1,\ldots,n)$, each $\eta_I$ is a function on $U$ (continuous, smooth, etc according as $\eta$ is), and
$$ \mathrm{d}x^I = \mathrm{d}x^{I_1} \wedge \cdots \wedge \mathrm{d}x^{I_p} $$
(for $p$ the length of the list $I$) is simply an abbreviation.  For a $p$-form, there are $\left(n \atop p\right)$ terms that appear.


## Twisted and vector-valued forms

Recall that a differential form on $X$ is a section of the exterior algebra of the cotangent bundle over $X$; call this bundle $\Lambda$.  Then given any [[vector bundle]] $V$ over $X$, a __$V$-valued form__ on $X$ is a section of the vector bundle $V \otimes \Lambda$.  The wedge product of a $V$-valued form and a $V'$-valued form is a $(V \otimes V')$-valued form, but if there is a commonly used multiplication map $V \otimes V' \to W$, then we may think of their wedge product as a $W$-valued form.

Of particular importance are $L$-valued forms when $L$ is a [[line bundle]]; these are also called __$L$-twisted forms__.  In local coordinates, a twisted form looks just like an ordinary form, once you choose a nonzero vector in $L$ as a basis.  Therefore, they can seem sneaky and confusing sometimes when you realise that they do not behave in the same way!

Let $\Psi$ be the [[pseudoscalar]] bundle; that is, a section of $\Psi$ (a pseudoscalar field) is given locally by a simple [[scalar]] field (a real-valued function) for each [[orientation]] of a local patch, with opposite orientations giving oppositely-signed scalars.  A __pseudoform__ is a $\Psi$-twisted form.

On an $n$-dimensional manifold $X$, the space $\Omega^n(X)$ of $n$-forms is itself a line bundle; a $p$-form twisted by this line bundle is a __densitised form__.  Sometimes an $n$-form is itself called a __density__.  Actually, as we will see under integration below, it is really an $n$-*pseudo*form that should be called a density, but that is not the traditional terminology.

Given any real number $w$, there is a line bundle called the line bundle of $w$-[[weighted representation|weighted]] scalars; a form twisted by this line bundle is a __$w$-weighted form__.  Note that a $0$-weighted form is just an ordinary form; also, an $n$-pseudoform turns out to be equivalent to a $1$-weighted $0$-form.  (And thus a densitised form is equivalent to a $1$-weighted pseudoform.)


## Pulling back forms

Given manifolds $X$ and $Y$ and a map $f: X \to Y$, any differential form $\eta$ on $Y$ defines a __pullback__ form $f^*(\eta)$ on $X$.  This is quite straightforward, once one knows how to push forward tangent vectors on $X$ to tangent vectors on $Y$; to apply $f^*(\eta)$ to a list of vectors on $X$, push them forward to $Y$ and apply $\eta$ to them there.  If $f$ and $\eta$ are smooth, continuous, etc, then so is $f^*(\eta)$.

Thus, the operation that maps $X$ to $\Omega^*(X)$ extends to a [[contravariant functor]] $\Omega^*$.  Perhaps confusingly, forms are traditionally known in physics as 'covariant' concepts, because of how the components transform under a change of coordinates.  (Ultimately, this confusion goes back to that between active and passive [[coordinate transformation]]s.)

Note that twisted and (more general) vector-valued forms cannot be pulled back so easily.  One needs some extra structure on $f$ to do so; see the discussion of integration of $p$-pseudoforms below for an example.


## Integration of forms

Let $X$ be an $n$-dimensional manifold, and let $\omega$ be an $n$-pseudoform on $X$.  Suppose that $X$ is [[paracompact space|paracompact]] and [[Hausdorff space|Hausdorff]], so that we may find a [[locally finite cover]] of $X$ with a subordinate smooth [[partition of unity]] and a smooth coordinate chart on each patch.  Then $\omega$ defines a [[measure space|measure]] on $X$ as follows:

*  On each coordinate patch $U$, fix the orientation given by the coordinates to turn $\omega$ into an untwisted $n$-form $\hat{\omega}$; then write $\hat{\omega}$ in coordinates as
   $$ \hat{\omega} = \omega_U \wedge \mathrm{d}x^1 \wedge \cdots \wedge \mathrm{d}x^n .$$
   In this situation, it is convenient also to write
   $$ \omega = \omega_U \mathrm{d}x^1 \cdots \mathrm{d}x^n ,$$
   although this really does nothing but define the symbol '$\mathrm{d}x^1 \cdots \mathrm{d}x^n$' (without the wedges).

*  The coordinates on $U$ define a [[diffeomorphism]] between $U$ and an open subset of $\mathbf{R}^n$ that we\'ll also call $U$; so use the latter formula to interpret
   \[ \label{absvalposs} \int_U \omega = \int_U \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n ,\]
   where the right-hand side is now interpreted in the usual way as as integral with respect to [[Lebesgue measure]].

*  Using the partition of unity, write
   $$ \omega = \sum_U w_U \omega_U ,$$
   where $w_U$ is a weight function defined on $U$ and $\omega_U$ is the [[restriction]] of $\omega$ to $U$.
   Then we have
   $$ \int_X \omega = \sum_U \int_U w_U(x^1,\ldots,x^n) \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n ,$$
   or more generally,
   $$ \int_E \omega = \sum_U \int_U \chi_E(x^1,\ldots,x^n) w_U(x^1,\ldots,x^n) \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n $$
   for $E$ a measurable subset of $X$ and $\chi_E$ the [[characteristic function]] of $E$.

_A priori_, this definition depends not only on the particular coordinate patches chosen but also on the partition of unity chosen to go with them.  Furthermore, the defintion could be done just as easily (perhaps even more easily) for something other than an $n$-pseudoform.  But the (perhaps surprising) fact that justifies it all is this:

+-- {: .standout}
When $\omega$ is an $n$-pseudoform, the definition of $\int_E \omega$ is independent of the coordinates and partition chosen.  Furthermore, the map from $n$-pseudoforms to measures is linear.
=--

Note that, if $\omega$ were an $n$-form instead of a pseudoform, then the definition would depend on the orientation of the coordinates chosen.  We could fix that by using the absolute value $|\omega_U|$ in place of $\omega_U$ in (eq:absvalposs) and in the following equations, but then the map from forms to measures would not be linear.


It may also be enlightening to consider how to go back from a measure to an $n$-pseudoform.  If $\omega$ is an [[absolutely continuous measure|absolutely continuous]] [[Radon measure]] (see [Wikipedia](http://en.wikipedia.org/wiki/absolute_continuity) [articles](http://en.wikipedia.org/wiki/Radon_measure) until we get our own) on $X$, then it defines an $n$-pseudoform (which we may also call $\omega$) as follows:

*  Given a point $a$, choose one of the two local orientations at $a$.
*  Given $n$ linearly independent vectors $(v_1,\ldots,v_n)$ at $a$, develop them into a coordinate system on a neighbourhood $U$ of $a$.
*  For sufficiently large natural number $k$, the coordinate cube $C_k$ of points with coordinates in $[0,1/k]^n$ exists (lies within $U$).
*  Let $L$ be $\lim_{k \to \infty} k^n \omega(C_k)$.
*  If the coordinate system on $U$ is positively oriented at $a$, then let $\omega(v_1,\ldots,v_n)$ be $L$; if the coordinate system on $U$ is negatively oriented at $a$, then let $\omega(v_1,\ldots,v_n)$ be $-L$.
*  Extend the definition to $n$ arbitrary vectors by continuity (which necessarily maps a linearly dependent list of vectors to zero).

Again, this definition is independent of the coordinate system chosen (as long as it extends the given vectors); or if that\'s not true, then we need to add further restrictions to the absolutely continuous Radon measure $\omega$.  The definition is *not* independent of the orientation chosen, of course; thus we get a pseudoform rather than an untwisted form.  You might try to ignore the orientation and take $\omega(v_1,\ldots,v_n)$ to be $L$ always, but that does not define an exterior form, as is most easily seen if two vectors are switched (which does not change $L$).


One can integrate forms other than $n$-pseudoforms, of course, but only over certain structures within the manifold $X$.  Specifically, if $R$ is a $p$-dimensional [[submanifold]] of $X$ (that is a $p$-dimensional manifold $U$ equipped with a map $R: U \to X$), then we would like to integrate $p$-forms or $p$-pseudoforms (defined on $X$) over $R$.  Here is how we do this:

*  We may integrate a $p$-form $\eta$ over $R$ if $R$ is _oriented_, that is if $U$ is oriented.  We pull back $\eta$ from $X$ to $U$, then use the orientation on $U$ to turn $\eta$ into a $p$-pseudoform, which we can then integrate on the $p$-dimensional manifold $U$.

*  We may integrate a $p$-pseudoform $\eta$ over $R$ if $R$ is _pseudooriented_, that is if it is equipped with a map that, for each point $a$ on $U$, takes a local orientation of $X$ at $R(a)$ to a local orientation of $U$ at $a$, continuously in $a$ and taking opposite orientations to opposite orientations.  Then locally, we turn $\eta$ into a $p$-form on $X$ using a local orientation on $X$, pull that back to $U$, and use the corresponding local orientation on $U$ to turn that back into a $p$-pseudoform, which we can then integrate on $U$.

Thus, while integration of $n$-pseudoforms is the most basic, integration of general $p$-forms is actually a bit simpler than integration of general $p$-pseudoforms.  Integration of other twisted or vector-valued forms can also be done, again given appropriate structure on $R$.  Note that, if $X$ is thought of a submanifold of itself, then it has a natural pseudoorientation that takes each local orientation to itself, and so we recover the original definition of integration of $n$-pseudoforms on $X$.


One often sees the definition of integration given for *parametrised* submanifolds, that is submanifolds where $U$ is an open subset of $\mathbf{R}^p$.  This amounts to a combination of the concepts above, with the two uses of $U$ (as a coordinate patch in $X$ or as the source of a submanifold of $X$) identified.  The theorem that the integral of an $n$-pseudoform on $X$ is independent of the coordinates chosen now becomes a theorem that the integral of a parametrised submanifold is independent of the parametrisation (up to some details about orientation), which in the end returns the result that one can integrate forms over arbitrary submanifolds (given an orientation or pseudoorientation as above).

+--{.query}
[[Zoran Škoda]]: Should maybe this entry have a discussion on heuristics behind the usual trick in supersymmetry which asserts that the inner hom for supermanifolds, gives the statement that the algebra of smooth differential forms on $M$ is the space of functions on the odd tangent bundle $\Pi T M$? I am not the most competent to do this succinctly enough... 

_Toby_:  Possibly that should go at [[differential forms on supermanifolds]]?

[[Zoran Škoda]]: By no means. Ordinary differential forms on ORDINARY manifolds are the same as functions on odd tangent bundle. I did not want to say anything about the generalization of differential forms on  supermanifolds. So it is NOT a different notion, but a different way to define it. If going to toposes hence synthetic framework is not separated why would be separated the equality which involves a parity trick...

_Toby_:  Ah, I see; your $M$ above need not be super, and it still works.  Then yes, that should be mentioned here too.
=--


## Cohomology of forms

There is a [[cohomology]] theory of smooth differential forms; we have a [[chain complex]]
$$ \cdots \stackrel{\mathrm{d}}\to C^\infty\Omega^2(X) \stackrel{\mathrm{d}}\to C^\infty\Omega^1(X) \stackrel{\mathrm{d}}\to C^\infty\Omega^0(X) \stackrel{\mathrm{d}}\to 0 ;$$
the [[chain cohomology]] of this complex is the __[[de Rham cohomology]]__ of $X$.

As smooth differential forms are the cochains in de Rham cohomolgy, the theory of integration of forms allows us to interpret [[relatively compact subspace|relatively compact]] oriented submanifolds as chains on $X$, giving us a [[homology]] theory.  Combining these, we have __[[Stokes's theorem]]__
$$ \int_{\partial{R}} \omega = \int_R \mathrm{d}\omega ,$$
where $\partial{R}$, which may be interpreted as the __boundary__ of $R$, is also called the __codifferential__ as it is dual to $\mathrm{d}$.


## References

* Schreiber & Waldorf, _Smooth Functors vs. Differential Forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

Much fun discussion between [[Eric Forgy]], [[Toby Bartels]], and [[John Baez]], about whether integration of forms or pseudoforms is most fundamental (and about whether twisted forms in general are useful and interesting geometric objects or the bastard spawn of hell) may be found in [this giant Usenet thread](http://groups.google.com/group/sci.physics.research/browse_thread/thread/6a231426b3a313c0/2888a120a9b1f5ad).  More specifically:
*  [John\'s alter ego the Wizard](http://groups.google.com/group/sci.physics.research/msg/3c6a1a7237b66c8c?dmode=source) explains why $n$-pseudoforms are the most natural things to integrate on an $n$-dimensional manifold;
*  [applications of pseudoforms](http://groups.google.com/group/sci.physics.research/msg/2774cbbc982e200e?dmode=source) to classical contexts where absolute values appear;
*  [the general notion of form](http://groups.google.com/group/sci.physics.research/msg/47bbd29289f208f8?dmode=source) corresponding to an arbitrary representation of the [[general linear group]] (towards the end of the post);
*  [absolute values of forms](http://groups.google.com/group/sci.physics.research/msg/424da828e75b6b90?dmode=source) and how to integrate them even when they don\'t exist (near the end of the post).


[[!redirects differential form]]
[[!redirects differential forms]]
[[!redirects exterior form]]
[[!redirects exterior forms]]
[[!redirects exterior differential form]]
[[!redirects exterior differential forms]]
[[!redirects p-form]]
[[!redirects p-forms]]
[[!redirects n-form]]
[[!redirects n-forms]]

[[!redirects exterior derivative]]
[[!redirects exterior derivatives]]
[[!redirects exterior differential]]
[[!redirects exterior differentials]]
[[!redirects exterior differentiation]]
[[!redirects de Rham derivative]]
[[!redirects de Rham derivatives]]
[[!redirects deRham derivative]]
[[!redirects deRham derivatives]]
[[!redirects de Rham differential]]
[[!redirects de Rham differentials]]
[[!redirects deRham differential]]
[[!redirects deRham differentials]]
[[!redirects de Rham differentiation]]
[[!redirects deRham differentiation]]

[[!redirects integration of forms]]

[[!redirects pseudoform]]
[[!redirects pseudoforms]]
[[!redirects pseudo-form]]
[[!redirects pseudo-forms]]
[[!redirects pseudo form]]
[[!redirects pseudo forms]]
[[!redirects p-pseudoform]]
[[!redirects p-pseudoforms]]
[[!redirects n-pseudoform]]
[[!redirects n-pseudoforms]]
[[!redirects pseudo-p-form]]
[[!redirects pseudo-p-forms]]
[[!redirects pseudo-n-form]]
[[!redirects pseudo-n-forms]]
[[!redirects pseudo p-form]]
[[!redirects pseudo p-forms]]
[[!redirects pseudo n-form]]
[[!redirects pseudo n-forms]]

[[!redirects twisted form]]
[[!redirects twisted forms]]
[[!redirects densitized form]]
[[!redirects densitized forms]]
[[!redirects densitised form]]
[[!redirects densitised forms]]
[[!redirects densitized pseudoform]]
[[!redirects densitized pseudoforms]]
[[!redirects densitised pseudoform]]
[[!redirects densitised pseudoforms]]
[[!redirects weighted form]]
[[!redirects weighted forms]]
[[!redirects weighted pseudoform]]
[[!redirects weighted pseudoforms]]
