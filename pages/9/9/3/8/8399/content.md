
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], the term _general covariance_ is meant to indicate the property of a [[physical system]] or [[model (in theoretical physics)]] whose [[configuration space|configurations]], [[action functional]] and [[equations of motion]] are all [[equivariance|equivariant]] under the [[action]] of the [[diffeomorphism group]] on the [[smooth manifold]] underlying the [[spacetime]] or the [[worldvolume]] of the system. Here "covariance" is as in "[[covariant tensor]]" another term for behaviour under diffeomorphisms.

The term _[[general relativity]]_ for [[Einstein]]-[[gravity]] originates in related ideas, and Einstein-gravity is the archtypical example of a generally covariant physical system: 

here, the [[configuration space]] of fields over a [[smooth manifold]] $X$ is not quite the space of [[Riemannian metrics]] on $X$ itself, but is the [[quotient]] of this space by the [[action]] of the [[diffeomorphism group]] $Diff(X)$: two Riemannian metrics $g_1$ and $g_2$ on $X$ represent the same field of [[gravity]] on $X$ if there is a [[diffeomorphism]] $f : X \stackrel{\simeq}{\to} X$ such that $g_2 = f^* g_1$.

Or rather, such a diffeomorphism is a [[gauge transformation]] between the two field configurations. The configuration space is not the naive [[quotient]] of fields by diffeomorphisms, but is the [[homotopy quotient]], or _[[action groupoid]]_. In the physics literature this action groupoid is most familiar in its [[infinitesimal cohesion|infinitesimal approximation]], the corresponding [[Lie algebroid]], whose formal dual is a [[BRST complex]] whose degree-1 elements are accordingly called the _diffeomorphism ghosts_ (see there).

As with all [[gauge transformations]], they relate physical configurations which may be nominally different, but [[equivalence|equivalent]],.
Thereofore _general covariance_ is an instance of the general _[[principle of equivalence]]_ in mathematics which says that sensible statements about [[objects]] must respect the [[isomorphisms]] and more general [[equivalences]] between these objects. 

A physical system which is not generally covariant in this sense is hence one where the [[smooth manifold]] $X$ as abover, underlying [[spacetime]]/[[worldvolume]] is not regarded as modelling an absolute physical system (such as the [[observable universe]] in gravity), but a [[subsystem]] that is equipped with ambient [[structure]] that [[spontneous symmetry breaking|breaks]] the diffeomorphism symmetry. Notably systems like [[electromagnetism]] or [[Yang-Mills theory]] have traditionally been written in a non-generally covariant form describing gauge fields on a fixed gravitational background, as for instance the space inhabited by a particle accelerator. This ambient structure on the spacetime $X$ breaks its general diffeomorphism invariance and hence the effective resulting theory on this background is not generally covariant (a special case of the general phenomenon of [[spontaneous symmetry breaking]]). 

On the other hand, such a model consisting of background (e.g. the particle accelerator) and quantum fields propagating in it is ultimately to be understood as an approximation to a more encompassing model in which also the background is dynamical, and which is again generally covariant. Specifically for electromagnetism and Yang-Mills theory this refined generally covariant model is known as _[[Einstein-Maxwell theory]]_ or more generally _[[Einstein-Yang-Mills theory]]_.

