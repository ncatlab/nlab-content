
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a [[ringed space]] $(X, \mathcal{O}_X)$ there is its [[Picard group]] of [[invertible objects]] in the category of $\mathcal{O}_X$-[[modules]]. When $X$ is a [[projective morphism|projective]] [[integral scheme]] over $k$ the [[Picard group]] underlies a $k$-scheme, this is the _Picard scheme_ $Pic_X$.
This scheme varies in a family as $X$ varies in a family. From this starting point one can naturally generalize to more general relative situations. 

Often one considers just the connected component $Pic_X^0$ of the neutral element in $Pic_X$, and often (such as in the discussion below, beware) it is that connected component (only) which is referred to by "Picard scheme". The difference between the two is measured by the [[quotient]] $Pic_X/Pic_X^0$, which is called the _[[Néron-Severi group]]_ of $X$. Though at least for $X$ an [[algebraic curve]], $Pic_X^0$ goes by a separate name: it is the _[[Jacobian variety]]_ of $X$.

The [[completion]] of the Picard scheme at its neutral element (hence either of $Pic_X$ or $Pic_X^0$) is the _[[formal Picard group]]_.


## Definition

The __Picard variety__ of a complete [[smooth scheme|smooth]] algebraic [[variety]] $X$ over an [[algebraically closed field]] parametrizes the [[Picard group]] of $X$, more precisely the set of classes of isomorphic invertible [[quasicoherent sheaves]] with vanishing [[first Chern class]].

The __Picard scheme__ is a scheme [[representable functor|representing]] the relative Picard functor $Pic_{X/S}: (Sch/S)^{op}\to Set$ by $T\mapsto Pic(X_T)/f^*Pic(T)$. In this generality the Picard functor has been introduced by [[Grothendieck]] in [[FGA]], along with the proof of representability. An alternate form of this functor (with respect to the Zariski topology) in terms of the [[derived functor]] of $f_*$ is $Pic_{X/S}(T)=H^0(T, R^1f_{T*}\mathcal{O}_{X_T}^*)$.

Note we must work with the relative functor because the global Picard functor $Pic_X(T)=Pic(X_T)$ has no hope of being representable as it is not even a  [[sheaf]]. Consider any non-trivial invertible sheaf $\mathcal{L}$ in $Pic(T)$. Then $f^*\mathcal{L}$ becomes trivial on some cover $\{T_i\to T\}$, so $Pic(X_T)\to \prod Pic(X_{T_i})$ is not injective.

## Representability

For this section suppose $f:X\to S$ is s [[separated morphism of schemes|separated]] map, [[finite type]] map of schemes. Many general forms of [[representable functor|representability]] have been proven several of which are given in _[[FGA explained]]_. Here we list several of the common forms:

* Suppose $\mathcal{O}_S\to f_*\mathcal{O}_X$ is universally an isomorphism (stays an [[isomorphism]] after any [[base change]]), then we have a comparison of relative Picard functors $Pic_{X/S}\hookrightarrow Pic_{X/S, zar}\hookrightarrow Pic_{X/S, et}\hookrightarrow Pic_{X/S, fppf}$. They are all isomorphisms if $f$ has a section.

* If $Pic_{X/S}$ is representable by a scheme, then by [[descent theory]] for sheaves it is representable by the same scheme in all the topologies listed above. In general, representability gives representability in a finer topology (of the ones listed).

* If $Pic_{X/S}$ is representable then a universal sheaf $\mathcal{P}$ on $X\times Pic_{X/S}$ is called a [[Poincaré sheaf]]. It is universal in the following sense: if $T\to S$ and $\mathcal{L}$ is invertible on $X_T$, then there is a unique $h:T\to Pic_{X/S}$ such that for some $\mathcal{N}$ invertible on $T$ we get $\mathcal{L}\simeq (1\times h)^*\mathcal{P}\otimes f_T^*\mathcal{N}$.

* If $f$ is (Zariski) [[projective morphism|projective]], [[flat morphism|flat]] with [[integral scheme|integral]] geometric fibers then $Pic_{X/S, et}$ is representable by a [[separated scheme|separated]] and [[morphism of finite type|locally of finite type]] scheme over $S$.

