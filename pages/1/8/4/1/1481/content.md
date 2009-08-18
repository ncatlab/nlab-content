
+-- {.standout}

  An entry on the formalization of the process of [[quantization]] -- by [[category theory|abstract nonsense]] -- from classical [[sigma-model]] data to the corresponding [[quantum field theory]] .

=--

# Background and motivation #

The search is on for the abstract formalization of the process of _quantization_, the process that reads in a "classical field theory" for instance presented in form of a [[gauge theory]] or of [[sigma-model]] background field data and spits out the corresponding [[quantum field theory]].

While for various aspects and facets of this question there are well-developed formalisms -- such as [[geometric quantization]] or [[deformation quantization]] or [[BV theory]] -- a full answer is certainly still missing, not the least because the full formalization of the question has still to be established.

Considerable progress on this formulation of the question itself has been achieved with the formalization and proof of the [[cobordism hypothesis]] in [[On the Classification of Topological Field Theories]] by [[Jacob Lurie]]. This at least indicates what the _result_ of any full quantization procedure should in that it clarifies what exactly an [[TFT]] [[FQFT]] is: a morphism from the [[(infinity,n)-category of cobordisms]] $Z : Bord_n \to C$.

Already in [[On the Classification of Topological Field Theories]] Jacob Lurie indicates the desire to find a similar formalization of "classical field theory" and a systematic procedure for turning the classical theory into the quantum theory.

These thoughts were further developed in [TFT from compact Lie groups](Topological Quantum Field Theories from Compact Lie Groups), but remain sketchy for the moment. 

For the purpose of the present entry this indication of a quantizaton proposal by Lurie et al. mainly serves as a reference for the idea itself that a formalization of something interesting is to be sought here, and of the kind of [[category theory|abstract nonsense]] answer one hopes to find. We will however discuss a somewhat different-looking approach. It may well be related to the Lurie-et al proposal in the end, but for the time being we shall not concentrate on that.

Rather, the approach for a formalization of the quantization  procedure that shall be discussed at this entry here is more in the spirit as indicated to some extent in the work of [[David Ben-Zvi]] et. al, which is described in some detail at [[geometric infinity-function theory]]. This is essentially based on the idea that a [[quantum field theory]] is obtained from a [[sigma-model]] target space object $X$ by homming [[extended cobordism]] [[cospan]]s $\Sigma_in \to \Sigma \leftarrow \Sigma_{out}$ into the target object and then pull-pushing [[geometric function object]]s through the resulting [[span]]s of configuration space objects $[\Sigma_{in},X] \leftarrow [\Sigma,X] \to [\Sigma_{out},X]$. 

The resulting pull-push operation is an example or a generalization of what [[John Baez]] discusses under the term [[groupoidification]]. David Ben-Zvi et al would speak of [[geometric function theory]].

The main result of David Ben-Zvi et. al. work on this approach is that they point out that as soon as the [[geometric function object]] one uses satisfies the two [[geometric infinity-function theory|fundamental theorems of geometric infinity-function theory]], a considerable amount of rich structure that has in parts been known by itself gets unified into one coherent elegant story: the nature of partition functions (i.e. traces), of centers, of Hochschild (co)homology, Deligne-Kontsevich-statements, etc. all are understood by means of a suitable [[geometric function theory]] as induced from the underlying geometry of configuration space objects $[\Sigma,X]$ as well as the [[loop space object]]s of $X$.

Here in this entry the aim is to discuss in detail aspects and models for the quantization procedure that is suggested by applying [[geometric function theory]] to [[sigma-model]] backgrounds.

But more precisely, the premise of the discussion here is that for a fundamental understanding of the situation is obtained after taking serious the fact that

1. background fields are not just encoded by the [[cohomology]] with coefficients in the target space object $X$, but by the corresponding [[differential cohomology]];

