
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Normal subgroups

A [[subgroup]] $N$ of a [[group]] $G$ is **normal** if the [[conjugation action|conjugation]] $n\mapsto g^{-1}n g$ by any element $g\in G$ leaves $N$ [[invariant]], i.e. $g^{-1}N g \coloneqq \{g^{-1}n g\,|\,n\in N\} = N$.

A subgroup $N$ is normal iff the [[partition]] of the group into left *[[cosets]]* of the subgroup $N$, that is the sets $g N = \{ g n\,|\,n\in N\}$, is *stable* in the sense that the left coset $g_1 g_2 N$ of the product $g_1 g_2$ of any two elements $g_1,g_2\in G$ depends only on the coset $g_1 N$, $g_2 N$. Thus there is well defined product on the set of cosets making the set of left cosets $N\backslash G$ a group. By $g N = g N g^{-1}g = N g$ the set of left cosets and the set of right cosets of a normal subgroup coincide; thus the induced group structure on the right coset set $G/N$ is the same and called the [[quotient group]] (see [[quotient object]]). 

Thus normal subgroups may also be defined as [[kernels]] $f^{-1}(e)$ of group homomorphisms $G \to H$ ($e \in H$ is the identity), and this is largely the point of normal subgroups: they are equivalent to [[congruence relations]] in the category of groups. 


### Normal subobject in a semiabelian category

A normal subgroup is a [[normal subobject]] of a group in the [[Grp|category of groups]]: the more general notion of 'normal subobject' makes sense in [[semiabelian category|semiabelian categories]] and some other setups. If we consider a group as a special case of an $\Omega$-[[Omega-group|group]], then a normal subgroup corresponds to an [[ideal of an Omega-group|ideal]]. 

