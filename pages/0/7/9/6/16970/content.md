
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization of the concept of [[homotopy group]] from [[homotopy theory]] and [[stable homotopy theory]] to [[equivariant homotopy theory]] and [[equivariant stable homotopy theory]].

## Definition

### Abstractly

For $X$ a [[pointed topological space|pointed]] [[topological G-space]] and $H \subset G$ a closed [[subgroup]], the $n$th _unstable_ $H$-equivariant homotopy group of $X$ is simply the ordinary $n$-th [[homotopy group]] of the $H$-[[fixed point]] space $X^H$:

$$
  \pi_n^H(X) \coloneqq \pi_n(X^H)
  \,.
$$

With $G/H$ denoting the [[quotient space]], this is equivalently the $G$-[[homotopy classes]] of $G$-equivariant [[continuous functions]] from the [[smash product]] $S^n \wedge G/H_+$ to $X$:

$$
  \pi_n^H(X) \simeq [G/H_+ \wedge S^n, X]^G
  \,.
$$

In this form the definition directly generalizes to [[G-spectra]] and hence to stable equivariant homotopy groups: for $E$ a [[G-spectrum]], and $n \in \mathbb{Z}$, write 

$$
  \pi_n^H(X) \simeq [G/H_+ \wedge S^n, X]^G
  \,.
$$

where now $S^n$ is the $n$-fold suspension of the [[suspension spectrum]] of the [[n-sphere]] and $[-,-]^G$ now denotes the [[hom functor]] in the [[equivariant stable homotopy category]]..

In particular, the [[(∞,1)-category]] of $G$-spectra is stable, and hence it is cotensored over the [[(∞,1)-category of spectra]];
using this structure, we produce a chain of [[natural equivalences]]
$$
  \pi_n^H(X) 
 \simeq \pi_0 \mathrm{Map}(\Sigma^\infty S^n, \mathrm{map}^G(G/H_+, X))
 \simeq \pi_0 \mathrm{Map}(\Sigma^\infty, S^n, X^H)
 \simeq \pi_n(X^H),
