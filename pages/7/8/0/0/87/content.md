#Idea#

**Anafunctors** are the proper notion of morphism to use between categories in a context where the [[axiom of choice]] fails. Functors, as normally defined, are really not the correct concept.

Anafunctors were first developed by [[Michael Makkai]] to do ordinary category theory with a [[foundations]] that does not include the axiom of choice. Later they were applied by [[Toby Bartels]] to [[internalization|internal categories]], where the axiom of choice is simply not an option. These actually turned out to be known already (at least up to equivalence) in some contexts, in particular as [[Hilsum-Skandalis morphism]]s between [[Lie groupoid]]s.

#Defintion (external)#

Given categories $C$ and $D$, an __anafunctor__ $F: C \to D$ consists of:

* a set $|F|$ of _specifications_ of $F$;
* maps $\sigma: |F| \to C$ and $\tau: |F| \to D$ (taking values in objects). Given $x: C$ and $y: D$, we say that $y$ is a _specified value_ of $F$ at $x$ if, for some $s: |F|$, $x = \sigma(s)$ and $y = \tau(s)$; in this case, $s$ _specifies_ $y$ as a value of $F$ at $x$, and we write $F_s(x) = y$. We say that $y$ is a _value_ of $F$ at $x$ if $y$ is isomorphic (in $D$) to some specified value of $F$ at $x$; we write $F(x) \cong y$. (There is no notion of *the* value of $F$ at $x$, and $F(x) = y$ is meaningless.);
* for each $s, t: |F|$ and morphism $f: \sigma(s) \to \sigma(t)$ in $C$, a morphism $F_{s,t}(f): \tau(s) \to \tau(t)$ in $D$. Similarly to the above, we can define whether a given morphism $g$ in $D$ is a _specified value_ of $F$ at a given morphism $f$ in $C$ or whether $g$ is (merely) a _value_ of $F$ at $f$. (Again, there is no notion of *the* value of $F$ at $f$.);
* $\sigma$ is a surjective function. Thus, $F$ has *some* value at any given object or morphism of $C$. (In the [[internalization|internalized]] case, this requirement can become quite complicated; for example, internal to manifolds, one requires a surjective submersion.);
* $F$ preserves identities. That is, $s: |F|$, the value of $F$ specified by $s$ and $s$ at the identity of $\sigma(s)$ is the identity of $\tau(s)$, or (in symbols) $F_{s,s}(\id_{\sigma(s)}) = \id_{\tau(s)}$, or (whenever this makes sense) $F_{s,s}(\id_x) = \id_{F_s(x)}$;
* $F$ preserves composition. That is, given $s, t, u: |F|$, $f: \sigma(s) \to \sigma(t)$, and $g: \sigma(t) \to \sigma(u)$, $F_{s,u}(f;g) = F_{s,t}(f);F_{t,u}(g)$. (Here the semicolon indicates composition in the anti-Leibniz order.).

