
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Bondal-Orlov reconstruction theorem

* table of contents
{: toc}


## Idea

Thomason and Balmer showed that the [[triangulated categories of sheaves|derived category of coherent sheaves]] on a [[smooth variety]], when considered as a [[monoidal category]] (i.e. with the tensor product) in addition to its [[triangulated category]] structure (i.e. as a [[tensor triangulated category]]), completely determines the variety uniquely; see [[spectrum of a triangulated category]].  However, the derived category still turns out to be an interesting invariant when considered without the monoidal category structure; moreover triangulated equivalences and autoequivalences are also important in relation to the [[homological mirror symmetry]] and similar phenomena.  In fact, Bondal and Orlov show how to reconstruct a smooth [[variety]] from its [[triangulated categories of sheaves|derived category of coherent sheaves]] when its [[canonical sheaf]] is ample or anti-ample, using only the graded structure (i.e. the translation functor).

## Statement

+-- {: .num_theorem }
Let $X$ be a smooth projective variety and suppose that its canonical sheaf $\omega_X$ is ample or anti-ample.  If $Y$ is another smooth projective variety such that there is an equivalence $F : D^b(X) \stackrel{\sim}{\to} D^b(Y)$ between the bounded derived categories of coherent sheaves on $X$ and $Y$, then there is an isomorphism $X \simeq Y$.
=--

## Sketch of proof

The idea of the proof is to characterize "cohomologically" the closed points, invertible sheaves, and Zariski topology.

The main tool we use is the [[Serre functor]].  Due to [[Grothendieck-Serre duality]], both $D^b(X)$ and $D^b(Y)$ have Serre functors $S_X = (\cdot \otimes \omega_X)[n]$ and $S_Y = (\cdot \otimes \omega_Y)[m]$, $n$ and $m$ being the dimensions of $X$ and $Y$ respectively.

For simplicity assume $\omega_X$ is ample; the anti-ample case is analogous.

**Step 1.**  First we characterize the closed points of $X$ and $Y$.

+-- {: .num_defn}
###### Definition
Let $\mathcal{C}$ be a [[linear category|k-linear]] [[graded category]].  A **point object** of $\mathcal{C}$ is an object $P$ satisfying

* (PO-1)  $S(P) \simeq P[n]$,
* (PO-2)  $\Hom^i(P, P) = 0$ for $i \lt 0$,
* (PO-3)  $k(P) := \Hom(P, P)$ is a field.
=--

It is clear that the [[skyscraper sheaf]] $\mathcal{O}_x = \mathrm{Sky}_x(k(x))$ of the [[residue field]] at any closed point $x \in X$ is a point object of $D^b(X)$, as is any translation $\mathcal{O}_x[r]$.  In fact, when we impose the ampleness condition on $\omega_X$, it turns out that all point objects are of this form.

+-- {: .num_prop}
###### Proposition
If $\omega_X$ is ample, then a complex $\mathcal{F}^\bullet$ in $D^b(X)$ is a point object iff $\mathcal{F}^\bullet \simeq \mathcal{O}_x[r]$ for some closed point $x \in X$, $r \in \mathbb{Z}$.
=--

In fact, even though we don't know that $\omega_Y$ is also ample, we get the same result for $D^b(Y)$.  Let $G$ be the inverse equivalence to $F$ and note that $F$ and $G$ preserve point objects.  Suppose there was a point object $P$ in $D^b(Y)$ not isomorphic to any $\mathcal{O}_y[s]$, and note $G(P) \simeq \mathcal{O}_{x_0}[r]$ for some closed $x_0$.  Now for any $y \in Y$, $\Hom(P, \mathcal{O}_y) = \Hom(G(P), G(\mathcal{O}_y)) = \Hom(\mathcal{O}_{x_0}[r], \mathcal{O}_x[r']) = 0$ since $x_0 \ne x$.  But $\{\mathcal{O}_y : y \in Y\}$ form a [[spanning class]] of $D^b(Y)$ which implies that $P = 0$.

**Step 2.**  Next we characterize the invertible sheaves on both varieties.

+-- {: .num_defn}
###### Definition
Let $\mathcal{C}$ be a $k$-linear graded category.  An **invertible object** of $\mathcal{C}$ is an object $L$ satisfying for some $s \in \mathbb{Z}$

* (IO-1)  $\Hom^s(L, P) = k(P)$ for all point objects $P$,
* (IO-2)  $\Hom^i(L, P) = 0$ for $i \ne s$.
=--

+-- {: .num_prop}
###### Proposition
If all point objects of $D^b(X)$, for a smooth projective variety $X$, are translations of skyscraper sheaves of closed points, then all invertible objects of $D^b(X)$ are translations of invertible sheaves on $X$.
=--

This means that the invertible objects of both $D^b(X)$ and $D^b(Y)$ are translations of invertible sheaves, by step 1.

