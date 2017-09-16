
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

The question to be analyzed here is how this classical action $\exp(i S_\nabla) : Bord_n(X) \to F$ transmutes systematically to an [[FQFT]] $Z_\nabla : Bord_n \to C$ on abstract bordisms (possibly with extra structure, if we pass from [[TQFT]] to richer theories like [[CFT]]).

The basic idea that we shall follow is the one that is sketched in the notes

* [[schreiber:Nonabelian cocycles and their sigma model QFTs]]. 

These notes in turn have grown out of the blog entry [An Exercise in Groupoidification -- the path integral](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html) from which the present entry draws its name. We hope to refine the discussion a bit more now, provide more details and more systematics.


# General procedure #

...

# More concrete examples #

...

+-- {.standout}

...

=--





[[!redirects exercise in groupoidification -- the path integral]]


[[!redirects An Exercise in Groupoidification]]