An anafunctor $F$ is __saturated__ if, whenever $F(x) \cong y$, $F_s(x) = y$ for some unique specification $s$, where the unicity of $s$ depends not only on $x$ and $y$ but also on how $y$ is a value of $F$ at $x$. To be precise: if $g: y' \to y$ is an isomorphism in $D$ and $F_{s'}(x) = y'$ for some specification $s'$, then there is a unique specification $s$ such that $F_{s',s}(\id_x) = g$ (so in particular, $\sigma(s) = x$ and $F_s(x) = y$). Every anafunctor $F: C \to D$ has a _saturation_ $\overline{F}$; $\overline{F}$ is a saturated anafunctor and $F \cong \overline{F}$ in the category of anafunctors from $C$ to $D$. In fact, the inclusion of the saturated anafunctors into the anafunctors (as a full subcategory) is an equivalence of categories (given fixed $C$ and $D$).

Every functor may be interpreted as an anafunctor, with $|F|$ always taken to be the set of objects in $C$. That every anafunctor is equivalent to a functor is equivalent to the axiom of choice, in which case the inclusion of functors into anafunctors is in fact an equivalence of categories. But if you ignore functors and deal only with anafunctors (or saturated anafunctors), then the theory is entirely constructive (without using the axiom of choice or even excluded middle). Theorems that classically required choice now don\'t require choice (and indeed become constructive) with anafunctors. Thus, anafunctors (or even saturated anafunctors) are the correct notion to use if you are a constructivist (at least as long as you [[foundations|found]] mathematics on some sort of set theory at all); but they are also the correct notion to use in [[internalization|internal]] category theory.

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

+-- {: .query}

_Urs says:_ I had this thing about saturation wrong before and Toby corrected me. Hope it is right now. Please check.

_Mathieu says:_ No, this condition is some kind of surjectivity for the anafunctor.  I think you can define a saturated anafunctor as a "normal" anafunctor such that some diagram is a pullback.  Between internal groupoids, a saturated anafunctor is simply an internal distributor which is "functional" and "everywhere defined".

_Urs says:_ Okay, thanks. Somebody should fix the above then. 

_Toby says:_ I'm not sure that there is anything to say. Remember that, up to equivalence, all anafunctors are saturated. If I grasped more fully what cofibrations are, then I might be able to say something sensible here. (By the way, $k$-surjectivity doesn't na&#239;vely apply; at best, you'll have to replace epimoprphims with surjective submersions or something.)

_Urs says_: yes, I still need to complete the entry discussion on the [[homotopy theory]] structure on $n$-categories internal to spaces: the point is that one sets it up for the very general $Spaces := Sheaves(test domains)$ in which case epimorphisms are precisely the local/stalkwise section admitting maps. Then one can restrict that to $Manifolds \hookrightarrow Spaces$. If one requires that also all fiber products sit in $Manifolds$ (which is a matter of cosmetics more than of necessity) then one finds the need that the local section admitting surjections must actually be submersions.

_Toby says_: OK, that reminds me: Do you have a reference handy for the fact that submersions are precisely the maps in $Manifolds$ such that all pullbacks of these maps exist? This is a folk theorem for me, but I\'ve never written out a proof, so it always gives me doubts. (Anyway, I\'ll probably want to cite it sometime.)

_Urs says_: don't know a reference. But notice from the chain rule that a local smooth sections admitting surjection is already a submersion when restricted to the image of all possible local smooth sections. This gives a handle on how bad behaved local smooth sections admitting maps are that are not submersions on their entire domain.

_Toby says_: OK, thanks. I\'ll probably just have to sit down and work out the proofs and counterexamples for myself. (Possibly I can get David Roberts to do it, now that I think about it &#8230; I\'ll ask him.)

_Toby says_: I gave a more elementary definition of anafunctor above, including saturated anafunctor. So I removed the bad definition here.

=--

An anafunctor is an **anaequivalence** if it is a span as above, with the right leg also an acyclic fibration.
(For [[Lie groupoid]]s, these are the [[Morita equivalence]]s).

If we restrict from categories to groupoids, then according to the [[folk model structure|groupoid folk model structure]] by Brown-Golasinski all objects are _fibrant_ and then according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization of $Groupoids$ in that they represent all morphisms in the [[homotopy category]] $Ho(Groupoids)$.

By the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycle]]s on groupoids with values in groupoids. By the notion of [[descent and codescent|codescent]] such homotopical cocycles are related to [[descent and codescent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.

##Generalizations##

Since the [[folk model structure]] on $Categories$ extends to $\omega$-[[omega-category|categories]], also the anafunctor concept generalizes to these strict [[higher category theory|higher categories]]. Indeed, again by Brown-Golasinski, $\omega$-groupoids are fibrant with respect to the [[folk model structure]], so that the corresponding _$\omega$-anafunctors_ between $\omega$-groupoids represent cocycles in [[nonabelian cohomology]].

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