**Step 3.**  Now we establish a bijection between the sets of points of the varieties.

Since $\mathcal{O}_X$ is an invertible object, we can assume without loss of generality that $F(\mathcal{O}_X)$ is isomorphic to some invertible sheaf $\mathcal{L}_0$ on $Y$.  For any $x \in X$,
  \[ k(x) = \Hom(\mathcal{O}_X, \mathcal{O}_x) = \Hom(\mathcal{L}_0, \mathcal{O}_y[s]) \]
for some $y \in Y$, which implies $s=0$ and $F(\mathcal{O}_x) \simeq \mathcal{O}_y$, $k(x) \simeq k(y)$.  We get a bijection of sets $\phi : X \to Y$ by mapping $x \mapsto y$.

**Step 4.**  Now we can get an isomorphism of the [[canonical ring]]s of the varieties.

Assume WLOG $F(\mathcal{O}_X) \simeq \mathcal{O}_Y$.  Note that $S_X^k(\mathcal{O}_X)[-nk] \simeq \omega_X^{nk}$ for any $k$.  By commutativity of $F$ with the Serre functor, $F(\omega_X^{nk}) = S_Y^k(\mathcal{O}_Y)[-nk] = \omega_Y^{nk}$.  Therefore
  \[ H^0(X, \omega_X^{nk}) = \Hom(\mathcal{O}_X, \omega_X^{nk}) = \Hom(\mathcal{O}_Y, \otimes_Y^{nk}) = H^0(Y, \omega_Y^{nk}) \]
and $\bigoplus_k H^0(X, \omega_X^{nk}) \simeq \bigoplus_k H^0(Y, \omega_Y^{nk})$, that is we have an isomorphism of the canonical rings $A(X)$ and $A(Y)$.

**Step 5.**  Since $X = \mathrm{Proj}(A(X))$ iff $\omega_X$ is ample, it remains therefore only to show that $\omega_Y$ is ample.  To do this we characterize the Zariski topology "cohomologically".

For any invertible sheaf $\mathcal{L}$ on $X$, $\alpha \in \Hom(\mathcal{O}_X, \mathcal{L})$, and $x \in X$, let $\alpha_X^* : \Hom(\mathcal{L}, \mathcal{O}_x) \to \Hom(\mathcal{O}_X, \mathcal{O}_x)$ be the induced map that takes $f$ to $f \circ \alpha$, and define the subset $U_\alpha = \{ x \in X : \alpha_x^* \ne 0 \} \subset X$.  Now $\omega_X$ being ample is equivalent to the subcollection $\{ U_\alpha : \alpha \in \Hom(\mathcal{O}_X, \omega_X^m), m \in \mathbb{Z} \}$ forming a basis of the Zariski topology on $X$.  Now the equivalence $F$ maps any $\mathcal{O}_X \stackrel{\alpha}{\to} \mathcal{L} \to \mathcal{O}_x$ to
  \[ \mathcal{O}_Y \stackrel{F(\alpha)}{\to} F(\mathcal{L}) \to \mathcal{O}_{\phi(x)}[s].\]
$F(\alpha)$ corresponds bijectively to some $\beta \in \Hom(\mathcal{O}_Y, \omega_Y^m)$ and in fact our bijection $f : X \to Y$ becomes a homeomorphism mapping $U_\alpha$ to $V_{F(\alpha)}$.  It follows that $\{ V_\beta : \beta \in \Hom(\mathcal{O}_Y, \omega_Y^m), m \in \mathbb{Z} \}$ forms a basis of the Zariski topology on $Y$, which implies $\omega_Y$ is ample.

## See also

* [[triangulated categories of sheaves]]
* [[2-ring]]
* [[spectrum of a triangulated category]]
* [[spectrum of an abelian category]]
* [[Tannaka duality for geometric stacks]]
* [[higher geometry]]

## References

The original paper:

* [[Aleksei Bondal]], [[Dmitri Orlov]], _Reconstruction of a variety from the derived category and groups of autoequivalences_, Compositio Mathematica __125__ (03), 327-344 [doi](http://dx.doi.org/10.1023/A:1002470302976), [pdf](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)_[Reconstruction of a variety from the derived category and groups of autoequivalences](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)_, Compositio Mathematica 125 (03), 327-344.

A nice exposition of the proof with more details can be found in section 3.1 of the course notes of [[Igor Dolgachev]] on [[derived categories]]:

* [[Igor Dolgachev]], [_Derived categories_](http://www.math.lsa.umich.edu/~idolga/derived9.pdf).

The theorem is also discussed in:

* [[Raphaël Rouquier]], _[Cat&#233;gories d&#233;riv&#233;es et g&#233;om&#233;trie birationnelle](http://arxiv.org/abs/math/0503548)_, S&#233;minaire Bourbaki, no 947, March 2005.

* [[Daniel Huybrechts]], _Fourier-Mukai transforms in algebraic geometry_, 2006.