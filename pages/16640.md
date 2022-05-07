+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents #
* table of contents 
{: toc}


## Idea 

The term *class equation* (or *class formula*, or *orbit decomposition* formula) refers to a basic type of counting argument that comes about by decomposing a [[finite set|finite]] [[G-set]] as a [[union]] of its [[orbits]]. This has a number of fundamental applications in [[group theory]]. 

## Statement 

Let $G$ be a [[group]] and let $A$ be a [[G-set]] (given by a [[homomorphism]] $G \to \hom_{Set}(A, A)$ of [[monoids]], with which is associated an [[action]] $\alpha: G \times A \to A$). Recall that $A$ is [[connected object|connected]] in the [[category of G-sets]] if $A$ is [[inhabited set|inhabited]] and the action is [[transitive action|transitive]]; in this case, choosing an [[element]] $a \in A$, there is a [[surjection]] of $G$-sets $G \to A$ sending $1 \mapsto a$, and this induces an [[isomorphism]] $G/Stab(a) \cong A$ where $Stab(a)$ is the [[stabilizer]] of $a$ and $G/Stab(a)$ is the $G$-set consisting of left [[cosets]] of $Stab(a)$. 

More generally, each $G$-set $A$ admits a canonical decomposition as a [[coproduct]] of its connected components; the components are usually called the [[orbits]] of the action. Choosing a representative element $a_x$ in each orbit $x$, this means we have an isomorphism of $G$-sets 

$$A \cong \sum_{orbits x} G/Stab(a_x).$$ 

By taking $G$ and $A$ to be [[finite set|finite]] and counting elements, we get an equation of the form 

$${|A|} = \sum_{orbits x} \frac{{|G|}}{{|Stab(a_x)|}}.$$ 

We call an instance of this equation a *class equation*. By judicious choice of groups $G$ and $G$-sets $A$, often in combination with [[number theory|number-theoretic]] arguments, one can derive many useful consequences; some sample applications are given below. 

Notice that reading the class equation equivalently as 

$$\sum_{orbits x} \frac{{1}}{{|Stab(a_x)|}} = \frac{|A|}{|G|} $$

it expresses the [[groupoid cardinality]] of the [[action groupoid]] of $G$ acting on $A$.

## Applications 

### Centers of $p$-groups 

Let $p$ be a [[prime number|prime]]; recall that a $p$-[[p-primary group|group]] is a [[finite group]] whose [[order of a group|order]] is a power of $p$. A basic structural result is the following. 

