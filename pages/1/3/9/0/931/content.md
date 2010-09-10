
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **torsor** over a [[group]] is an [[object]]/[[space]] $P$ with an [[action]] $\rho : G \times P \to P$ by $G$ that is

* free: only the identity element acts trivially;

and

* transitive: for every two points in (a fiber of) the space, there is an element of the group taking one to the other.

Or in other words:

a $G$-torsor (over the point) is an object $P$ [[isomorphism|isomorphic]] to $G$ such that every choice of point $p \in P$ induces an isomorphism

$$
  \rho(-,p) : G \stackrel{\simeq}{\to} P
  \,.
$$

This says equivalently that _after picking any point of $P$ as the identity_ , $P$ becomes isomorphic to $G$. But this is a non-canonical isomorphism: every choice of point of $P$ yields a different isomorphism.

As a **slogan** we can summarize this as: _A torsor is a group that has forgotten its neutral element._

This applies to torsors "over the point". More generally one considers torsors parameterized over some base space. In this sesne the term __torsor__ is essentially a synonym for the term [[principal bundle]], but is usually used in slightly different contexts than that term. While the terminology 'principal bundle' is usually used in the setting of [[topological spaces]], torsors are traditionally used in the setting of [[Grothendieck topology|Grothendieck topologies]] (faithfully flat and &#233;tale topology in particular), [[topos|topoi]] and for generalizations in various category-theoretic setups. While in the phrase '$G$-principal bundle' $G$ is usually a (topological) [[group]] or [[groupoid]], when we say '$G$-torsor', $G$ is usually a [[presheaf]] or [[sheaf]] of group(oid)s, or $G$ is a plain [[category]] (not necessarily even a groupoid).

A __$G$-torsor__, without any base space given, can also simply be an inhabited transitive free $G$-[[action|set]], which is the same as a principal $G$-bundle over the [[point]]. The notion may also be defined in any category with products: a torsor over a [[group object]] $G$ is a [[well-supported object]] $E$ together with a $G$-action $\alpha: G \times E \to E$ such that the arrow 

$$\langle \pi_1, \alpha \rangle: G \times E \to E \times E$$ 

is an isomorphism. 

To 'deconstruct' this a bit, in a simple case, we suppose given a base space $B$ over which everything is happening and a sheaf of groups $G$ on $B$.

## Definition

Let $G$ be a [[group]] object in some [[category]] $C$, that in the following is assumed, for simplicity, to be a [[cartesian closed category]].

The [[object]]s of $C$ we call [[space]]s.

A left **$G$-torsor** on $B$ is a [[bundle]] $P\stackrel{\pi}{\to} B$ over $B$ together with a left group [[action]]

$$
  \rho : G\times_B P \to P
$$

which in terms of [[generalized element]]s we write

$$
  (g,p)\to g.p
$$

such that the induced morphism of [[product]]s

$$
  \phi := (\rho, p_2) : G\times_B P \to P\times_B P
$$

which on elements acts as

$$
  (g,p)\to (g.p,p)
$$ 

is an [[isomorphism]].  


If the torsor is required to be **locally trivial**, then 
in addition we require that there exists a family of local sections, $s_i : U_i \to P$, for some [[cover]] $\mathcal{U} = (U_i)_{i\in I}$ of $B$. 

(The condition on the action can be translated to give transitivity etc. in the case of $B$ is a point (left as a standard exercise).)

## Properties {#Properties}

Let $P$ be a $G$-torsor over the point. Then as objects of $C$, $P$ is [[isomorphism|isomorphic]] to $G$: 

pick any point $p : * \to P$ of $P$. We shall write $\{p\} \to P$ for this morphism, for emphasis.  One sees that the diagram

$$
  \array{
  G \simeq G \times \{p\} &\stackrel{(Id, p)}{\to}& G \times P
  \\
  \downarrow^{\mathrlap{\rho(-,p)}} && \downarrow^{\mathrlap{\rho}}
  \\
  P \times \{p\} &\stackrel{(Id,p)}{\to}& P \times P
  }
$$

is a [[pullback]] diagram. But since $\rho$ is by assumption an [[isomorphism]], and since pullbacks of isomorphisms are isomorphisms, also $\rho(-,p) : G \to P$ is an isomorphism.



## Example

* Let $C = $ [[Set]]. 

  An [[affine space]] of dimension $n$ over a [[field]] $k$ is a torsor for the additive group $k^n$: this acts by _translation_ .


* Let $C = Sh(S)$ be a [[category of sheaves]]. 

  The canonical example for a torsor in $C$ is the [[trivial torsor]] over a [[sheaf]] of groups, $G$.


## References 

See also [[torsor with structure category]]. In [[noncommutative algebraic geometry]], faithfully flat [[Hopf-Galois extension]]s are considered a generalization of (affine) torsors in algebraic geometry.

For elementary examples of torsors, see:

* [[John Baez]], Torsors made easy.  ([web](http://math.ucr.edu/home/baez/torsors.html))


Some categorically-oriented articles discussing torsors are

* Tomasz Brzezi&#324;ski, On synthetic interpretation of quantum principal bundles, [arXiv:0912.0213](http://arxiv.org/abs/0912.0213)

* D. H. Van Osdol, Principal homogeneous objects as representable functors.
Cahiers Topologie G&#233;om. Diff&#233;rentielle 18 (1977), no. 3, 271--289, [numdam](http://www.numdam.org/item?id=CTGDC_1977__18_3_271_0).

*  K. T. S. Mohapeloa, A $2$-colimit characterization of internal categories of torsors. J. Pure Appl. Algebra 71 (1991), no. 1, 75--91, [doi](http://dx.doi.org/10.1016/0022-4049%2891%2990041-Y). 

* Thomas Booker, Ross Street, Torsors, herds and flocks, [arXiv:0912.4551](http://arxiv.org/abs/0912.4551)

* J. Duskin,  Simplicial mehtods and the interpretation of &#171;triple&#187; cohomology, Memoirs AMS __3__, issue 2, n&#176; 163, 1975.  MR393196

* A. Vistoli, Grothendieck topologies, fibered categories and descent theory. Fundamental algebraic geometry, 1--104, Math. Surveys Monogr., 123, AMS 2005, [math.AG/0412512](http://front.math.ucdavis.edu/0412.5512).

* [[Ieke Moerdijk]], Introduction to the language of stacks and gerbes, [math.AT/0212266](http://arxiv.org/abs/math/0212266).

A standard elementary discussion of torsors in algebraic geometry is in J. Milne's book *Etale cohomology*. Much material is also in Giraud's book on nonabelian cohomology. 


[[!redirects torsors]]