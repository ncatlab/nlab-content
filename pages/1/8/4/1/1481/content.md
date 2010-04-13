
> under construction


+-- {.standout}

  On the formalization of the process of [[quantization]] -- by [[category theory|abstract nonsense]] -- from classical [[∞-model]] data to the corresponding [[quantum field theory]] .

=--



#Contents#
* automatic table of contents goes here
{:toc}





## Background and motivation

The search is on for the abstract formalization of the process of _[[quantization]]_ -- the process that reads in a "[[classical field theory]]" -- for instance presented in form of a [[gauge theory]] or in form of a [[∞-model]] background field data -- and spits out the corresponding [[quantum field theory]].

+-- {.standout}

There is an open problem of mathematical (-[[physics]]) model building: 

* what is the true formalism behind [[quantization]]?  

One that is to quantization as, say, [[symplectic geometry]] is to [[Hamiltonian mechanics]]?

The formalism of [[FQFT]] clearly suggests that the fundamental description of [[quantization]] is some natural operation on higher functors.

=--



While for various aspects and facets of this question there are well-developed formalisms -- such as [[geometric quantization]] or [[deformation quantization]] or [[BV-BRST formalism]] -- a full answer is certainly still missing, not the least because the full formalization of the _question_ itself has still to be established.

Considerable progress on this formulation of the question has been achieved with the formalization and proof of the [[cobordism hypothesis]] in _[[On the Classification of Topological Field Theories]]_ by [[Jacob Lurie]]. This at least indicates what the _result_ of any full quantization procedure should be in that it clarifies what exactly a [[TQFT]] [[FQFT]] is: a morphism from the [[(∞,n)-category of cobordisms]] $Z : Bord_n \to C$.

In _[[On the Classification of Topological Field Theories]]_ Jacob Lurie indicates some first towards finding a similar formalization of "classical field theory" (in terms of his $(\infty,n)$-categories of "families") and a systematic procedure for turning the classical theory into the quantum theory. These thoughts were further developed in the article _[[Topological Quantum Field Theories from Compact Lie Groups]]_ . But for the moment, that, too, remains a bit sketchy.

For the purpose of the present entry this indication of a quantizaton proposal by Lurie et al. mainly serves as a reference for the idea itself that a formalization of something interesting is to be sought here, and of the kind of [[category theory|abstract nonsense]] answer one hopes to find. We will however discuss a somewhat different-looking approach. It may well be related to the Lurie-et al proposal in the end, but for the time being we shall not concentrate on that relation.

Rather, the approach for a formalization of the quantization procedure that shall be discussed at this entry here draws from a few different sources:

1. The observation that a classical background field that should serve as the input for a quantization of a $\sigma$-model that describes the dynamics of an object charged under this field is encoded by differential cocycles as as described at [[schreiber:differential cohomology in an (∞,1)-topos]].

1. The idea that by applying a pull-push quantization prescription a differential cocycle on a target space $X$ gives rise to a differential cocycle on a _parameter space_ $\Sigma$, which may be thought of as one of the bordisms appearing in the [[FQFT]]-description of quantum field theory. 

   The pull-push operation here is akin to that in [[geometric ∞-function theory]], where a [[quantum field theory]] is obtained from a [[∞-model]] target space object $X$ by homming [[extended cobordism]] [[cospan]]s $\Sigma_in \to \Sigma \leftarrow \Sigma_{out}$ into the target object and then pull-pushing [[geometric function object]]s through the resulting [[span]]s of configuration space objects $[\Sigma_{in},X] \leftarrow [\Sigma,X] \to [\Sigma_{out},X]$. 

   The main result of David Ben-Zvi et. al.'s work on this approach is that they point out that as soon as the [[geometric function object]] one uses satisfies the two [[geometric ∞-function theory|fundamental theorems of geometric infinity-function theory]], a considerable amount of rich structure that has in parts been known by itself gets unified into one coherent elegant story: the nature of partition functions (i.e. traces), of centers, of Hochschild (co)homology, Deligne-Kontsevich-statements, etc. all are understood by means of a suitable [[geometric function theory]] as induced from the underlying geometry of configuration space objects $[\Sigma,X]$ as well as the [[loop space object]]s of $X$.

   The resulting pull-push operation is an example or a generalization of what [[John Baez]] discusses under the term [[groupoidification]]. 

1. The observation that a differential coccycle on a [[Lorentzian manifold]] $\Sigma$ gives rise to a [[local net]] of observables, as used in the formalizaton of QFT known as [[AQFT]]. (As described [here](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf)).

   So the procedure discussed here regards differential cocycles on target space as classicai field theories, regards their quantization as a way to obtain a differential cocycle on Lorentzian parameter space, and identifies this as a quantum field theory by associating a local net of observables to it. 

   These local nets, in turn, are akin to [[factorization algebra]]s, which in the Euclidean (meaning non-Lorentzian setting) relate back to cobordism representations via the notion of [[topological chiral homology]]. However the -- physically crucial -- Lorentzian structure invoked here is not otherwise considered in these functorial axiomatization of quantum field theory.

