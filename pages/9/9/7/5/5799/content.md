
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Definition

Let $C_{et}$ be the [[etale site]] of complex [[scheme]]s of finite type. For $X$ a [[scheme]], its **infinitesimal site** $Cris(X)$ is the [[big site]] $C_{et}/X_{dR}$ of the [[de Rham space]] $X_{dR} : C_{et} \to Set$:

the site whose objects are pairs $(Spec A, (Spec A)_{red} \to X)$ of an affine $Spec A$ and a morphism from its reduced part ($(Spec A)_{red} = Spec (A/I)$ for $I$ the [[nilradical]] of $A$) into $X$.

More generally, for positive [[characteristic]], the definition is more involved than that.

## Properties

The [[abelian sheaf cohomology]] over $Cris(X)$ is the [[crystalline cohomology]] of $X$.


## Logical characterization

Let $k$ be a ring. Let $k \to R$ be a finitely presented $k$-algebra. Then the big infinitesimal topos of the $Spec(k)$-scheme $Spec(R)$ [[classifying topos|classifies]] the theory of commutative squares of ring homomorphisms
$$
  \array{A & \rightarrow & B \\
         \uparrow &&\uparrow \\
         k & \rightarrow& R
}$$
where the rings $A$ and $B$ are local, the top arrow $A \to B$ is surjective and has nilpotent kernel (i.e. every element of the kernel is nilpotent) This result is due to ([Hutzler 2018](#Hutzler18)). By the conditions on the top morphism, it is enough to require that $A$ or $B$ is local.

Routine arguments, to be made explicit in a further revision of this entry, allow to generalize this description to the non-affine case. Let $f \colon X \to S$ be a scheme over $S$. Assume that $X$ is locally of finite presentation over $S$. Then the big infinitesimal topos of the $S$-scheme $X$ classifies, as a $Sh(X)$-topos, the $Sh(X)$-theory of commutative squares of ring homomorphisms
$$
  \array{A & \rightarrow & B \\
         \uparrow &&\uparrow \\
         f^{-1}\mathcal{O}_S & \rightarrow& \mathcal{O}_X
}$$
where the rings $A$ and $B$ are local, the top arrow $A \to B$ is surjective and has nilpotent kernel (i.e. every element of the kernel is nilpotent), and both vertical arrows are local (i.e. reflect invertibility).




## Related concepts

* [[crystalline cohomology]]

* [[crystalline differential operator]]

## References

An original account of the definition of the crystalline topos is [section 7, page 299](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf#page=299) of

* [[Alexander Grothendieck]], _Crystals and de Rham cohomology of schemes_ , chapter IX in _Dix Exposes sur la cohomologie des schema_ ([pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf))

A review of some aspects is in

* [[Jacob Lurie]], Notes on [[crystal|Crystals]] and algebraic D-modules ([pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19%28Crystals%29.pdf))

and on page 7 of

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

In the article 

* Arthur Ogus, _Cohomology of the infinitesimal site_ Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 8 no. 3 (1975), p. 295-318 ([numdam](http://www.numdam.org/item?id=ASENS_1975_4_8_3_295_0))

it is shown that if $X$ is proper over an algebraically closed field $k$ of [[characteristic]] $p$, and embeds into a smooth scheme over $k$, then the infinitesimal cohomology of $X$ coincides with [[etale cohomology]] with coefficients in $k$  (or more generally $W_n(k)$ if we work with the infinitesimal site of $X$ over $W_n(k)$). 

The result about the geometric theory classified by the big infinitesimal topos appears in

* {#Hutzler18}[[Matthias Hutzler]], _Internal language and classified theories of
toposes in algebraic geometry_, Master's thesis at the University of Augsburg, 2018, [GitLab](https://gitlab.com/MatthiasHu/master-thesis/blob/master/thesis.pdf), [pdf download](https://gitlab.com/MatthiasHu/master-thesis/raw/master/thesis.pdf?inline=false)

* [[Matthias Hutzler]], _Syntactic presentations for glued toposes and for crystalline toposes_, Phd. diss. Universität Augsburg 2021. ([arXiv:2206.11244](https://arxiv.org/abs/2206.11244))


[[!redirects infinitesimal site]]
[[!redirects crystaline site]]