2: that the functorial notion of the [[FQFT]] that one wants to obtain suggests that these differential cocycles themselves are encoded functorially, as described at [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

This means that we shall take the classical structure $\nabla$ which the sought-after quantization procedure is supposed to send to an [[FQFT]] $Z_\nabla : Bord_n \to C$ to be, essentially, a functor

$$
  \nabla : \Pi_n(X) \to A
$$

from some [[path n-groupoid]] of $X$ to some coefficient object $A$. 

Here the [[k-morphism]]s in $\Pi_n(X)$ are generated from the existing $k$-morphisms in $X$ as well as the $k$-dimensional smooth paths in $X$. The functor $\nabla$ on this encodes the _parallel transport_ of a connection on a [[principal infinity-bundle]] over $X$: this assignment of [[k-morphism]]s in $A$ to $k$-dimensional paths in $X$ is the assignment of the **classical action** to trajectories in $X$.

More precisely, this is the classical action assigned to topologically disk-shaped $k$-paths. The full classical action of a classical [[sigma-model]] quantum field theory is an extension of $\nabla$ 

$$
  \array{ 
    \Pi(X) \stackrel{\nabla}{\to}  A &\to& F
    \\
    \downarrow & \nearrow_{\exp(S_\nabla)}
    \\
    Bord_\infty(X)
  }
$$

from disk-shaped to all [[cobordism]]s in $X$ (possibly and usually after an extension of the codomain to some new codomain $F$). This extension $\exp(i S_\nabla)$ knows not just the parallel transport, but also the **holonomy** of the classical background field.

The question to be analyzed here is how this classical action $\exp(i S_\nabla) : Bord_n(X) \to F$ transmutes systematically to an [[FQFT]] $Z_\nabla : Bord_n \to C$ on abstract bordisms (possibly with extra structure, if we pass from [[TQFT]] to richer theories like [[CFT]]). This step should be the **[[path integral]]**: 

in some way the assignment of $Z_\nabla$ to a [[cobordism]] $\Sigma$ is expected to be obtained by "summing" in some way the value of $\exp(i S_\nabla)$ on elements in the fiber of the [[forgetful functor]] $Bord_n(X) \to Bord_n$ over $\Sigma$, i.e. over all possible ways to map $\Sigma$ into $X$ -- the sum of $\exp(S_\nabla(\phi))$ over all _paths_ or _field configurations_  $\phi : \Sigma \to X$.

The basic idea that we shall follow has been sketched to some extent in the notes

* [[schreiber:Nonabelian cocycles and their sigma model QFTs]]. 

These notes in turn have grown out of the blog entry [An Exercise in Groupoidification -- the path integral](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html) from which the present entry draws its name. We hope to refine the discussion a bit more now, provide more details and more systematics.


# General procedure #


## the notion of space ##

We need to talk about _spaces_ of sorts: 

* a space $X$ that is the **target space** -- often, but not always, to be interpreted as physical spacetime -- in which the $d$-dimensional object -- for $d=0$ for instance a point particle such as an [[electron]] -- whose dynamics we want to encode propagates.

  This space may be just a [[manifold]] but we want to allow it to be a kind of space a bit more general than that, for instance an [[orbifold]].

  When we are describing [[gauge theory]] the target space is smooth refinement of a [[classifying space]] $\mathbf{B}G$.

  When we are describing finite gauge theory such as [[Dijkgraaf-Witten theory]], the target space is just the one-object [[groupoid]] $\mathbf{B}G$ that is the [[delooping]] of the gauge group $G$. 

* for each $(d+1)$-dimensional [[manifold]] $\Sigma$ a **path space** or **configuration space** $[\Sigma,X]$ of maps from $\Sigma$ into $X$.

The [[category theory|general abstract nonsence]] for dealing with general spaces of this sort is that of [[space and quantity]]. As described at [[motivation for sheabes, cohomology and higher stacks]], this leads one to describe a space as an [[infinity-stack]] on some [[site]] $S$.

In the simplest case, which the reader should keep in mind, the [[site]] in question is the [[point]] and an [[infinity-stack]] on it is just an [[infinity-groupoid]]. In turn in simple cases of this, which the reader should still keep in mind, this [[infinity-groupoid]] will be just a [[groupoid]] or at most a [[2-groupoid]].

Whichever choice one makes, the collection of all such generalized spaces modeled on a certain [[site]] $S$ forms an [[(infinity,1)-topos]] $\mathbf{H}$. 

Despite possibly its appearance, the reader should take this statement as suggesting an immense simplification instead of a huge complification: the language of [[(infinity,1)-topos]] is a user interface that makes pretty sophisticated and rich notions of generalized spaces have the same look-and-feel as just plain [[topological space]]s. It's the inner workings of the formalism that will take of things coming out right even when we talk about richer objects.

In particular, it is the machinery of [[models for infinity-stack (infinity,1)-toposes]] that provides all the tools for actually performing the operations that we shall consider. The reader unfamiliar with that will suffer little loss from concentrating his or attention on the toy examples where all "spaces" involved are finite [[groupoid]]s and trust that everything goes through analogously also in the other examples.

## the notion of path ##


With an [[(infinity,1)-topos]] context $\mathbf{H}$-fixed we are in a context that allows us to study [[cohomology]]. A classical background field on a target space $X$ is in parts a cocycle on $X$ with values in some coefficient object $A \in \mathbf{H}$.

But, as indicated above, it is actually, more: it is a _differential cocycle_ on $X$: something that depends not just on $X$ itself, but also on a notion of paths in $X$.

To encode this we may pick a [[simplicial object|cosimplicial object]]

$$
  \Delta_H : \Delta \to \mathbf{H}
$$

in our $(\infty,1)$-category of spaces, that encodes which object in $\mathbf{H}$ models the standard $k$-[[simplex]] regarded as a space. For instance if $\mathbf{H}$ is the [[(infinity,1)-topos]] of [[Lie infinity-gropupoid]]s modeled by [[infinity-stack]]s on [[Diff]], we would take $\Delta_H^n$ to be the standard $n$-simplex $\Delta^n_H \subset \mathbb{R}^n$ regarded as a smooth [[manifold]] in the standard way.

Then the space of disk-shaped $k$-dimensional paths in $X$ is $[\Delta_H^n,X]$.

These spaces glue together to the [[path infinity-groupoid]]

$$
  \Pi(X) := \lim_\to [\Delta_H^\bullet, X]
  \,.
$$

This is an [[infinity-groupoid]] whose [[k-morphism]] are generated from the original $k$-morphisms of $X$ and the $k$-dimensional path $\phi : \Delta^k_H \to X$.

For instance if $X = Y//G$ is a global [[orbifold]], the 1-morphisms in $\Pi(X)$ will be generated from smooth paths $\gamma: y_1 \to y_2$ in $Y$ as well as orbifold jumps $g : y_1 \to g(y_1)$ subject to the relation

$$
  \array{
    y_1 &\stackrel{g}{\to}& g(y_1)
    \\
    \downarrow^{\gamma} && \downarrow^{g(\gamma)}
    \\
    y_2 &\stackrel{g}{\to}& g(y_2)
  }
  \,.
$$

Or if $X = C(Y)$ is realized as the [[Cech nerve]] of some [[Cech cover]] $(U = \coprod_i U_i) \to Y$ then $\Pi(X)$ will be generated from paths $(\gamma,i) : (y_1,i) \to (y_2,i)$ in $U_i$ for all $i$ and transitions $(y,i) \to (y,j)$ for all $y \in U_i \cap U_j$ subject to the condition

$$
  \array{
    (y_1,i) &\stackrel{}{\to}& (y_1,j)
    \\
    \downarrow^{(\gamma,i)} && \downarrow^{(\gamma,j)}
    \\
    (y_2,i) &\stackrel{}{\to}& (y_2,j)
  }
  \,.
$$



More generally, let $D$ be some [[poset]] and specify a functor

$$
  \Sigma_H : D \to \mathbf{H}
  \,.
$$

We think of as the image of some $k \in D$ under $\Sigma_H$  as the realization in $\mathbf{H}$ of some abstract [[cobordism]] whose boundary component inclusions are the images $\Sigma^j_H \to \Sigma_H^k$ of all morphisms $j \to k$ in $D$.

So $\Sigma_H$ encodes a [[multispan|multi-cospan]] of cobordisms in $H$. In principle $\Sigma_H$ will in general be supposed to range over _all_ cobordisms in some sense, but for our discussion it will be complete sufficient to concentrate on much less. Most of our discussion concerns a handful of cobordisms, usually just two of them and their composites.

In any case, by slight abuse of notation, we shall write

$$
  Bord(X) := \lim_\to [\Sigma_H^\bullet, X]
$$

and speak of the $\infty$-groupoid of **bordisms in $X$**. If we assume that $\Sigma_H$ ranges at least over the disk-shaped cobordisms $\Delta^k_H$ we have a canonical inclusion

$$
  \Pi(X) \hookrightarrow Bord(X)
  \,.
$$



# More concrete examples #

...

+-- {.standout}

...

=--





[[!redirects exercise in groupoidification -- the path integral]]


[[!redirects An Exercise in Groupoidification]]