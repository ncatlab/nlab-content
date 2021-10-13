
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context###
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A connected object is a generalisation of the concept of [[connected space]] from [[Top]] to an arbitrary [[extensive category]]. 


## Definitions

Let $C$ be an [[extensive category]], then:

+-- {: .num_defn #ConnectedObject}
###### Definition

An [[object]] $X$ of $C$ is **connected** if the [[representable functor]] 

$$ hom(X, -) \colon C \to Set $$

[[preserved limit|preserves]] all [[coproducts]]. 

=--

+-- {: .num_remark}
###### Remark

By definition, $hom(X,-)$ preserves binary coproducts if the canonically defined morphism $hom(X,Y) + hom(X,Z) \to hom(X,Y + Z)$
is always a [[bijection]].

=--

+-- {: .num_remark}
###### Remark

By this definition, the [[initial object]] of $C$ is *not* in general connected (except for degenerate cases of $C$); it is [[too simple to be simple]].  This matches the notion that the [[empty space]] should not be considered connected, discussed at [[connected space]].

=--

+-- {: .num_remark}
###### Remark

If $C$ is a [[infinitary extensive category]] then for $X \in Ob(C)$ to be connected it is enough to require that $hom(X,-)$ preserves *binary* coproducts. This is theorem \ref{RespectForBinaryCoproductsIsSufficient} below.

=--

## Properties

### Characterization in terms of coproducts

Let $C$ be an infinitary [[extensive category]], then


\begin{prop}
\label{RespectForBinaryCoproductsIsSufficient}
 An [[object]] $X$ of $C$ is connected, def. \ref{ConnectedObject}, if and only if the [[hom-functor]] $\hom(X, -) \colon C \to Set$ [[preserved limit|preserves]] binary [[coproducts]]. 
\end{prop}

\begin{proof}
The "only if" is clear, so we just prove the "if". 

We first show that $\hom(X, -)$ preserves the [[initial object]] $0$. Indeed, if $\hom(X, -)$ preserves the binary product $X + 0 = X$, then the canonical map 

$$\hom(X, X) + \hom(X, 0) \to \hom(X, X)$$ 

is a bijection of sets, where the restriction to $\hom(X, X)$ is also a bijection of sets $id: \hom(X, X) \to \hom(X, X)$. This forces the set $\hom(X, 0)$ to be empty. 

Now let $\{Y_\alpha: \alpha \in A\}$ be a set of objects of $C$. We are required to show that each map 
$$ f\colon X \to \sum_\alpha Y_\alpha $$
factors through a unique inclusion $i_\alpha: Y_\alpha \to \sum_\alpha Y_\alpha$. By infinite extensivity, each pullback $U_\alpha \coloneqq f^\ast (Y_\alpha)$ exists and the canonical map $\sum_\alpha U_\alpha \to X$ is an isomorphism. We will treat it as the identity. 

Now all we need is to prove the following. 

* Claim: $X = U_\alpha$ for exactly one $\alpha$. For the others, $U_\beta = 0$. 

Indeed, for each $\alpha$, the identity map factors through one of the two summands in 

$$ id\colon X \to U_\alpha + \sum_{\beta \neq \alpha} U_\beta $$ 

because $\hom(X, -)$ preserves binary coproducts. In others words, either $X = U_\alpha$ or $X = \sum_{\beta \neq \alpha} U_\beta$ (and the other is $0$). We cannot have $U_\alpha = 0$ for every $\alpha$, for then $X = \sum_\alpha U_\alpha$ would be $0$, contradicting the fact that $\hom(X, 0) = 0$. So $X = U_\alpha$ for at least one $\alpha$. And no more than one $\alpha$, since we have $U_\alpha \cap U_\beta = 0$ whenever $\alpha \neq \beta$. 
\end{proof}

\begin{remark}
This above proof of Prop. \ref{RespectForBinaryCoproductsIsSufficient} is not [[constructive mathematics|constructive]], as we have no way to construct a particular $\alpha$ such that $X = U_\alpha$.  (It is constructive if [[Markov's principle]] applies to $A$.)
\end{remark}

From the proof above, we extract a result useful in its own right, giving an alternative definition of connected object. 

\begin{proposition}
\label{InExtensiveCategoryCOnnectedObjectsArePrimitiveUnderCoproduct}
**(in extensive categories connected objects are primitive under coproduct)**
\linebreak
An object $X$ in an [[extensive category]] is connected, def. \ref{ConnectedObject}, if and only if in any [[coproduct]] decomposition $X \simeq U + V$, exactly one of $U$, $V$ is not the [[initial object]]. 
\end{proposition}

\begin{proof}
\label{ProofThatInExtensiveCategoryCOnnectedObjectsArePrimitiveUnderCoproduct}
In one direction, assume that $X$ is connected. If now $X \,\simeq\, U + V$ is a coproduct decomposition, then, by connectedness, the [[isomorphism]] $X \xrightarrow{\sim} U + V$ factor through one of the coproduct inclusions of $i_U, i_V \colon U, V \hookrightarrow U + V$. If it factors through say $U$, then the [[subobject]] $i_U$ is all of $X$, and $V$ is forced to be initial: by [[disjoint coproducts|disjointness of coproducts]], which holds in any extensive category, see [here](extensive+category#DisjointAndPullbackStableCoproducts). 

In the other direction, assume that $X$ has non non-trivial coproduct decomposition and consider any [[morphism]] $f \colon X \to Y + Z$ into a coproduct. By [[extensive category|extensivity]], 
this implies (see [here](extensive+category#eq:HomIntoCoproductIsPullbackIfDomainIsCoproduct))
a coproduct decomposition $X = U + V$ 
with $U \coloneqq f^\ast(i_Y)$ and $V \coloneqq f^\ast(i_Z)$. 
But, by assumption, either $U$ or $V$ is initial, meaning that $X$ is [[isomorphism|isomorphic]] to either $V$ or $U$, respectively, so that $f$ factors through either $Y$ or $X$, respectively. In other words, $f$ belongs to exactly one of the two subsets $\hom(X, Y) \hookrightarrow \hom(X, Y + Z)$ or $\hom(X, Z) \hookrightarrow \hom(X, Y + Z)$. 
\end{proof}

### General properties 

+-- {: .num_prop}
###### Proposition

A [[colimit]] of connected objects over a [[connected category|connected]] [[diagram]] is itself a connected object. 

=--

+-- {: .proof} 
###### Proof 

Because coproducts in $Set$ commute with _limits_ of connected diagrams. 

=--

+-- {: .num_prop}
###### Proposition

If $X \in Ob(C)$ is connected and $X \to Y$ is an [[epimorphism]], then $Y$ is connected. 

=--

+-- {: .proof} 
###### Proof 

Certainly $Y$ is not [[initial object|initial]], because initial objects in extensive categories are [[strict initial object|strict]]. Suppose $Y = U + V$ (see prop. \ref{InExtensiveCategoryCOnnectedObjectsArePrimitiveUnderCoproduct} above), so that we have an epimorphism $X \to U + V$. By connectedness of $X$, this epi factors through one of the summands, say $U$. But then the inclusion $i_U: U \hookrightarrow U + V$ is epic, in fact an epic equalizer of two maps $U + i_1, U + i_2: U + V \rightrightarrows U + V + V$. This means $i_U$ is an isomorphism; by disjointness of coproducts, this forces $V$ to be initial. Of course $U$ is not initial; otherwise $Y$ would be initial. 

=--

+-- {: .num_remark}
###### Remark

It need not be the case that products of connected objects are connected. For example, in the topos $\mathbb{Z}$-Set, the product $\mathbb{Z} \times \mathbb{Z}$ decomposes as a countable coproduct of copies of $\mathbb{Z}$. (For more on this topic, see also [[cohesive topos]].) 

=--

We do have the following partial result, generalizing the case of $Top$. 


+-- {: .num_theorem #prod} 
######Theorem 

Suppose $C$ is a cocomplete $\infty$-[[extensive category]] with 
[[finite products]]. Assume that the [[terminal object]] is a [[separator]], and that [[Cartesian product]] functors $X \times (-) : C \to C$ preserve [[epimorphisms]]. Then a product of finitely many connected objects is itself connected. 

=-- 

+-- {: .proof} 
######Proof 

In the first place, $1$ is connected. For suppose $1 = U + V$ where $U$ is not initial. The two coproduct inclusions $U \to U + U$ are distinct by disjointness of sums. Since $1$ is a separator, there must be a map $1 \to U$ separating these inclusions. We then conclude $U \cong 1$, and then $V \cong 0$ by disjointness of sums. 

Now let $X$ and $Y$ be connected. The two inclusions $i_1, i_2: X \to X + X$ are distinct, so there exists a point $a \colon 1 \to X$ separating them. For each $y \colon 1 \to Y$, the +-shaped object $T_y = (X \times y) \cup (a \times Y)$ is connected (we define $T_y$ to be a sum of connected objects $X \times y$, $a \times Y$ amalgamated over the connected object $a \times y = 1 \times 1 = 1$, i.e., to be a connected colimit of connected objects). We have a map 

$$\phi: \bigcup_{y \colon 1 \to Y} T_y \to X \times Y$$

where the union is again a sum of connected objects $T_y$ amalgamated over $a \times Y$, so this union is connected. The map $\phi$ is epic, because the evident map 

$$\sum_{y \colon 1 \to Y} X \times y \cong X \times \sum_{y \colon 1 \to Y} 1 \to X \times Y$$ 

is epic (by the assumptions that $1$ is a [[separator]] and $X \times -$ preserves epis), and this map factors through $\phi$. It follows that the codomain $X \times Y$ of $\phi$ is also connected. 

=-- 

+-- {: .num_remark #prod2} 
###### Remark 
The same method of proof shows that for an arbitrary family of [[connected spaces]] $\{X_\alpha\}_{\alpha \in A}$, the connected component of a point $x = (x_\alpha)$ in the product space $X = \prod_{\alpha \in A} X_\alpha$ contains at least all those points which differ from $x$ in at most finitely many coordinates. However, the set of such points is dense in $\prod_{\alpha \in A} X_\alpha$, so $\prod_{\alpha \in A} X_\alpha$ must also be connected. 
=-- 



## Examples

* Connected objects in [[Top]] are precisely [[connected topological spaces]]. 

* For a [[group]] $G$, connected objects in the category $G Set$ of [[permutation representation]]s are precisely the ([[inhabited set|inhabited]]) [[transitive action|transitive]] $G$-sets. 

* Objects in a [[locally connected topos]] are [[coproducts]] of connected objects. 
 
  (This includes categories such as $G Set$, [[permutation representations]] of a [[group]] $G$.)

* A [[scheme]] is connected as a scheme (which by definition means that its underlying topological space is connected) if and only if it is connected as an object of the category of schemes. See [here](http://gausyu.github.io/MathBlog/2016/02/13/Connectedness-of-Schemes/).

* [[connected graph]]



## Related concepts

* [[connected topos]], [[locally connected topos]]

* [[disjoint coproduct]]

* [[coproduct-preserving representable]]

* [[n-connected object in an (∞,1)-topos]]



[[!redirects connected object]]
[[!redirects connected objects]]

[[!redirects connected]]