## General ambient structure

The ambient context is the [[(∞,1)-topos]] $\mathbf{H} := Sh_{(\infty,1)}(CartSp)$ of [[Lie ∞-groupoid]]s and the $(\infty,2)$-topos of smooth $(\infty,1)$-categories, which we model, respectively, as the [[Bousfield localization of model categories|left Bousfield localization]] of the [[model structure on functors]] $[CartSp^{op}, sSet_{Quillen}]$ and $[CartSp^{op}, sSet^+]$, respectively, where 

* [[CartSp]] is the site of Cartesian spaces, 

* $sSet_{Quillen}$ the standard [[model structure on simplicial sets]];
 
* and $sSet^+$ the [[model structure for Cartesian fibrations]] over the points, hence the [[simplicial model category]] for quaasi-categories.

For the definition of the [[schreiber:path ∞-groupoid]] functor $\mathbf{\Pi}$ and the induced theory of [[schreiber:differential cohomology in an (∞,1)-topos]], we make use of the discussion at [[schreiber:differential cohomology in an (∞,1)-topos -- survey]].

When working with fibrant objects in the model, we will frequently use the constructions and notation from [[category of fibrant objects]]. Notably for $\mathbf{B}G$ a fibrant [[delooping]] object in the model we write $(\mathbf{B}G)^I$ for the [[path object]] we write $\mathbf{E}G$ for the [[pullback]]

$$
  \array{
    \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    (\mathbf{B}G)^I &\stackrel{d_1}{\to}& \mathbf{B}G
  }
$$

and $\mathbf{E}G \to \mathbf{B}G$ for the remaining map, induced from
$d_0 : (\mathbf{B}G)^I \to \mathbf{B}G$.

## The charged particle

We describe the general theory for the simple example of the charged
particle. 


### Target space and background field

The background field for the charged particle that we want to consider is the [[electromagnetic field]]. The data involved is

* the **target space** $X$ -- a smooth [[manifold]];

* the **structure group** or **gauge group** $G = U(1)$;

* a choice of representation

  $$
    \rho : \mathbf{B}G \to Vect_{\mathbb{C}}
    \,,
  $$

  taken to be the canonical representation on $V = \mathbb{C}$;

* the **background field** given by a 

  * a $U(1)$-[[principal bundle]] $P \to X$ classified by a [[cocycle]]
    $g : X \to \mathbf{B}U(1)$ in $\mathbf{H}$ which in the model is 
    given by an [[anafunctor]] $X \stackrel{\simeq}{\leftarrow} Y \to \mathbf{B}U(1)$;

  * a [[connection on a bundle|connection]] $\nabla$ on this bundle, 
    which in the model is given by a diagram

    $$
      \array{
         Y &\stackrel{g}{\to}& \mathbf{B}U(1)
         \\
         \downarrow && \downarrow
         \\
         \mathbf{\Pi}(Y) &\stackrel{\nabla}{\to}& 
         \mathbf{E}\mathbf{B}U(1)
      }
      \,,
    $$

    and whose [[field strength]] is given by the composite

    $$
      F : \mathbf{\Pi}(Y) \stackrel{\nabla}{\to}
      \mathbf{E}\mathbf{B}U(1) \to \mathbf{B}^2 U(1)
      \,.
    $$


### Parameter space and kinetic action

