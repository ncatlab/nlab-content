
#Contents#
* table of contents
{:toc}

## Idea

**Morse theory** is the method of studying the [[topology]] of a [[smooth manifold]] $M$ by the study of [[Morse functions]] $M\to\mathbb{R}$ and their associated [[gradient flows]]. 

Classical Morse theory centered around simple statements like Morse inequalities, concerning just the [[Betti number]]s. It is useful not only for studying manifolds, but also for studying infinite CW-type spaces *homotopically filtered in manifolds*, as by Milnor and Bott (especially *The stable homotopy of the classical groups*) for spaces of paths in a smooth manifold.

Novikov--Morse theory is a variant using [[multivalued functions]]. There is also a [[discrete Morse theory]] for combinatorial cell complexes.

There are some infinite-dimensional generalizations like Floer instanton homology for 3-dimensional manifolds and also the Hamiltonian variant of [[Floer homology]] (and cohomology) for (finite dimensional) [[symplectic manifolds]]. Especially well studied is the case of the [[cotangent bundle]] of a differentiable manifold with its standard symplectic structure; this is sometimes called Floer--Oh homology. Floer homology has been partly motivated by Arnold's conjecture on periodic trajectories in [[classical mechanics]]. The symplectic variant of Floer cohomology is related to [[quantum cohomology]]. 

Founders of Morse theory were [[Marston Morse]], [[Raoul Bott]] and [[Albert Schwarz]].

## Definitions

On a smooth manifold $M$, a [[smooth map|smooth]] function $\varphi: M \to \mathbb{R} $ is said to be *Morse* (or *a Morse function*) if

* the zero set of $ d \varphi $ consists of isolated points, and
* the [[Hessian]] of $\varphi$ at these points is nondegenerate.

The Morse functions on $M$ are dense in most reasonable topologies you could put on $C^{\infty}(M)$.
A further condition which is useful in case $M$ is not compact is 

* if the (closed!) preimage of $( -\infty , \lambda ] $ under $\varphi$ is compact for all $\lambda$, then $\varphi$ is said to be *coercive*, whether or not it is Morse.

Together with a (smooth) Riemann structure $g =\langle \cdot,\bullet\rangle$, any real function $\varphi$ on $M$ defines a [[flow]] on $M$ by the equation
$$ - \langle \dot x, Y_x \rangle = Y_x \varphi = d\varphi(Y_x).$$
The Morse functions are notable in that the flows they define have isolated fixed-points with trivially linearizable dynamics, and <nowiki>...[fixme: less vague?]...</nowiki> no other stable cyles.

When $\varphi$ is Morse and coercive, the unstable manifolds of the fixpoints can be arranged into a [[CW complex]] $C_{unstable} (\varphi,g)$, canonically homeomorphic to $M$.  When $M$ is compact, $\varphi$ and $-\varphi$ are automatically both coercive, and $-\varphi$ induces a [[Poincare duality|dual]] CW complexe $ C_{stable} (\varphi,g) $.  Concretely, ....<nowiki>[details]</nowiki>.

### Sketch of a trivial application

Let $ X \to Y $ be a surjective submersion of compact smooth manifolds, and assume $Y$ is connected.  By suitable implicit function theorems, the preimage of any parametrized nonstationary curve $\gamma :(0,1)\to Y$ is a submanifold of $X$, and furthermore the parameter is a Morse function on this submanifold, having *no critical points*. (It is *not* coercive).  By a very little more analysis, the Morse gradient flow is therefore a smooth family of homotopy equivalences.  A trivial adjustment of the Riemann structure further allows that the Morse flow sends fibers to fibers diffeomorphically, so that in fact the fibers over neighboring points of $Y$ are diffeomorphic.  But since $Y$ is connected, this implies that *all* the fibers are diffeomorphic, so that $X\to Y$ is a smooth fiber bundle over $Y$.

### Slightly less-trivial example

The restriction to the [[unit sphere]] in $\mathbb{R}^{n+1}$ of a generic quadratic form is Morse with $2(n+1)$ critical points --- two of each [[bilinear form|index]]; and furthermore this restriction clearly descends to $\mathbb{RP}^n$ as a Morse function with $n+1$ critical points, one of each index.  It can be shown that this is indeed the minimal collection of critical points supported by real projective space.

## References

### General

* [[Raoul Bott]], _[Morse theory indomitable](http://archive.numdam.org/article/PMIHES_1988__68__99_0.pdf)_, _Publications Math&#233;matiques de L'IH&#201;S_, 1988, Volume 68, Number 1, Pages 99-114.

* [[Raoul Bott]], [Lectures on Morse Theory, Old and New](http://www.ams.org/journals/bull/1982-07-02/S0273-0979-1982-15038-8/),  Bull. Amer. Math. Soc. 7 (1982), 331-358.

* [[Raoul Bott]], The stable homotopy of the classical groups.
 Ann. of Math. (2) 70 1959 313&#8211;337.

* [[Daniel Freed]], [Commentary](http://www.ams.org/journals/bull/2011-48-04/S0273-0979-2011-01349-0/) on "Lectures on Morse Theory, Old and New", Bull. Amer. Math. Soc., 48(4), October 2011, 517&#8211;523

* [[Marco Gualtieri]], _[Course page](http://www.math.toronto.edu/mgualt/Morse%20Theory/Morse_2009.html)_, lecture notes and links.

* [[Martin Guest]], [Morse theory in the 1990s](http://arxiv.org/abs/math/0104155).

* [[Loring Tu]], _Morse theory_ [node](http://www.math.harvard.edu/history/bott/bottbio/node9.html) on online bio of R. Bott

* [[M. M. Postnikov]], &#1042;&#1074;&#1077;&#1076;&#1077;&#1085;&#1080;&#1077; &#1074; &#1090;&#1077;&#1086;&#1088;&#1080;&#1102; &#1052;&#1086;&#1088;&#1089;&#1072; &#8212; &#1052;.: &#1053;&#1072;&#1091;&#1082;&#1072;, 1971

### Morse complex and homology

* [[John Milnor]], _Lectures on the h-cobordism theorem_, Notes by L. Siebenmann & J. Sondow, Princeton Univ.
Press, 1965.
* Matthias Schwarz, _Morse homology_, Progress in Mathematics __111__, 1993 

There is also a variant due Barannikov, and in more abstract form Viterbo:

* S. Barannikov, _The framed Morse complex and its invariants_, Advances in Soviet Math. 21 (1994), 93-115.

* Fran&#231;ois Laudenbach, _On an article by S. A. Barannikov_, [arxiv/1509.03490](http://arxiv.org/abs/1509.03490) 

### Relation to supersymmetric quantum mechanics

The relation to [[supersymmetric quantum mechanics]] is due to 

* [[Edward Witten]], _Supersymmetry and morse theory_ ([Euclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.jdg/1214437492))

Reviews include

* [[Gábor Pete]], section 2 of _Morse theory_, lecture notes 1999-2001   ([pdf](http://www.math.bme.hu/~gabor/morse.pdf))


