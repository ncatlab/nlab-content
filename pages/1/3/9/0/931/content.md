

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* [[principal bundle]] / **torsor**

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* **principal 3-bundle** / [[bundle 2-gerbe]]

* [[principal ∞-bundle]]

***



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A $G$-**torsor** for a [[group]] $G$ is an [[inhabited object]]/[[space]] $P$ with an [[action]] $\rho : G \times P \to P$ by $G$ that is

* free: only the identity element acts trivially;

and

* transitive: for every two points in (a fiber of) the space, there is an element of the group taking one to the other.

In other words, in the classical case where we are working in the category of sets:

a $G$-torsor (over the point; see below) is a $G$-set $P$ with action $\rho: G \times P \to P$ such that every choice of point $p \in P$ induces an isomorphism of $G$-sets

$$
  \rho(-,p) : G \stackrel{\simeq}{\to} P
  \,.
$$

This says equivalently that _after picking any point of $P$ as the identity_ , $P$ acquires a group structure isomorphic to $G$. But this is a non-canonical isomorphism: every choice of point of $P$ yields a different isomorphism.

As a **slogan** we can summarize this as: _A torsor is a group that has forgotten its neutral element._

Again, this applies to torsors "over the point" in $Set$. More generally, one may consider torsors over some base space $B$ (in other words, working in the [[topos]] of sheaves over $B$ instead of $Set$). In this case the term __torsor__ is more or less a synonym for the term [[principal bundle]], but torsors are generally applied in contexts much wider than the term "principal bundle" implies. Thus, while the terminology 'principal bundle' is usually used in the setting of [[topological spaces]], torsors are traditionally used in the setting of [[Grothendieck topology|Grothendieck topologies]] (faithfully flat and &#233;tale topology in particular), [[topos|topoi]] and for generalizations in various category-theoretic setups. While in the phrase '$G$-principal bundle' $G$ is usually a (topological) [[group]] or [[groupoid]], when we say '$G$-torsor', $G$ is usually a [[presheaf]] or [[sheaf]] of group(oid)s, or $G$ is a plain [[category]] (not necessarily even a groupoid).

A __$G$-torsor__, without any base space given, can also simply be an inhabited transitive free $G$-[[action|set]], which is the same as a principal $G$-bundle over the [[point]]. The notion may also be defined in any category with products: a torsor over a [[group object]] $G$ is a [[well-supported object]] $E$ together with a $G$-action $\alpha: G \times E \to E$ such that the arrow 

$$\langle \pi_1, \alpha \rangle: G \times E \to E \times E$$ 

is an isomorphism. 

To 'deconstruct' this a bit, in a simple case, we suppose given a base space $B$ over which everything is happening and a sheaf of groups $G$ on $B$.

## Definition

Let $G$ be a [[group]] object in some [[category]] $C$, that in the following is assumed, for simplicity, to be a [[cartesian closed category]].
The [[object]]s of $C$ we sometimes call [[space]]s.

Let $G$ be a [[group object]] in $C$. A left **$G$-torsor** is an [[inhabited object]] $P$ equipped with a $G$-action $\rho: G \times P \to P$ (subject to the usual laws for actions) such that the map 

$$\langle \rho, \pi_2 \rangle: G \times P \to P \times P$$ 

is an isomorphism. 

More generally, suppose $C$ is [[finitely complete category|finitely complete]], and let $B$ be an object. Then the [[slice category|slice]] $C/B$ is finitely complete, and the pullback functor $- \times B: C \to C/B$ preserves finite limits. Thus $\pi_2: G \times B  \to B$ acquires a group structure in $C/B$. A left **$G$-torsor over $B$** is by definition a 
$G$-torsor in $C/B$. Thus, if $B = 1$ is a point, a torsor over a point is the same as an ordinary torsor in $C$, but sometimes the additional "over a point" is convenient for the sake of emphasis. 

In more nuts-and-bolts terms, a left $G$-torsor over $B$ is a [[bundle]] $P\stackrel{\pi}{\to} B$ over $B$ together with a left group [[action]]

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

* **Remarks:** As we explain below under Properties, a torsor is in some tautological sense **locally trivial**, but some care must be taken in interpreting this. One sense is that there is a cover $U$ of $1$ (so that $U \to 1$ is epi, i.e., $U$ is inhabited) such that the torsor, when pulled back to $U$, becomes trivial (i.e., isomorphic to $G$ as $G$-torsor). But this is a very general notion of "cover". A more restrictive sense frequently encountered in the literature is that "cover" means a coproduct of subterminal objects $U_i \hookrightarrow 1$ such that $U = \sum_i U_i$ is inhabited (e.g., an open cover of a space $B$ seen as the terminal object of the sheaf topos $Sh(B)$), and "torsor" would then refer to the local triviality condition for some such $U$. This is the more usual sense when referring to principal bundles as torsors. Or, "cover" could refer to a covering sieve in a [[Grothendieck topology]]. 

(The condition on the action can be translated to give transitivity etc. in the case of $B$ is a point (left as a standard exercise).)

## Examples

* Let $C = $ [[Set]]. 

  An [[affine space]] of dimension $n$ over a [[field]] $k$ is a torsor for the additive group $k^n$: this acts by _translation_.

* Let $C = Top$ (objects are topological spaces, groups $G$ are topological groups). A principal $G$-bundle $\pi: P \to B$ is an example of a torsor over $B$ in $Top$. This becomes a definition of principal bundle if we demand local triviality with respect to some open cover of $B$ (see the remarks above). 

* Let $C = Sh(S)$ be a [[category of sheaves]]. 

  The canonical example for a torsor in $C$ is the [[trivial torsor]] over a [[sheaf]] of groups, $G$.

## Properties {#Properties}

Let $P$ be a $G$-torsor over the point in the category $C = Set$. Then as objects of $C$, $P$ is [[isomorphism|isomorphic]] to $G$: 

since $P$ is inhabited (here meaning non-empty), we may pick an point $p : * \to P$ of $P$. Write $\{p\} \to P$ for this morphism, for emphasis.  One sees that the diagram

$$
  \array{
  G \simeq G \times \{p\} &\stackrel{(Id, p)}{\to}& G \times P
  \\
  \downarrow^{\mathrlap{\rho(-,p)}} && \downarrow^{\mathrlap{\langle \rho, \pi_2}}
  \\
  P \times \{p\} &\stackrel{(Id,p)}{\to}& P \times P
  }
$$

is a [[pullback]] diagram. But since $\rho$ is by assumption an [[isomorphism]], and since pullbacks of isomorphisms are isomorphisms, also $\rho(-,p) : G \to P$ is an isomorphism. 

In other language, we say $P$ is **trivial** if it is isomorphic to $G$ as $G$-torsor, and a choice of isomorphism such as $\rho(-, p): G \to P$ is a **trivialization**. Notice that the composite 

$$P \times P \stackrel{\rho^{-1}}{\to} G \times P \stackrel{\pi_1}{\to} G$$ 

can be interpreted as "division" $d: P \times P \to G$, dividing one element of $P$ by another to get an element of $G$. If we further compose division with a choice of trivialization, 

$$P \times P \stackrel{d}{\to} G \stackrel{\rho(-, p)}{\to} P,$$ 

then we get a division structure $D$ on $P$ for which $p$ behaves as an identity (i.e., $D(x, x) = p$ for all $x \in P$), so that $P$ acquires a group structure isomorphic to that of $G$. 

In other categories $C$ besides $Set$, we cannot just "pick a point" of $P$ even if $P \to 1$ is epi, so this argument cannot be carried out, and indeed trivializations may not exist. However, it is possible to construct a local trivialization of a torsor, following a general philosophy from topos theory that a statement is "locally true" in a category $C$ if it becomes true when reinterpreted in a slice after pulling back $C \to C/U$, where $U$ is inhabited. (This in some sense is the basis of [[Kripke-Joyal semantics]].) 

In the present case, we may take $U = P$. Although we cannot "pick a point" of $P$ (= global section of $P \to 1$), we can pick a point of $P$ if we reinterpret it by pulling back to $C/P$. In other words, $\pi_2: P \times P \to 1 \times P \cong P$ does have a global section regarded as an arrow in $C/P$. In fact, there is a "generic point": the diagonal $\Delta: P \to P \times P$. Then, we may mimic the argument above, and consider the pullback diagram 

$$\array{
G \times P & \to & G \times P \times P \\
\downarrow & & \downarrow \mathrlap{\langle \rho, \pi_2 \rangle \times id} \\
P \times P & \underset{id \times \Delta}{\to} & P \times P \times P
}$$ 

living in $C/P$. As argued above, the vertical arrow on the left is an isomorphism; in fact, it is the isomorphism $\langle \rho, \pi_2 \rangle: G \times P \to P \times P$ we started with! 

Thus, a $G$-torsor in a category with products can be tautologically interpreted in terms of $G$-actions on objects $P$ which become trivialized upon pulling back to the slice $C/P$. 

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