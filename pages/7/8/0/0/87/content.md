#Idea#

**Anafunctors** are the proper notion of morphism to use between categories in a context where the [[axiom of choice]] fails. Functors, as normally defined, are really not the correct concept.

Anafunctors were first developed by [[Michael Makkai]] to do ordinary category theory with a [[foundations]] that does not include the axiom of choice. Later they were applied by [[Toby Bartels]] to [[internal category|internal categories]], where the axiom of choice is simply not an option. These actually turned out to be known already (at least up to equivalence) in some contexts, in particular as [[Hilsum-Skandalis morphism]]s between [[Lie groupoid]]s.

#Definition (external)#

Given categories $C$ and $D$, an __anafunctor__ $F: C \to D$ consists of:

* a set $|F|$ of _specifications_ of $F$;
* maps $\sigma: |F| \to C$ and $\tau: |F| \to D$ (taking values in objects). Given $x: C$ and $y: D$, we say that $y$ is a _specified value_ of $F$ at $x$ if, for some $s: |F|$, $x = \sigma(s)$ and $y = \tau(s)$; in this case, $s$ _specifies_ $y$ as a value of $F$ at $x$, and we write $F_s(x) = y$. We say that $y$ is a _value_ of $F$ at $x$ if $y$ is isomorphic (in $D$) to some specified value of $F$ at $x$; we write $F(x) \cong y$. (There is no notion of *the* value of $F$ at $x$, and $F(x) = y$ is meaningless.);
* for each $s, t: |F|$ and morphism $f: \sigma(s) \to \sigma(t)$ in $C$, a morphism $F_{s,t}(f): \tau(s) \to \tau(t)$ in $D$. Similarly to the above, we can define whether a given morphism $g$ in $D$ is a _specified value_ of $F$ at a given morphism $f$ in $C$ or whether $g$ is (merely) a _value_ of $F$ at $f$. (Again, there is no notion of *the* value of $F$ at $f$.);
* $\sigma$ is a surjective function. Thus, $F$ has *some* value at any given object or morphism of $C$. (In the [[internalization|internalized]] case, this requirement can become quite complicated; for example, internal to manifolds, one requires a surjective submersion.);
* $F$ preserves identities. That is, $s: |F|$, the value of $F$ specified by $s$ and $s$ at the identity of $\sigma(s)$ is the identity of $\tau(s)$, or (in symbols) $F_{s,s}(\id_{\sigma(s)}) = \id_{\tau(s)}$, or (whenever this makes sense) $F_{s,s}(\id_x) = \id_{F_s(x)}$;
* $F$ preserves composition. That is, given $s, t, u: |F|$, $f: \sigma(s) \to \sigma(t)$, and $g: \sigma(t) \to \sigma(u)$, $F_{s,u}(f;g) = F_{s,t}(f);F_{t,u}(g)$. (Here the semicolon indicates composition in the anti-Leibniz order.).

