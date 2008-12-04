#Idea#

**Anafunctors** are the proper notion of morphism to use between categories in a context where the [[axiom of choice]] fails. Functors, as normally defined, are really not the correct concept.

Anafunctors were first developed by [[Michael Makkai]] to do ordinary category theory with a [[foundations]] that does not include the axiom of choice. Later they were applied by [[Toby Bartels]] to [[internalization|internal categories]], where the axiom of choice is simply not an option. These actually turned out to be known already (at least up to equivalence) in some contexts, in particular as [[Hilsum–Skandalis morphism]]s between [[Lie groupoid]]s.

#Homotopy-theoretic interpretation#

From the point of view of the [[homotopy theory]] of categories -- the [[folk model structure]] -- anafunctors are precisely the spans out of [[homotopy theory|acyclic fibrations]] in $Cat$

$$
  (anafunctor: C \to D)
  \Leftrightarrow
  (span in Cat: \;\;
    C \lt\stackrel{\simeq}{\leftarrow}
    \hat H \to D
  )
$$

and hence precisely the one-step generalized morphisms. 

**Saturated anafunctors** are those spans as above where the right leg is furthermore [[k-surjectivity|0-surjective]].

+-- {: .query}

_Urs says:_ I had this thing about saturation wrong before and Toby corrected me. Hope it is right now. Please check.

=--

An anafunctor is a **[[Morita equivalence]]** if it is a span as above, with the right leg also an acyclic fibration.
(This terminology is used for [[Lie groupoid]]).

If we restrict from categories to groupoids, then according to the [[folk model structure|groupoid folk model structure]] by Brown-Golasinski all objects are _fibrant_ and then according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization of $Groupoids$ in that they represent all morphisms in the [[homotopy category]] $Ho(Groupoids)$.

By the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycles]] on groupoids with values in groupoids. By the notion of [[descent and codescent|codescent]] such homotopical cocycles are related to [[descent and codescent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.

##Generalizations##

Since the [[folk model structure]] on $Categories$ extends to [[omega-category|omega-categories]], also the anafunctor concept generalizes to these strict [[higher category theory|higher categories]]. Indeed, again by Brown-Golasinski, $\omega$-groupoids are fibrant with respect to the [[folk model structure]], so that the corresponding _$\omega$-anafunctors_ between $\omega$-groupoids represent cocycles in [[nonabelian cohomology]].

More details on $\omega$-anafunctors are described in the context of [[schreiber:Differential Nonabelian Cohomology]] in the private area of the $n$Lab. 

## Additive version ##

The notion of abelian [[butterfly]] introduced by Behrang Noohi [Weak maps of 2-groups](http://arxiv.org/abs/math.CT/0506313) is the additive version of the notion of (saturated) anafunctor: the equivalence between, on the one hand, internal groupoids and internal functors and, on the other hand, arrows and commutative squares in an abelian category extends to an equivalence between saturated anafunctors and butterflies.

+-- {: .query}

_Urs says:_ Why do you restrict this to the abelian case? From 
[page  16](http://arxiv.org/PS_cache/math/pdf/0506/0506313v3.pdf#page=16)  of Noohi's article I got the impression that he is precisely describing the ana-2-functors between one-object 2-groupoids in terms of the corresponding (possibly nonabelian) crossed modules. 

=--


## References

* [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/) (first explicit formulation of anafunctors)
* [Higher gauge theory I: 2-Bundles](http://arxiv.org/abs/math.CT/0410328) (first explicit formulation of internal anafunctors)
* [Local Transition of Transport, Anafunctors and Descent of n-Functors](http://golem.ph.utexas.edu/category/2006/12/local_transition_of_transport.html) (first explicit formulation of $n$-anafunctors)