Let $\Sigma = \mathbb{R}$ be the **parameter space**, the **worldline**,
regarded as a [[Lorentzian manifold]] and write $\mathbf{\Pi}(\Sigma)$ for the [Lorentzian path category](http://ncatlab.org/nlab/show/smooth+Lorentzian+space#PathnCategory).


To define the kinetic action, we first form the $\rho$-associated background field

$$
  \array{
    X &\stackrel{g}{\to}& \mathbf{B}U(1) &\stackrel{\rho}{\to}& Vect
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\stackrel{\nabla}{\to}& \mathbf{E} \mathbf{B}U(1) 
      &\stackrel{}{\to}& \mathbf{E}\mathbf{B}U(1) \coprod_{\mathbf{B}U(1)} Vect
  }
$$

and then pull this back to the [[multisymplectic geometry|extended configuration space]] $X \times \Sigma$.

The morphisms in the [[product]] category $\mathbf{\Pi}(X) \times \mathbf{\Pi}(\Sigma)$ are paths $\gamma_X : [0,1] \to X$ in $X$ on whose base we have a (pseudo)[[Riemannian metric]], which is the pullback of the metric $\mu_\Sigma$  on $\Sigma$ along $\gamma_\Sigma : [0,1] \to \Sigma$.  We can consider the _kinetic action_ to be a differential cocycle

$$
  \array{
    \Sigma \times X 
     &\stackrel{}{\to}& \mathbf{B}U(1) &\stackrel{}{\to}& Vect
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{\Pi}(\Sigma) \times 
     \mathbf{\Pi}(X) &\to& \mathbf{E} \mathbf{B}U(1) 
      &\stackrel{}{\to}& \mathbf{E}\mathbf{B}U(1) 
      \coprod_{\mathbf{B}U(1)} Vect
  }
$$

which sends the path $\gamma_X : [0,1] \to X$ of parameter length $\gamma_\Sigma : [0,1] \to \Sigma$ to 

$$
  \mathbb{C}
    \stackrel{\exp(-\frac{1}{i \hbar}\int_{0}^1 |\gamma'_X|^2 d \gamma_\Sigma}{\to}
  \mathbb{C}
  \,.
$$


Notice that $\mathbf{\Pi}(X)\times \mathbf{\Pi}(\Sigma) \simeq \mathbf{\Pi}(X \times \Sigma)$.

### The quantization

The total action is differential cocycle

$$
  \array{
    \Sigma \times X 
    &\stackrel{}{\to}& Vect
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{\Pi}(\Sigma) \times 
     \mathbf{\Pi}(X) &\stackrel{\exp(S_{kin})tra_\nabla}{\to}& \mathbf{E}\mathbf{B}\mathbb{R} 
      \coprod_{\mathbf{B}U(1)} Vect
  }
  \,.
$$



We want to consider the diagram

$$
  \array{
    \Sigma \times X & \to&  Vect
    \\
    \downarrow & \searrow && \searrow
    \\
    \Sigma && \mathbf{\Pi}(\Sigma)\times \mathbf{\Pi}(X) &\to& \mathbf{E}\mathbf{B}U(1)\coprod_{\mathbf{B}U(1)} Vect
    \\
    & \searrow & \downarrow
    \\
    && \mathbf{\Pi}(\Sigma)
  }
$$

and use it to obtain a differential cocycle on $\Sigma$, by forming something like a lax pullback ("comma object") of the point inclusion

$$
 \array{
   * &\to& *
   \\
   \downarrow && \downarrow
   \\
   Vect &\to& Vect \coprod_{\mathbf{B}U(1)} \mathbf{E}\mathbf{B}U(1)
 }
 \,,
$$

where the left vertical morphism picks the ground field $\mathbb{C}$, along this cocycle. For the underlying cocycle this is obtained as the ordinary pullback of $\mathbf{E}Vect$ defined as the ordinary pullback

$$
  \array{
    \mathbf{E}Vect &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{k}}
    \\
    Vect^I &\stackrel{d_1}{\to}& Vect    
  }
  \,,
$$

where $I$ is the [[interval category]], $Vect^I$ the [[functor category]] and $k : * \to Vect$ picks the ground field vector space. Via the remaining map $d_0 : Vect^I \to Vect$ this maps to $Vect$ and then further to $Vect \coprod_{\mathbf{B}U(1)} \mathbf{E}\mathbf{B}U(1)$.

The pullback of

$$
 \array{
   \mathbf{E}Vect &\to& \mathbf{E}Vect
   \\
   \downarrow && \downarrow
   \\
   Vect &\to& Vect \coprod \mathbf{E}\mathbf{B}U(1)
 }
$$

along our differential cocycle, i. e. the pullback of the top part of the diagram

$$
  \array{
    && \mathbf{E}Vect
    \\
    && \downarrow & \searrow
    \\
    \Sigma \times X & \to&  Vect && \mathbf{E}Vect
    \\
    \downarrow & \searrow && \searrow & \downarrow
    \\
    \Sigma && \mathbf{\Pi}(\Sigma)\times \mathbf{\Pi}(X) &\to& \mathbf{E}\mathbf{B}U(1)\coprod_{\mathbf{B}U(1)} Vect
    \\
    & \searrow & \downarrow
    \\
    && \mathbf{\Pi}(\Sigma)
  }
$$

is over $X \times \Sigma$ the total space of the pullback of the underlying vector bundle $E$ on $X$ to $X \times \Sigma$, and over $\mathbf{\Pi}(X \times \Sigma)$ is a groupoid $E_{\mathbf{\Pi}}$


$$
  \array{
    E &\to& E_{\mathbf{\Pi}}
    \\
    \downarrow && \downarrow
    \\
    X\times \Sigma &\to& \mathbf{\Pi}(X \times \Sigma)
    \\
    \downarrow && \downarrow
    \\
    \Sigma &\to& \mathbf{\Pi}(\Sigma) 
  }
  \,.
$$

To see what $E \to E_{\mathbf{\Pi}}$ is like, first notice that we have a [[fibration sequence]]

$$
  \array{
    &&  && V
    \\
    && && \downarrow
    \\
    V &\to& E &\to & V//U(1) &\to& *
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    {*} &\stackrel{x}{\to}
    &X &\stackrel{g}{\to}& \mathbf{B}U(1) &\stackrel{\rho}{\to}&
    Vect 
  }
$$

with the bottom right square a lax pullback and everything else [[homotopy pullback]]s. Here $V$ is the vector space that $\rho : \mathbf{B}U(1) \to Vect$ is a representation on (which for the [[electromagnetic field]] will be $\mathbb{C}$ itself).

The groupoid $E_{\mathbf{\Pi}}$ has the following description:

* its objects are triples $(x,\sigma, v)$, where $v \in E_{x}$ is a vector in the fiber of $E$ over $x$;

* its morphisms are triples $(x \stackrel{\gamma}{\to} y, \sigma \to \sigma', v)$ that go from $(x,\sigma,v)$ to $(y, \sigma', \exp(\int_0^1 |...|) \rho(\nabla(\gamma)))(v)$, i.e. from a vector in the fiber over the source to the corresponding vector in the fiber over the target, obtained by evaluating the action functional on the path.

To obtain from this a cocycle on $\Sigma$, we proceed as follows: we regard an interval $\sigma := [\sigma_{in}, \sigma_{out}] \in \mathbf{\Pi}(\Sigma)_1$ as a [[cospan]]

$$
  \array{
    \sigma_{in} &\to& \sigma &\leftarrow& \sigma_{out}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \sigma_{in} &\to& \mathbf{\Pi}(\sigma) &\leftarrow& \sigma_{out}
    \,,
  }
$$

where in the top row we regard these subsets of $\Sigma$ as discrete smooth sub-categories, and in the bottom row form the path $\infty$-groupoids.

Then we take [[section]]s of $\array{E &\to& E_{\mathbf{\Pi}}\\ \downarrow && \downarrow \\ \Sigma &\to& \mathbf{\Pi}(\Sigma)}$ to produce a [[span]] of sections

$$
  \left[
    \array{
      \sigma_{in}
      \\
      \downarrow
      \\
      \sigma_{in} 
    }
    \,,
    \array{
      E
      \\
      \downarrow
      \\
      E_{\mathbf{\Pi}} 
    }
  \right]_\Sigma
  \leftarrow
  \left[
    \array{
      \sigma
      \\
      \downarrow
      \\
      \mathbf{\Pi}(\sigma)
    }
    \,,
    \array{
      E
      \\
      \downarrow
      \\
      E_{\mathbf{\Pi}} 
    }
  \right]_\Sigma  
  \to 
  \left[
    \array{
      \sigma_{out}
      \\
      \downarrow
      \\
      \sigma_{out} 
    }
    \,,
    \array{
      E
      \\
      \downarrow
      \\
      E_{\mathbf{\Pi}} 
    }
  \right]_\Sigma
  \,.
$$

of smooth $\infty$-groupoids. 

Consider an $\infty$-groupoid

$$
  \Psi \to
  \left[
    \array{
      \sigma_{in}
      \\
      \downarrow
      \\
      \sigma_{in} 
    }
    \,,
    \array{
      E
      \\
      \downarrow
      \\
      E_{\mathbf{\Pi}} 
    }
  \right]_\Sigma
$$

over the left foot. Under [[groupoid cardinality]], if $\Psi$ is tame, this corresponds to a collection of rational numbers over vectors in fibers of $E$. Under "degrupoidification" we may think of this as specifying a section $|\Psi| \in \Gamma(E)$. The above span is supposed to give us the propagation of this state along $\sigma$. 

To determine this, consider the special case where $\Psi$ is a "delta-section", $* \mapsto (x,\sigma_{in}, v)$ supported on a single vector $v$ in a single fiber $E_x$ over $x$. Then its pull-push through this span yields the $\infty$-groupoid over $E$, which over $(y,\sigma_{out},w)$ consists of the set of paths $\gamma : x \to y$ such that $w = \exp(\int...)\rho(\gamma)(v)$, i.e. such that $w$ is the vector obtained from applying the action to $v$ along this path.

If everything were suitably finite, we could take cardinalities of the result and obtain the familiar path integral (sum)

$$
  \Psi'(y)
  =
  \int_{x \stackrel{\gamma}{\to} y}
  \exp( S_{kin}(\gamma)) tra_\nabla(\gamma) \Psi(x)  
  \,.
$$



[[!redirects exercise in groupoidification -- the path integral]]
[[!redirects An Exercise in Groupoidification]]