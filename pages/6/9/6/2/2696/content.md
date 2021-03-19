+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### (∞,1)-Topos theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Classical case

The classical **Whitehead theorem** asserts that 

+-- {: .num_theorem }
###### Theorem (Whitehead)

Every [[weak homotopy equivalence]] between [[CW-complexes]] is a [[homotopy equivalence]].

=--

(See also the discussion at [[m-cofibrant space]]).

Using the [[homotopy hypothesis]]-theorem this may be reformulated:

+-- {: .num_cor }
###### Corollary

In the [[(∞,1)-category]] [[∞Grpd]] every [[weak homotopy equivalence]] is a [[homotopy equivalence]].

=--

## Simplicial version

\begin{theorem}
A [[simplicial map]] $f\colon X\to Y$ between [[Kan complexes]]
is a [[simplicial homotopy equivalence]] if and only if
for any $a$ and $b$ that make the following square commute
$$\array{
\partial\Delta^n&\stackrel{a}{\to}&X\\
\downarrow^\iota&{}^{\exists d}\nearrow&\downarrow^f\\
\Delta^n &\stackrel{b}{\to}&Y\\
}
$$
there is a diagonal arrow $d$ that makes the upper triangle
commutative and the lower triangle commutative up to a homotopy
$h\colon \Delta^1\times\Delta^n\to Y$
that is constant on the boundary $\Delta^1\times\partial\Delta^n$.
\end{theorem}

Of course, this statement can be reformulated using
homotopy groups like the version for topological spaces,
but the above statement is more practical.

\begin{remark}
In the above criterion, the boundary inclusion
$$\partial\Delta^n\to\Delta^n$$
can be replaced by any weakly equivalent [[cofibration]].
\end{remark}

\begin{remark}
If $X$ or $Y$ is not a [[Kan complex]],
one can formulate a similar criterion
using [[barycentric subdivisions]] of $\partial\Delta^n$ and $\Delta^n$.
A [[simplicial map]] $f\colon X\to Y$ between [[simplicial sets]]
is a [[weak homotopy equivalence]] if and only if
for any $k\ge0$ and for any $a$ and $b$ that make the following square commute
$$\array{
Sd^k \partial\Delta^n&\stackrel{a}{\to}&X\\
\downarrow^{Sd^k \iota}&{}^{\exists d}\nearrow&\downarrow^f\\
Sd^k \Delta^n &\stackrel{b}{\to}&Y\\
}
$$
there is $l\ge k$ such that in the outer rectangle in the diagram
$$\array{
Sd^l \partial\Delta^n&\to&Sd^k \partial\Delta^n&\stackrel{a}{\to}&X\\
\downarrow^{Sd^l \iota}&&\downarrow^{Sd^k \iota}&&\downarrow^f\\
Sd^l \Delta^n &\to&Sd^k \Delta^n &\stackrel{b}{\to}&Y\\
}
$$
we can find a diagonal arrow
$$d\colon Sd^l \Delta^n \to X$$
that makes the upper triangle in the diagram
$$\array{
Sd^l \partial\Delta^n&\stackrel{a}{\to}&X\\
\downarrow^{Sd^l \iota}&{}^{\exists d}\nearrow&\downarrow^f\\
Sd^l \Delta^n &\stackrel{b}{\to}&Y\\
}
$$
commutative and the lower triangle commutative up to a homotopy
$$h\colon Sd^l(\Delta^1\times\Delta^n)\to Y$$
that is constant on the boundary $Sd^l(\Delta^1\times\partial\Delta^n)$.
\end{remark}

## Equivariant version

In $G$-[[equivariant homotopy theory]] the statement is that $G$-homotopy equivalences between [[G-CW complexes]] are equivalent to maps that are weak homotopy equivalences on [[fixed point]] spaces $H^H$ for all [[closed subset|closed]] [[subgroups]] $H \subset G$ (e.g. [Greenlees-May 95, theorem 2.4](#GreenleesMay95)). See at _[[equivariant Whitehead theorem]]_.

## In general $(\infty,1)$-toposes 

There is a notion of [[homotopy groups]] for objects in every [[∞-stack]] [[(∞,1)-topos]], as described at [[homotopy group (of an ∞-stack)]]. Accordingly, there is a notion of [[weak homotopy equivalence]] in every [[∞-stack]] [[(∞,1)-topos]] and hence an analog of the statement of Whiteheads theorem. One finds that

**Warning** Whitehead's theorem **fails** for general [[(∞,1)-toposes]] and non-[[truncated object in an (infinity,1)-category|truncated]] objects.

The [[∞-stack]] [[(∞,1)-topos]]es in which the Whitehead theorem does hold are the [[hypercomplete (∞,1)-topos]]es. These are precisely the ones that are [[presentable (∞,1)-category|presented]] by a local [[model structure on simplicial presheaves]]. 

For instance the hypercomplete $(\infty,1)$-topos [[Top]] is presented by the model structure on simplicial presheaves on the point, namely the [[model structure on simplicial sets]].


## In homotopy type theory

Since [[homotopy type theory]] admits models in [[(∞,1)-toposes]] (and in particular in non-hypercomplete ones), Whitehead's theorem is not provable when regarded as a statement about types in homotopy type theory.  From this perspective, the truth of Whitehead's theorem is a [[foundational axiom]] that may be regarded as a "classicality" property, akin to [[excluded middle]] or the [[axiom of choice]] --- we call it **Whitehead's principle** (not to be confused with [[Whitehead's problem]], another statement that is independent of the usual axioms of set theory).

Whitehead's principle does hold, however, for maps between [[homotopy n-types]] for any finite $n$; this is provable in homotopy type theory by [[induction]] on $n$.

## Related concepts

* [[mod p Whitehead theorem]]

* [[equivariant Whitehead theorem]]

* [equivariant stable Whitehead theorem](G-spectrum#EquivariantWhitehead)

* [[CW-approximation theorem]]

* [[cellular approximation theorem]]

## References

Named after [[J. H. C. Whitehead]].

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 1 of _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.),  _[[Handbook of Algebraic Topology]]_,  1995 Amsterdam: North-Holland, pp. 213&#8211;253,   ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

Discussion for [[equivariant homotopy theory]] includes

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

The $(\infty,1)$-topos version is in section 6.5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

A formalization in [[homotopy type theory]] written in [[Agda]] is in 

* [[Dan Licata]], _[Whitehead.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Whitehead.agda)_

category: foundational axiom

[[!redirects Whitehead's theorem]]
[[!redirects Whitehead's principle]]
[[!redirects Whitehead principle]]

[[!redirects simplicial Whitehead theorem]]