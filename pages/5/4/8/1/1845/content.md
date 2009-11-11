<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

Given a [[stable (∞,1)-category]] $C$, its [[decategorification]]

$$
  K_0(C) = \{equivalence \,classes\; [c]\; of \,objects \,c \in C\}
$$

naturally inherits the structure of an abelian [[group]] from the [[fibration sequence]]s in $C$:

for 

$$
  a \to x \to c
$$ 

a [[fibration sequence]] (i.e. a homotopy exact sequence) the abelian group operation

$$
  + : K_0(C) \times K_0(C) \to K_0(C)
$$

is such that

$$
  [x] = [a] + [c]
  \,.
$$

The group $K_0(C)$ is called the **K-group** of $C$ or the [[Grothendieck group]] of $C$. See in particular the latter entry for more details.

The "K" is chosen by Grothendieck for the German word _Klasse_ for "class". The K-group of $C$ is the group of equivalence classes of $C$: it is a group due to the existence of a notion of exact sequences in $C$.

K-theory starts with the study of these K-groups and their higher analogues. Sometimes the K-groups themseles are called "K-theory". One would say for instance: "$K(C)$ is the K-theory of $C$."

More generally, there is a [[symmetric monoidal (infinity,1)-category|symmetric groupal ∞-groupoid]] $\mathbf{K}(C)$  -- i.e. a connective [[spectrum]] -- in between the [[decategorification]] from $C$ to $K(C)$ of which $K(C)$ is the set of [[simplicial homotopy group|connected components]]

$$
  C \mapsto \mathbf{K}(C) \to \pi_0 \mathbf{K}(C) = K(C)
  \,.
$$

In nice cases this is the degree 0 part of a non-connective [[spectrum]] which is then the **K-theory spectrum** of $C$.
This is also called the **Waldhausen K-theory** of $C$.


## Special cases and models ##

Much of the literature on K-theory discusses constructions that _model_ the above abstract setup in terms of [[model category|model categories]], or just their [[homotopy category|homotopy categories]], often of the [[derived category|derived catgeories]] type and then often expressed in terms of the [[abelian category]] or more generally [[Quillen exact category]] from which the derived category is derived.

Only a subset of the structure on a [[model category]] is necessary in order to conveniently extract the K-groups of the [[presentable (infinity,1)-category|presented]] [[stable (∞,1)-category]]. For that reason the axioms of a [[Waldhausen category]] have been devised to provide just the necessary convenient prerequesites to compute the K-groups of the [[(∞,1)-category]] [[presentable (infinity,1)-category|presented]] by the underlying [[homotopical category]].

* In particular, the K-group associated to the [[stable (∞,1)-category]] $Ch^b(A)$ of _bounded_ [[chain complex]]es in an [[abelian category]] or [[exact category]] $A$ is often called the K-group of $A$ itself and just denoted

  $$
    K(A) := K(Ch^b(A))
    \,.
  $$

  Most explicit constructions of K-theory spectra start with the data of an [[exact category]], such as notably Quillen's [[Q-construction]] and the [[Waldhausen S-construction]].

* In particular if the exact category $A$ is that of [[vector bundle]]s on a [[topological space]] $X$

  $$
    A = VectBund(X)
  $$

  the corresponding K-group is degree 0 [[topological K-theory]]. This was the original of the notion and the term K-theory.

## Definition ##

Recall that given a [[(∞,1)-category]] $C$, we may regard it as a [[complete Segal space]] $C_{\bullet,\bullet}$, a [[bisimplicial object|bisimplicial set]]. For instance if $C$ is originally given as a [[quasicategory]] then

$$
  C_{\bullet,\bullet} : [n],[m] \mapsto
  Core(Func(\Delta^n,C))_{m}
  \,,
$$

where $Core(Func(\Delta^n,C))$ denotes the maximal [[Kan complex]] inside the [[(∞,1)-category of (∞,1)-functors]] from $\Delta^n$ to $C$.


+-- {: .un_defn}
###### Definition 

Let $C$ be a [[stable (∞,1)-category]]. Then its **Waldhausen K-theory $\mathbf{K}(C)$ is given by the the diagonal simplicial set

$$
  \mathbf{K}(C) = diag C_{\bullet, \bullet}
$$

where $C_{\bullet,\bullet}$ is the corresponding [[complete Segal space]].

=--

This is [remark 11.4](http://arxiv.org/PS_cache/math/pdf/0608/0608228v5.pdf#page=43) in [[stable (infinity,1)-category|StCat]] in view of the lemma above that and using the discussion on [p. 27](http://www-math.mit.edu/~lurie/papers/cobordism.pdf#page=27) of _CobHyp_ .

This construction is also conjectured in the last section of Toen-Vezzosi's _A remark on K-theory_ .

In the case that $C$ is the [[simplicial localization]] of a [[Waldhausen category]] $\bar C$ the explicit way to obtain this is the [[Waldhausen S-construction]].

**Proposition**

It should be true that with this definition we have an isomorphism of groups

$$
  K(C) \simeq \pi_0 \mathbf{K}(C)
  \,.
$$



## Related entries ##
 
* [[Grothendieck group]]

* [[K-theory spectrum]]

* [[topological K-theory]]

* [[algebraic K-theory]]

* [[Karoubi K-theory]]

* [[twisted K-theory]]

* [[differential K-theory]]

* [[K-theory and physics]]


## References ##

It was in 

* [[Bertrand Toen]], Gabriele Vezzosi, _A remark on K-theory and $S$-categories_ ([arXiv](http://arxiv.org/PS_cache/math/pdf/0210/0210125v2.pdf)).

that it was proven that the the [[Waldhausen S-construction]] of the [[K-theory spectrum]] depends precisely on the [[simplicial localization]] of the [[Waldhausen category]], i.e. of the [[(∞,1)-category]] that it presents.

In view of this remark 11.4 in

* [[Jacob Lurie]], [[stable (infinity,1)-category|Stable ∞-Categories]] .

interprets the construction of the K-theory spectrum as a natural operation of 
[[stable (infinity,1)-category|stable (∞,1)-categories]], as described above.


The standard constructions of K-theory spectra from [[Quillen exact categories]] are discussed in detail in chapter 1 of

* Eric M. Friedlander, Daniel R. Grayson, _Handbook of K-theory_, Springer Verlag .

A useful introduction to the definition and computation of K-groups (with a little on K-spectra) is

* Charles Weibel, _The K-book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))