
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### General

There are several ways to make sense of the notion of the [[n-sphere]] in the limit (rather: [[colimit]]) that $n \to \infty$. Typically the resulting _infinite-dimensional sphere_ $S^\infty$ has the remarkable property that it is [[contractible topological space|contractible]] as a [[topological space]] or at least weakly contractible, in that its map to the [[point]] is a [[weak homotopy equivalence]].


### In homotopy theory

Due to their [[weak homotopy equivalence]] to points, in [[homotopy theory]] infinite-dimensional spheres provide nothing new in themselves, but as a source of big contractible spaces they serve as a starting point for making concrete models of [[classifying spaces]]. 

For example, the [[n-sphere|2k-sphere]] is the total space of the [[tautological line bundle|tautological]] [[circle group]]-[[principal bundle]] over [[complex projective space|complex projective k-space]], so that in the [[colimit]] $2k \to \infty$ the infinite-dimensional sphere emerges as a model for the [[universal principal bundle]] over the [[classifying space]] $B \mathrm{U}(1)$. This being contractible relates to important statements such as that [[zero-section into Thom space of universal line bundle is weak equivalence|the zero-section into the Thom space of the universal line bundle is a weak equivalence]].



## Realizations

### An an infinite spherical cell complex
 {#AsAnInfiniteSphericalCellComplex}

Realizing the [[n-sphere]] as a [[cell complex]] of sorts, such that $S^n \hookrightarrow S^{n+1}$ is a [[relative cell complex]]-inclusion for all $n \in \mathbb{N}$, the infinite-dimensional sphere may be taken to be the [[colimit]] over this sequence of inclusions.

For example, in the [[category]] [[Top]] of [[topological spaces]], the [[n-sphere]] has a standard [[CW-complex]] structure with exactly 2-cells in each dimension, obtained [[induction|inductively]] by [[space attachment|attaching]] two $n$-dimensional [[hemispheres]] to the $(n-1)$-sphere regarded as the [[equator]] in the $n$-sphere.

Since forming [[homotopy groups]] $\pi_k(-)$ commutes with taking the colimit over these [[relative cell complex]] inclusions (by the [[skeleton]] filtration), and since the [[n-sphere]] has trivial homotopy groups in dimension $k \lt n$, it follows at once that the homotopy groups of the infinite-dimensional sphere all vanish, and hence that it is [[weak equivalence|weakly equivalent]] to the point in the [[classical model structure on topological spaces]]:

$$
  \begin{aligned}
    \pi_k
    \big(
      S^\infty
    \big)
    & =\; 
    \pi_k 
    \big(
      \underset{ \underset{n \in \mathbb{N}}{\longrightarrow} }{\lim} 
      \;
      S^n
    \big)
    \\
    & = \;
    \underset{ \underset{n \in \mathbb{N}}{\longrightarrow} }{\lim} 
    \;
    \pi_k 
    \big(
      S^n
    \big)
    \\
    & = \;  
    \underset{ \underset{n \in \mathbb{N}}{\longrightarrow} }{\lim} 
    \;
    \underset{
      = \, \ast
    }{
    \underbrace{
    \pi_k 
    \big(
      S^{n+k+1}
    \big)
    }
    }
    \\
    & \simeq
    \ast
  \end{aligned}
$$





### As the unit spheres in a topological vector space

One can also talk about a sphere in an arbitrary (possibly infinite-dimensional) [[normed vector space]] $V$:
$$ S(V) = \{ x: V \;\text{such that}\; {\|x\|} = 1 \} .$$

If a [[LCTVS|locally convex topological vector space]] admits a continuous linear injection into a [[normed vector space]], this can be used to define its sphere.  If not, one can still define the sphere as a *quotient* of the space of non-zero vectors under the scalar action of $(0,\infty)$.

Homotopy theorists define $S^\infty$ to be the sphere in the (incomplete) [[normed vector space]] (traditionally with the $l^2$ norm) of infinite [[sequences]] almost all of whose values are $0$, which is the [[directed colimit]] of the $S^n$:

$$ 
  S^{-1} 
    \hookrightarrow 
  S^0 
    \hookrightarrow 
  S^1 
    \hookrightarrow 
  S^2 
    \hookrightarrow 
  \cdots 
    S^\infty 
  \,.
$$


If the vector space is a [[shift space]], then contractibility is straightforward to prove.

+-- {: .num_theorem #theorem}
###### Theorem
Let $V$ be a [[shift space]] of some order.  Let $S V$ be its sphere (either via a norm or as the quotient of non-zero vectors).  Then $S V$ is contractible.
=--

+-- {: .proof}
###### Proof
Let $T \colon V \to V$ be a [[shift map]].  The idea is to homotop the sphere onto the image of $T$, and then down to a point.

It is simplest to start with the non-zero vectors, $V \setminus \{0\}$.  As $T$ is injective, it restricts to a map from this space to itself which commutes with the scalar action of $(0,\infty)$.  Define a homotopy $H \colon [0,1] \times (V \setminus
 \{0\}) \to V \setminus \{0\}$ by $H_t(v) = (1 - t)v + t T v$.  It is clear that, assuming it is well-defined, it is a homotopy from the identity to $T$.  To see that it is well-defined, we need to show that $H_t(v)$ is never zero.  The only place where it could be zero would be on an eigenvector of $T$, but as $T$ is a [[shift map]] then it has none.

As $T$ is a [[shift map]], it is not surjective and so we can pick some $v_0$ not in its image.  Then we define a homotopy $G \colon [0,1] \times (V \setminus \{0\}) \to V \setminus \{0\}$ by $G_t(v) = (1 - t)T v + t v_0$.  As $v_0$ is not in the image of $T$, this is well-defined on $V \setminus \{0\}$.  Combining these two homotopies results in the desired contraction of $V \setminus \{0\}$.

If $V$ admits a suitable function defining a spherical subset (such as a norm) then we can modify the above to a contraction of the spherical subset simply by dividing out by this function.  If not, as the homotopies above all commute with the scalar action of $(0,\infty)$, they descend to the definition of the sphere as the quotient of $V \setminus \{0\}$.

=--

## Related concepts

* [[Kuiper's theorem]]

[[!redirects infinite-dimensional spheres]]

[[!redirects infinite-dimensional sphere is contractible]]
[[!redirects infinite-dimensional sphere is weakly contractible]]

[[!redirects the infinite-dimensional sphere is contractible]]
[[!redirects the infinite-dimensional sphere is weakly contractible]]

[[!redirects infinite-dimensional spheres are contractible]]
[[!redirects infinite-dimensional spheres are weakly contractible]]

