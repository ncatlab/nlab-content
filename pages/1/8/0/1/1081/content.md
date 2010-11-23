
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Under the [[Dold-Kan correspondence]] [[∞-groupoids]] with strict abelian group structure (modeled by [[Kan complexes]] that are [[simplicial object|simplicial]] abelian groups) are identified with non-negatively graded [[chain complexes]] of abelian groups

$$
  N_\bullet : SimpAb \stackrel{\simeq}{\to} Ch_+
  \,.
$$

The **homology groups** of a [[chain complex]] of abelian groups are the image under this identification of the [[homotopy groups]] of the corresponding [[∞-groupoids]]. More details on this are at [[chain homology and cohomology]].


So at least for the case of chain complexes of abelian groups we have the slogan

+-- {: .standout}

**homology** = [[homotopy]] under [[Dold-Kan correspondence]]

=--

Of course historically the development of concepts was precisely the oppposite: chain homology is an old fundamental concept in [[homological algebra]] that is simpler to deal with than [[simplicial homotopy groups]]. The computational simplification for chain complexes is what makes the [[Dold-Kan correspondence]] useful after all.

But conceptually it is useful to understand homology as a special kind of [[homotopy]]. This is maybe most vivid in the [[duality|dual]] picture: [[cohomology]] derives its name from that fact that [[chain homology and cohomology]] are dual concepts. But later generalizations of [[cohomology]] to [[generalized (Eilenberg-Steenrod) cohomology]] and further to [[nonabelian cohomology]] showed that the restricted notion of homology is an insufficient dual model for cohomology: what cohomology is really dual to is the more general concept of [[homotopy]].  More on this is at [[cohomotopy]] and [[Eckmann-Hilton duality]].


## Definition

The category of abelian groups is in particular an [[abelian category]].
We can define [[chain complexes]] and their homology in any [[abelian category]] $C$. 

Let $C$ be an [[abelian category]] and let
$$
  V_\bullet = ( \cdots  \to V_{n+1} \stackrel{\partial_n}{\to}
  V_n \stackrel{\partial_{n-1}}{\to}
  V_{n-1} \to \cdots
  )
$$
be a [[chain complex]] in $C$. For each interger $n \in \mathbb{N}$ this induces the following diagram of [[kernel]]s, [[cokernel]]s and [[image]]s

$$
  \array{
    && im \delta_n &&\to&& ker \delta_{n-1}
    \\
    & \nearrow && \searrow && \swarrow
    \\
    V_{n+1}
    &&\stackrel{\partial_n}{\to}&&
    V_n
    &&\stackrel{\partial_{n-1}}{\to}&&
    V_{n-1}
    \\
    & &&
    \swarrow && \searrow && \nearrow
    \\
    && coker \delta_n &&\stackrel{}{\to}&&
    im \delta_{n-1}
  }
$$

the **homology** $H_n(V)$ of $V$ in degree $n$ is the object

$$
  \begin{aligned}
    im(ker \delta_{n-1} \to  V_n \to coker \delta) 
    & \simeq
    coker(im \delta_n \to ker \delta_{n-1})
    \\
    & \simeq
    coker(V_{n+1} \to ker \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to im \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to V_{\delta_{n-1}})
  \end{aligned}
$$


* If $H_n(V) \simeq 0$ then one says that the complex $V$ is [[exact sequence|exact]] in degree $n$.

## Examples 

In the special case that $C$ is the category of abelian groups, or of vector spaces, this definition reduces to the more familiar simpler statement:

the $n$-th homology group of the [[chain complex]] $V_\bullet$ is the quotient group

$$
  H_n(V) = ker(\partial_n) / im(\partial_{n+1})
  \,.
$$

[[!redirects homology group]]
[[!redirects homology groups]]