* Grothendieck's Generic Representability: If $f$ is [[proper morphism|proper]] and $S$ is [[integral scheme|integral]], then there is a nonempty open $V\subset S$ such that $Pic_{X_V/V, fppf}$ is representable and is a disjoint union of open [[quasi-projective scheme| quasi-projective]] subschemes.

* If $f$ is a flat, cohomologically flat in dimension 0, proper, [[finitely presented]] map of of [[algebraic space]]s, then $Pic_{X/S}$ is representable by an algebraic space locally of finite presentation over $S$.

## Picard Stack
 {#PicardStack}

The *[[Picard stack]]* $\mathcal{Pic}_{X/S}$ is the [[stack]] of invertible sheaves on $X/S$, i.e. the [[fiber category]] over $T\to X$ is the [[groupoid]] of [[line bundles]] on $X_T$ (not just their [[isomorphism classes]]). (Hence it is the [[Picard groupoid of a monoidal category|Picard groupoid]] equipped with geometric structure). 

If $X$ is proper and flat, then $\mathcal{Pic}_{X/S}$ is an [[Artin stack]] since $\mathcal{Pic}_{X/S}=\mathcal{Hom}(X, B\mathbb{G}_m)$ is the [[Hom stack]] which is Artin.

Note the following "failure" of the relative Picard scheme: points on $Pic_{X/S}$ do not parametrize line bundles. The low degree terms of the Leray [[spectral sequence]] give the following exact sequence $H^1(X_T, \mathbb{G}_m)\to H^0(T, R^1f_*\mathbb{G}_m)\to H^2(T, \mathbb{G}_m)\to H^2(X_T, \mathbb{G}_m)$, but as noted above $Pic_{X/S}(T)=H^0(T, R^1f_*\mathbb{G}_m)$, so we see exactly when a $T$-point comes from a line bundle it is when that point maps to $0$ in this sequence. 

This gives us an obstruction theory lying in $H^2(T, \mathbb{G}_m)$ for a point corresponding to a line bundle. If $Pic_{X/S}$ is representable we could take $T=Pic_{X/S}$ to find a universal obstruction. Intuitively this is because the Picard stack is the right object to look at for the moduli problem of line bundles over $X$. The Picard scheme is the $\mathbb{G}_m$-[[rigidification]] of the Picard stack.

The natural map $\mathcal{Pic}_{X/S}\to Pic_{X/S}$ is a $\mathbb{G}_m$-[[gerbe]]. But isomorphism classes of $\mathbb{G}_m$-gerbes over $T$ are in bijective correspondence with $H^2(T, \mathbb{G}_m)$ and so the above map could be thought of as a geometric realization of the universal obstruction class.

## Related concepts

* [[dual abelian group scheme]]

* [[Poincaré line bundle]]

* [[Albanese variety]]

* [[Prym variety]]

[[!include moduli of higher lines -- table]]


## References

* Springer eom: [Picard variety](http://eom.springer.de/p/p072690.htm), [Picard scheme](http://eom.springer.de/p/p072670.htm)
* wikipedia [Picard group](http://en.wikipedia.org/wiki/Picard_group)
* [[Steven Kleiman|Steven L. Kleiman]], _The Picard scheme_, pp. 235--321 in [[FGA explained]], MR2223410 (draft [pdf](http://cdsagenda5.ictp.it//askArchive.php?categ=a0255&id=a0255s6t3&ifd=15022&down=1&type=lecture_notes)), [arxiv](http://arxiv.org/abs/math/0504020)

* [[Akhil Mathew]], _[The Picard Scheme I](http://amathew.wordpress.com/2013/03/19/the-picard-scheme-i/)_, _[The Picard Scheme II: deformation theory](http://amathew.wordpress.com/2013/03/19/the-picard-scheme-ii-deformation-theory/)_

Specifically on the [[Picard stack]]:

* [[The Stacks Project]], _[The Picard stack](http://stacks.math.columbia.edu/tag/0372)_

category: algebraic geometry

[[!redirects Picard schemes]]

[[!redirects Picard variety]]
[[!redirects Picard varieties]]

