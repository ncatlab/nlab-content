
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
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

An [[action]]

$$
  (-)\cdot(-) \;\colon\; G \times X \to X
$$

of a [[group]] $G$ on an [[inhabited set]] $X$ is called _regular_ if it is both [[transitive action|transitive]] and [[free action|free]].

In terms of [[elements]] this means that if for any pair of elements $x,y \in X$, there is _exactly one_ group element $g \in G$ such that $g \cdot x = y$.

More abstractly this means that the [[shear map]] 

$$
  \array{
    G \times X
    &
    \overset
      { (pr_2, \cdot) }
      {\longrightarrow}&
    X \times X
    \\
    (g, x) 
    &
    \mapsto
    & 
    \big( x, g \cdot x \big)
    \,.
  }
$$

is an [[isomorphism]].

In this case $X$ is also called a *$G$-[[torsor]]*. If the condition is dropped that $X$ be [[inhabited object|inhabited]] it is still called a *[[pseudo-torsor]]*.

## Properties

+-- {: .num_prop}
###### Proposition
Suppose $G$ acts transitively on $X$ by $* : G \times X \to X$, and suppose moreover that this action is [[faithful action|faithful]].  Then $G$ acts freely (and hence regularly) on $X$ if and only if the group $Aut_G(X)$ of $G$-equivariant automorphisms (i.e., [[bijections]] $\phi : X \to X$ commuting with the action of $G$) acts transitively (and hence regularly) on $X$.
=--

+-- {: .proof} 
###### Proof 

First we show that $Aut_G(X)$ acts freely on $X$. Suppose $\phi \in Aut_G(X)$ is such that $\phi(x) = x$ for some $x\in X$, and let $y\in X$ be arbitrary.  By the assumption that $G$ acts transitively, there is a $g \in G$ such that $y = g*x$. But then $G$-equivariance implies that
$$\phi(y) = \phi(g*x) = g*\phi(x) = g*x = y.$$
Since this holds for all $y\in Y$, $\phi$ must be equal to the identity $\phi = id_X$, and therefore $Aut_G(X)$ acts freely on $X$.

Next, suppose that $G$ also acts freely on $X$, and let $x,y \in X$ be arbitrary.  Then we can define a $G$-equivariant automorphism $\phi$ such that $\phi(x) = y$ by
$$\phi = z \mapsto g_z*y,$$
where for each $z$, $g_z$ is the unique group element such that $z = g_z*x$.  Conversely, suppose that $Aut_G(X)$ acts transitively on $X$, and let $x\in X$, $g\in G$ such that $g*x = x$.  By the assumption, for any $y \in X$, there exists $\phi \in Aut_G(X)$ such that $\phi(x) = y$, from which it follows that
$$g*y = g*\phi(x) = \phi(g*x) = \phi(x) = y.$$
Since $g*y = y$ for all $y \in X$, therefore $g = 1$ by the assumption that $G$ acts faithfully on $X$.

=--

## Examples

* The action of $G$ on itself by multiplication $\cdot : G \times G \to G$ (on the left or on the right) is a regular action, called the (left or right) [[regular representation]] of $G$.

