

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
* automatic table of contents goes here
{:toc}

## Idea

A _Chern-Simons 2-gerbe_ is a cocycle in degree 4 [[ordinary differential cohomology]] that is canonically associated to a $G$-[[principal bundle]] with [[connection on a bundle|connection]].

For $G$ a [[Lie group]] and $c : \mathcal{B}G \to K(\mathbb{Z},4)$ a cocycle for a degree 4 [[characteristic class]] in [[integral cohomology]] and $X$ a [[smooth manifold]], [[Chern-Weil theory]] provides a morphism (the refined [[Chern-Weil homomorphism]])

$$
  \hat c : G Bund_\nabla(X) \to H_{diff}^4(X)
$$

from $G$-[[principal bundle]]s with [[connection on a bundle|connection]] $\nabla$ to degree 4 [[ordinary differential cohomology]]. The cocycles on the right may be thought of as

* [[circle n-bundle with connection|circle 3-bundles with connection]] $\hat c(\nabla)$;

* [[bundle gerbe|bundle 2-gerbe]]s with connection.

By construction, the [[curvature]] 4-form of $\hat c(\nabla)$ is the [[curvature characteristic form]] $\langle F_\nabla \wedge F_\nabla\rangle$ of $\nabla$ and accordingly the 3-form connection on $\hat c(\nabla)$ is locally a [[Chern-Simons form]] $CS(\nabla)$ of $\nabla$.

Accordingly, the [[parallel transport]] induced by $\hat c(\nabla)$ over 3-dimensional manifolds $\phi : \Sigma \to X$ is the [[action functional]] of the [[quantum field theory]] called [[Chern-Simons theory]]. In this form it appears for instance as the [[gauge field]] called the [[supergravity C-field]] in certain [[supergravity]] theories. In particular, if (with due care) one takes $\nabla$ to be the _universal connection on the $G$-[[universal principal bundle]]_ over a smooth version of $B G$, then $\hat c(\nabla)$ is the background [[gauge field]] for bare [[Chern-Simons theory]].

Therefore this structure $\hat c(\nabla)$ has become known as the **Chern-Simons 2-gerbe**  of $\nabla$. We may also think of it as the _Chern-Simons [[circle n-bundle with connection|circle 3-bundle]]_ .

At least for simply connected $G$ one may enhance the assignment $\nabla \mapsto \hat c(\nabla)$ to a morphism of [[∞-groupoid]]s

$$
  \hat \mathbf{c} : \mathbf{H}_conn(X,\mathbf{B}G)
  \to \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  \,,
$$

where on the left we have the [[groupoid]] of smooth $G$-principal bundles with connection on $X$, and on the right the 3-groupoid of circle 3-bundles with connection. The [[homotopy fiber]]s of this morphism over a trivial circle 3-bundle with connection are 3-groupoids whose objects are naturally identified with pairs consisting of a connection $\nabla$ on a $G$-bundle and a _trivialization_ of its corresponding Chern-Simons 3-bundle. This in particular implies a trivialization of the underlying cocycle in degree 4 [[integral cohomology]] and therefore defines a [[string structure]]. One calls these homotopy fibers therefore [[differential string structure]]s.


## Constructions

### In Cech-Deligne cohomology {#InCechDelineCohomology}

