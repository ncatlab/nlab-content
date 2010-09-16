
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

* **connection on a bundle**

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* [[connection on an ∞-bundle]]

***

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A **connection** on a [[bundle]]  $P \to X$ --  a [[principal bundle]] or an [[associated bundle]] like a [[vector bundle]] -- is a rule that identifies [[fiber]]s of the bundle along paths in the base space $X$. 

There are several different but equivalent formalizations of this idea:

* as a  __[[parallel transport]]__ functor, 

* as a rule for a __[[covariant derivative]]__, 

* as a __distribution (field) of horizontal subspaces__  -- an [[Ehresmann connection]] -- and via a __connection $1$-form__ which annihilates the distribution of horizontal subspaces. The connection in that sense induces a smooth version of [[Hurewicz connection]]. 

The usual textbook convention is to say just connection for the distribution of horizontal subspaces, and the objects of the other three approaches one calls more specifically covariant derivative, connection $1$-form and [[parallel transport]].

In the remainded of this Idea-section we discuss a bit more how to understand connections in terms of parallel transport.

Given a smooth [[bundle]] $P \to X$, for instance a $G$-[[principal bundle]] or a [[vector bundle]], a _connection_ on $P$ is a prescription to associate with each path

$$
  \gamma : x \to y
$$

in $X$  (which is a [[morphism]] in the [[path groupoid]] $\mathbf{P}_1(X)$) a morphism $tra(\gamma)$ between the fibers of $P$ over these points

$$
  \array{
     P_x &\stackrel{tra(\gamma)}{\to}& P_y
     \\
     x &\stackrel{\gamma}{\to}& y
  }
$$

such that

* this assignment respects the structure on the fibers $P_x$ (for instance is $G$-equivariant in the case that $P$ is a $G$-bundle or that is linear in the case that $P$ is a vector bundle);

* this assignment is smooth in a suitable sense;

