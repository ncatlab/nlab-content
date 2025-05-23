

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a given [[manifold]] $X$ of finite [[dimension]] there exists an [[embedding]] $i : X \to \mathbb{R}^n$ into some [[Cartesian space]]. Using the [[Pontrjagin-Thom collapse map]] this induces a morphism in [[topological K-theory]]

$$
  i_! : K(T X) \to K(T \mathbb{R}^n)
  \,.
$$

Similarly for any point inclusion $j : * \to \mathbb{R}^n$ there is such a morphism $j_! : \mathbb{Z} = K(*) \to K(T \mathbb{R}^n)$ which is an [[isomorphism]] -- the [[Thom isomorphism]]. 

The **topological index** of [[topological K-theory]] on $X$ is the composite

$$
  ind_{top} : \mathbb{Z} = K(T X) \stackrel{i_!}{\to}
   K(T \mathbb{R}^n) \stackrel{j_!^{-1}}{\to} K(*) = \mathbb{Z}
  \,.
$$

One can prove that this is independent of all the occurring choices. In particular it does not depend on the specific choice of embedding of the manifold $X$ into the [[Euclidean space]]. The _topological index function_ is uniquely fixed by two properties (this is the content of the [[Atiyah-Singer index theorem]]):

1. For $X$ a point we have $ind_t=id$.

1. Index functions commute with the maps $i_!$.

From this one defines the _topological index of an [[elliptic operator]]_ . The [[principal symbol]] of the operator defines a homogenous length-one [[chain complex]] of [[bundles]] on $T X$ [[exact sequence|exact]] outside the null section. Elements of this kind are precisely cycles for the compactly supported [[K-theory]] of $T X$ hence an elliptic operator $D$ has a topological index only depending on its principal symbol. 

On the other hand, analysis associates to $D$ its [[analytical index]] that is

$$
\operatorname{dim}\operatorname{Ker}(D)-\operatorname{dim}\operatorname{coKer}(D)
$$ 

on one (hence all) [[Sobolev space]] that $D$ is defined on. 

The [[Atiyah-Singer index theorem]] states that the [[analytical index]] of $D$ is equal to its topological index.


### More on the Thom map

The story starts with an embedding $i:X\to Y$ of [[compact space|compact]] [[manifolds]]. In this situation one can construct a [[homomorphism]] 

$$
  i_{!} : K(T X)\longrightarrow K(T Y)
$$ 

between the [[compact support|compactly supported]] [[K-theory|K-theories]] of their [[tangent bundles]]. 

Notice here the reverse [[functor|functoriality]]: for the base space $K$ is contravariant while for the total spaces of the tangent bundles it is covariant. This uses the [[Pontrjagin-Thom collaps map|Thom mapping]]: if $X$ is a compact manifold and $V$ a real [[vector bundle]] over $X$ there is a natural map

$$
  \varphi:K(X)\longrightarrow K(V)
  \,.
$$ 

One of the most important results of [[K-theory]], namely [[Bott periodicity]], can be seen as the statement of the fact that this map is an [[isomorphism]]. Now apply this construction to the [[normal bundle]] $N$ of $X$ in $Y$ to get

$$
  \varphi
  :
  K(T X)\longrightarrow K(T N)
$$

and (looking at $N$ as a [[tubular neighbourhood]] of $X$ in $Y$) compose it with the natural map  

$$
  K_*
  :
  K(T N)\longrightarrow K(T Y)
$$ 

to get $i_!$. 

Now given a manifold $X$, embed it in a [[Euclidean space]] $\mathbb{R}^n$ for some suitable $n$ and consider the inclusion $\{0\}\to \mathbb{R}^n$. This induces the ([[Thom isomorphism]]) mapping $j_!:\mathbb{Z}=K(\{0\}) \longrightarrow K(T\mathbb{R}^n)$. 

The _topological index_ is defined to be

$$
  ind_t
  :=
  j_!^{-1}\circ i_!
  \,.
$$ 

## Related concepts

* [[index theory]]

  * **topological index**

  * [[analytical index]]

  * [[Atiyah-Singer index theorem]]

* [[eta invariant]], [[zeta function of an elliptic differential operator]], [[functional determinant]]

* [[fiber integration in differential K-theory]]

[[!redirects topological indices]]

[[!redirects index of an operator]]

