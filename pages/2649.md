
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

Let $\mathcal{C}$ be an [[extensive category]].

+-- {: .num_defn #ConnectedObject}
###### Definition

An [[object]] $X$ of a [[category]] $\mathcal{C}$ is called *connected* if the [[hom-functor]] out of $X$

$$ 
  \mathcal{C}(X, -) \,\colon\, \mathcal{C} \to Set 
  \,.
$$

[[preserved limit|preserves]] all [[coproducts]]. 

=--

+-- {: .num_remark}
###### Remark

By definition, $\mathcal{C}(X,-)$ preserves binary coproducts if the canonically defined morphism $\mathcal{C}(X,Y) + \mathcal{C}(X,Z) \to \mathcal{C}(X,Y + Z)$ is a [[natural bijection]].

=--

\begin{remark}
\label{InitialObjectIsNotConnected}
**(initial object is not connected)**
\linebreak
By Def. \ref{ConnectedObject}, the [[initial object]] $\varnothing$ of a category $\mathcal{C}$ is *not* connected: 

Because, $\mathcal{C}(\varnothing, -) \,\colon\, \mathcal{C} \to Set$ is, by definition of [[initial objects]], the [[constant functor]] with value the [[singleton]] $\ast \,\in\, Set$, so that for $X , Y \,\in\, \mathcal{C}$ we have

$$
  \mathcal{C}
  \big( 
    \varnothing
    ,\,
    X \sqcup Y
  \big)
  \;\simeq\;
  \ast
  \;\;
  \neq
  \;\;
  \ast \sqcup \ast
  \;\simeq\;
  \mathcal{C}
  (\varnothing,\, X)
  \sqcup
  \mathcal{C}
  (\varnothing,\, Y)
  \;\;\;
  \in
  \;
  Set
  \,.
$$

One may understand this as part of the pattern by which degenerate objects may be "[[too simple to be simple]]".  For example, also the [[empty space]] should not be considered connected, see [this remark](connected+space#ConnectedEmptySpace) at *[[connected space]]* .

\end{remark}

+-- {: .num_remark}
###### Remark

If $C$ is a [[infinitary extensive category]] then for $X \in Ob(\mathcal{C})$ to be connected it is enough to require that $\mathcal{C}(X,-)$ preserves *binary* coproducts. This is theorem \ref{RespectForBinaryCoproductsIsSufficient} below.

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
In one direction, assume that $X$ is connected and consider an [[isomorphism]] $X \xrightarrow{\sim} X_1 \sqcup X_2$ to a [[coproduct]]. By assumption of connectedness, this morphism factors through one of the summands, say through $X_1$, as shown in the bottom row of the following diagram: 

\begin{tikzcd}
    X_2
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny (pb)}"]
    &
    \varnothing
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny (pb)}"]
    &
    X_2
    \ar[d, "i_2"{right}]
    \\
    X
    \ar[r]
    \ar[
      rr, 
      rounded corners,
      to path={
        -- ([yshift=-7pt]\tikztostart.south)
        -- node[below]{\scalebox{.7}{$\sim$}} 
           ([yshift=-6pt]\tikztotarget.south)
        -- ([yshift=-0pt]\tikztotarget.south)
      }
    ]
    &
    X_1
    \ar[r, "i_1"{below}]
    &
    X_1 \sqcup X_2
    \mathrlap{\,.}
\end{tikzcd}
Consider then the [[pullback]] of the total bottom morphism along the inclusion $i_2$ of the other summand. Since pullbacks of isomorphisms are isomorphisms, the resulting top left object must be (isomorphic to) $X_2$, as shown. On the other hand, by the [[pasting law]] this pullback factors into two pullback squares, as shown above. But the pullback on the right gives the [[initial object]], since [[disjoint coproducts|coproducts are disjoint]] in an extensive category (see [here](extensive+category#DisjointAndPullbackStableCoproducts)). This exhibits a morphisms $X_2 \to \varnothing$. But since the initial objects in extensive categories are [[strict initial objects]], this must be an isomorphism, $X_2 \simeq \varnothing$. By the same argument, $X_1$ cannot be an initial object, since otherwise $X$ would be too, which it is not by assumption of connectedness (Rem. \ref{InitialObjectIsNotConnected}). Hence we have shown that exactly one of the two summands in $X \simeq X_1 \sqcup X_2$ is initial.

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