+-- {: .num_prop #pgroup} 
###### Proposition 
A non-trivial $p$-group $G$ has a nontrivial [[center]] $Z(G)$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $G$ act on itself by the [[conjugation action]] $G \times G \to G$, $(g, h) \mapsto g h g^{-1}$. In this case an orbit $Orb(h)$ is usually called the [[conjugacy class]] of $h$, and $Orb(h)$ is trivial (consists of exactly one element $h$) iff $h$ belongs to $Z(G)$. In any case ${|Orb(h)|} = \frac{{|G|}}{{|Stab(h)|}}$ divides ${|G|} = p^n$, and therefore $p$ divides ${|Orb(h)|}$ if $h$ is noncentral. In this case the class equation takes the form  

$${|G|} = {|Z(G)|} \; + \sum_{nontrivial\; orbits x} \frac{{|G|}}{{|Stab(a_x)|}}$$ 

and now since $p$ divides ${|G|}$ as well as each term in the sum over nontrivial orbits, it must also divide ${|Z(G)|}$. In particular, $Z(G)$ has more than one element. 
=-- 

It follows by [[induction]] that $p$-groups are [[solvable group|solvable]], since the center is a [[normal subgroup]] and the quotient $G/Z(G)$ is also a $p$-group.  Since a group obtained from an abelian group by repeated central extensions is nilpotent, $p$-groups are in fact [[nilpotent group|nilpotent]].

### Number of fixed points 

An elementary observation that is frequently useful is that the number of [[fixed points]] of an [[involution]] on a [[finite set]] $S$ has the same parity as $S$. This is a statement about $\mathbb{Z}/(2)$-sets; we generalize this to a statement about $G$-sets for general $p$-groups $G$. (Again, a fixed point of a $G$-set is an element whose orbit is a singleton.) 

+-- {: .num_prop #pparity} 
###### Proposition 
If $G$ is a $p$-group acting on a set $A$, then 

* ${|A|} \equiv {|Fix(A)|} \; mod p$. 

As special cases, if there is just one fixed point, then ${|A|} \equiv 1 \; mod p$, and if $p$ divides ${|A|}$, then $p$ divides ${|Fix(A)|}$. 
=-- 

+-- {: .proof} 
###### Proof 
The class equation takes the form 

$${|A|} = {|Fix(A)|} \; + \sum_{nontrivial\; orbits x} \frac{{|G|}}{{|Stab(a_x)|}}$$ 

where $p$ divides each summand over nontrivial orbits on the right, since $G$ is a $p$-group. Now reduce mod $p$. 
=-- 

### Wedderburn's theorem 

In the theory of finite [[projective planes]], an important result is that a projective plane is Pappian if it is Desarguesian. The purely algebraic version of this is Wedderburn's theorem: 

+-- {: .num_theorem} 
###### Theorem 
A finite [[division ring]] $D$ is commutative. 
=-- 

+-- {: .proof} 
###### Proof 
**(Witt)** 
The center of $D$ is a [[field]]; if $D$ is of characteristic $p \gt 0$, then the center $F$ has $q = p^f$ elements for some $f$. We may regard $D$ as an $F$-vector space of dimension $n$, whence the number of elements of its multiplicative group $D^\times$ is $q^n-1$. 

The conjugation action of $D^\times$ on itself yields a decomposition 

$$D^\times \cong F^\times \; + \sum_{nontrivial\; orbits x} \frac{{|D^\times|}}{{|Stab(a_x)|}}$$ 

where again the elements of the center $F^\times = Z(D^\times)$ correspond to the trivial orbits. The stabilizer of any $a_x$, together with $0$, forms a division ring (strictly) intermediate between $F$ and $D$; usually this is called the [[centralizer]] $C(a_x)$ of $a_x$. Putting $d_x = dim_F(C(a_x))$, the division ring $C(a_x)$ has $q^{d_x}$ elements, and notice $d_x$ divides $n$ because $n/d_x$ is just the dimension of $D$ seen as a vector space (module) over $C(a_x)$. Thus ${|Stab(a_x)|} = q^{d_x} - 1$, and we have a class equation 

$$q^n - 1 = q - 1 + \sum_x \frac{q^n - 1}{q^{d_x} - 1}.$$ 

Now let $\zeta \in \mathbb{C}$ be any primitive $n^{th}$ [[root of unity]]. Since $z - \zeta$ divides each polynomial $z^n-1$ and $\frac{z^n - 1}{z^{d_x} - 1}$, so does $\prod_{prim.\; \zeta} (z-\zeta)$. It follows that the algebraic integer $\prod_{prim.\; \zeta} (q - \zeta)$ divides each of the integers $q^n-1$ and $\frac{q^n - 1}{q^{d_x} - 1}$, and hence divides $q-1$ according to the class equation. But also ${|q - \zeta|} \geq {|q-1|}$ for any root of unity $\zeta$. Thus ${|q - \zeta|} = {|q-1|}$ and $n = 1$, i.e., $F = Z(D)$ is all of $D$ as was to be shown. 
=-- 

### Sylow theorems 

Let $G$ be a finite group of order $n$, and suppose that $p$ is a prime that divides $n$; say $n = p^f u$ where $p$ does not divide $u$. Recall that a [[Sylow p-subgroup]] is a $p$-subgroup of maximal order $p^f$. 

A fundamental fact of group theory is that Sylow $p$-subgroups exist and they are all conjugate to one another; also the number of Sylow $p$-subgroups is $\equiv 1 \; mod p$. 

Existence of Sylow $p$-subgroups can be proven by exploiting the same type of argument as in the proof of Proposition \ref{pgroup}: 

+-- {: .num_theorem #ppower} 
###### Theorem 
If $G$ has order $n$ and $p^k$ is a prime power dividing $n$, then there is a subgroup of $G$ of order $p^k$. 
=-- 

+-- {: .proof} 
###### Proof 
First we show that Sylow subgroups exist. We start by observing that if a group $H$ has a $p$-Sylow subgroup $P$, then so does any subgroup $G$. First note that if we let $G$ act on $H/P$ by left translation, then the stabilizer of any element $h P$ is $G \cap h P h^{-1}$, a $p$-group since $h P h^{-1}$ is. Then note that since $H/P$ has cardinality prime to $p$, so must one of its [[connected object|connected components]] $G/Stab(a_x)$ in its $G$-set decomposition 

$$H/P \cong \sum_{orbits\; x} G/Stab(a_x),$$ 

and this makes $Stab(a_x)$ a $p$-Sylow subgroup of $G$. 

Then, if $G$ is any group, and $n = ord(G)$, apply this observation to the embedding 

$$G \stackrel{Cayley}{\hookrightarrow} Perm({|G|}) \cong S_n \hookrightarrow GL_n(\mathbb{Z}/(p)) = H$$ 

where we embed the [[symmetric group]] $S_n$ via [[permutation matrices]] into the group $H$ of $n \times n$ invertible matrices over $\mathbb{Z}/(p)$. The group $H$ has order $(p^n - 1)(p^n - p)\ldots (p^n - p^{n-1})$, with maximal $p$-factor $p^{n(n-1)/2}$. It thus has a $p$-Sylow subgroup given by unitriangular matrices, i.e., upper-triangular matrices with all $1$\'s on the diagonal. Therefore $p$-Sylow subgroups $P$ exist for any $G$. 

Finally, note that by Proposition \ref{pgroup}, $P$ is solvable and therefore has a [[composition series]] 

$$\{1\} = P_0 \subset P_1 \subset \ldots \subset P$$ 

where each $P_k$ has order $p^k$. 
=-- 


+-- {: .num_theorem} 
###### Theorem 
If $H$ is a $p$-subgroup of $G$ and $P$ is a Sylow $p$-subgroup, then $g^{-1} H g \subseteq P$ for some $g \in G$. In particular, all Sylow $p$-subgroups are conjugate to one another. 
=-- 

+-- {: .proof} 
###### Proof 
$G$ acts on the set of cosets $G/P$ as usual by left translation, and we may restrict the action to the $p$-subgroup $H$. By maximality of $P$, we see ${|G/P|}$ is prime to $p$, and so by Proposition \ref{pparity}, ${|Fix_H(G/P)|}$ is also prime to $p$. In particular, $Fix_H(G/P)$ has at least one element, say $g P$. We infer that $h g P = g P$ for all $h \in H$, or that $g^{-1} h g P = P$ for all $h \in H$, and this implies that $g^{-1} H g \subseteq P$. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
The number of Sylow $p$-subgroups of $G$ is $\equiv 1 \; mod p$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $Y$ be the set of Sylow $p$-subgroups; $G$ acts on $Y$ by conjugation. As all Sylow $p$-subgroups are conjugate, there is just one orbit of the action, and the stabilizer of an element $P \in Y$ is just the [[normalizer]] $N_G(P)$ (by definition of normalizer). Thus $Y \cong G/N_G(P)$ as $G$-sets. 

Restrict the action to the subgroup $P$. Of course the element $P \in Y$ is a fixed point of this restricted action, and if $Q$ is any other fixed point, it means $x Q x^{-1} = Q$ for all $x \in P$, whence $P \subseteq N_G(Q)$. Now: $P, Q$ are both Sylow $p$-subgroups of $N_G(Q)$ and are therefore conjugate to each other (as seen within the group $N_G(Q)$). But $Q$ is already fixed by the conjugation action in its stabilizer $N_G(Q)$, so we conclude $P = Q$. We conclude $Fix_P(Y)$ has exactly one element. From ${|Y|} \equiv {|Fix_P(Y)|} \; mod p$, the theorem follows. 
=-- 

## Related concepts

* [[class function]]

* [[Klein geometry]]

[[!redirects class equations]]

[[!redirects class formula]]
[[!redirects class formulas]]
[[!redirects conjugation class formula]]
[[!redirects conjugation class formulas]] 
[[!redirects orbit decomposition formula]] 

[[!redirects Sylow theorem]]
[[!redirects Sylow theorems]]

[[!redirects Sylow's theorem]]
[[!redirects Sylow's theorems]]



