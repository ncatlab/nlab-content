
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

The notion of _Ehresmann connection_ describes a [[connection on a bundle|connection on]] a $G$-[[principal bundle]] $p : P \to X$ (for $G$ some [[Lie group]]) in terms of a distribution of horizontal subspaces $H \subset T P$ which is a subbundle of the [[tangent bundle]] of $P$ complementary at each point to the vertical tangent bundle to the fiber. This subbundle can be expressed as field of subspaces $H_x = Ker A_x = Ann A_x\subset T P$ ($x\in P$) which are pointwise annihilators of a smooth [[Lie algebra]]-valued $1$-[[differential form|form]] $A \in \Omega^1(P,Lie(G))$ on $P$ that satisfies two conditions spelled out below. 

## Definition

### In terms of differential forms

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $P \to X$ a $G$-[[principal bundle]]. Let

$$
  \rho : P \times G \to P
$$

be the [[action]] of $G$ on $P$ and

$$
  \rho_* : \mathfrak{g} \to \Gamma(T X)
$$

its derivative, sending each element $x \in \mathfrak{g}$ to the [[vector field]] on $P$ that gives the flow it induces under $\rho$.

For $v \in \Gamma(T X)$ and $\omega$ a differential form on $P$ write $\iota_v \omgea$ for the contraction.

A **Cartan-Ehresmann connection** on $P$ is a [[Lie algebra-valued 1-form]]

$$
  A\in \Omega^1(P, \mathfrak{g})
$$

satisfying two conditions

1. **first Ehresmann condition** 

   for every $x \in \mathfrak{g}$ we have

   $$
     \iota_{\rho_*(x)} A = x
     \,.
   $$

2. **second Ehresmann condition**

   for every $x \in \athfrak{g}$ we have

   $$
     \iota_{\rho_*(x)} F_A = 0
     \,.
   $$

**Proposition** These two conditions are equivalent to

1. $\iota_x A = x$

1. $\mathcal{L}_x A = ad_x A$ .

(...)

### In terms of distributions

As already mentioned a connection can equally well be defined by a consistent separation of every tangent space $T_u P$ into the vertical subspace $V_u P$ and the horizontal subspace $H_u P$ such that

1. $T_u P \: = \: H_u P \oplus V_u P$

2. Every smooth vector field X on P is separated into smooth vector fields $X^H \in H_u P$ and $X^V \in V_u P$ such that $X = X^H + X^V$

3. $H_{ug}P = R_{g*}H_u P$ for every $u \in P$ and $g \in G$.

The condition 3. states that horinzontal subspaces $H_u P$ and $H_{ug}P$ on the same fibre are related by a linear map $R_{g*}$ induced by the right action of the gauge group. 

**theorem: equivalence of definitions**: Every connection one-form $A$ defines a separation of tangent spaces as defined above, the horizontal subspaces are given by the kernel of $A$. Conversly, given a separation of tangent spaces it is possible to construct a connection one-form.

### References

* Nakahara, Mikio: _Geometry, topology and physics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1090.53001&format=complete))
 
## Note on terminology 

The terminology for the various incarnations of the single notion of [[connection on a bundle]] varies throughout the literature. What we here call an Ehresmann connection is sometimes, but not always, called **principal connection** (as it is defined for [[principal bundle]]s).



## References 


The original definition is due to

* [[Charles Ehresmann]], _Les connexions infinit&#233;simale dans une espace fibr&#233; diff&#233;rentiable_, Colloque
de Topologie, Bruxelles (1950) 29-55, [MR0042768](http://www.ams.org/mathscinet-getitem?mr=0042768)

A useful statement of the definition in terms of a 1-form on the total space is for instance on [p. 13](http://arxiv.org/PS_cache/gr-qc/pdf/0611/0611154v2.pdf#page13) of

* Derek Wise, _MacDowell-Mansouri gravity and Cartan geometry_ ([arXiv](http://arxiv.org/abs/gr-qc/0611154))

A formulation and discussion of Ehresmann connections using language and tools from [[synthetic differential geometry]] is in section 6 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]
[[!redirects Ehresmann-connection]]