### Normal morphisms of $\infty$-groups
 {#NormalMorphismOfInfinityGroups}

The notion of normal subgroups generalizes from groups to [[∞-groups]].

We may take as the characteristic propery of normal subgroup inclusions $K \hookrightarrow G$ that the [[quotient]] $G/K$ inherits a group structure. This quotient may be identified with the [[homotopy fiber]] of the induced morphism of [[delooping]] [[groupoids]] $\mathbf{B}K \to \mathbf{B}G$ (see example \ref{CrossedModulesAreHomotopyNormalGroupMaps} below). The following definition takes this as the defining property of "normality" of morphisms.


+-- {: .num_defn}
###### Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] of [[homotopy dimension]] 0 (for instance a [[cohesive (∞,1)-topos]]) and let $K,G$ be [[∞-group]] objects in $\mathbf{H}$.

A [[morphism]] $f : K \to G$ of [[∞-groups]] in $\mathbf{H}$ is **normal** if its [[delooping]] is the [[homotopy fiber]] of a morphism to a [[0-connected]] object, hence if it fits into a [[fiber sequence]] of the form

$$
  \mathbf{B}K \stackrel{\mathbf{B}f}{\to} \mathbf{B}G \to \mathbf{B}(G\sslash K)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Here the object on the right is any [[0-connected]] [[∞-groupoid]]. By the assumption of [[homotopy dimension]] 0 and by the discussion at [[looping and delooping]] this is necessarily the [[delooping]] of some [[∞-group]], to be denoted $G\sslash K$. By the discussion at [[fiber sequence]] it follows that $G\sslash K \simeq \Omega \mathbf{B}(G \sslash K)$ is the [[homotopy fiber]] of $\mathbf{B}f$, hence that we have a long fiber sequence

$$
 G\sslash K \to \mathbf{B}K \stackrel{\mathbf{B}f}{\to}\mathbf{B}G \to \mathbf{B}(G\sslash K)
  \,.
$$

Therefore equivalently this says that $f : K \to G$ is normal precisely if $\mathbf{B}f : \mathbf{B}K \to \mathbf{B}G$ is a [[principal ∞-bundle]]. The above fiber sequence says that this principal $\infty$-bundle has typical [[fiber]] $G\sslash K$ and is classified by the [[cocycle]] $\mathbf{B}G \to \mathbf{B}(G\sslash K)$.

=--


For the case $\mathbf{H} = $ [[∞Grpd]] -- hence for [[discrete ∞-groups]] -- and with [[∞Grpd]] [[presentable (∞,1)-category|presented]] by the standard [[model structure on topological spaces]], this notion is discussed in ([Prezma](#Prezma)). The further special where $f$ is a morphism of [[discrete group|discrete 1-groups]], such that $G\sslash K$ is a [[2-group]] (example \ref{CrossedModulesAreHomotopyNormalGroupMaps} below) is discussed in ([Farjoun-Segev](#FarjounSegev)).


+-- {: .num_remark}
###### Remark

Such a normal morphism equivalently exhibits an [[∞-group extension]] $G$ of $G \sslash K$ by $K$. See there for more details.

=--

+-- {: .num_remark}
###### Remark

Every ordinary normal subgroup inclusion $K \hookrightarrow G$ is also a normal morphism of ∞-groups, but there are more morphisms of 1-groups that are normal as morphisms of $\infty$-groups. See example \ref{CrossedModulesAreHomotopyNormalGroupMaps} below.

=--

## Properties 

* The lattice of normal subgroups of a group $G$ is a [[modular lattice]], because the category of groups is a [[Mal'cev category]] and, as mentioned earlier, normal subgroups are tantamount to congruence relations. (N.B.: it need not be true that the lattice of subgroups is modular: take for example the lattice of subgroups of the [[dihedral group]] of order $8$, which contains a forbidden pentagon.) 

### Recognition of homotopy-normal maps
 {#Recognition}

A recognition principle for normality of morphisms of [[∞-groups]] is ([Prezma, theorem 6.2](#Prezma)).

## Examples

### Normal sub-1-groups

+-- {: .num_example}
###### Example

Every [[subgroup]] of an [[abelian group]] is normal, trivially.  

=--

+-- {: .num_example}
###### Example

For $G$ a group equipped with an [[action]] on another group $N$ by group [[automorphisms]] $\rho : G \to Aut(N)$, the canonical inclusion 

$$
  N \hookrightarrow G \ltimes N
$$

exhibits $N$ as a normal subgroup of the [[semidirect product group]] $G \ltimes N$.

=--


+-- {: .num_prop #inverse} 
###### Proposition 
If $N$ is a normal subgroup of $H$ and $\phi: G \to H$ is a group homomorphism, then the [[inverse image]] $\phi^{-1}(N)$ is normal in $G$ and $\phi$ induces a group homomorphism $G/f^{-1}(N) \to H/N$. 
=-- 

The proof is entirely straightforward and will be omitted. 

### Normal sub-2-groups

+-- {: .num_example #CrossedModulesAreHomotopyNormalGroupMaps}
###### Example

Let $f : K \to G$ be a morphism of [[discrete groups]] (not necessarily a [[monomorphism]]) regarded as a morphisms of [[0-truncated]] [[discrete ∞-groups]]. Then the [[homotopy fiber]] of its [[delooping]] is the [[action groupoid]] 

$$
  G\sslash K = 
  \left(
    G \times K
    \stackrel{\overset{(-)\cdot f(-)}{\to}}{\underset{p_1}
   {\to}}
    G
  \right)
  \,.
$$ 


(This follows for instance by computing the [[homotopy pullback]] via the [[factorization lemma]].)

Since $G\sslash K$ is a [[homotopy type|1-type]], this being an [[∞-group]] means that it is a [[2-group]], hence (see the discussion there) that $f : K \to G$ makes a [[crossed module]] of groups. 

So [normal morphisms](#NormalMorphismOfInfinityGroups) of [[0-truncated]] [[discrete ∞-groups]] are equivalently morphisms underlying [[crossed modules]] of [[discrete groups]].

=--

This observation apparently goes back to [[Whitehead]].


## References

Normal morphisms of [[discrete ∞-groups]] are discussed in 

* [[Matan Prezma]], _Homotopy Normal Maps_ (2010) ([arXiv:1011.4708](http://arxiv.org/abs/1011.4708))
 {#Prezma}

The special case of this for morphisms of 1-groups is discussed in 

* E. D. Farjoun and Y. Segev, _Crossed modules as homotopy normal maps_, Topology and its applications 157 pp. 359&#8211;368 (2010).
 {#FarjounSegev}

[[!redirects normal subgroups]]

[[!redirects normal morphism of ∞-groups]]
[[!redirects normal morphism of infinity-groups]]

[[!redirects normal morphisms of ∞-groups]]
[[!redirects normal morphisms of infinity-groups]]

[[!redirects normal sub Lie algebra]]
[[!redirects normal sub Lie algebras]]
