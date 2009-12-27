

A __torsor__ is almost a synonym for a [[principal bundle]], but is usually used in slightly different contexts than that term. While the terminology 'principal bundle' is usually used in the setting of [[topological spaces]], torsors are traditionally used in the setting of [[Grothendieck topology|Grothendieck topologies]] (faithfully flat and &#233;tale topology in particular), [[topos|topoi]] and for generalizations in various category-theoretic setups. While in the phrase '$G$-principal bundle' $G$ is usually a [[group]] or [[groupoid]], when we say '$G$-torsor', $G$ is usually a [[presheaf]] or [[sheaf]] of group(oid)s, or $G$ is a plain [[category]] (not a groupoid).

A __$G$-torsor__, without any base space given, can also simply be an inhabited transitive free $G$-[[action|set]], which is the same as a principal $G$-bundle over the [[point]]. The notion may also be defined in any category with products: a torsor over a [[group object]] $G$ is a [[well-supported object]] $E$ together with a $G$-action $\alpha: G \times E \to E$ such that the arrow 

$$\langle \pi_1, \alpha \rangle: G \times E \to E \times E$$ 

is an isomorphism. 

See also [[torsor with structure category]].

##Deconstruction##
To 'deconstruct' this a bit, in a simple case, we suppose given a base space $B$ over which everything is happening and a sheaf of groups $G$ on $B$.

##Definition##

  A left **$G$-torsor** on $B$ is a space $P\stackrel{\pi}{\to} B$ over $B$ together with a left group action

$$G\times_B P \to P$$

$$(g,p)\to g.p$$

such that the induced morphism

$$\phi : G\times_B P \to P\times_B P$$

$$(g,p)\to (g.p,p)$$ 

is an isomorphism.  In addition we require that there exists a family of local sections, $s_i : U_i \to P$, for some open cover $\mathcal{U} = (U_i)_{i\in I}$ of $B$. 

(The condition on the action can be translated to give transitivity etc. in the case of $B$ is a point (left as a standard exercise).)

## Example## 
The canonical example is the [[trivial torsor]] over a [[sheaf]] of groups, $G$.

## References ##

For elementary examples of torsors, see:

* John Baez, Torsors made easy.  ([web](http://math.ucr.edu/home/baez/torsors.html))

[[!redirects torsors]]