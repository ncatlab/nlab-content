<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of $(\infty,1)$-category of $(\infty,1)$-sheaves is the generalization of the notion of [[category of sheaves]] from [[category theory]] to the [[higher category theory]] of [[(∞,1)-categories]].

## Definition

+-- {: .un_defn}
###### Definition

An **$(\infty,1)$-category of $(\infty,1)$-sheaves** is a [[reflective sub-(∞,1)-category]] 

$$
  Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

of an [[(∞,1)-category of (∞,1)-presheaves]] such that 

* $L$ is a [[topological localization]];

* equivalently: there is the structure of an [[(∞,1)-site]] on $C$ such that the objects of $Sh(C)$ are precisely those [[(∞,1)-presheaves]] $A$ that are [[local object]]s with respect to the _covering_ [[monomorphism in an (∞,1)-category|monomorphisms]] $p : U \to j(c)$ in $PSh(C)$ in that

  $$
    A(c) \simeq PSh(j(c),A) \stackrel{PSh(p,A)}{\to} PSh(U,A)
  $$

  is an [[(∞,1)-equivalence]] in [[∞Grpd]]. 

  This is the [[descent]] condition and the presheaves satisfying it are the
  **[[(∞,1-sheaves)]]** .


=--

This is [[Higher Topos Theory|HTT, def. 6.2.2.6]].

An $(\infty,1)$-category of $(\infty,1)$-sheaves is an [[(∞,1)-topos]].


## Terminology

Sometimes [[(∞,1)-sheaves]] are called **[[∞-stack]]**s, though sometimes the latter term is reserved for [[hypercomplete]] $(\infty,1)$-sheaves.

The counting is

* [[sheaf]] = 0-stack = 0-[[truncated]] $(\infty,1)$-sheaf

* $(2,1)$-sheaf = [[stack]] = 1-truncated $(\infty,1)$-sheaf

* $(3,1)$-sheaf = 2-stack = 2-truncated $(\infty,1)$-sheaf

* etc

* $(\infty,1)$-sheaf = [[∞-stack]].


## Properties

We reproduce the proof that the two definitions above really are equivalent, i.e. that:

+-- {: .un_prop}
###### Proposition

For $C$ an [[(∞,1)-site]], the full [[sub-(∞,1)-category]] of $PSh(C)$ on [[local object]]s with respect to the covering monomorphisms in $PSh(C)$ is indeed a [[topological localization]]. and hence $Sh(C)$ is indeed an exact [[reflective sub-(∞,1)-category]] of $PSh(C)$ and hence an [[(∞,1)-topos]]. 

=--

This is [[Higher Topos Theory|HTT, lemma 6.2.2.7]]

+-- {: .proof}
###### Proof

...

=--





## Models 


The topological localizations of an [[(∞,1)-category of (∞,1)-presheaves]] are [[presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] of the global [[model structure on simplicial presheaves]] at the set of [[Cech cover]]s.

The [[hypercompletion|hypercomplete]] $(\infty,1)$-sheaf toposes are [[presentable (infinity,1)-category|presented]] by the local Joyal-Jardine [[model structure on simplicial presheaves]]. 

Detailed discussion of this [[model category]] presentation is at 

* [[models for infinity-stack (infinity,1)-toposes|models for (infinity,1)-category of (infinity,1)-sheaves]] .

## References

The study of simplicial presheaves apparently goes back to 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

which considers locally [[Kan complex|Kan]] [[simplicial presheaf|simplicial presheaves]] as a [[category of fibrant objects]].

This was later conceived in terms of a [[model structure on simplicial presheaves]] and on simplicial sheaves by Joyal and Jardine. To&#235; summarizes the situation and emphasizes the interpretation in terms of [[∞-stacks]] living in $(\infty,1)$-categories for instance in

B. To&euml;n, _Higher and derived stacks: a global overview_   ([arXiv](http://arxiv.org/abs/math/0604504)) .

This concerns mostly [[hypercomplete]] $(\infty,1)$-sheaves, though.

The full picture in terms of Grothendieck-[[(∞,1)-topos]]es of [[(∞,1)-sheaves]] is the topic of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

  * localization $(\infty,1)$-functors ($(\infty,1)$-sheafification for the present purpose) are discussed in section 5.2.7;

  * local objects ($(\infty,1)$-sheaves for the present purpose) and [[local isomorphism]]s are discussed in section 5.5.4;

  * the definition of $(\infty,1)$-topoi of $(\infty,1)$-sheaves is then definition 6.1.0.4 in section 6.1;

  * the characterization of $(\infty,1)$-sheaves in terms of [[descent|descent and codescent]] is in section 6.1.3 

  * the relation between the [[model structure on simplicial presheaves|Brown?Joyal?Jardine model]] and the general story is discussed at length in section 6.5.4


[[!redirects (infinity,1)-category of (infinity,1)-sheaves]]
[[!redirects (∞,1)-category of (∞,1)-sheaves]]
[[!redirects (infinity,1)-categories of (infinity,1)-sheaves]]
[[!redirects (∞,1)-categories of (∞,1)-sheaves]]
