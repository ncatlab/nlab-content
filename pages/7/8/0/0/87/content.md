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

_Mathieu says:_ No, this condition is some kind of surjectivity for the anafunctor.  I think you can define a saturated anafunctor as a "normal" anafunctor such that some diagram is a pullback.  Between internal groupoids, a saturated anafunctor is simply an internal distributor which is "functional" and "everywhere defined".

_Urs says:_ Okay, thanks. Somebody should fix the above then. 

_Toby says:_ I'm not sure that there is anything to say. Remember that, up to equivalence, all anafunctors are saturated. If I grasped more fully what cofibrations are, then I might be able to say something sensible here. (By the way, $k$-surjectivity doesn't na&#239;vely apply; at best, you'll have to replace epimoprphims with surjective submersions or something.)

_Urs says_: yes, I still need to complete the entry discussion on the [[homotopy theory]] structure on $n$-categories internal to spaces: the point is that one sets it up for the very general $Spaces := Sheaves(test domains)$ in which case epimorphisms are precisely the local/stalkwise section admitting maps. Then one can restrict that to $Manifolds \hookrightarrow Spaces$. If one requires that also all fiber products sit in $Manifolds$ (which is a matter of cosmetics more than of necessity) then one finds the need that the local section admitting surjections must actually be submersions.

_Toby says_: OK, that reminds me: Do you have a reference handy for the fact that submersions are precisely the maps in $Manifolds$ such that all pullbacks of these maps exist? This is a folk theorem for me, but I\'ve never written out a proof, so it always gives me doubts. (Anyway, I\'ll probably want to cite it sometime.)

=--

An anafunctor is an **anaequivalence** if it is a span as above, with the right leg also an acyclic fibration.
(For [[Lie groupoid]]s, these are the [[Morita equivalence]]s).

If we restrict from categories to groupoids, then according to the [[folk model structure|groupoid folk model structure]] by Brown-Golasinski all objects are _fibrant_ and then according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization of $Groupoids$ in that they represent all morphisms in the [[homotopy category]] $Ho(Groupoids)$.

By the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycle]]s on groupoids with values in groupoids. By the notion of [[descent and codescent|codescent]] such homotopical cocycles are related to [[descent and codescent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.

##Generalizations##

Since the [[folk model structure]] on $Categories$ extends to [[omega-category|omega-categories]], also the anafunctor concept generalizes to these strict [[higher category theory|higher categories]]. Indeed, again by Brown-Golasinski, $\omega$-groupoids are fibrant with respect to the [[folk model structure]], so that the corresponding _$\omega$-anafunctors_ between $\omega$-groupoids represent cocycles in [[nonabelian cohomology]].

More details on $\omega$-anafunctors are described in the context of [[schreiber:Differential Nonabelian Cohomology]] in the private area of the $n$Lab. 

## Additive version ##

The notion of abelian [[butterfly]] introduced by Behrang Noohi [Weak maps of 2-groups](http://arxiv.org/abs/math.CT/0506313) is the additive version of the notion of (saturated) anafunctor: the equivalence between, on the one hand, internal groupoids and internal functors and, on the other hand, arrows and commutative squares in an abelian category extends to an equivalence between saturated anafunctors and butterflies.

+-- {: .query}

_Urs says:_ Why do you restrict this to the abelian case? From 
[page  16](http://arxiv.org/PS_cache/math/pdf/0506/0506313v3.pdf#page=16)  of Noohi's article I got the impression that he is precisely describing the ana-2-functors between one-object 2-groupoids in terms of the corresponding (possibly nonabelian) crossed modules. 

_Mathieu says:_ I don't see that (or something like that) on that page, but saturated anafunctors should correspond to butterflies also in the semi-abelian case (using the notion of internal crossed module in a semi-abelian category introduced by Janelidze), but I have not checked it.  The special case of groups is probably easy to check: saturated anafunctors between two internal groupoids in the category of groups should correspond to butterflies between the corresponding crossed modules.

_Urs says:_ I haven't checked the details. But he is looking at derived homs of crossed complexes. By general nonsense these derived hom should be given by homs out of cofibrant replacements. This is another way of talking about the anafunctor picture. Somebody should check the details.

=--


## References

* [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/) (first explicit formulation of anafunctors)
* [Higher gauge theory I: 2-Bundles](http://arxiv.org/abs/math.CT/0410328) (first explicit formulation of internal anafunctors)
* [Local Transition of Transport, Anafunctors and Descent of n-Functors](http://golem.ph.utexas.edu/category/2006/12/local_transition_of_transport.html) (first explicit formulation of $n$-anafunctors)