
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

  such that $\hat g_{i j}(x,0 ) = e$ is the identity in $g$, and such that such that \hat g_{i j}(x,1) = g_{i j}(x)$;

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
      \searrow^{\mathrlap{\hat g_{j k}}}
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


**Proposition**

The [[Cech cohomology]] cocycle with coefficients in $\mathbf{B}^3 \mathbb{R}/\mathbb{Z}$ which is given by

$$
  c(g)_{i j k l} := \int_{\Delta^3} \hat g_{i j k l}^* \mu \;\; mod \mathbb{Z} 
$$

is well defined and represents the class $c(P) \in H^4(X)$ in [[integral cohomology]]. 

Moreover, this refine to the Cech-[[Deligne cohomology]] given by

$$
  \left(
     CS(\sigma_i^* A)
     \,,\;\;
     \int_{\Delta^1} CS(\hat g_{i j}^* A)
     \,,\;\;
     \int_{\Delta^2} CS(\hat g_{i j k}^* A)
     \,,\;\;
     \int_{\Delta^3} \hat g_{i j k l}^* \mu
  \right)
$$

where

* $A \in \Omega^1(P,\mathfrak{g})$ is the incarnation of the connection $\nabla$ as an [[Ehresmann connection]] given by a gllobally defined 1-form on $A$;

* $\sigma_i : U_i \to P$ are the local [[section]]s of $P \to X$ that induce the original Cech cocycle $(g_{i j} := \sigma_i \cdot \sigma_j^{-1})$;

* $CS(...)$ denotes the [[Chern-Simons form]] of the given $\}mathfrak{g}$-valued 1-form


+-- {: .proof}
###### Proof

First notice that this is indeed well-defined: by compactness and simplicty of $G$ we have$\pi_3(G) = \mathbb{Z}$. By assumption on $\mu \in \Omega^3(G)$ we have that for any map $f : S^3 \to G$ we have $\int_{S^3} f^*\mu \in \mathbb{Z} \subset \mathbb{R}$. This implies that $c(g)$ is indeed a Cech cocycle.


Then the proof is effectively just the observation that the given collection of differential forms indeed does refine this to a Deligne cocycle, and that therefore we can read off the image of the integral cohomoloy class $[c(g)]$ in de Rham cohomology from the curvature 4-form of this Deligne cocycle. That is by construction $\langle F_\nabla \wedge F_\nabla \rangle \in \Omega^4_{cl}(X)$, which by [[Chern-Weil theory]] is indeed the image of the claimed integral class.

=--