* If one views a [[combinatorial map]] $M$ as the transitive action of a certain group of permutations, then $M$ represents a _regular map_ ([Siran 2006](#SiranSurvey)) just in case this action is regular.  For example, the five [[Platonic solids]] may be represented as regular combinatorial maps.

##In homotopy type theory
 {#InHomotopyTypeTheory}

We discuss regular actions via [[homotopy type theory]].

Since doing group [representation theory in homotopy type theory](representation+theory#InHomotopyTypeTheory) corresponds to working in the [[context]] of a [[delooped group]] in [[homotopy type theory]], the regularity of an action is naturally expressed there. Transitivity ensures that all the points in the [[homotopy quotient]] are connected by equivalences, while freeness means that the space of equivalences between two points is itself [[contractible space|contractible]]. Hence if $\ast \colon \mathbf{B} G \vdash X(\ast): Type$ corresponds to a regular action, then the quotient $\sum_{\ast: \mathbf{B} G} X(\ast)$ is contractible.

Restriction to 1-groups is unnecessary here, and we say

+-- {: .num_defn #RegularInfinityAction}
###### Definition

An [[∞-action]] of an [[∞-group]] is a **regular $\infty$-action** if its [[homotopy quotient]] is [[contractible type|contractible]].

=--


For any $G$-action ([[∞-action]]) $X \colon BG \to U$, its [[automorphism group]] is (see at [automorphism ∞-group in HoTT](automorphism+infinity-group#InHomotopyTypeTheory))

$$
  B Aut_G(X) \coloneqq \sum_{(P:BG \to U)} \|P=X\|
$$

and 

$$
   \tilde{X} \colon B Aut_G(X) \to U
$$ 

by $\tilde{X}(P,-) \coloneqq P(\ast)$.

+-- {: .num_prop}
###### Proposition

If $X$ is regular, then $\tilde{X}$ is regular.

=--

+-- {: .proof} 
###### Proof

First, we need to argue that $X(\ast)$ is [[mere proposition|merely]] [[inhabited type|inhabited]]. Since $X$ is regular, we have $\sum_{(b:BG)} X(b)$ [[contractible type|contractible]]. This gives a center of contraction $(b,x)$. Now, since $B G$ is connected, it follows that $\|b=\ast\|$. Since we are proving the [[mere proposition]] $\|X(\ast)\|$, we get to use $b=\ast$. Now we obtain $\|X(\ast)\|$. 

Next, to show that $\tilde{X}$ is regular we need to show that $\tilde{X}$ has a contractible total space. The [[dependent sum]] type $\sum_{(b : BAut_G(X))} \tilde{X}(b)$ is equivalent to $\sum_{(P:BG \to U)} \|P=X\| \times P(\ast)$. Contractibility is a [[mere proposition]], and we have $\|X(\ast)\|$, so we get to use a point $x:X(\ast)$. This gives us a center of contraction $(X,refl,x)$ of the total space of $\tilde{X}$. 

Now let $P : BG \to U$, let $ \| P = X \|$, let $p_0 : P(\ast)$. To show regularity, it suffices to find a [[term]] of type

$$
  \sum_{\alpha : P = X} \mathrm{trans}(\alpha)(p_0) = x
  \,.
$$

This type is equivalent to showing that there are

$$
  K : \prod_{b:BG} P(b) \simeq X(b)
  \;\;\;\;
  \text{and}
  \;\;\;\;\;
  K(*,p_0) = x_0
  \,.
$$

Now we use that $X(b)$ is equivalent to $b=\ast$ (we get this fact from regularity, together with a point $x:X(\ast)$). 
Since we need this particular fiberwise [[equivalence in homotopy type theory|equivalence]], it suffices to show that

$\sum_{b:BG} P(b)$

is [[contractible type|contractible]]. Now this is a [[mere proposition]], so we can eliminate $t : \| P = X \|$ to obtain the proof.

=--

+-- {: .num_prop}
###### Proposition

If $X$ is a principal homogeneous space on $G$, in the sense that the type $\sum_{(g:G)} g_\ast(x)=y$ is contractible for all $x,y:X(\ast)$, and $\tilde{X}$ is regular, then $X$ is regular.

=--

+-- {: .proof}
###### Proof

Again, we first show that $X(\ast)$ is [[mere proposition|merely]] [[inhabited type|inhabited]]. The total space of $\tilde{X}$ has center of contraction $(P,p_0)$. Since $\|P=X\|$ and since we are proving a [[mere proposition]], we get to use $P=X$. Now $\|X(\ast)\|$ follows from $p_0:P(\ast)$. The regularity of $X$ is a mere proposition, so we get to use $x_0:X(\ast)$. This gives us the center of contraction $(\ast,x_0)$. It remains to show that

$\prod_{(b:BG)} \prod_{(x:X(b))} \sum_{(\alpha : b=\ast)} \mathrm{trans}(\alpha,x) = x_0$.

Of course, it would suffice to prove the stronger statement

$\prod_{(b:BG)} \prod_{(x:X(b))} \mathrm{isContr} (\sum_{(\alpha : b=\ast)} \mathrm{trans}(\alpha,x) = x_0)$.

However, now we get to use that $BG$ is connected. Therefore it suffices to show that

$\prod_{x:X(*)} isContr (\sum_{\alpha : G} \mathrm{trans}(\alpha,x) = x_0)$

This holds by assumption.
=--

## Related concepts

* [[transitive action]], [[free action]], [[semi-free action]], [[regular action]],

* [[proper action]], [[properly discontinuous action]]

* [[torsor]]

## References

* {#SiranSurvey} Jozef Siran, "Regular Maps on a Given Surface: A Survey", _Topics in Discrete Mathematics_, 2006. ([pdf](http://dfgm.math.msu.su/files/papers-sym/regular%20maps%20on%20a%20given%20surface.pdf))

* Group Properties Wiki: [Regular group action](http://groupprops.subwiki.org/wiki/Regular_group_action).

[[!redirects regular actions]]
[[!redirects regular group action]]
[[!redirects regular group actions]]

[[!redirects regular infinity-action]]
[[!redirects regular ∞-action]]
[[!redirects regular infinity-actions]]
[[!redirects regular ∞-actions]]