An anafunctor $F$ is __saturated__ if, whenever $F(x) \cong y$, $F_s(x) = y$ for some unique specification $s$, where the unicity of $s$ depends not only on $x$ and $y$ but also on how $y$ is a value of $F$ at $x$. To be precise: if $g: y' \to y$ is an isomorphism in $D$ and $F_{s'}(x) = y'$ for some specification $s'$, then there is a unique specification $s$ such that $F_{s',s}(\id_x) = g$ (so in particular, $\sigma(s) = x$ and $F_s(x) = y$). Every anafunctor $F: C \to D$ has a _saturation_ $\overline{F}$; $\overline{F}$ is a saturated anafunctor and $F \cong \overline{F}$ in the category of anafunctors from $C$ to $D$. In fact, the inclusion of the saturated anafunctors into the anafunctors (as a full subcategory) is an equivalence of categories (given fixed $C$ and $D$).

Every functor may be interpreted as an anafunctor, with $|F|$ always taken to be the set of objects in $C$. That every anafunctor is equivalent to a functor is equivalent to the axiom of choice, in which case the inclusion of functors into anafunctors is in fact an equivalence of categories. But if you ignore functors and deal only with anafunctors (or saturated anafunctors), then the theory is entirely [[constructive mathematics|constructive]] (without using the axiom of choice or even excluded middle). Theorems that classically required choice now don\'t require choice (and indeed become constructive) with anafunctors. Thus, anafunctors (or even saturated anafunctors) are the correct notion to use if you are a constructivist (at least as long as you [[foundations|found]] mathematics on some sort of [[set theory]] at all); but they are also often the correct notion to use in [[internal category]] theory.


#Definition (internal)#

Given an anafunctor $F:C\to D$ as above, we can construct a new category $\overline{F}$ whose objects are the specifications of $F$ and whose morphisms from $s$ to $t$ are the morphisms from $\sigma(s)$ to $\sigma(t)$ in $C$.  Then the projection $\overline{F}\to C$ is a (weak) [[equivalence of categories]] which is surjective on objects, and the rest of the data of $F$ is encapsulated in a functor $\overline{F}\to D$.  Conversely, from any span $C \leftarrow E \to D$ such that $E\to C$ is a surjective equivalence we can reconstruct an anafunctor whose specifications are the objects of $E$.  Thus, anafunctors $C\to D$ can be identified with such spans.  (We can also construct an anafunctor when $E \to C$ is merely an equivalence, but using a much larger class of specifications.)

More generally, let $S$ be a category containing a collection of morphisms called "covers" such that

* every isomorphism is a cover,
* covers are closed under composition,
* any [[pullback]] of a cover exists and is a cover ([[pullback stability]]),
* every cover is the [[quotient object]] of its [[kernel pair]] (equivalently, every cover is a [[regular epimorphism]]).

+--{: .query}
_David R_ says: aren't these two conditions  only equivalent if the category has pullbacks? That is what it says at [[regular epimorphism]]. A map being the quotient of its kernel pair is an effective epimorphism, is it not?

_Mike_: I think it only <del>says</del> said that at regular epimorphism because <del>whoever wrote that sentence</del> I wasn't thinking about the case of categories that have _particular_ pullbacks but not all pullbacks.
=--

Note that these are precisely the axioms saying that the singleton families $\{p:V\to U\}$ where $p$ is a cover form a [[subcanonical coverage|subcanonical]] [[Grothendieck pretopology]].  One important class of examples is when $S$ is a [[regular category]] and the covers are the [[regular epimorphism]]s.  Another is when $S$ is the category of smooth manifolds and the covers are the surjective submersions.

In such a situation, if $C$ and $D$ are [[internal category|internal categories]] in $S$, we define an __anafunctor__ $C\to D$ to consist of a span $C\leftarrow F \to D$ of internal functors such that:

1. $F_0\to C_0$ (the map of objects) is a cover.

1. $F\to C$ is [[ff morphism|fully-faithful]], in the internal sense that the following is a pullback square:
$$\array{F_1 & \to & C_1 \\ \downarrow && \downarrow \\ F_0\times F_0&   \to & C_0\times C_0}$$

Note that assuming $F_0\to C_0$ is a cover, so is $F_0\times F_0\to C_0\times C_0$ (it is a composition of pullbacks of $F_0\to C_0$); thus the above pullback always exists.

By the remarks above, if $S$ is [[Set]] and "cover" means "[[surjection]]" (an example where the covers are the regular epimorphisms), then we recover the original external notion of ([[small category|small]]) anafunctor.

If $C\leftarrow F \to D$ and $C\leftarrow G \to D$ are internal anafunctors, we define a __natural transformation__ between them to be a natural transformation between the two induced internal natural transformations $F\times_C G \to D$.  We can then prove that internal categories, anafunctors, and natural transformations form a [[bicategory]].  (Interestingly, you may need the axiom of choice in the [[metalogic]] to conclude this, depending on whether their is a natural way to choose the necessary pullbacks; else you get an [[anabicategory]], which is Makkai\'s version of a bicategory to be used in the absence of choice.)

The role of the assumptions about covers is:

* Identity maps must be covers in order to have identity anafunctors (and more generally, for every functor to give rise to an anafunctor).
* To compose anafunctors by pullback, the pullbacks of covers must exist and be covers, and covers must be closed under composition.
* To define $F \times_C G$ and obtain a notion of natural transformation, we again need covers to have pullbacks.
* To define composition of natural transformations between anafunctors, we need covers to be effective; see diagram (118) in [HGT I][].

In Section 1.1.5 of [HGT I][], the following additional axiom was assumed on the class of covers:

* every [[congruence]] involving a cover has a quotient object which is a cover.

This is not needed for anafunctors but is used to relate descent to bundles (and then to $2$-bundles).





#Homotopy-theoretic interpretation#

Observe that the surjective-on-objects equivalences are precisely the [[model category|acyclic fibrations]] for the [[folk model structure]] on [[Cat]].  Therefore, anafunctors can be identified with the "one-step generalized morphisms" in $Cat$ whose first leg is not just a [[weak equivalence]] but an acyclic fibration.

More generally, it is proven in [EKV 2004][] that if $S$ has a Grothendieck coverage, then under suitable additional conditions on $S$, there is a [[model category|model structure]] on the category $Cat(S)$ of internal categories in $S$ relative to that coverage.  The internal anafunctors relative to the given coverage, as defined above, can then once again be identified with the spans whose first leg is an acyclic fibration.

An anafunctor is an **anaequivalence** if it is a span as above, with the right leg also an acyclic fibration.
(For [[Lie groupoid]]s, these are the [[Morita equivalence]]s).

If we restrict from categories to groupoids, then according to the [[folk model structure|groupoid folk model structure]] by Brown-Golasinski all objects are _fibrant_ and then according to Kenneth Brown's theorem in [[homotopical cohomology theory]] it follows that one-step generalized morphisms already realize the full localization of $Groupoids$ in that they represent all morphisms in the [[homotopy category]] $Ho(Groupoids)$.

By the general idea of [[homotopical cohomology theory]]
this means that anafunctors between groupoids represent [[nonabelian cocycle]]s on groupoids with values in groupoids. By the notion of [[descent and codescent|codescent]] such homotopical cocycles are related to [[descent and codescent|descent data]] that enters the definition of [[sheaf|sheaves]] and [[stack]]s.

##Generalizations##

Since the [[folk model structure]] on $Cat$ extends to $\omega$-[[strict omega-category|categories]], also the anafunctor concept generalizes to these strict [[higher category theory|higher categories]]. Indeed, again by Brown-Golasinski, strict $\omega$-groupoids are fibrant with respect to the [[folk model structure]], so that the corresponding $\omega$-[[schreiber:omega-anafunctors|anafunctors] between $\omega$-groupoids represent cocycles in [[nonabelian cohomology]].

More details on $\omega$-anafunctors are described in the context of [[schreiber:Differential Nonabelian Cohomology]] in the private area of the $n$Lab. See [[schreiber:omega-anafunctor]].

## Additive version ##

The notion of abelian [[butterfly]] introduced by Behrang Noohi [Weak maps of 2-groups](http://arxiv.org/abs/math.CT/0506313) is the additive version of the notion of (saturated) anafunctor: the equivalence between, on the one hand, internal groupoids and internal functors and, on the other hand, arrows and commutative squares in an abelian category extends to an equivalence between saturated anafunctors and butterflies.

+-- {: .query}

_Urs says:_ Why do you restrict this to the abelian case? From 
[page  16](http://arxiv.org/PS_cache/math/pdf/0506/0506313v3.pdf#page=16)  of Noohi's article I got the impression that he is precisely describing the ana-2-functors between one-object 2-groupoids in terms of the corresponding (possibly nonabelian) crossed modules. 

_Mathieu says:_ I don't see that (or something like that) on that page, but saturated anafunctors should correspond to butterflies also in the semi-abelian case (using the notion of internal crossed module in a semi-abelian category introduced by Janelidze), but I have not checked it.  The special case of groups is probably easy to check: saturated anafunctors between two internal groupoids in the category of groups should correspond to butterflies between the corresponding crossed modules.

_Urs says:_ I haven't checked the details. But he is looking at derived homs of crossed complexes. By general nonsense these derived hom should be given by homs out of cofibrant replacements. This is another way of talking about the anafunctor picture. Somebody should check the details.


=--
# References

* [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/) (first explicit formulation of anafunctors)

* [Higher gauge theory I: 2-Bundles][HGT I] (first explicit formulation of internal anafunctors)

* [Local Transition of Transport, Anafunctors and Descent of n-Functors](http://golem.ph.utexas.edu/category/2006/12/local_transition_of_transport.html) (first explicit formulation of $n$-anafunctors)

* [Model structures for homotopy of internal categories][EKV 2004]


[EKV 2004]: http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html
[HGT I]: http://arxiv.org/abs/math.CT/0410328

#Discussion#

The following discussion was about the effect of different notions of [[coverage]] on the definition of and operations on anafunctors. 


David Roberts says: If one uses a coverage, then composing anafunctors means a choice has to be made in the filler of $U \to D_0 \leftarrow V$ with the right map a cover. Presumably the resulting bicategory of anafunctors is independent, up to biequivalence, of the choices made. Also, at the very least the identity map has to be a cover, so as to define the identity anafunctor. 

DR says: Well I suppose we could follow Makkai's philosophy twice and have a composition anafunctor (in the original sense) for composing anafunctors (in the internal sense) and end up with an anabicategory.

_Mike_: Yes, presumably it won't depend on the fillers chosen; I haven't checked the details, though.  "Grothendieck coverage" means the same as "Grothendieck topology" and thus includes closure under lots of things, including composition and containing identities.

_David R_: I noticed the adjective Grothendieck in the preceeding sentence half-way through asking the question, but I think my point still holds for general coverages, without the closure properties.

_Mike_: Well, as you pointed out, you need at least identity maps to be covers to have identity anafunctors, and you need covers to be stable under composition, as well as pullback, in order to define composition of anafunctors.  An arbitrary coverage might not satisfy those, although pretty much any coverage arising in practice does.  The other point that a choice has to be made unless you have honest pullback-stability is certainly true.  So probably the most natural-feeling context in which to work is a (possibly singleton) [[Grothendieck pretopology]].  I would be happy for this page to ignore the case where covers don't have pullbacks; I did some rewriting above to reflect this discussion.  I think this discussion could now be deleted; feel free to do so if you agree.

_David R_: After some thought, one could do without _the_ identity anafunctor, and be satisfied with a anafunctor (of the external variety) giving the identity: $1 \to Ana(X,X)$. I think I should move this discussion to a section of its own, and develop these ideas there. As an aside, I think I saw an example of a non-Grothendieck coverage in John and Alex's [[generalized smooth space|smooth spaces]] paper.

_Toby_: You only get an anabicategory anyway, because of the choice of pullbacks (unless the structure of the coverage fixes these, as can be done in $Set$).

Anafunctors really should make sense in any [[site]] whatsoever (as long as we can compose ananatural transformations, which I guess we can if the site is subcanonical).  The trick of getting away with single maps (as one can do, for example, in a superextensive site) is not really necessary.  In fact, using a coverage makes the definitions, while more complicated, really look more natural in topological categories.