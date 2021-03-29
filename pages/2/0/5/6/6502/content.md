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

#Contents#
* table of contents
{:toc}

## Idea

A _Cartan connection_ is a _[[principal connection]]_ on a [[smooth manifold]] equipped with a certain compatibility condition with the [[tangent bundle]] of the manifold. It combines the concept of [[G-structure]] with that of [[soldering form]]. This combination allows us to express various types of geometric structures on $X$ -- such as notably ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian geometry]], [[conformal geometry]] and many more (see [below](#TableOfExamples)) -- in terms of [[connection on a bundle|connection]] data, i.e. in terms of [[nonabelian cohomology|nonabelian]] [[differential cohomology]]-data. In particular the [[first order formulation of gravity]] in terms of Cartan connections has been one of the historical motivations ([Cartan 23](#Cartan23)).

In a little bit more detail, a Cartan connection on a manifold $X$ for a given [[subgroup]] inclusion $H \hookrightarrow G$ is data that identifies all the [[tangent spaces]] $T_x X$ of $X$ with the tangent space $\mathfrak{g}/\mathfrak{h} = T_{e H} (G/H)$ of the [[coset space]] [[Klein geometry]] $G/H$, such that the choice of these identifications is transported along compatibly.

Therefore a manifold equipped with a Cartan connection is also called a _[[Cartan geometry]]_ (see also there), a generalization (globalization) of the concept of [[Klein geometry]].


In yet a little bit more detail, an _$(H \hookrightarrow G)$-Cartan connection_ on $X$ is a $G$-[[principal connection]] on $X$ equipped with a [[reduction of structure groups|reduction of its structure group]] along $H \to G$ and such that the connection 1-form linearly identifies each [[tangent space]] $T_x X$ of $X$ with the tangent space $\mathfrak{g}/\mathfrak{h} = T_{e H} (G/H)$ of the [[coset space]].

## History

The concept essentially originates around ([Cartan 23](#Cartan23)), but the formulation in terms of [[principal connections]] and in fact the terminology "Cartan connection" is due to [[Charles Ehresmann]] who formulated principal connections as what, in turn, today are called _[[Ehresmann connections]]_ ([Ehresmann 50](#Ehresmann50)). 

In ([Ehresmann 50](#Ehresmann50)) Cartan's ideas  are formalized (see [Marle 14, page 9, 10](#Marle14) for review) by saying that an $(G \hookrightarrow H)$-Cartan connection is a $G$-Ehresmann connection on a $G$-[[principal bundle]] $P$ equipped with an $H$-principal subbundle $Q$, such that the restriction of the connection form along this inclusion yields a form that determines an isomorphism of each tangent space of $Q$ with $\mathfrak{g}$. 

## Definition

### Traditional

Let $G$ be a [[Lie group]] and $H \hookrightarrow G$  a sub-Lie group. (So that we may think of the [[coset space]] $G/H$ as a [[Klein geometry]].) Write $\mathfrak{h} \hookrightarrow \mathfrak{g}$ for the corresponding [[Lie algebras]]. 

There are various equivalent forms of the definition of Cartan connections. The following one characterizes it as a $G$-[[principal connection]] equipped with extra [[stuff, structure and property|structure and property]].

+-- {: .num_defn #Traditional}
###### Definition

A $(H \hookrightarrow G)$-Cartan connection over a [[smooth manifold]] $X$ is;

* a $G$-[[principal connection]] $\nabla$ on $X$;

* such that 

  1. there is a [[reduction of structure groups]] along $H \hookrightarrow G$;

  1. for each point $x \in X$ the canonical composite (for any local trivialization)

     $$
       T_x X \stackrel{\nabla}{\to} \mathfrak{g} \to \mathfrak{g}/\mathfrak{h}
     $$

     is an [[isomorphism]].

=--


+-- {: .num_remark}
###### Remark

More explicitly for various component-realizations of principal connections, this means the following:


1. In terms of **[[Ehresmann connection]]-data** def. \ref{Traditional} says that an $(H\hookrightarrow G)$-Cartan connection is an Ehresmann connection form $A$ on a $G$-principal bundle $P$ together with an $H$-principal bundle $Q$ and an $H$-equivariant map $i \colon Q\to P$ such that $i^\ast A$ yields an isomorphism $T Q \simeq Q\times \mathfrak{g}$.

   In this form the definition is due to ([Ehresmann 50](#Ehresmann50)), recalled in ([Marle 14, def. 4](#Marle14)). Often this definition is stated by describing $i^\ast A$ directly without mentioning of $A$, e.g. ([Sharpe 97, section 5.3, def. 3.1](#Sharpe), [Cap-Slov&#225;k 09, 1.5.1](#CapSlovak09)). Beware that $A$ is a [[principal connection]] but $i^\ast A$ is not.


1. In terms of **[[Cech cohomology|Cech]] [[cocycle]] data**, def. \ref{Traditional} says that an $(H\hookrightarrow G)$-Cartan connection is a cover $\{U_i \to X\}$ equipped with 1-forms $A_i \in \Omega^1(U_i, \mathfrak{g})$ and with transition functions $h_{i j} \in C^\infty(U_i \cap U_j, H)$ such that

   * $h_{i j} h_{j k} = h_{i k}$ on $U_i \cap U_j \cap U_k$;

   * $A_j = h_{i j}^{-1}(A_i + \mathbf{d})h_{i j}$ on $U_i \cap U_j$;

   * $A_i(-)_x \colon T_x U_i \stackrel{\simeq}{\longrightarrow} \mathfrak{g}/\mathfrak{h}$.

   In this form, the definition appears in ([Sharpe 97, section 5.1 def. 1.3 together with section 5.2](#Sharpe), [Cap-Slov&#225;k 09, 1.5.4](#CapSlovak09)).  


=--

See also [Wikipedia -- Cartan connection -- As principal connections](http://en.wikipedia.org/wiki/Cartan_connection#Cartan_connections_as_principal_connections).

+-- {: .num_defn #Torsion}
###### Definition

Given a Cartan connection $\nabla$, def. \ref{Traditional}, its [[torsion of a Cartan connection]] is the image of its [[curvature]] under the projection $\mathfrak{g} \to \mathfrak{g}/\mathfrak{h}$.

=--

([Sharpe, section 5.3, below def. 3.1](#Sharpe), [Cap-Slov&#225;k 09, section 1.5.7, p. 85](#CapSlovak09), [Lott 01, section 3](#Lott)).

+-- {: .num_remark}
###### Remark

In the case of vanishing torsion, the resulting [[flat connection|flat]] [[parallel transport]] with values in $G/H$ identifies an [[open neighbourhood]] of each point of $X$ with an open neighbourhood in $G/H$.

=--


+-- {: .num_remark}
###### Remark

The last clause in def. \ref{Traditional} says that the [[tangent space]] of $X$ at any point $x$ is being identified with the tangent space of the [[homogeneous space]] $G/H$ at the base point $e H$. This may be visualized by imagining that $X$ "tangentially touches" $G/H$ at $x\in X$ and $e H \in G/H$.

But by homogeneity, all the tangent spaces of $G/H$ are [[isomorphism|isomorphic]], and canonically so by [[invariant differential form|left translation]]. Hence by the path-lifting property of [[principal connections]], one may (at least for vanishing [[torsion]], def. \ref{Torsion}) visualize the Cartan connection as describing how the $G/H$ touching $X$ at $x$  "rolls" along paths (infinitesimal paths, vectors) through $x$. This picture of "rolling" is particularly vivid for the case that $(H \hookrightarrow G) = (O(n)\hookrightarrow O(n+1))$ is the inclusion of [[orthogonal groups]], which gives that $G/H = S^n$ is the [[n-sphere]] (for more on this see at _[[conformal connection]]_).

This picture of model spaces rolling along was influential in the historical development of the concept of Cartan geometry in the spirit of [[Klein geometry]].

=--


### Synthetically in terms of differential cohesion
 {#InTermsOfSmoothModuliStacks}

We discuss a [[synthetic mathematics|synthetic]] formulation of Cartan connections in terms of [[differential cohesion]].

> under construction

Write

* $\Omega^1(-,\mathfrak{g})$ for the [[sheaf]] (on the [[site]] of [[formal manifold|formal]] [[smooth manifolds]]) of [[Lie algebra valued differential forms]], regarded as the [[smooth set|smooth]] [[moduli space]] of $\mathfrak{g}$-differential forms (as explained at _[[geometry of physics]]_ in the chapter _[[geometry of physics -- differential forms|on differential forms]]_)

* $\mathbf{B} G_{conn} \simeq \Omega^1(-,\mathfrak{g})//G$ for the universal [[moduli stack of connections]], which is equivalently the [[homotopy quotient]] of $\Omega^1(-,\mathfrak{g})$ by the [[action]] of $G$ (regarded as a [[smooth group]]) by [[gauge transformations]];

* $\Omega^1(-,\mathfrak{g})//H$ for the [[homotopy quotient]] by just the [[subgroup]] $H \hookrightarrow G$;

* $\mathbf{J} \;\colon\;\Omega^1(-,\mathfrak{g})//H \longrightarrow \Omega^1(-,\mathfrak{g})//G\simeq \mathbf{B}G_{conn}$ for the canonical morphism.

+-- {: .num_prop #MCFormAsFiberOfDifferentialModuli}
###### Proposition

There is a [[homotopy fiber sequence]] of [[smooth groupoids]]

$$
  \array{
     G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})//H
     \\
     && \downarrow^{\mathrlap{\mathbf{J}}}
     \\
     && \mathbf{B}G_{conn}
  }
  \,,
$$

where $\theta/H$ is the $G$-[[Maurer-Cartan form]] modulo $H$.

=--

+-- {: .proof}
###### Proof

A detailed proof for the statement as given is spelled out at _[this proposition](orbit+method#ThetaAsHomotopyFiberOfJ)_.

But this statement holds generally in [[cohesive (∞,1)-toposes]] and an argument at this generality proceeds as follows: via the discussion at _[[∞-action]]_ the action of $G$ on $\Omega^1(-,\mathfrak{g})$ is exhibited by the forgetful map $\mathbf{B}G_{conn}\to \mathbf{B}G$ and since the action of $H$ on $\Omega^1(-,\mathfrak{g})$ is the restricted action, the square on the right of 

$$
  \array{
     G/H &\stackrel{\theta/H}{\longrightarrow}& \Omega^1(-,\mathfrak{g})//H
     &\longrightarrow& \mathbf{B}H
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{J}}} && \downarrow
     \\
     \ast &\longrightarrow& \mathbf{B}G_{conn} &\longrightarrow& \mathbf{B}G
  }
$$

is a [[homotopy pullback]]. From this the [[pasting law]] implies that in the top left corner we have indeed $G/H$, this being the [[homotopy fiber]] of $\mathbf{B}H \to \mathbf{B}G$. Similar considerations show that the top left map is the abstractly defined [[Maurer-Cartan form]].

=--

+-- {: .num_example}
###### Example


For $G$ a [[semisimple Lie group|semisimple]] [[compact Lie group|compact]] [[Lie group]] and $H = T\hookrightarrow G$ a [[maximal torus]], then prop. \ref{MCFormAsFiberOfDifferentialModuli} plays a central role in the stacky formulation of the [[orbit method]]. See there at _[this proposition](orbit+method#ThetaAsHomotopyFiberOfJ)_.

=--

We need this and one more ingredient for synthetically formalizing Cartan connections:

+-- {: .num_remark #FactorizationOfConnection}
###### Remark

Let $\mathbb{D}^d_x \hookrightarrow X$ be the first-oder [[infinitesimal neighbourhood]] of a point in a manifold $X$. This being first order means that every [[differential p-form]] for $p \geq 2$ vanishes on $\mathbb{D}^d$. In particular therefore every [[principal connection]] restricted to $\mathbb{D}^d$ becomes a [[flat connection]] and hence is indeed gauge equivalent to the trivial connection. In particular every map

$$
  \mathbb{D}^d_x \longrightarrow \Omega^1(-,\mathfrak{g})//H \to \mathbf{B}G_{conn}
$$

has a null-homotopy, hence fits into a square of the form

$$
  \array{
    \mathbb{D}^d_x 
      &\stackrel{\nabla_H}{\longrightarrow}& 
    \Omega^1(-,\mathfrak{g})//H
    \\
    \downarrow &\swArrow_{\mathrlap{\simeq}}& \downarrow^{\mathrlap{\mathbf{J}}} 
    \\
    \ast &\longrightarrow& \mathbf{B}G_{conn}
  }
  \,.
$$

It follows by prop. \ref{MCFormAsFiberOfDifferentialModuli} that $\nabla_H$ here factors through the [[Maurer-Cartan form]]

$$
  \nabla_H|_{\mathbb{D}^d_x}
  \;\colon\;
  \mathbb{D}^d_x 
     \stackrel{}{\longrightarrow} 
  G/H 
     \stackrel{\theta/H}{\longrightarrow}
  \Omega^1(-,\mathfrak{g})//H
  \,.
$$

=--

The following is a synthetic formulation of Cartan connections, def. \ref{Traditional}. 

+-- {: .num_defn #CartanConnectionSynthetically}
###### Definition

Let $X$ be a [[smooth set]]. Then an _$(H \hookrightarrow G)$-Cartan connection_ on $X$ is

1. a $G$-[[principal connection]] 

   $$
     \nabla \colon X \longrightarrow \mathbf{B}G_{conn}
   $$

1. equipped with a [[reduction of structure groups]] given by a lift through $\mathbf{J}$ in prop. \ref{MCFormAsFiberOfDifferentialModuli}

   $$
     \array{
        && \Omega^1(-,\mathfrak{g})//H
        \\
        & {}^{\mathllap{\nabla^H}}\nearrow & \downarrow^{\mathrlap{\mathbf{J}}}
        \\
        X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}G_{conn}
     }
   $$

1. such that over each first-order [[infinitesimal neighbourhood]] $\mathbb{D}^d_x \hookrightarrow X$ any induced factorization, via remark \ref{FactorizationOfConnection},

   $$
     \mathbb{D}^d_x \stackrel{}{\longrightarrow} G/H
   $$

   is [[formally étale morphism|formally étale]].

=--

## Weaker definitions (pre- and semi-Cartan geometry)

We discuss here some weakining of the above definition of Cartan connection that have their uses.

### Pre-Cartan geometry

...([Kuranishi 95](#Kuranishi95))...




## Examples

### Table of example
 {#TableOfExamples}

[[!include local and global geometry - table]]


### (pseudo-)Riemannian geometry

Let $G = Iso(d,1)$ be the [[Poincare group]] and $H \subset G$ the [[orthogonal group]] $O(d,1)$. Then the quotient

$$
  \mathfrak{iso}(d,1)/\mathfrak{so}(d,1) \simeq
  \mathbb{R}^{d+1}
$$

is [[Lorentzian spacetime]]. Therefore an $(O(d,1)\hookrightarrow Iso(d,1))$-Cartan connection is equivalently an $O(d,1)$-connection on a manifold whose [[tangent space]]s look like [[Minkowski spacetime]]: this is  equivalently a [[pseudo-Riemannian manifold]] from the perspective discussed at [[first-order formulation of gravity]]:

the $\mathbb{R}^{d+1}$-valued part of the connection is the [[vielbein]]. 

### $G$-Structures
 {#ExampleGStructures}

More generally, [[G-structures]] equipped with compatible principal connections are given by Cartan connections. (We will speak of "$H$-structure" here, since the reudced structure will correspond to the group denoted $H$ above, while what is denoted $G$ above will be the semidirect product of $H$ with the [[translation group]]).

Let $H \to GL(\mathbb{R}^n)$ be a [[Lie group]] [[homomorphism]], so that [[reduction of the structure group]] of the [[frame bundle]] of a manifold of [[dimension]] $n$ along this map is an [[G-structure|H-structure]] on the manifold. Then write

$$
   G \coloneqq \mathbb{R}^n \rtimes H
$$

for the [[semidirect product]] of $H$ with the [[translation group]] $\mathbb{R}^n$, given via the induced [[action]] of $H$ on $\mathbb{R}^n$ via the canonical action of the [[general linear group]] $GL(\mathbb{R}^n)$.

With this an $(H \hookrightarrow G)= (H \hookrightarrow \mathbb{R}^n \rtimes H)$-Cartan connection is equivalently an [[G-structure|H-structure]] equipped with a [[vielbein field]] and with an $H$-[[principal connection]].

([CapSlovak 09, section 1.3.6 and 1.6.1](#CapSlovak09))

With this identification the [[torsion of a Cartan connection]] maps into the [[torsion of a G-structure]].

## Related concepts

* [[connection on a bundle]]

  * [[parallel transport]], [[holonomy]]

* [[principal connection]]

  * [[affine connection]], [[Levi-Civita connection]], **Cartan connection**

* [[connection on a 2-bundle]]

* [[connection on an ∞-bundle]]

  * [[higher Cartan geometry|∞-Cartan connection]]

  * [[higher parallel transport]]




## References
 {#References}

The idea originates in [[Élie Cartan]]'s "method of moving frames" (cf. [[Cartan geometry]]).

* {#Cartan23} [[Élie Cartan]] _Sur les vari&#233;t&#233;s &#224; connexion affine et la th&#233;orie de la relativit&#233; g&#233;n&#233;ralis&#233;e (premi&#232;re partie)_. Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 3, 40 (1923), p. 325-412  ([NUMDAM](http://www.numdam.org/item?id=ASENS_1923_3_40__325_0))

The formalization in terms of [[principal connections]] (in their incarnation as [[Ehresmann connections]]) is due to

* {#Ehresmann50} [[Charles Ehresmann]], _Les connexions infinitesimales dans un espace fibre diff&#180;erentiable_, Colloque de topologie de Bruxelles, 1950, p. 29&#8211;55.

reviewed in 

* {#Marle14} [[Charles-Michel Marle]], _The works of Charles Ehresmann on connections: from Cartan connections to connections on fibre bundles_ ([arxiv:1401.8272](http://arxiv.org/abs/1401.8272))

Textbook accounts include

* {#Sharpe97} R. Sharpe, _Differential Geometry -- Cartan's Generalization of Klein's Erlagen program_ Springer (1997)

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]], chapter 1 of _Parabolic Geometries I -- Background and General Theory_, AMS 2009

Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

 
See also

* {#Kuranishi95} [[Masatake Kuranishi]], _CR geometry and Cartan geometry_, Forum mathematicum (1995) Volume: 7, Issue: 2, page 147-206 ([EuDML page](https://eudml.org/doc/186418), [page with link to pdf](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=PPN481110151_0007&DMDID=dmdlog11))

* [[Dmiti Alekseevesky]], [[Peter Michor]], _Differential geometry of Cartan connections_ Publ. Math. Debrecen 47/3-4 (1995), 349-375 ([pdf](http://www.mat.univie.ac.at/~michor/cartan.pdf))



Further discussion of Cartan connections as models for the [[first order formulation of gravity]] is in 

*  [[Derek Wise]], _MacDowell-Mansouri gravity and Cartan geometry_, Class.Quant.Grav.27:155010,2010 ([arXiv:gr-qc/0611154](http://arxiv.org/abs/gr-qc/0611154/))

* [[Gabriel Catren]], _Geometrical Foundations of Cartan Gauge Gravity_ ([arXiv:1407.7814](http://arxiv.org/abs/1407.7814))

See also

* wikipedia [Cartan connection](http://en.wikipedia.org/wiki/Cartan_connection)


[[!redirects Cartan connections]]