So the only mystery about this construction is really: where does it come from? Apart from making this clever Ansatz and checking that it works, can one somehow systematically derive this construction? This we shall try to answer the section [below](#InInfChernWeil).



### In $\infty$-Chern-Weil theory {#InInfChernWeil}

Here we describe the construction of $\hat c(\nabla)$ in terms of the general methods described at [[∞-Chern-Weil theory]].

Let $\mathfrak{g} = \mathfrak{so}$ be the [[Lie algebra]] of the [[special orthogonal group]]. Write $P = \langle -,-\rangle \in W(\mathfrak{g})$ for the canonical binary [[invariant polynomial]].

The corresponding [[Lie algebra cohomology|3-cocycle]] is $\mu : \mathfrak{so} \to b^2 \mathbb{R}$

$$
  \mu = \langle -, [-,-]\rangle \in CE(\mathfrak{g})
  \,.
$$

As a Lie algebra cocycle it is the one that classifies the [[nLab:string Lie 2-algebra]] extension $\mathfrak{string} \to \mathfrak{o} \to b^2$

Reecall first the [[Lie integration]] of this bare cocycle:

The simply connected Lie group $G = Spin$ corresponding to $\mathfrak{g}$ has $\pi_2(G) = 0$ and $\pi_3(G) = \mathbb{Z}$. The Lie integrated model for $\mathbf{B}G$ on which the cocycle integrates is

$$
  \mathbf{B}G \stackrel{\simeq}{\leftarrow}
  \mathbf{cosk}_3 (\exp(\mathfrak{g})
  =
  \mathbf{cosk}_3(
  (U,[k]) \mapsto 
  \Omega^1_{flat}(\Delta^k,\mathfrak{g}) \otimes C^\infty(U))
  )
  \,.
$$

The weak equivalence to $\mathbf{B}G$ is given by [[nLab:parallel transport]]: it sends a flat $\mathfrak{g}$-valued form $A = \lambda d t$ with $\lambda \in C^\infty(U,\mathfrak{g})$ to the group element $P \exp(\int_0^1 \lambda d t)$.

Two such 1-forms $\lambda d t$ and $\lambda' d t$ are equivalent in $\mathbf{cosk}_3 \exp(\mathfrak{g})$ precisely if they are the restrictions of a flat $\mathfrak{g}$-valued 1-form on the disk, which indeed, by the [[nonabelian Stokes theorem]] is the case precisely if their parallel transport coincides. By identifying the basepoint with the neutral element in $G$, flat $\mathfrak{g}$-valued 1-form on $\Delta^k$ correspond bijectively with smooth maps $\Delta^k \to G$. Since $\pi_2(G)$ vanishes, any two such flat 1-forms on disks with coinciding boundary can be filled by a 3-ball. The coskeleton operation finally identifies all 3-balls with coinciding boundary. 

The integrated cocycle

$$
  \exp(\mu)
  : 
  \mathbf{cosk}_3 \exp(\mathfrak{g})
  \to 
  \mathbf{B}^3 \mathbb{R}/\mathb{Z}
$$

sends a 3-ball $\sigma : \Delta^3 \to G$ to the integral of $\mu$ over it

$$
  \exp(\mu) : \sigma \mapsto \int_{\Delta^3} \sigma^* \mu \; mod \mathbb{Z}
  \,.
$$

Now given a Cech cocycle $\{g_{i j}\}$ for a $G$-bundle, we may always find a refined cover $\{U_i \to X\}$ on which the cocycle lifts to this resolution

$$
  \array{
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

Choosing $\hat g$ amounts to

1. choosing on each double intersection $U_{i} \cap U_j$ a smooth based family of paths $\hat g_{i j} : U_i \cap U_j \times \Delta^1 \to G$ such that $\hat g_{i j}(0) = e$ and $\hat g_{i j}(1) = g_{i j}$;

1. choosing on each triple intersection a smooth family of based disks $\hat g_{i j k} : U_i \cap U_j \cap U_k \times \Delta^2 \to G$ in $G$, cobounding these paths.

1. choosing on each quadruple intersection a smooth family of based balls $\hat g_{i j k l} : U_i \cap U_j \cap U_k \cap U_l \times \Delta^3 \to G$ in $G$, cobounding these disks, or rather their homotopy class, relative boundaries, $[\hat g_{i j k l}]$.

That these choices exist locally, and hence for sufficiently refined cover $\{U_i \to X\}$ is the fact that $\pi_0(G) = *$ and $\pi_1(G) = 0$ and $\pi_2(G) = 0$, which is essential part of the statement that the morphism $\mathbf{B}G \stackrel{\simeq}{\leftarrow} \exp(\mathfrak{g})/_{\sim_3}$ that we are lifting through is indeed a weak equivalence.

The characteristic class corresponding to the Lie integated cocycle $\exp(\mu)$ is then modeled by the morphism

$$
  \array{
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    &\stackrel{\exp(\mu)}{\to}&
    \exp(b^2 \mathbb{R})_{\sim_3 / \mathbb{Z}}
    \\
    & {}^{\hat g}\nearrow & \downarrow^{\mathrlap{\simeq}} && 
    \downarrow^{\mathrlap{\simeq}}
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G && \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
  }
$$

which on quadruple intersections takes $[\hat g_{i j k l}]$ to $\int_{\Delta^3} \hat g_{i j k l}^* \mu  mod \; \mathbb{Z}$.

This [[Cech cohomology]] model for $\frac{1}{2}p_1$ is the one discussed [above](#InCechDelineCohomology).

We now further resolve this model in order to lift the characteristic class to differential cohomology.

$$
  \array{
     && 
     \exp(\mathfrak{g} \to inn(\mathfrak{g}))/_{\sim_3,\mathbb{Z}}
     &\stackrel{\exp(\mu,P)}{\to}&
     \exp(b^2 \mathbb{R} \to inn(b^2 \mathbb{R}))/_{\sim_3,\mathbb{Z}}
    &\to&
    \exp(* \to b^3 \mathbb{R})
    \\
    &{}^{\mathllap{\hat \nabla}}\nearrow& \downarrow^{\mathrlap{\simeq}} 
    && \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    && \exp(\mathfrak{g})_{\sim_3, \mathbb{Z}}
    &\stackrel{\exp(\mu)}{\to}&
    \exp(b^2 \mathbb{R})_{\sim_3 / \mathbb{Z}}
    && \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)_{simp}
    \\
    & {}^{\hat g}\nearrow & \downarrow^{\mathrlap{\simeq}} 
    && \downarrow^{\mathrlap{\simeq}}
    && \downarrow^{\mathrlap{\simeq}}
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G && \mathbf{B}^3 \mathbb{R}/\mathbb{Z}
   && \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)_{chn}
  }
  \,.
$$

For the connection $\hat \nabla$ we need to choose

1. $\mathfrak{g}$-valued 1-forms $A_i \in \Omega^1(U_i, \mathfrak{g})$;

1. $\mathfrak{g}$-valued 1-forms $\hat A_{i j} = A_{i j} + \lambda_{i j} \in \Omega^1(U_{i j} \times \Delta^1)$ whose restriction $\lambda_{i j}$ to $\Delta^1$ is the given path in $G$;

1. etc.

Recall that we say this forms a _genuine_ connection if the coresponding [[curvature]] 2-forms have no component along the simplices.

We can build a genuine connection $\hat \nabla$ from the cocycle $\{g_{i j}, A_i\}$ for an ordinary connection 
on the underlying ordinary cocycle $g_{i j}$: take $\hat A_{i j}(0) = A_i$ and then let $\hat A_{i j}$ be the unique solution to the differential equation

$$
  \frac{\partial}{\partial t} A_{i j}
  =
  d \lambda_t + [\lambda_t, \hat A_{i j}]
  \,.
$$

This is precisely the condition that he curvature 2-form has no component along the 1-simplex.

In other words, if $\hat g_{i j} : U_{i j } \times \Delta^1 \to G$ is the path obtained from parallel transport of $\lambda$, then we set

$$
  A_{i j}(t) := \hat g_{i j}(t)^{-1} (A_i + d) \hat g_{i j}(t)
  \,.
$$

Notably, by the fact that $\{A_i, g_{i j}\}$ is assumed to be a cocycle for an ordinary connection, this way we have

$$
  A_{i j}(1) = g_{i j}^{-1} (A_i + d) g^{i j} = A_j
 \,.
$$

Similarly we may transport the connection 1-forms around over the higher simplices to obtain $\hat A_{i j k}$ and $\hat A_{i j k l}$. This defines a lift $\hat \nabla : C(\{U_i\}) \to \exp(\mathfrak{g} \to inn(\mathfrak{g}))/_{\sim_3, \mathbb{Z}}$.

By collecting all this data, we find

+-- {: .un_prop }
###### Proposition

The composite morphism

$$
  C(\{U_i\})
  \stackrel{\hat \nabla}{\to}
  \exp(\mathfrak{g} \to inn(\mathfrak{g})/_\sim
  \stackrel{\exp(\mu,P)}{\to}
  \exp(b^2 \mathbb{R} \to inn(b^2 \mathbb{R})/_\sim
  \stackrel{\int_{\Delta^\bullet}}{\to}
  \mathbf{B}^3 U(1)_{diff}
$$

is the Cech-Deligne cocycle

$$
  (CS(A_i), \int_{\Delta^1} CS(\hat A_{i j} ), \int_{\Delta^2} CS(\hat A_{i j k}), \int_{\Delta^3} \mu(A_{i j k l}))
  \,.
$$


This is is exactly equal to the cocycle discussed [above](#InCechDelineCohomology). 

=--






### As a bundle 2-gerbe

See ([CJMS](#CJMS), [Waldorf CS](#WaldorfCS)) (...)

## References

### Cech-Deligne cohomology

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

* [[Alan Carey]] and [[Stuart Johnson]] and [[Michael Murray]] and [[Danny Stevenson]] and [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ Communications in Mathematical Physics, 259 (3). (2005) ([arXiv]())
{#CJMS}

This was later refined in 

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

Here are some slides from talks:

* [[Konrad Waldorf]], _Multiplicative gerbes and Chern-Simons theory_ ([pdf](http://www.konradwaldorf.de/docs/bonn.pdf))
{#WaldorfCS}

* [[Krzysztof Gawedzki]], _Wess-Zumino-Witten and Chern-Simons theories for non-simply connected Lie groups_ ([pdf](http://dftuz.unizar.es/ftzar/activities/highenergy09_talks/gawedzki.pdf))

[[!redirects Chern-Simons 2-gerbes]]