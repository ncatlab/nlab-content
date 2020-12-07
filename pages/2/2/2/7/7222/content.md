
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Grothendieck-Riemann-Roch theorem_ describes  (the failure of) the [[natural transformation|naturality]] of the behaviour of a _[[Chern character]]_ under [[fiber integration|push forward]] along [[proper maps]].

It says, in the formulation of ([Atiyah-Hirzebruch 61](#AtiyahHirzebruch61)), that for $f \colon X \longrightarrow Y$ a [[flat morphism]] of [[schemes]] which are [[flat morphism|flat]] and [[regular scheme|regular]] [[quasi-projective varieties]] over the [[spectrum of a commutative ring|spectrum]] of a [[Dedekind domain]], then the [[Chern character]] of the [[fiber integration|push-forward]] of some $E$ is the push-forward of the [[cup product]] of the Chern-character of $E$ with the [[Todd class]]. Hence it says that "Chern-cup-Todd is natural under pushforward" along proper maps, and generally along [[K-orientation|K-oriented]] maps.

If $f \colon X \to Y$ is a [[proper map]], then there is a [[commuting diagram]]

$$
  \array{
    K_0(X) &\stackrel{ch(-)\cup Td(X)}{\to}& H_\bullet(X, \mathbb{Q})
    \\
    \downarrow^{\mathrlap{\int_{f}}} && \downarrow^{\mathrlap{\int_f}}
    \\
    K_0(Y) &\stackrel{ch(-)\cup Td(Y)}{\to}& H_\bullet(Y,\mathbb{Q})
  }
  \,,
$$

where...

If $X$ is an [[algebraic curve]], then the Riemann-Roch theorem reduces to a statement about the [[Euler characteristic]]/[[genus of a curve|curve]]. This generalizes to [[arithmetic geometry]] with the notion of [[genus of a number field]].

There are various extensions of the Grothendieck-Riemann-Roch theorem,
such as the [[Atiyah-Singer index theorem]] (for elliptic operators and elliptic
complexes), the Connes-Moscovici local index formula (a non-commutative/equivariant version of Atiyah-Singer), and Bismut's hypoelliptic index formula in Bott-Chern cohomology (for non-K\"aeler complex manifolds).

Another approach due to Kashiwara and Schapira relies on the use of methods of Hochschild cohomology and its microlocalized version (which gives a refined index theorem, that takes care of the information related to the propagation of singularities).
It is essentially divided in two parts: the functorial one, which is based on Hochschild and cyclic homology (very similar to Toen and Vezzosi's approach to the construction of the Chern character), and the computational one (due to Bresler-Nest-Tsygan and others), that explicitly describes the relation between the functorial construction of the Chern character and its more classical construction. It is this last comparison statement that introduces the Todd class and makes the Riemann-Roch/index formula look complicated, despite the fact that it simply expresses the functoriality of Hochshild and cyclic homology classes with respect to the push-forward, that is evident. The microlocalized version of the index/RRG theorem is necessary to have a better understanding of the "deformation of the Laplacian" methods (introduced by Witten in his paper on the Morse inequalities, and used by Bismut in his work on the hypoelliptic Laplacian, by Laumon in his paper on local constants of functional equations, and by Kedlaya in his paper on p-adic Weil II) that have become a central tool in the study of cohomology theories and of (additive) index-type formulas and (multiplicative) product-type formulas.

One may hope for an extension of the Riemann-Roch-Grothendieck theorem to the
setting of a general proper morphism in non-strict [[global analytic geometry]] using
an extension of Bismut's approach to a setting of exotic [[global Hodge theory]]. However, it seems that for arithmetic applications (e.g., the study of special values of arithmetic L-functions), one will clearly have to prove a refined RRG theorem for strict [[global analytic geometry|global analytic spaces]], using semistable compactifications (&#224; la Deligne "th&#233;orie de Hodge II, III") and logarithmic methods: the (purely analytic) non-strict theorem will not suffice.


## Related concepts
 
* [[rational Todd class is Chern character of Thom class]]

* [[Hirzebruch-Riemann-Roch theorem]]

* [[arithmetic Riemann-Roch theorem]]

* [[push-forward in generalized cohomology]]

* [[transfer index conjecture]] for [[Becker-Gottlieb transfer]]

## References

The formulation in terms of [[topological K-theory]] is due to:

* {#AtiyahHirzebruch61} [[Michael Atiyah]], [[Friedrich Hirzebruch]], _Vector bundles and homogeneous spaces_, Proc. Symp. Pure Math. 3, 7&#8211;38 (1961) 

Early textbook accounts:

* {#Karoubi78} [[Max Karoubi]], Chapter V.4 of: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))

See also:

* Wikipedia, _[Grothendieck-Riemann-Roch theorem](http://en.wikipedia.org/wiki/Grothendieck%E2%80%93Riemann%E2%80%93Roch_theorem)_

* Wikipedia, _[Riemann-Roch theorem for surfaces](http://en.wikipedia.org/wiki/Riemann&#8211;Roch_theorem_for_surfaces)_

Discussion of Riemann-Roch over [[arithmetic curves]] is in 

* {#Neukirch92} [[Jürgen Neukirch]], chapter III, section 3 of _Algebraische Zahlentheorie_ (1992), English translation _Algebraic Number Theory_,  Grundlehren der Mathematischen Wissenschaften 322, 1999 ([pdf](http://www.plouffe.fr/simon/math/Algebraic%20Number%20Theory.pdf))


The refinement to [[differential cohomology]], hence [[differential K-theory]],  is discussed in section 6.2 of 

* [[Ulrich Bunke]], [[Thomas Schick]], _Differential K-theory. A survey_ ([arXiv:1011.6663](http://arxiv.org/abs/1011.6663))

Over [[algebraic stacks]]/[[Deligne-Mumford stacks]] the GRR theorem is discussed in 

* Roy Joshua, _Riemann-Roch for algebraic stacks_ ([pdf I](http://www.math.osu.edu/~joshua.1/rr1.pdf), [pdf II](http://www.math.osu.edu/~joshua.1/rr2.pdf), [pdf III](http://www.math.osu.edu/~joshua.1/rr3.pdf))

* [[Bertrand Toën]], _Th&#233;or&#232;mes de Riemann-Roch pour les champs de Deligne-Mumford_, K-Theory 18
(1999), no. 1, 33&#8211;76. 1, 23

* Dan Edidin, _Riemann-Roch for Deligne-Mumford stacks_ ([arXiv:1205.4742v1](http://arxiv.org/abs/1205.4742v1))

For a [[categorification]] of GRR, see

* Marc Hoyois, Pavel Safronov, Sarah Scherotzke, Nicolò Sibilla, _The categorified Grothendieck--Riemann--Roch theorem_, ([arXiv:1804.00879](https://arxiv.org/abs/1804.00879)) 

[[!redirects Riemann-Roch theorem]]