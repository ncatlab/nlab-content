
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Twisted K-theory is a [[twisted cohomology]] version of [[K-theory]], where the twist is given by a cocycle in degree 3 [[Eilenberg-MacLane spectrum|ordinary cohomology]].

## Definition 

### By sections of associated $K U$-bundles

Write $K U$ for the [[spectrum]] of complex [[topological K-theory]]. Its degree-0 space ism up to [[weak homotopy equivalence]],  the space 

$$
  B U \times \mathbb{Z} = {\lim_\to}_n B U(n) \times \mathbb{Z}
$$

or the space $Fred(\mathcal{H})$ of  [[Fredholm operator]]s on some separable [[Hilbert space]] $\mathcal{H}$.

$$
  (K U)_0 \simeq B U \times \mathbb{Z} \simeq Fred(\mathcal{H})
  \,.
$$

The ordinary [[topological K-theory]] of a [[topological space]] $X$ is

$$
  K(X)_\bullet \simeq [X, (K U)_\bullet]
  \,.
$$

The [[projective unitary group]] $P U(\mathcal{H})$ (a [[topological group]]) acts canonically by [[automorphism]]s on $(K U)_0$. Therefore for $P \to X$ any $PU(\mathcal{H})$-[[principal bundle]], we can form the [[associated bundle]] $P \times_{P U(\mathcal{H})} (K U)_0$.

Since the [[homotopy type]] of $P U(\mathcal{H})$ is that of an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, there is precisely one isomorphism class of such bundles representing a class $\alpha \in H^3(X, \mathbb{Z})$.

The **twisted K-theory** with twist $\alpha \in H^3(X, \mathbb{Z})$ is the set of [[homotopy]]-classes of [[section]]s of such a bundle

$$
  K^\alpha(X)_0
  :=
  \Gamma_X(P^\alpha \times_{P U(\mathcal{H})} (K U)_0)
  \,.
$$

### By twisted vector bundles (gerbe modules)

(...)

## Other constructions

Let $Vectr$ be the [[stack]] of [[vectorial bundle]]s. (If we just take [[vector bundle]]s we get a notion of twisted K-theory that only allows twists that are finite order elements in their [[cohomology group]]).

There is a canonical morphism

$$
  \rho : \mathbf{B} U(1) \to Vect \hookrightarrow Vectr
$$

coming from the standard [[representation]] of the [[group]] $U(1)$.

Let $\mathbf{B}_{\otimes} Vectr$ be the [[delooping]] of $Vectr$ with respect to the [[tensor product]] [[monoidal category|monoidal structure]] (not the additive structure).

Then we have a [[fibration sequence]]

$$
  Vectr \to {*} \to \mathbf{B}_\otimes Vectr
$$

of [[(infinity,1)-category|(infinity,1)-categories]] (instead of [[infinity-groupoid]]s).

The entire morphism above deloops

$$
  \mathbf{B}\rho : \mathbf{B}^2 U(1) \to \mathbf{B}_\otimes Vect \hookrightarrow \mathbf{B}_{\otimes} Vectr
$$

being the standard representation of the [[2-group]] $\mathbf{B}U(1)$.

From the general nonsense of [[twisted cohomology]] this induces canonically now for every $\mathbf{B}^2 U(1)$-[[cohomology|cocycle]] $c$ (for instance given by a [[bundle gerbe]]) a notion of $c$-twisted $Vectr$-cohomology:

$$
 \array{
   \mathbf{H}^c(X, Vectr)
   &\to&
   {*}
   \\
   \downarrow
   &&
   \downarrow^{\mathbf{B}\rho \circ c}
   \\
   {*} &\to& \mathbf{H}(X,\mathbf{B}_\otimes Vectr)
 }
  \,.
$$

After unwrapping what this means, the result of ([Gomi](#Gomi))
shows that [[concordance]] classes in $\mathbf{H}^c(X,Vectr)$ yield twisted K-theory.



## References 

The perspective of twisted K-theory by sections of a $K U$-bundle of spectra is discussed for instance in section 22 of 

* [[Peter May|May]], Sigurdsson, _Parametrized homotopy theory_ ([pdf]( http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf)) AMS Lecture notes 132
 {#MaySigurdsson}



Discussion in terms of [[twisted bundle]]s ([[bundle gerbe module]]s) is in 

* [[Alan Carey]], [[Peter Bouwknegt]], [[Varghese Mathai]], [[Michael Murray]] and [[Danny Stevenson]], _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv](http://arxiv.org/abs/hep-th/0106194))
  {#CBMMS} 

* [[Max Karoubi]], _Twisted bundles and twisted K-theory_, [arxiv/1012.2512](http://arxiv.org/abs/1012.2512) 
 {#Karoubi}

Discussion in terms of [[vectorial bundle]]s is in

* [[Kiyonori Gomi]], _Twisted K-theory and finite-dimensional approximation_ ([arXiv](http://arxiv.org/abs/0803.2327))
 {#Gomi}

* [[Kiyonori Gomi]] und Yuji Terashima, _Chern-Weil Construction for Twisted K-Theory_ Communication ins Mathematical Physics, Volume 299, Number 1, 225-254, 
 {#GomiTerashima}