* this assignment is [[functor]]ial in that for all pairs $x \stackrel{\gamma}{\to} y$, $y \stackrel{\gamma'}{\to} z$ of composable paths in $X$ we have
  $$
    \array{
       P_x &\stackrel{tra(\gamma)}{\to}& P_y &\stackrel{tra(\gamma')}{\to}& P_z
       \\
       x &\stackrel{\gamma}{\to}& y &\stackrel{\gamma'}{\to}& z
    }
    \;\;\;
    =
    \;\;\;
    \array{
       P_x &\stackrel{tra(\gamma' \circ \gamma)}{\to}& P_z
       \\
       x &\stackrel{\gamma'\circ \gamma}{\to}& z
    }
  $$


In other words, a connection on $P$ is a [[functor]] 

$$
  tra : \mathbf{P}_1(X) \to At''(P)
$$

from the [[path groupoid]] of $X$ to the [[Atiyah Lie groupoid]] of $P$ that is smooth in a suitable sense and _splits the Atiyah sequence_ in that $\mathbf{P}_1(X) \stackrel{tra}{\to} At''(X) \to \mathbf{P}_1(X)$ (see the notation at [[Atiyah Lie groupoid]]).

**Terminology**

The functor $tra$ is called the **[[parallel transport]]** of the connection. This terminology comes from looking at the orbits of all points in $P$ under $tra$ (i.e. from looking at the [[category of elements]] of $tra$): these trace out paths in $P$ sitting over paths in $X$ and one thinks of the image of a point $p \in P_x$ under $tra(\gamma)$ as the result of propagating $p$ parallel to these curves in $P$. 

**Flat connctions**

It may happen that the assignment $tra : \gamma \mapsto tra(\gamma)$ only depends on the [[homotopy]] class of the path $\gamma$ relative to its endpoints $x, y$. In other words: that $tra$ factors through the functor $P_1(X) \to \Pi_1(X)$ from the [[path groupoid]] to the [[fundamental groupoid]] of $X$. In that case the connection is called a **flat connection**.

### More concrete picture 

By [[Lie theory|Lie differentiation]] the functor $tra$, i.e. by looking at what it does to very short pieces of paths, one obtains from it a splitting of the [[Atiyah Lie groupoid|Atiyah Lie algebroid sequence]], which is a morphism

$$
  \nabla : T X \to at(P)
$$ 

of vector bundles. Locally on $X$ -- meaning: when everything is pulled back to a [[cover]] $Y \to X$ of $X$ -- this is a $Lie(G)$-valued 1-form $A \in \Omega^1(Y, Lie(G))$ with certain special properties.

In particular, since every $G$-[[principal bundle]] canonically trivializes when pulled back to its own total space $P$, a connection in this case gives rise to a 1-form $A \in \Omega^1(P)$ satisfying two conditions. This data is called an **[[Ehresmann connection]]**.

If instead $P = E$ is a vector bundle, then the two conditions satisfies by $A$ imply that it defines a linear map

$$
  \nabla : \Gamma(E) \to \Omega^1(X) \otimes \Gamma(E)
$$

from the space $\Gamma(E)$ of section of $E$ that satisfies the properties of a **covariant derivative**.

If again the connection is flat, then this is manifestly the datum of a [[Lie infinity-algebroid representation]] of the [[Lie algebroid|tangent Lie algebroid]] $T X$ of $X$ on $E$: it defines the action [[Lie algebroid]] which is the [[Lie theory|Lie version]] of the [[Lie groupoid]] classified by the parallel transport functor.

...

### More abstract picture 

Recall from the discussion at $G$-[[principal bundle]] that the $G$-bundle $P \to X$ is encoded in a a suitable morphism

$$
  X \to \mathbf{B}G
$$

(namely a morphism in the right [[(infinity,1)-category]] which may be represented by an [[anafunctor]]).

It turns out that similarly suitable morphisms

$$
  \mathbf{P}_1(X) \to \mathbf{B}G
$$

encode in one step the $G$-bundle together with its parallel transport functor.

This is described in great detail in the reference by Schreiber--Waldorf below.

(...am running out of time... for more see [[schreiber:Differential Nonabelian Cohomology|here]])
...


## Definition {#Definition}

Let $G$ be a [[Lie group]]. We recall briefly the following discussion of $G$-[[principal bundle]]s. Write

$$
  \mathbf{B}G : U \mapsto ( Hom_{Diff}(U,G) \stackrel{\to}{\to} *)
$$

for the [[functor]] that sends a [[Cartesian space]] $U$ to the [[delooping]] [[groupoid]] of the group of $G$-valued [[smooth function]]s on $U$: the groupoid with a single object and the [[group]] $Hom_{Diff}(U,G)$ of maps as its set of morphisms.

This is a groupoid-valued [[sheaf]] on the [[site]] [[CartSp]] and in fact is a [[2-sheaf]]/[[stack]]. 

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]], we may also regard it as a [[2-sheaf]] on [[CartSp]] in an evident way.

+-- {: .un_prop}
###### Observation

The groupoid $G Bund(X)$ of $G$-[[principal bundle]]s on $X$ is equivalent to the hom-groupoid

$$
  \mathbf{H}(X,\mathbf{B}G) \simeq G Bund(X)
$$

taken in the [[2-topos]] of 2-sheaves on [[CartSp]].

=---

A detailed discussion of this is at [[∞-Lie groupoid]] in the section <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieGroups">on Lie groups</a>.

Now write $\mathfrak{g}$ for the [[Lie algebra]] of $\mathfrak{g}$. Then consider the functor

$$
  \bar \mathbf{B} G : U \to 
  [\mathbf{P}_1(U),\mathbf{B}G]
  =
  \left\{
    A \stackrel{g}{\to} (g^{-1} A g + g^{-1} d g)
    |
    A \in \Omega^1(U,\mathfrak{g})\,, g \in C^\infty(U,G)
  \right\}
$$

that sends a Cartesian space $U$ to the **[[groupoid of Lie-algebra valued 1-forms]]** over $U$. 

There is an evident morphism of 2-sheaves

$$
  \bar \mathbf{B}G \to \mathbf{B}G
$$

that forgets the 1-forms on each object $U$.

+-- {: .un_defn}
###### Definition
**(connection)**

A **connection** on a $G$-[[principal bundle]] $g : X \to \mathbf{B}G$ is a lift $\nabla$ to $\bar \mathbf{B}G$

$$
  \array{
    && \bar \mathbf{B}G
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

The **groupoid of $G$-principal bundles with connection** on $X$ is

$$
  G Bund_\nabla(X) := Hom(X,\bar \mathbf{B}G)
  \,.
$$

=--

Explicitly, a morphism $g : X \to \mathbf{B}G$ is a nonabelian [[Cech cohomology]] cocycle on $X$ with values in $G$:

1. a choice of [[good open cover]] $\{U_i \to X\}$ of $X$;

1. a collection of functions $(g_{i j} \in C^\infty(U_i \cap U_j), G)$

such that on $U_i \cap U_j \cap U_k$ the equation

* $g_{i j} g_{j k} = g_{i k}$

holds.

A lift $\nabla : X \to \bar \mathbf{B}G$ of this is in addition 

1. a choice of [[Lie-algebra valued 1-form]]s 
   $(A_i \in \Omega^1(U_i, \mathfrak{g}))$

such that on $U_i \cap U_j$ the equation

* $A_j = g^{-1} A_i g + g^{-1} d g$

holds, where on the right we have the pullback $g^* \theta$ of the [[Maurer-Cartan form]] on $G$ (see there).



## Properties {#Properties}

+-- {: .un_defn}
###### Definition
**(existence of connections)**

Every $G$-principal bundle admits a connection. In other words, the forgetful functor

$$
  Hom(X,\bar \mathbf{B}G) \to Hom(X,\mathbf{B}G)
$$

is an [[essentially surjective functor]].

=--

+-- {: .proof}
###### Proof


Choose a [[partition of unity]] $(\rho_i \in C^\infty(X,\mathbb{R}))$ subordinate to the [[good open cover]] $\{U_i \to X\}$ with respect to which a given cocycle $g : X \to \mathbf{B}G$ is expressed:

* $(x \;not\; in\; U_i) \Rightarrow \rho_i(x) = 0$;

* $\sum_i \rho_i = 1$.

Then set

$$
  A_i := \sum_{i_0} \rho_{i_0}|_{U_{i_0}} g_{i_0 i}|_{U_{i_0}}
  \,.
$$

By slight abuse of notation we shall write this and similar expressions simply as 

$$
  A_i := \sum_{i_0} (d_{dR} \rho_{i_0} + g_{i i_0}^{-1} d_{dR} g_{i i_0})  
  \,.
$$

Using the that $(g_{i j})$ satisfies its cocycle condition, one checks that this satisfies the cocycle condition for the 1-forms:

$$
  \begin{aligned}
     A_j - A_i  &=
     \sum_{i_0} \rho_{i_0} ( g_{j i_0}^{-1} d g_{j i_0} -  
       g_{i i_0}^{-1} d g_{i i_0} )
     \\
     & = 
     \sum_{i_0} \rho_{i_0} ( g_{i j}^{-1} d g_{i j} )
     \\
     & =
     g_{i j}^{-1} d g_{i j}
  \end{aligned}
  \,.
$$


=--



## Special cases 

### Connections on the tangent bundle 

Connections on [[tangent bundle]]s are also called [[affine connection]]s.

They play a central role for instance on [[Riemannian manifold]]s and [[pseudo-Riemannian metric|pseudo-Riemannian manifold]]s. From the end of the 19th century and the beginning of the 20th centure originates a language to talk about these in terms of [[Christoffel symbol]]s. 

### Connections in physics

In [[physics]] connections on bundles model [[gauge field]]s. 

* The [[electromagnetic field]] is a connection on a [[circle group]]-principal bundle;

* A [[Yang-Mills field]] more generally is a connection on a [[unitary group]]-principal bundle.

* The field of [[gravity]] is encoded in a connection on the [[orthogonal group]]-principal bundle to which the [[tangent bundle]] is [[associated bundle|associated]].

## Generalizations

### Superconnections 

Generalizing the parallel transport definition from ordinary manifolds to [[supermanifold]]s yields the notion of [[superconnection]].


### Simons-Sullivan structured bundles

When the notion of connection on a principal bundle is slightly coarsened, i.e. when more connections are regarded as being ismorphic than usual, one arrives at a structure called a [[Simons-Sullivan structured bundle]]. This has the special property that for $G = U$  the [[unitary group]], the corresponding [[Grothendieck group]] of such bundles is a model for [[differential K-theory]].

### Connections on a principal $\infty$-bundle


See [[connection on a principal ∞-bundle]].



## References


References for the description of connections in terms of their parallel transport are collected at 

* [[Urs Schreiber]], _<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#HistConnAsParTrans">Differential cohomology in an (oo,1)-topos -- References -- Connections -- In terms of parallel transport</a>_

Basic facts about connections, such as the existence proof in terms of Cech cocycles, are collected in the brief lecture note

* [[Theodore Voronov]], _Differential Geometry, &#167;3 Connection on a vector bundle_ ([pdf](http://www.maths.manchester.ac.uk/~tv/Teaching/Differential%20Geometry/2008-2009/lecture3.pdf))


[[!redirects connections on a bundle]]
[[!redirects connections on bundles]]