The idea of general covariance has a long and convoluted history and the literature witnesses plenty of disagreement about how to interpret and formalize it in technical detail ([Norton](#Norton)). Already early arguments by [[Einstein]] himself (e.g. the "hole paradox") show that the discussion has suffered in parts from not being suitably informed by the basic [[category theory|category theoretic]] concept  of [[isomorphism]]  in the [[category]] [[Diff]] of [[smooth manifolds]]. Below in _[Formalization in homotopy type theory](#InHomotopyTypeTheory)_ we indicate a formalization of general covariance that is general, fundamental, and accurately reflects the role of the term in theoretical physics.

## Formalization on homotopy type theory
 {#InHomotopyTypeTheory}

Let $\mathbf{H}$ be the ambient [[homotopy type theory]]/[[(∞,1)-topos]].
(For standard applications in [[physics]] we have $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SmoothSuper∞Grpd]] or similar.)

For an [[object]] $\Sigma \in \mathbf{H}$ 
supposed to represent the [[space]] underlying [[spacetime]] or the [[worldvolume]] of a [[model (in theoretical physics)]], write $\mathbf{Aut}(\Sigma) \in Grp(\mathbf{H})$ for its [[automorphism ∞-group]]. 

In the standard [[categorical semantics|interpretation]] of the homotopy type theory in $\mathbf{H} = $ [[Smooth∞Grpd]] $\Sigma$ could be an ordinary [[smooth manifold]] or [[orbifold]], in particular, and then $\mathbf{Aut}(\Sigma) = \mathbf{\Diff}(\Sigma)$ is the [[diffeomorphism group]] of $\Sigma$, regarded as a [[diffeological space|diffeological]] [[group object]]. In view of this archetypical example we will in the following often say _[[diffeomorphism]]_ for short instead of _auto-equivalence in $\mathbf{H}$_ and similarly refer to $\mathbf{Aut}(\Sigma)$ loosely as the _diffeomorphism group_ of $\Sigma$. But even in the specifical model $\mathbf{H} = $ [[Smooth∞Grpd]]/[[SmoothSuper∞Grpd]], $\Sigma$ can be much more general than a [[smooth manifold]] or [[supermanifold]] or [[orbifold]]. 

Write then $\mathbf{B} \mathbf{Aut}(\Sigma) \in \mathbf{H}$ for the [[delooping]] of the diffeomorphism group.
By the discussion at _[[∞-action]]_, the [[context]] of this type

$$
  \mathbf{B} \mathbf{Aut}(\Sigma) \vdash \cdots
  \,,
$$

hence the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}\mathbf{Aut}(\Sigma)}$ is the context of objects in $\mathbf{H}$ equipped with $G$-[[∞-actions]] and with $G$-[[equivariance|equivariant]] [[morphisms]] between them

$$
  \mathbf{H}_{/\mathbf{B}\mathbf{Aut}(\Sigma)}
  \simeq
  Act_{\mathbf{H}}(\mathbf{Aut}(\Sigma))
  \,.
$$

Hence a [[type in context]] $\mathbf{B}\mathbf{Aut}(\Sigma)$ is a "generally covariant type" with respect to $\Sigma$ in the sense that it transforms consistently by equivalences under diffeomorphisms of $\Sigma$. Hence $\mathbf{B}\mathbf{Aut}(\Sigma)$ _is the [[context]] of general covariance_ with respect to $\Sigma$.

In particular, $\Sigma$ itself is canonically equipped with the defining action of $\mathbf{Aut}(\Sigma)$ on it, exhibited by the universal  [[associated ∞-bundle|associated]] $\Sigma$-[[fiber ∞-bundle]]

$$
  \array{
    \Sigma &\to& \Sigma \sslash \mathbf{Aut}(\Sigma)
    \\
    && \downarrow^{\overline{\rho_{\Sigma}}}
    \\
    && \mathbf{B} \mathbf{Aut}(\Sigma)
  }
  \,,
$$

where the total space $\Sigma \sslash \mathbf{Aut}(\Sigma) = \sum_{\mathbf{B}G} \rho_\Sigma$ is the [[homotopy quotient]] or [[action groupoid]]. Of $\Sigma$ by $\mathbf{Aut}(\Sigma)$. This is the type characterized by the fact that a [[function]] $f : U \to \Sigma \sslash \mathbf{Aut}(\Sigma)$ is a function to $\Sigma$ which is regarded as ([[gauge equivalence|gauge]]) [[equivalence|equivalent]] to another function to $\Sigma$ if both differ by a diffeomorphism of $\Sigma$.






## References

* J. D. Norton, _General covariance and the foundations of general relativity: eight decades of dispute_, Rep. Prog. Phys **56** (1993), ([original pdf](http://www.pitt.edu/~jdnorton/papers/decades.pdf), [reprint pdf](http://www.pitt.edu/~jdnorton/papers/decades_re-set.pdf))
 {#Norton}