In ([Brylinski-McLaughlin I](#GeomConstructionFirst)) is spelled out an explicit constructin of $\hat c(\nabla)$ for given $\nabla$ in [[Cech cohomology|Cech]]-[[Deligne cohomology]]. This is a special case of the general construction presented in ([Brylinski-McLaughlin II](#CechCocyclesForCharClasses)).


In this section here we review this exlicit cocycle construction. In the [next section](#InInfChernWeil) we discuss a systematic way to derive this construction.


Assume that $G$ is a [[simply connected]] compact simple [[Lie group]] such as the [[spin group]] and take the characteristic class $c$ to be that whose [[transgression]] to $G$ has as image in [[de Rham cohomology]] the de Rham class of the normalized canonical [[Lie algebra cohomology|Lie algebra cocycle]] $\mu \in CE(\mathfrak{g})$.


For $P \to X$ a $G$-bundle with connection $\nabla$, there exists an [[open cover]] $\{U_i \to X\}$ such that we have a [[Cech cohomology]] cocycle for $P$ given by a smooth transition function

$$
  g_{i,j} : U_i \cap U_j \to G 
$$ 

satisfying on $U_i \cap U_j \cap U_k$ the cocycle condition $g_{i j} \cdot g_{j k} = g_{i k}$.

Since $G$ is assumed connected and [[simply connected]] and since for every Lie group the second [[homotopy group]] is trivial we have that the first nonvanshing homotopy group of $G$ is the third one. 

Therefore we can always find (possibly after refining the cover) a lift of this cocycle as follows:

* on double intersections, choose smooth functions

  $$
    \hat g_{i j} : (U_i \cap U_j) \times \Delta^1 \to G
  $$

  such that $\hat g_{i j}(x,0 ) = e$ is the identity in $g$, and such that such that $\hat g_{i j}(x,1) = g_{i j}(x)$;

* on triple intersections, choose smooth functions

  $$
    \hat g_{i j k} : (U_i \cap U_j \cap U_k) \times \Delta^2 \to G
  $$

  that cobound these paths in the evident way

  $$
    \array{
      && g_{i j}
      \\
      & {}^{\mathllap{\hat g_{i j}}}\nearrow 
      &\Downarrow^{\mathrlap{\hat g_{i j k}}}& 
      \searrow^{g_{i j} \cdot \mathrlap{\hat g_{j k}}}
      \\
      e &&\underset{\hat g_{i k}}{\to}&& g_{i k}
    }
  $$

  (this can be done because $\pi_1(G) = *$)

* on quadruple intersection choose smooth functions

  $$
    \hat g_{i j k l} : (U_i \cap U_j \cap U_k \cap U_l) \times \Delta^3  \to G
  $$

  such that these 3-balls fill the evident tetrahedra.

  (this can be done because $\pi_2(G) = 0$).


+-- {: .un_prop }
###### Proposition

The [[Cech cohomology]] cocycle with coefficients in $\mathbf{B}^3 \mathbb{R}/\mathbb{Z}$ which is given by

$$
  c(g)_{i j k l} := \int_{\Delta^3} \hat g_{i j k l}^* \mu 
  \;\;\;\;\; mod \mathbb{Z} 
$$

is well defined and represents the class $c(P) \in H^4(X)$ in [[integral cohomology]]. 

Moreover, this refines to the cocycle in Cech-[[Deligne cohomology]] that is given by

$$
  \left(
     CS(\sigma_i^* A)
     \,,\;\;
     \int_{\Delta^1} CS((P\cdot \hat g_{i j})^* A)
     \,,\;\;
     \int_{\Delta^2} CS((P\cdot \hat g_{i j k})^* A)
     \,,\;\;
     \int_{\Delta^3} \hat g_{i j k l}^* \mu
     \;\;\; mod \mathbb{Z}
  \right)
  \,,
$$

where

* $A \in \Omega^1(P,\mathfrak{g})$ is the incarnation of the connection $\nabla$ as an [[Ehresmann connection]] given by a glbally defined 1-form on the total space $P \to X$ of the bundle;

* $\sigma_i : U_i \to P$ are the local [[section]]s of $P \to X$ that induce the original Cech cocycle $(g_{i j} := \sigma_i \cdot \sigma_j^{-1})$;

* $P \cdot \hat g_{i j} : \Delta^1 \to P$ is given by the right [[action]] of $G$ on $P$ and analogously for the other terms;

* $CS(...)$ denotes the [[Chern-Simons form]] of the given $\mathfrak{g}$-valued 1-form.

=--

+-- {: .proof}
###### Proof

First notice that this is indeed well-defined: by compactness and simplicty of $G$ we have$\pi_3(G) = \mathbb{Z}$. By assumption on $\mu \in \Omega^3(G)$ we have that for any map $f : S^3 \to G$ we have $\int_{S^3} f^*\mu \in \mathbb{Z} \subset \mathbb{R}$. This implies that $c(g)$ is indeed a Cech cocycle.

Then the proof is effectively just the observation that the given collection of differential forms indeed does refine this to a Cech-cocycle with coefficients in the Deligne complex, and that therefore we can read off the image of the integral cohomoloy class $[c(g)]$ in de Rham cohomology from the curvature 4-form of this Deligne cocycle. That is by construction $\langle F_\nabla \wedge F_\nabla \rangle \in \Omega^4_{cl}(X)$, which by [[Chern-Weil theory]] is indeed the image of the claimed integral class.

=--

So the only mystery about this construction is really: where does it come from? Apart from making this clever Ansatz and checking that it works, can one somehow systematically derive this construction? This we shall try to answer the section [below](#InInfChernWeil).



### In $\infty$-Chern-Weil theory {#InInfChernWeil}

The above Cech-Deligne cocycle construction of $\hat c(\nabla)$ may be understood as a special case of the general construction of Chern-Weil homomorphism by the methods discussed at [[∞-Chern-Weil theory]]. 

We briefly recall the general approach and then spell out the details.

The basic ingredients in [[∞-Chern-Weil theory]] that give the refinement of a [[characteristic class]] to a morphism

$$
  \mathbf{H}_{conn}(X,\mathbf{B}G) \to \mathbf{H}_{diff}(X, \mathbf{B}^k U(1))
$$

from the $G$-principal bundles with connection to [[ordinary differential cohomology]] are this:

1. for a given [[Lie algebra]] $\mathfrak{g}$ the realization of the corresponding [[Lie group]] as a truncation of the simplicial presheaf

   $$
     (U,[n]) \mapsto \{C^\infty(U)\otimes \Omega^\bullet(\Delta^n) \leftarrow CE(\mathfrak{g})\}
   $$

   (see [[Lie integration]]);

1. the observation that, up to subtleties with the truncation, a [[Lie algebra cohomology|Lie algebra cocycle]] 

   $$
     CE(\mathfrak{g}) \leftarrow CE(b^{k-1}\mathbb{R}) : \mu
   $$

   induces therefore an integrated cocycle $\mathbf{B}G \to \mathbf{B}^k U(1)$;

1. the observation that this is lifted to connections and differential refinement by 

   1. thickening the simplicial presheaf for $\mathbf{B}G$ to

      $$
        (U,[n]) \mapsto
        \left\{
          \array{
              C^\infty(U) \otimes \Omega^\bullet(\Delta^n)
              &\stackrel{}{\leftarrow}&
              CE(\mathfrak{g})
              \\
              \uparrow && \uparrow
              \\
              \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^n)
              &\stackrel{A}{\leftarrow}&
              W(\mathfrak{g})
          }
        \right\}
      $$

   1. thickening the Lie algebra cocycle by its [[invariant polynomial]]
      and Chern-Simons element
 
      $$
        \array{
           CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{k-1}\mathbb{R})
           \\
           \uparrow && \uparrow
           \\
           W(\mathfrak{g}) &\stackrel{(cs,\langle -\rangle)}{\leftarrow}&
           W(b^{k-1} \mathbb{R})
        }
      $$

   and then postcomposing with that.


For the case at hand, let $\mathfrak{g}$ be a [[semisimple Lie algebra]], $\langle -\rangle \in W(\mathfrak{g})$ its canonical [[Killing form]] [[invariant polynomial]], $\mu = \langle -,[-,-]\rangle \in CE(\mathfrak{g})$ the corresponding [[Lie algebra cohomology|Lie algebra cocycle]], $cs \in W(\mathfrak{g})$ the Chern-Simons elements exhibiting the transgression betweemn the two, $G$ the [[simply connected]] [[Lie group]] [[Lie integration|integrating]] it.

First consider the bare cocycle for the Chern-Simons circle 3-bundle as the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">Lie integration of the cocycle </a> $\mu$.


+-- {: .un_def }
###### Definition

Consider the [[simplicial presheaf]]

$$
  \exp(\mathfrak{g}) : (U,[n]) 
   \mapsto 
  \{C^\infty(U) \otimes \Omega^\bullet(\Delta^n) \leftarrow CE(\mathfrak{g})\} 
  \,,
$$

where here and in the following differential forms $\omega$ on simplices are taken to have _sitting instants_ in that for all $k \in \mathbb{N}$ there exists for every $k$-face of $\Delta^n$ an open neighbourhood such that $\omega$ restricted to that open neighbourhood is constant in the direction perpendicular to the boundary.

=--

+-- {: .un_lemma }
###### Lemma

The canonical map 

$$
  \mathbf{cosk}_3 \exp(\mathfrak{g}) \to \mathbf{B}G
$$

from the 3-[[coskeleton]] of $\exp(\mathfrak{g})$ to the [[delooping]] of the simply connected Lie group $G$ which is given on 1-morphisms by [[parallel transport]] is an equivalence ( in the [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj}$).

=--

+-- {: .proof}
###### Proof


Use that a $\mathfrak{g}$-valued 1-form on the interval is canonically identified with a based path in $G$. Then use that for $k \leq 2$ we have $\pi_k(G) = 0$. See [[Lie integration]] for more.

=--


+-- {: .un_prop }
###### Proposition

There is a commuting diagram

$$
  \array{
    \exp(\mathfrak{g}) &\stackrel{\exp(\mu)}{\to}& \exp(b^2 \mathbb{R})
    \\
    \downarrow && \downarrow^{\mathrlap{\int_{\Delta^\bullet}}}
    \\
    \mathbf{cosk}_3 \exp(\mathfrak{g}) &\stackrel{}{\to}&
    \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
  }  
  \,,
$$

where the right vertical morphism is the composite of the equivalence

$$
  \int_{\Delta^\bullet}  : \exp(b^2 \mathbb{R}) \stackrel{\simeq}{\to} \mathbf{B}^3 \mathbb{R}
$$

discussed at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfBnR">Integration to Line n-groups</a> with the evident quotient $\mathbf{B}^3 \mathbb{R} \to \mathbf{B}^3 \mathbb{R}/\mathbb{Z}$, where the copy of $\mathbb{Z}$ in $\mathbb{R}$ is the lattice of periods of $\mu$ over 3-speheres in $G$.

=--

The top morphism sends a $U$-family of 3-morphisms $C^\infty(U) \otimes \Omega^\bullet(\Delta 3) \stackrel{A}{\leftarrow} CE(\mathfrak{g})$ -- which we may  think of as a $U$-family of based 3-balls $\Sigma : U \times \Delta^3 \to G$ -- to the family of 3-forms

$$
  C^\infty(U) \otimes \Omega^\bullet(\Delta 3) \stackrel{\Sigma}{\leftarrow} CE(\mathfrak{g})
  \stackrel{\mu}{\leftarrow}
  CE(b^2 \mathbb{R})
  : 
  \mu(A)
  \,.
$$

The right vertical morphism sends this to the [[fiber integration]]

$$
  U \mapsto \int_{\Delta^3} \mu(A) \;\;\; \in \mathbb{R} 
$$

and regards the result then modulo $\mathbb{Z}$. That this indeed gives a morphism down at the bottom is the statement that for a 4-morphism in $\mathbf{cosk}_3 \exp(\mathfrak{g})$ -- which is a 3-sphere $V : S^3 \to G$ -- we have that $\int_{S^3} V^* \mu(A) = 0 \;mod\; \mathbb{Z}$, which is true by the fact that we take $\mathbb{Z}$ to be precisely generated by these periods. (Alternatively we can assume $\mu$ to be  normalized such that it generates the image in deRham cohomology of $H^3(G,\mathbb{Z}) \simeq \mathbb{Z}$).

We shall by slight abuse of notation write $\exp(\mu)$ also for the morphism $\mathbf{cosk}_3 \exp(\mathfrak{g}) \to \mathbf{B}^3 \mathbb{R}/\mathbb{Z}$.


+-- {: .un_lemma }
###### Observation

For $\{U_i \to X\}$ a [[cover]] and $C(U) \in [CartSp^{op}, sSet]_{proj}$ the corresponding [[Cech nerve]] we have that

* a morphism $g : C(U) \to \mathbf{B}G$ is precisely a Cech 1-cocycle with values in $G$;

* a lift

  $$
    \array{
       && \mathbf{cosk}_3 \exp(\mathfrak{g})
       \\
       & {}^{\mathllap{\hat g}}\nearrow & \downarrow^{\mathrlap{\simeq}}
       \\
       C(U) &\stackrel{g}{\to}& \mathbf{B}G
    }
  $$

  is precisely a lift of this cocycle to a system of paths, triangles and tetrahedra in $G$, as [above](#InCechDelineCohomology).

=--

+-- {: .un_def }
###### Definition

Write $\exp(\mathfrak{g})_{diff}$ for the [[simplicial presheaf]]

$$
  (U,[n]) \mapsto
  \left\{
    \array{
      C^\infty(U)\otimes \Omega^\bullet(\Delta^n)
      &\stackrel{}{\leftarrow}& CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      W(\mathfrak{g})
    }
  \right\}
  \,.
$$

=--

Its 3-[[coskeleton]] $\mathbf{cosk}_3 \exp(\mathfrak{g} \to inn(\mathfrak{g}))$ is the coefficient for $G$-principal bundles with [[pseudo-connection]] adapted to the model $\mathbf{cosk}_3 \exp(\mathfrak{g})$ for $\mathbf{B}G$.

+-- {: .un_lemma }
###### Lemma

Pseudo-connections $\hat \nabla$

$$
  \array{
    && \mathbf{cosk}_3 \exp(\mathfrak{g})_{diff}
    \\
    &{}^{\mathllap{\hat \nabla}}\nearrow& \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathbf{cosk}_3 \exp(\mathfrak{g})
    \\
    & {}^{\mathllap{\hat g}}\nearrow & \downarrow^{\mathrlap{\simeq}}
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

which are _genuine_ $\infty$-connections in that their curvature components have no leg along the simplicial directions are in bijection with ordinary connections on the $G$-bundle given by $C(U) \to \mathbf{B}G$.

=--

+-- {: .proof}
###### Proof

On single patches $\hat \nabla$ is a collection of $\mathfrak{g}$-valued 1-forms $A_i \in \Omega^1(U_i, \mathfrak{g})$.


On double intersection it is a collection

$$
  \hat A_{i j} = A_{i j} + \lambda_{i j} \in 
  \Omega^1(U_i \cap U_j, \mathfrak{g})\otimes C^\infty(\Delta^1) \oplus
   C^\infty(U)\otimes \Omega^1(\Delta^1, \mathfrak{g})
  \subset \Omega^1(U_i \cap U_j  \times \Delta^1, \mathfrak{g})
$$

whose restriction $\lambda_{i j}$ to $\Delta^1$ is the given path $\hat g_{i j}$ that is being covered. The condition that the curvature of $\hat A_{i j}$ has no component in the simplicial direction is the [[differential equation]]

$$
  \frac{\partial}{\partial t} A_{i j} = d_U (\lambda_{i j})_t + [(\lambda_{i j})_t, A_{i j}]
 \,.
$$

This differential equation has a unique solition for the boundary condition $A_{i j}(0) = A_i$ given by

$$
  A_{i j}(t) = \hat g_{i j}(t)^{-1}(A_i + d)\hat g_{i j}(t)
  \,.
$$

(To see this, use the formulas from [[parallel transport]]. If we assume just for notational simplicity that we are dealing with a [[matrix Lie algebra]] then we have $\frac{\partial}{\partial t} \hat g_{i j} = \hat g_{i j} \cdot \lambda$ (by definition) and using that the claim follows.)

In particular this implies  the forms on single patches satisfy the ordinary cocycle relation

$$
  A_{i j}(1) = A_j = g_{i j}^{-1}(A_i + d)g_{i j}
$$

for connections. 

Similarly there are differential equations on 2-simplices and 3-simplices with unique solutions.

=--


+-- {: .un_lemma }
###### Observation

Pasting postcomposition with the diagram

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^2 \mathbb{R})
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{(cs,\langle \rangle)}{\leftarrow}& 
     W(b^2 \mathbb{R})
  }
$$

indudes a morphism $\exp(\mathfrak{g})_{diff} \to \exp(b^2\mathbb{R})_{diff}$ and we obtain a commuting diagram

$$  
  \array{
     \exp(\mathfrak{g})_{diff} &\to& \exp(b^2\mathbb{R})_{diff}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{cosk}_3\exp(\mathfrak{g})_{diff} &\to& 
     \mathbf{B}^3 U(1)_{chn,diff}
  }
$$

that covers the corresponding diagram we had before.

=--

Here we are using the object $\mathbf{B}^3 U(1)_{ch,diff}$ described in detail at [[circle n-bundle with connection]].

+-- {: .un_remark }
###### Remark

The deeper reason for this construction is that the zig-zag comosite 

$$
  \mathbf{B}G
  \stackrel{\simeq}{\leftarrow}
  \mathbf{cosk}_3\exp(\mathfrak{g})_{diff}
  \to 
  \mathbf{B}^3 U(1)_{diff,chn}
  \to
  \mathbf{\flat}_{dR}\mathbf{B}^4 U(1)_{chn}
$$

of morphisms of simplicial presheaves models the intrinsically defined morphism

$$
  \mathbf{B}G \to \mathbf{\flat}_{dR}\mathbf{B}^4 U(1)
$$

in the [[(∞,1)-topos]] [[?LieGrpd]].

=--


+-- {: .un_prop }
###### Proposition

The outer composite morphism

$$
  \array{
    && \mathbf{cosk}_3 \exp(\mathfrak{g})_{diff}
    &\stackrel{\exp((cs,\langle -\rangle))}{\to}&
    \mathbf{B}^3 U(1)_{diff}
    \\
    &{}^{\mathllap{\hat \nabla}}\nearrow& \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathbf{cosk}_3 \exp(\mathfrak{g})
    \\
    & {}^{\mathllap{\hat g}}\nearrow & \downarrow^{\mathrlap{\simeq}}
    \\
    C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

is precisely the Cech-Deligne cocycle

$$
  (CS(A_i), \int_{\Delta^1} CS(\hat A_{i j} ), \int_{\Delta^2} CS(\hat A_{i j k}), \int_{\Delta^3} \mu(A_{i j k l}))
  \,.
$$


This is is exactly equal to the cocycle discussed [above](#InCechDelineCohomology). 

=--

Notice by the way that this construciton also serves as a manifest proof that this collection of data indeed does constitute a Deligne cocycle.


+-- {: .proof}
###### Proof

This is a matter of plugging the above pieces into each other. For instance on double intersections we have that the 3-form $CS(\hat A_{i j})$ is the image of the degree 3-generator on $W(b^2 \mathbb{R})$ under the composite

$$
  \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
  \stackrel{\hat A_{i j}}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{(cs,\langle -\rangle)}{\leftarrow}
  W(b^2 \mathbb{R})
  \,.
$$

The remaining fiber integration is then that exhibiting the equivalence of simplicial differential forms

$$
  \int_{\Delta^\bullet} : 
  \mathbf{\flat}_{dR} \mathbf{B}^3 U(1)_{diff,simp}
    \stackrel{\simeq}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^3 U(1)_{diff,chn}
$$

that is described in some detail at <a href="http://ncatlab.org/nlab/show/circle+n-bundle+with+connection#U1FromLieIntegration">Circle n-bundle with connection -- models from ∞-Lie integration</a>.

=--



### As a bundle 2-gerbe

We indicate (for the moment) the way the Chern-Simons 3-bundle is realized as a [[bundle 2-gerbe]] (for instance in [CJMS](#CJMS) and [Waldorf CS](#WaldorfCS)) .

One first constructs the canonical [[bundle gerbe]] $\mathcal{G} \to G$ on the Lie group and notices that (more or less implicitly by recourse to its [[delooping]] 2-gerbe on $\mathbf{B}G$) that this has a _multiplicative structure_ .

Using this one see that for $P \to X$ any $G$-[[principal bundle]] and $P^{[2]} : = P \times_X P \to P \times G$ the principality isomorphism, the pullback of $\mathcal{G}$ along 

$$
  f : P^{[2]} \to P \times G \stackrel{p_2}{\to} G
$$

serves to provide the diagram

$$
  \array{
     f^* \mathcal{G}
     \\
     \downarrow
     \\
     P^{[2]} &\stackrel{\to}{\to}& P
     \\
     && \downarrow
     \\
     && X
  }
$$

on which the pullback of the multiplicative structure on $\mathcal{G}$ induces the structure of a bundle 2-gerbe, in that we get morphisms of bundle gerbes

$$
  \mu : \pi_0^* f^* \mathcal{G} \otimes \pi_2^* f^* \mathcal \to \pi_2^* f^* \mathcal{G}
$$

that are associative up to a higher coherent morphisms, etc.

## Related concepts

* The [[higher parallel transport]] of a Chern-Simons circle 3-bundle is the [[action functional]] for [[Chern-Simons theory]].

* For the case that $G = O$ is the [[orthogonal group]] and $X \to \mathbf{B}O$ the classifying map of the [[tangent bundle]] of $X$, a trivialization of the corresponding Chern-Simons 3-bundle is a [[string structure]] on $X$. A trivialization of the Chern-Simons 3-bundle _with connection_ is a [[differential string structure]] on $X$.

## References

### The Cech-Deligne cohomology realization

As cocycles in [[Cech cohomology|Cech]]-[[Deligne cohomology]] the Chern-Simons 2-gerbe has been constructed explicitly in 

* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _A geometric construction of the first Pontryagin class_ (1993) ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-I.pdf))
{#GeomConstructionFirst}

as a special case of the general construction in 

* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _Cech cocycles for characteristic classes_ ,  Communications in Mathematical Phiysics, Volume 178, Number 1, ([Springer](http://www.springerlink.com/content/762g1m76jp6425x5/))
{#CechCocyclesForCharClasses}

### The 2-gerbe realization {#2GerbeReferences}

Conceived as a genuine [[gerbe]] the Chern-Simons 2-gerbe appears in


* [[Jean-Luc Brylinski]] and Dennis McLaughlin, _The geometry of degree-4 characteristic classes and of line bundles on loop spaces II_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-Duke-II.pdf)).

Among the first references to apply specifically [[bundle gerbe]] technology to this construction is 

* [[Alan Carey]], Stuart Johnson, [[Michael Murray]], [[Danny Stevenson]] and [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ Communications in Mathematical Physics, 259 (3). (2005) ([arXiv]())
{#CJMS}

This was later refined in 

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

Here are some slides from talks:

* [[Konrad Waldorf]], _Multiplicative gerbes and Chern-Simons theory_ ([pdf](http://www.konradwaldorf.de/docs/bonn.pdf))
{#WaldorfCS}

* [[Krzysztof Gawedzki]], _Wess-Zumino-Witten and Chern-Simons theories for non-simply connected Lie groups_ ([pdf](http://dftuz.unizar.es/ftzar/activities/highenergy09_talks/gawedzki.pdf))

