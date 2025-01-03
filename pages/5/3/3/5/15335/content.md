\tableofcontents

## Definition

Let $SemiLat$ be the category of meet-[[semilattices]] (i.e., [[posets]] admitting finite meets); equivalently, the category of idempotent commutative monoids. Regarding [[Sierpinski space]] $\mathbf{2} = \{0 \leq 1\}$ ambimorphically either as a [[topological space]] or as a meet-semilattice, i.e., an internal idempotent commutative monoid in $Top$ seen as a [[dualizing object]], there is a pair of [[adjoint functors]] given by homming into $\mathbf{2}$, 

$$Top \stackrel{Top(-, \mathbf{2})^{op}}{\to} SemiLat^{op} \;\; \dashv \;\; SemiLat^{op} \stackrel{SemiLat(-, \mathbf{2})}{\to} Top.$$ 

In more detail: for a space $X$, the set of continuous maps $X \to \mathbf{2}$ is naturally identified with the set of open subsets, i.e., the topology $\mathcal{O}(X)$ (where the pointwise meet-semilattice structure on $\hom(X, \mathbf{2})$ coincides with the meets defined by intersection on $\mathcal{O}(X)$). For a meet-semilattice $L$, the set $SemiLat(L, \mathbf{2})$ is topologized as a subspace of the product space $\mathbf{2}^{{|L|}}$, a product of ${|L|}$ copies of Sierpinski space. The adjunction says that there is a natural bijection 

$$\frac{L \to Top(X, \mathbf{2})}{X \to SemiLat(L, \mathbf{2})}$$ 

between semilattice maps above and continuous maps below. 

The **filter monad** is the monad $Filt$ on $Top$ induced by this adjunction. (Compare [[ultrafilter monad]].) 

For a space $X$, $Filt(X)$ is the set of meet-preserving maps $\mathcal{O}(X) \to \mathbf{2}$. This is in natural bijection with subsets of $\mathcal{O}(X)$ that are upward-closed and closed under finite intersections, i.e., [[filters]] in $\mathcal{O}(X)$. The unit of the monad evaluated at $X$ is $u_X: X \to Filt(X)$, taking $x \in X$ to the filter $u_X(x)$ of open sets containing $x$. 

We can read off the multiplication $m$ on the filter monad directly from this description. For $\Phi \in Filt(Filt(X))$, we have 

$$\mu_X(\Phi) \coloneqq \{U:\mathcal{O}(X)\; |\; \{F: Filt(X)\; |\; U \in F\} \in \Phi\}.$$ 

However, there is another description often encountered in the literature: 

$$\mu_X(\Phi) = \bigcup \{\bigcap \mathcal{U}: \mathcal{U} \in \Phi\}.$$ 

+-- {: .proof} 
###### Proof 
To see $\bigcup \{\bigcap \mathcal{U}: \mathcal{U} \in \Phi\} \subseteq \mu_X(\Phi)$, suppose $U \in \bigcup \{\bigcap \mathcal{U}: \mathcal{U} \in \Phi\}$, i.e., suppose there is $\mathcal{U}$ with $\mathcal{U} \in \Phi$ and $U \in \bigcap \mathcal{U}$. Then $U \in F$ for all $F \in \mathcal{U}$, and since 
already $\mathcal{U} \in \Phi$, we see $\{F \in Filt(X): U \in F\} \in \Phi$ by upward closure of $\Phi$. Hence $U \in \mu_X(\Phi)$. 

To see $\mu_X(\Phi) \subseteq \bigcup \{\bigcap \mathcal{U}: \mathcal{U} \in \Phi\}$, suppose $U \in \mu_X(\Phi)$, and then put $\mathcal{U}' = \{F: Filt(X)\; |\; U \in F\}$. Then $\mathcal{U}' \in \Phi$, and $U \in \bigcap \mathcal{U}'$ by definition, so $U \in \bigcup \{\bigcap \mathcal{U}: \mathcal{U} \in \Phi\}$. 
=-- 

## Related concepts

* [[filter]]
