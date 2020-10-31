
This entry provides some hyperlinks for the articles

* [[Daniel S. Freed]], [[Michael Hopkins]], [[Constantin Teleman]], 

  1. _Loop Groups and Twisted K-Theory I_, 

     J. Topology, 4 (2011), 737-789  
   
     ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019))

  1. {#PartII} _Loop Groups and Twisted K-Theory II_, 

     J. Amer. Math. Soc. 26 (2013), 595-644  

     ([arXiv:0511232](http://arxiv.org/abs/math/0511232), [doi:10.1090/S0894-0347-2013-00761-4](https://doi.org/10.1090/S0894-0347-2013-00761-4))

  1. _Loop Groups and Twisted K-Theory III_, 

     Annals of Mathematics, Volume 174 (2011) 947-1007 

     ([arXiv:math/0312155](http://arxiv.org/abs/math/0312155), [doi:10.4007/annals.2011.174.2.5](http://dx.doi.org/10.4007/annals.2011.174.2.5))
  
about the [[twisted ad-equivariant K-theory]] of [[compact Lie groups]], and the [[positive energy representations]] of their [[loop groups]] (forming the [[Verlinde ring]]). Part II also deals with [[Dirac induction]] and the [[orbit method]] for producing representations by the [[geometric quantization]] of [[coadjoint orbits]].

The result on twisted K-groups has been lifted to an [[equivalence of categories]] in

* [[Daniel S. Freed]], [[Constantin Teleman]], 

  _Dirac families for loop groups as matrix factorizations_, 

  Comptes Rendus Mathematique, Volume 353, Issue 5, May 2015, Pages 415-419

  ([arxiv/1409.6051](http://arxiv.org/abs/1409.6051), [doi:10.1016/j.crma.2015.02.011](https://doi.org/10.1016/j.crma.2015.02.011))

> We identify the category of integrable lowest-weight representations of the loop group $L G$ of a compact Lie group $G$ with the linear category of twisted, conjugation-equivariant curved Fredholm complexes on the group $G$: namely, the twisted, equivariant [[matrix factorizations]] of a super-potential built from the loop rotation action on $L G$. This lifts the isomorphism of K-groups of [FHT1,2, 3] to an equivalence of categories. The construction uses families of Dirac operators. 

## Statement of the theorem

Every $\mathfrak{g}$-[[Lie algebra valued differential form|valued differential form]] $A \in \Omega^1(S^1, \mathfrak{g})$ on the [[circle]] defines an element in the free [[loop group]]. Also it can be understood as a [[connection on a bundle|connection]] on a $G$-[[principal bundle]] over the circle.

Given a [[Dirac operator]] $D$ on an [[associated bundle|associated]] [[spinor bundle]] over the circle, and using a [[loop group representation]] $V$ one can hence shift its defining connection by $A$ and form the associated Dirac operator $D_A$.

By remembering for each $A$ its [[holonomy]] $hol(A) \in G$, this construction defines a $G$-parameterized family of [[Fredholm operators]] over $G$, one for each loop group representation. 

This construction is ([FHT, part II, cor. 3.39](#PartII)).

The FHT-theorem asserts that this construction gives an equivalence of the category of loop group representations at some level $\tau$ ([[Verlinde ring]]) and the $\tau$-[[twisted K-theory]], [[equivariant cohomology|equivariant]] with respect to $Ad_G$, on $G$.

This is ([FHT, part II, theorem. 3.43](#PartII)).


## Notes

> Some raw notes from a Teleman talk, to be polished

Group actions on categories and Langlands duality

I. Index formula on moduli of G_bundles and TQFT

* revolves around the [[Verlinde formula]]

* formulation in twisted K-theory

* generalization from [[line bundle]]s to general [[vector bundle]]s

* For line bundles, relation between [[loop groups]] reps on twisted K-theory

construction of twisted K-theory classes from families of Dirac operators

* puzzling appearance of Langlands dual group in relation to Lie group action on categories


start

$G$ a [[compact space|compact]] [[Lie group]] [[connected]] [[simply connected]]

$T \subset G$ [[maximal torus]], $T^\vee$ the dual torus, $W$ [[Weyl group]]

$k \in \mathbb{Z} \simeq H^4(B G, \mathbb{Z})$ called the "level"

$\Sigma$ a closed [[oriented]] [[Riemann surface]]

$K_G(\Sigma) = Flat G Bund(\Sigma) \simeq Hom(\pi_1 \Sigma, G)/G$ the [[moduli space]] of [[connection on a bundle|flat]] $G$-[[principal bundle]]s on $\Sigma$. This inherits a [[complex structure]] from $\Sigma$

$$
  \mathcal{O}(k) \to M_G(\Sigma)
$$

the [[determinant line bundle]] for $G = SU(n)$  $det^{-k} H^\bullet(\Sigma, standard vector bundle)$

Intense activity was generated in 1990s by the [[Verlinde formula]] suggested by [[CFT]]

$$
 d = dim H^0 ( M_G(\Sigma), \mathcal{O}(k))
$$

which is the [[partition function]] of a [[CFT]]
level-$k$ [[line bundle]]
  
Digression recall that [[2d TQFT]]s correspond to [[Frobenius algebra]]s.

If $A$ is a [[semi-simple algebra]] $\simeq \oplus \mathbb{C} P_i$, where

$\theta(P_i) = \theta_i \in \mathbb{C}^\times$ and $Z(\Sigma) = \sum \theta_i^{1-g(\Sigma)}$

In our case, the [[Verlinde ring]] is a Frobenius ring / $\mathbb{Z}$. It is a quotient of the ring of representations $R_G$ by the ideal of characters vanishing at the regular points  $F = ker(T \stackrel{k+c}{\to}T^\vee)$, where $c$ is the [[dual Coxeter number]]

the [[isogeny]] of $k$ being defined by the level

$$
  k \in H^4(B G, \mathbb{Z}) \to H^4(B T, \mathbb{Z}) = Sym^2 \pi_1(T)^\vee
$$

the projectors $P_f$ range over $f \in F^{reg}/W$ ($F$ a Weyl orbit)

The traces $\theta(P_f) = \frac{vol(c_f)}{|F|} = \frac{\Delta(f)^2}{|F|}$

Where $c_F$ is order of conjugacy class of $F$

Substantial work went into proving various casesy of the formula...

A distinction aroise between the [[moduli space]] [[topological space]] and the [[moduli stack]] of all algebraic $G_{\mathbb{C}}$-bundles;

turned out to be immaterial for holomorphic sections (and higher cohomology of line bundles, which vanishes in both cases)

But for more general vector bundles it became cleat that the Verline-style formulas apply to the [[moduli stack]] 
 and not the space

Recall that Narasimhan-Sechadri identity the moduli space of semi-stable algebraic $G_{\mathbb{C}}$ bundles (modulo grade invariance)

The [[moduli stack]] of all holomorphic $G_{\mathbb{C}}$-bundles

Has an atractive complex analytic presentation due to [[Graeme Segal]]

choose a disk $\Delta \subset \Sigma$ with smooth parameterized boundary $\partial \Delta$. Then the stack $\mathcal{M}_G(\Sigma)$ is the double [[coset]] $  Hol(\Delta, G_{\mathbb{C}})\backslash L G_{\mathbb{C}} / Hol(\Sigma \backslash \Delta, G_{\mathbb{C}})$

where the holomorphic maps have smooth boundary values

The variety 

$$
  X_{\Sigma \backslash \Delta} = L G / Hol(\Sigma \backslash \Delta, G_{\mathbb{C}})$$

is a complex K&#228;hler homogeneous space for $L G_{\mathbb{C}}$ analogous in many ways to a [[flag variety]] of complex semsimple Lie groups

As a [[symplectic manifold]] it can be realized as 

$$
  (flat G bundles in \Sigma \backslash \Delta) / {gauge equivalences trivial on \partial \Delta}
$$

The symplectic structure here is independent of the complex structure omn $\Sigma$

The $L G$ action is projective Hamiltonian, being a central extension lift to the prequantum line bundle

So holomorphic and cohomological questions about the stack of all $G_{\mathbb{C}}$-bundles on $\Sigma$ is equivalently

$Hol(\Delta, G)$-equivariant holomorphic and cohomological  on $X_{\Sigma \backslash \Delta}$

Example: What is $H^0(X_{\Sigma \backslash \Delta}, \mathcal{O}(k))$ as an $L G$-representation? Turns out the multiplicity of a certain "vacuum" representation inside is equal to $dim H^0(K_G(\Sigma), \mathcal{O}(k))$

While complex analysis on such infinite-dimensional manifolds is still out of reach, there exists an algebraic model for $X_{\Sigma \backslash \Delta}$ for which we can ask and answer analogous question

Example: $H^{\gt 0}(X^{ab}_{\Sigma \backslash \Delta}, \mathcal{O}(k)) = 0$
"Kodeira vanishing"

So we have an analytic index theorem for these varieties but without a topological side (this was "paradoxical", because usually the topological side is easier.)

But this requires finding a receptable fot the topological index ([[Riemann-Roch theorem]])

Whet $\mathcal{G}$ acts on R%X%, RR takes values in 

$$
  Rep(\mathcal{G}) = K_{\mathcal{G}}(point) :
 K_{\mathcal{G}}(X) \stackrel{p_*}{\to} K_{\mathcal{G}}(point)
$$

[[fiber integration]] in [[generalized cohomology theory]]

Here $K_{L G}(point)$ is not "topological", not got equivariant K-theory for non-compact groups!, so that map $p_*$

But it turns out that both problems have a simultaneous solution.

Instead consider $K_{L G}(\mathcal{A}_{S^1})$ for the gauge action of $L G$ inb tge space of flat $G$-connections on the circle

Instead of projecting $X_{\Sigma \backslash \Delta}$ to a point, use the flat connection model and restrict to the boundary $\partial \Delta : X_{\Sigma \backslash \Delta} \o \mathcal{A}_{\partial \Delta}$

This is a [[proper map]]!

The based loop group $\Omega G$ acts freely and we can 

which leads to a well-defined map

$$
  K_G(G^{2 g}) \stackrel{p_*}{\to} K_G(G)
$$

Amendments;

we wanted projective representations of $L G$ with cocycle 

$$
  k \in H^2_{L G}(\mathcal{O}^\times)(\stackrel{\sim}{\to} H^3_G(G, \mathbb{Z}))  
$$

So we should map to the [[twisted K-theory]] group

$$
  K_G^{k}(G)
$$


actually there is an extra shift by the dual Coxeter number $c$ ($= n $ for $SU(n)$) coming from the [[spinor]]s $\sqrt K$ on $X_{\Sigma \backslash \Delta}$, and the key theorem is

[[Freed-Hopkins-Teleman theorem]]: 

$$
  {}^{k + c}K_G^{dim G}(G) 
$$

is a free abelian group generated by the positive energey irreps of $L G$ at level $k$.

generalization by Teleman and Woodward: 

analytical index = topological index for $X_{\Sigma \backslash \Delta}^alg$

for essentially all K-theory clases, at least after inverting $k+ c$

II. From loop group representations to K-theory

Preparation: Compact groups:

Recall the Kirillov correspondence between 

irreducilble representations and co-adjoint orbits (+ line bundles)

In the connected case it can be summarized by saying that both of those correspond to the set of dominant integral regular wheights.

Example: $n$-dimensional rep of $SU(2)$: sphere of radius $n$ in $\mathfrak{su}(2) \simeq \mathbb{R}^3$ 

for $SO(3)$, odd radii,

but one can describe a canonical correspondence without directs reference to the classification of irreps

Each [[coadjoint orbit]] has a [[symplectic form]] (see at _[[orbit method]]_)

$$
  \omega_2(ad^*_\xi(\lambda), ad^*_\eta(\lambda))
  = 
  \langle \lambda | [\xi,\eta]]\rangle
$$

For a vector bundle $V$ on the orbit $O_\lambda$ of $\lambda$, which is a sum of line bundles with curvature $\omega_\lambda$ and which carries a lifted $G$-action.

The Dirac index $D Ind(O_\lambda, V)$ is a representation of $G$ and this establishes the Kirillov correspondence

Remarks: For connected $G$, $V$ carries no information beyond its rank

Wehn $\pi_1(G) \neq 0$ the $G$-action on $V$ should be projective and cancel the spinor projective cocycle

The Dirac family consruction (Freed, Hopkins, Teleman) provides an inverse to this, assigning an orbit,...

Input: irreducible representation $V_\lambda$ of $G$ 

$\omega$ highest weight $\lambda$
invariant metric on $\mathfrak{g}$

Use Kostant's "cubic Dirac operator" on $G$, which is the [[Dirac operator]] on $G$ for the metric connection with canonical torsion coming from $H^3(G, \mathbb{Z}) \simeq \mathbb{Z}$.

Two key properties of this Dirac operator

$$
  [D, \psi(\xi)] = 2 T(\xi)
$$

(translation)

$$
  D^2 = - (\lambda + p)^2
$$

on $V_\lambda \otimes S^{\pm}$

The Dirac family is the $\mathbb{Z}/2$-graded vector bundle with fiber $V \otimes S^{\pm}$ over $\mathfrak{g}$ and odd operator

$$
  D_\xi^V := D^V + \psi(\xi)
$$

Theorem (FHT): The kernel of $D^V_\xi$ is supported on the orbit of $(\lambda + p)$ and equals $(Kirillov line bundle) \otimes (Spinors to normal bundle)$ In fact $D^V_\xi$ is a model for the Atiyah-Bott-Shapiro...






[[!redirects Freed-Hopkins-Teleman theorem]]
[[!redirects FHT theorem]]


category: reference