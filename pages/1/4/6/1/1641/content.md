## Warning

The term 'topological category' is traditional, and comes from the frequent examples in [[topology]].  It does *not* mean an [[internal category]] in [[Top]]!


## Idea

A _topological category_ is a [[concrete category]] with nice features matching the ability to form 'weak' and 'strong' topologies in [[Top]].


## Definition

Most generally, the definition relates to a [[functor]] $U: C \to D$ (such as the [[forgetful functor]] from $Top$ to [[Set]]), but we think of this as giving $C$ as a [[bundle]] over $D$.  Let a _space_ be an object of $C$, an _algebra_ be an object of $D$, a _map_ be a morphism in $C$, and a _homomorphism_ be a morphism in $D$.  (The reason is that, typically, $C$ will be a category of spaces with some kind of topological structure while $D$ will be, if not $Set$, then some kind of algebraic category.)

Then $C$ is a __topological category__ over $D$ if, given any algebra $X$ and any (small) family of spaces $S_i$ and homomorphisms $f_i: X \to U(S_i)$, there exist
*  a space $T$, an [[isomorphism]] $g: U(T) \to X$, and maps $m_i: T \to S_i$ such that each [[composite]] $g ; f_i$ equals $U(m_i)$ and,
*  given any space $T'$, homomorphism $g': U(T') \to X$, and maps $m'_i: T' \to S_i$, if each composite $g' ; f_i$ equals $U(m'_i)$, then there exists
   *  a map $n: T' \to T$ such that $U(n) ; g = g'$ and
   *  given any map $n': T' \to T$, if $U(n') ; g = g'$, then $n = n'$.

Here are some illustrative commutative diagrams (if you can read them):
$$ \array {
T' \\
n \downarrow \downarrow n' & \searrow^{m'_i} \\
T                          & \underset{m_i}\rightarrow & S_i
} \;\;\; \stackrel{U}\mapsto \;\;\; \array {
U(T') \\
U(n) \downarrow \downarrow U(n') & \searrow^{g'}           &                                  & \searrow^{U(m'_i)} \\
U(T)                             & \underset{g}\rightarrow & X                                & \underset{f_i}\rightarrow & U(S_i) \\
                                 &                         & \underset{U(m_i)}\longrightarrow
} $$


Here are some immediate consequences:
*  One may assume that $U(T) = X$ and that $g$ is the [[identity morphism]].
*  The forgetful functor $U: C \to D$ must be [[faithful functor|faithful]].

(Let me check this ...)