$$
where $X^H$ is the $H$-[[fixed point spectrum]] of $X$
(e.g. [Schwede 15, prop. 7.2](#Schwede15)).

### Via equivariant cohomology of the point
 {#ViaEquivariantCohomologyOfThePoint}

The identification via fixed point spectra in turn is the [[equivariant cohomology]] of the point, 

$$
  E^{-k}_G(\ast)
  \;\coloneqq\;
  \left[ \epsilon^\sharp \Sigma^k \mathbb{S} , E\right]_G
  \;\simeq\;
  \left[ \Sigma^k \mathbb{S}, F^G E \right]
  \;\simeq\;
  \pi_k(F^G E)
$$

due to the [[base change]] [[adjunction]]

$$
  G Spectra
    \underoverset
      { \underset{ F^G }{\longrightarrow} }
      {\overset{ \epsilon^\sharp }{\longleftarrow}}
      { \phantom{AA} \bot \phantom{AA} }
  Spectra
$$


### With $\mathrm{RO}(G)$-grading

If $V$ is a [[real number|real]] [[orthogonal]] $G$-[[representation]] and $H \subset G$ is a subgroup, then we define the functor $\pi^H_V(-):\mathcal{S}_{G,*} \rightarrow \mathrm{Set}$ by 
$$
  \pi^H_V(X) \coloneqq \pi_0 \mathrm{Map}^H_*(S^V,X);
$$
for fixed $V$ these are functorial in $H$, and the resulting structure is called a _$V$-Mackey functor_ by [Lewis](#Lewis92).

Similarly, if $\mathrm{RO}(G)$ denotes the [[real number|real]] [[orthogonal]] [[representation ring]] and $V \in \mathrm{RO}(G)$ is a [[real number|real]] [[orthogonal]] [[virtual representation]] of $G$, then we define the functor $\pi^H_V(-):\mathrm{Sp}_{G} \rightarrow \mathrm{Ab}$ by
$$
  \pi^H_V(X) \coloneqq \pi_0 \mathrm{Map}^H_*(\mathbb{S}^V,X).
$$
These together bear the structure of an $\mathrm{RO}(G)$-graded [[Mackey functor]], i.e. they take the form of a functor
$$
  \pi_{\star}^{\bullet}:\mathrm{Sp}_{G} \rightarrow \mathcal{M}_G(\mathrm{Ab})^{\mathrm{RO}(G)}.
$$
Often one fixes $H = G$, in which case one simply writes
$$
  \pi_{\star} \coloneqq \pi_{\star}^{G}:\mathrm{Sp}_G \rightarrow \mathrm{Ab}^{\mathrm{RO}(G)}.
$$

See more at [[C_2-equivariant homotopy groups of spheres]].

### Via genuine $G$-spectra

Consider [[genuine G-spectra]] modeled on a [[G-universe]] $U$.

For a _finite_ based [[G-CW complex]] $X$ and base [[topological G-space]] $Y$, write

$$
  \{X,Y\}_G = [\Sigma^\infty_G X, \Sigma^\infty_G Y] \coloneqq \underset{\longrightarrow}{\lim}_{V \subset U} [\Sigma^V X, \Sigma^V Y]_G
$$

for the [[colimit]] over $G$-[[homotopy classes]] of maps between [[suspensions]] $\Sigma^V X \coloneqq S^V \wedge X$, where $V$ runs through the indexing spaces in the universe and $S^V$ denotes its [[representation sphere]].

([May 96, IX.2 def. 2.1](#May96))

The equivariant stable homotopy groups of $X$ are

$$
  \pi_V^G(\Sigma^\infty_G X) \coloneqq \{S^V,X\}_G
  \,.
$$

([May 96, IX.2 remark 2.4](#May96))

And for subgroups $H \subset G$

$$
  \pi_V^H(\Sigma^\infty_G X) \coloneqq \{G/H_+ \wedge S^V,X\}_G
$$

([Greenlees-May 95, p. 11](#GreenleesMay95))


### Via orthogonal spectra and $G$-equivariant maps

Let $G$ be a [[finite group]]. For $X$ a $G$-[[equivariant spectrum]] modeled as an [[orthogonal spectrum]] with $G$-[[action]], then for $k \in \mathbb{N}$ the $k$th equivariant homotopy group of $X$ is the [[colimit]]

$$
  \pi_k^G(X)
  \coloneqq
  \underset{\longrightarrow_{\mathrlap{n}}}{\lim} [S^{n \rho_G}, (\Omega^k X)(n \rho_G)]_H
  \,,
$$

where

* $\rho_G$ denotes the [[fundamental representation]] of $G$

* $n \rho_G = (\rho_G)^{\oplus_n}$;

* $S^{n \rho_G}$ is its [[representation sphere]];

* $X(n \rho_G)$ is the value of $X$ in [[RO(G)-degree]] $n\rho_G$;

* $[-,-]_G$ is the set of [[homotopy classes]] of $G$-equivariant maps of pointed [[topological G-spaces]].

(e.g. [Schwede 15, section 3](#Schwede15))

More generally for $H \hookrightarrow G$ a [[subgroup]] then one writes $\pi_\bullet^H(X)$ for the $H$-equivariant subgroups of $X$ with $X$ regarded now as an $H$-[[equivariant spectrum]], via restriction of the action.

(e.g. [Schwede 15, p. 16](#Schwede15))






## Examples

### Of equivariant suspension spectra

For $X$ a [[pointed topological space|pointed]] [[topological G-space]], then by the discussion [there](equivariant+suspension+spectrum#ROGDegrees)) the formula for the equivariant homotopy groups of its [[equivariant suspension spectrum]] $\Sigma^\infty_G X$ reduces to

$$
  \pi_k^G(\Sigma^\infty_G X)
  \coloneqq
  \underset{\longrightarrow_n}{\lim} [S^{n \rho_g}, (\Omega^k X)\wedge S^{n \rho_G}]_G
$$

which in turn decomposes as a [[direct sum]] of ordinary [[homotopy groups]] of [[Weyl group]]-[[homotopy quotients]] of naive [[fixed point]] spaces -- see at _[[tom Dieck splitting]]_.

### Of the equivariant sphere spectrum

For the [[equivariant sphere spectrum]] $\mathbb{S} = \Sigma^\infty_G S^0$ the [[tom Dieck splitting]] gives that its 0th [[equivariant homotopy group]]
is the [[free abelian group]] on the set of [[conjugacy classes]] of [[subgroups]] of $G$:

$$
  \pi_0^G(\mathbb{S})
  \simeq
  \underset{[H \subset G]}{\oplus} \pi_0^{W_G H}(\Sigma_+^\infty E (W_G H))
  \simeq
  \mathbb{Z}[conjugacy\;classes\;of\;subgroups]
$$

(e.g. [Schwede 15, p. 64](#Schwede15))

In the case $G = C_2$, the [RO(G)](#ROG)-graded stable equivariant homotopy groups $\pi_{s,c}(\mathbb{S}) := \pi_{c + (s-c)\sigma}(\mathbb{S})$ of the sphere have been determined in the following ranges:

* stems $s \leq 25$ and coweights $-1 \leq c \leq 9$ ([Guillou-Isaksen 24](#Guillou24)); 

* $s \leq 7$ and coweights $-9 \leq c \leq -2$ ([Guillou-Isaksen 24](#Guillou24)).

## Properties

### Relation to Mackey functors

As $H$-varies over the [[subgroups]] of a $G$-[[equivariant spectrum]] $E$, the $H$-equivariant homotopy groups organize into a [[contravariant functor|contravariant]] [[additive functor]] from the [[full subcategory]] of the [[equivariant stable homotopy category]] (called a [[Mackey functor]])

$$
  \underline{\pi}_\bullet(E)
  \colon
  G/H \mapsto \pi^H_\bullet(X)
  \,.
$$

(e.g. [Schwede 15, p. 16 and section 4](#Schwede15))

(...)

### Equivariant Whitehead theorem

See at *[[equivariant Whitehead theorem]]*.



## Related concepts

* [[equivariant weak homotopy equivalence]]

* [[equivariant Whitehead theorem]]

* [[homotopy group]]

* [[stable homotopy group]]

## References

* {#Lewis92} [[Gaunce Lewis]], _The equivariant Hurewicz map_ (1992) ([TAMS](https://www.ams.org/journals/tran/1992-329-02/S0002-9947-1992-1049614-9/S0002-9947-1992-1049614-9.pdf))

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#May96} [[Peter May]], section IX.4 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comeza&#732;na, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))


* {#Schwede15} [[Stefan Schwede]], _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

* {#Guillous24} [[Bertrand Guillou]], [[Daniel Isaksen]], _$C_2$-Equivariant Stable Stems_m ([arXiv:2404.14627](https://arxiv.org/abs/2404.14627))


[[!redirects equivariant homotopy groups]]

[[!redirects equivariant stable homotopy group]]
[[!redirects equivariant stable homotopy groups]]


