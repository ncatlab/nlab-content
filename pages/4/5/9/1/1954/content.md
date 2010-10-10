
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
  \rho_* : \mathfrak{g} \to \Gamma(T X)
$$

its derivative, sending each element $x \in \mathfrak{g}$ to the [[vector field]] on $P$ that at $p \in P$ is the push-forward $\rho(p,-)_*(x)$.

For $v \in \Gamma(T X)$ and $\omega$ a differential form on $P$ write $\iota_v \omega$ for the contraction.

+-- {: .un_defn}
###### Definition

A **Cartan-Ehresmann connection** on $P$ is a [[Lie algebra-valued 1-form]]

$$
  A\in \Omega^1(P, \mathfrak{g})
$$

on $P$ satisfying two conditions

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


+-- {: .un_prop}
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

Using $\iota_x A = x$ we have by [[Cartan calculus]]

$$
  \begin{aligned}
     \iota_{\rho_*(x)} F_A &=
     \iota_{\rho_*(x)} d_{dR} A + \frac{1}{2}[A\wedge A]
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

An Ehresmann connection describes a [[connection on a bundle|connection on]] a $G$-[[principal bundle]] $p : P \to X$ (for $G$ some [[Lie group]]) in terms of a distribution of horizontal subspaces $H \subset T P$ which is a subbundle of the [[tangent bundle]] of $P$ complementary at each point to the vertical tangent bundle to the fiber. This subbundle can be expressed as field of subspaces $H_x = Ker A_x = Ann A_x\subset T P$ ($x\in P$) which are pointwise annihilators of a smooth [[Lie algebra]]-valued $1$-[[differential form|form]] $A \in \Omega^1(P,Lie(G))$ on $P$ that satisfies two conditions 

1. $T_u P \: = \: H_u P \oplus V_u P$

2. Every smooth vector field X on P is separated into smooth vector fields $X^H \in H_u P$ and $X^V \in V_u P$ such that $X = X^H + X^V$

3. $H_{ug}P = R_{g*}H_u P$ for every $u \in P$ and $g \in G$.

The condition 3. states that horinzontal subspaces $H_u P$ and $H_{ug}P$ on the same fibre are related by a linear map $R_{g*}$ induced by the right action of the gauge group. 


## Properties

### General

+-- {: .un_defn}
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

+-- {: .un_defn}
###### Remark

This means we may think of $A$ as measuring how [[infinitesimal object|infinitesimal]] paths in $P$ fail to be _horizontal_ or _parallel_ to $X$ in the sense of [[parallel transport]].

=--

### Curvature characteristic forms

Let $\langle - \rangle \in W(\mathfrak{g})$  be an [[invariant polynomial]] on the Lie algebra. For $A \in Omega^1(P,\mathfrak{g})$ an Ehresmann connection, write

$$
  \langle F_A \rangle = \langle F_A \wedge F_A \wedge \cdots F_A\rangle
$$

for the [[curvature characteristic form]] obtained by evaluating this on wedge powers of the [[curvature]] 2-form.

+-- {: .un_prop}
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

+-- {: .un_remark}
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

* [[Charles Ehresmann]], _Les connexions infinit&#233;simale dans une espace fibr&#233; diff&#233;rentiable_, Colloque
de Topologie, Bruxelles (1950) 29-55, [MR0042768](http://www.ams.org/mathscinet-getitem?mr=0042768)

See also

* Nakahara, Mikio: _Geometry, topology and physics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1090.53001&format=complete))

A formulation and discussion of Ehresmann connections using language and tools from [[synthetic differential geometry]] is in section 6 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_


[[!redirects Ehresmann-connection]]

[[!redirects Ehresmann connections]]

[[!redirects Cartan-Ehresmann connection]]
[[!redirects Cartan-Ehresmann connections]]