
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The notion of _Ehresmann connection_ is one of the various equivalent definitions of [[connection on a bundle]].

## Definition

### In terms of differential forms {#InTermsDiffForms}

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $P \to X$ a $G$-[[principal bundle]]. Let

$$
  \rho : P \times G \to P
$$

be the [[action]] of $G$ on $P$ and

$$
  \rho_* : \mathfrak{g} \to \Gamma(T P)
$$

its derivative, sending each element $x \in \mathfrak{g}$ to the [[vector field]] on $P$ that at $p \in P$ is the push-forward $\rho(p,-)_*(x)$.

For $v \in \Gamma(T P)$ and $\omega$ a differential form on $P$ write $\iota_v \omega$ for the contraction.

+-- {: .num_defn #CartanEhresmannConnection}
###### Definition


Given a $G$-[[principal bundle]] $P$ over $X$,  a **Cartan-Ehresmann connection** on $P$ is a [[Lie algebra-valued 1-form]]

$$
  A\in \Omega^1(P, \mathfrak{g})
$$

on the total space $P$ satisfying two conditions:

1. **first Ehresmann condition** 

   for every $x \in \mathfrak{g}$ we have

   $$
     \iota_{\rho_*(x)} A = x
     \,.
   $$

2. **second Ehresmann condition**

   for every $x \in \mathfrak{g}$ we have

   $$
     \mathcal{L}_{\rho_*(x)} A = ad_x A
     \,,
   $$

   where $\mathcal{L}_{\rho_*(x)}$ is the [[Lie derivative]] along $\rho_*(x)$ 
   and where $ad_x : \mathfrak{g} \to \mathfrak{g}$ is the [[adjoint action]] 
   of $\mathfrak{g}$ on itself.

=--


+-- {: .num_prop #FormulationInTermsOfCurvatureForm}
###### Proposition

This is equivalent to

1. **first Ehresmann condition** 

   for every $x \in \mathfrak{g}$ we have

   $$
     \iota_{\rho_*(x)} A = x
     \,.
   $$


2. **second Ehresmann condition**

   for every $x \in \mathfrak{g}$ we have

   $$
     \iota_{\rho_*(x)} F_A = 0
     \,,
   $$

   where $F_A \in \Omega^2(P, \mathfrak{g})$ is the [[curvature]] 2-form of
   $A$.

=--

+-- {: .proof}
###### Proof

Using $\iota_{\rho_*(x)} A = x$ we have by [[Cartan calculus]]

$$
  \begin{aligned}
     \iota_{\rho_*(x)} F_A &=
     \iota_{\rho_*(x)} ( d_{dR} A + \frac{1}{2} [A\wedge A] )
     \\
     & =
     \mathcal{L}_{\rho_*(x)} A - d_{dR} \iota_{\rho_*(x)} A +
     [x,A]
     \\
     & = \mathcal{L}_{\rho_*(x)} A + [x,A]
     \,.
  \end{aligned}
$$

=--


### In terms of distributions

Given a smooth bundle $\pi: E\to X$ with typical fiber $F$ (e.g. a smooth vector bundle or a smooth principal $G$-bundle), there is a well defined vector subbundle $V E\subset T E$ over $E$ such that $V_p$ consists of the  tangent vectors $v_p$ such that $(T_p \pi)(v_p) = 0$. A __smooth distribution (field) of horizontal subspaces__ is a choice of a vector subspace $H_p E\subset T_p E$ for every $p$ such that 

E1. (complementarity) $T_u E \: = \: H_u E \oplus V_u E$

E2. $p\mapsto H_p E$ is smooth. That means that in the unique decomposition of any smooth vector field $X$ on $E$ into vector fields $X^H \in \Gamma(H_u E)$ and $X^V \in \Gamma(V_u E)$ such that $X = X^H + X^V$ the vector field $X^H$ is smooth (or equivalently $X^V$ is smooth, or equivalently both) as a section of $T E$ (there exist yet several other equivalent formulations of the smooothness criterion).

An Ehresmann connection describes a [[connection on a bundle|connection on]] a $G$-[[principal bundle]] $\pi : P \to X$ (for $G$ some [[Lie group]]) in terms of a distribution of horizontal subspaces $H \subset T P$ which is a subbundle of the [[tangent bundle]] of $P$ complementary at each point to the vertical tangent bundle to the fiber. More precisely, an __Ehresmann connection__ on a principal $G$-bundle $\pi:P\to X$ is a smooth distribution of horizontal subspaces $p\mapsto H_p P$ which is __equivariant__:

E3. $H_{p g}P = (T_p R_g) H_p P$ for every $p \in P$ and $g \in G$.

This subbundle $H = \cup_p H_p\subset T X$ over $X$ can be expressed as a field of subspaces $H_x = Ker A_x = Ann A_x\subset T P$ ($x\in P$) which are pointwise annihilators of a smooth [[Lie algebra]]-valued $1$-[[differential form|form]] $A \in \Omega^1(P,Lie(G))$ on $P$ that satisfies two Ehresmann conditions from the previous subsection. 

The Ehresmann connections on a principal $G$-bundle are in 1-1 correspondence with an appropriate notion of a connection on the associated
bundle. Namely, if $T^H P\subset T P$ is the smooth horizontal distrubution of subspaces defining the principal connection on a principal $G$-bundle $P$ over $X$, where $G$ is a Lie group and $F$ a smooth left $G$-space, then consider the total space $P\times_G F$ of the associated bundle with typical fiber $F$. Then, for a fixed $f\in F$ one defines a map $\rho_f : P\to P\times_G F$ assigning the class $[p,f]$ to $p\in P$. If $(T_p \rho_f)(T^H_p P) =: T_{[p,f]}^H P\times_G F$ defines the horizontal subspace $T_{[p,f]}^H P\times_G F\subset T_{[p,f]} P\times_G F$, the collection of such subspaces does not depend on the choice of $(p,f)$ in the class $[p,f]$, and the correspondence $p\mapsto T_{[p,f]}^H P\times_G F$ is a connection on the associated bundle $P\times_G F\to X$.

### In terms of cohesive homotopy type theory

One may also describe(flat) Ehresmann connections in 
[[cohesive homotopy type theory]]. 

The general abstract discussion is [here](cohesive+%28infinity%2C1%29-topos+--+structures#FlatEhresmannConnections). The discussion of how in [[smooth infinity-groupoids]] this reduces to the traditional notion is [here](smooth+infinity-groupoid+--+structures#FlatEhresmannConnections).

## Properties

### General

+-- {: .num_defn}
###### Definition

The two definitions in terms of 1-forms and in terms of horizontal distributions are equivalent.

=--

+-- {: .proof}
###### Proof

At each $p \in P$ take the horizontal subspace $H_p P$ to be the [[kernel]] of $A(p) : T_p P \to \mathfrak{g}$

$$
  H_p P := ker A(p)
$$

=--

+-- {: .num_defn}
###### Remark

This means we may think of $A$ as measuring how [[infinitesimal object|infinitesimal]] paths in $P$ fail to be _horizontal_ or _parallel_ to $X$ in the sense of [[parallel transport]].

=--

### Curvature characteristic forms

Let $\langle - \rangle \in W(\mathfrak{g})$  be an [[invariant polynomial]] on the Lie algebra. For $A \in \Omega^1(P,\mathfrak{g})$ an Ehresmann connection, write

$$
  \langle F_A \rangle = \langle F_A \wedge F_A \wedge \cdots F_A\rangle
$$

for the [[curvature characteristic form]] obtained by evaluating this on wedge powers of the [[curvature]] 2-form.

+-- {: .num_prop}
###### Proposition

The forms $\langle F_A \rangle \in \Omega^{2k}(P)$ are closed,  descend along $p : P \to X$, in that they are pullbacks of forms along $p$, and their class in [[de Rham cohomology]] $H^{2k}(X)$ are independent of the choice of $A$ on $P$.

=--

+-- {: .proof}
###### Proof

That the forms are closed follows from the [[Bianchi identity]]

$$
  d F_A = [A\wedge F_A]
$$

satisfied by the curvature 2-form and the defining as-invariance of $\langle-\rangle$.  More abstractly, the 1-form $A$ itself may be identified with a morphism of [[dg-algebra]]s out of the [[Weil algebra]] $W(\mathfrak{g})$ (see there)

$$
  \Omega^\bullet(P) \leftarrow W(\mathfrak{g}) : A
$$

and the evaluation of the curvature in the invariant polynomials corresponds to the precomposition with the morphism

$$
  W(\mathfrak{g}) \leftarrow CE(b^{2k-1}\mathbb{R} ) : \langle - \rangle
$$

described at [[∞-Lie algebra cohomology]].

to show that these forms descend, it is sufficient  to show that for all $x \in \mathfrak{g}$ we have 

1. $\iota_{\rho_*(X)} \langle F_A \rangle = 0$

1. $\mathcal{L}_{\rho_*(x)} \langle F_A \rangle = 0$

The first follows from $\iota_{\rho_*(x)} F_A = 0$. The second from this, the $d_{dR}$-closure just discussed and [[Cartan's magic formula]] for the [[Lie derivative]].

=--

+-- {: .num_remark}
###### Remark

The form $\langle F_A \rangle$ is called the [[curvature characteristic form]] of the connection $A$. The map

$$
  \inv(\mathfrak{g}) \to \Omega^\bullet(X)
$$

induced by $(P,A)$ as above is the [[Chern-Weil homomorphism]].

=--

## Note on terminology 

The terminology for the various incarnations of the single notion of [[connection on a bundle]] varies throughout the literature. What we here call an Ehresmann connection is sometimes, but not always, called **principal connection** (as it is defined for [[principal bundle]]s).



## References 


The original definition is due to

* [[Charles Ehresmann]], _Les connexions infinitésimales dans un espace fibré différentiable_, [[Séminaire Bourbaki]], Vol. 1, Exp. No. 24, 153–168, [numdam](http://www.numdam.org/article/SB_1948-1951__1__153_0.pdf).
A paper with the same author and title appeared in
Colloque de topologie (espaces fibrés), Bruxelles, 1950, pp. 29–55. Georges Thone, Liège; Masson et Cie., Paris, 1951.

See also

* Nakahara, Mikio: _Geometry, topology and physics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1090.53001&format=complete))

A formulation and discussion of Ehresmann connections using language and tools from [[synthetic differential geometry]] is in section 6 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_

Generalization to [[principal 2-bundles]] is discussed in

* {#Waldorf16} [[Konrad Waldorf]], _A global perspective to connections on 
principal 2-bundles_ ([arXiv:1608.00401](https://arxiv.org/abs/1608.00401))

Generalization to [[connections on principal ∞-bundles]]:


* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes]] -- An $\infty$-Lie theoretic construction_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735), [Euclid](http://projecteuclid.org/euclid.atmp/1358950853)) 

A more comprehensive account is in sections 3.9.6, 3.9.7 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


[[!redirects Ehresmann-connection]]

[[!redirects Ehresmann connections]]

[[!redirects Cartan-Ehresmann connection]]
[[!redirects Cartan-Ehresmann connections]]