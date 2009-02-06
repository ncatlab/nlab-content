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

Every functor may be interpreted as an anafunctor, with $|F|$ always taken to be the set of objects in $C$. That every anafunctor is equivalent to a functor is equivalent to the axiom of choice, in which case the inclusion of functors into anafunctors is in fact an equivalence of categories. But if you ignore functors and deal only with anafunctors (or saturated anafunctors), then the theory is entirely [[constructivism|constructive]] (without using the axiom of choice or even excluded middle). Theorems that classically required choice now don\'t require choice (and indeed become constructive) with anafunctors. Thus, anafunctors (or even saturated anafunctors) are the correct notion to use if you are a constructivist (at least as long as you [[foundations|found]] mathematics on some sort of set theory at all); but they are also often the correct notion to use in [[internal category]] theory.


#Definition (internal)#

Given an anafunctor $F:C\to D$ as above, we can construct a new category $\overline{F}$ whose objects are the specifications of $F$ and whose morphisms from $s$ to $t$ are the morphisms from $\sigma(s)$ to $\sigma(t)$ in $C$.  Then the projection $\overline{F}\to C$ is an [[equivalence]] of categories which is surjective on objects, and the rest of the data of $F$ is encapsulated in a functor $\overline{F}\to D$.  Conversely, from any span $C \leftarrow E \to D$ such that $E\to C$ is a surjective equivalence we can reconstruct an anafunctor whose specifications are the objects of $E$.  Thus, anafunctors $C\to D$ can be identified with such spans.

More generally, let $S$ be a category containing a collection of morphisms called "covers" such that

* every isomorphism is a cover,
* any [[pullback]] of a cover exists and is a cover,
* covers are closed under composition,
* every cover is the quotient of its kernel pair.

The first three axioms are the requirements for the covers to form a [[Grothendieck pretopology]] with covering families only containing a single map. The fourth axiom says that this pretopology is [[subcanonical]], and is needed to compose natural transformations between anafunctors. Note that if $S$ has pullbacks, the fourth axiom just says that covers are regular epimorphisms.

One important class of examples is when $S$ is a [[regular category]] and the covers are the [[regular epimorphism]]s.  Another is when $S$ is the category of smooth manifolds and the covers are the surjective submersions.  More generally, $S$ could be equipped with a Grothendieck [[coverage]] and the covers are the maps which generate a covering sieve.

+-- {: .query}

David Roberts says: If one uses a coverage, then composing anafunctors means a choice has to be made in the filler of $U \to D_0 \leftarrow V$ with the right map a cover. Presumably the resulting bicategory of anafunctors is independent, up to biequivalence, of the choices made. Also, at the very least the identity map has to be a cover, so as to define the identity anafunctor. 

DR says: Well I suppose we could follow Makkai's philosophy twice and have a composition anafunctor (in the original sense) for composing anafunctors (in the internal sense) and end up with an anabicategory.

_Mike_: Yes, presumably it won't depend on the fillers chosen; I haven't checked the details, though.  "Grothendieck coverage" means the same as "Grothendieck topology" and thus includes closure under lots of things, including composition and containing identities.

=--



In such a situation, if $C$ and $D$ are [[internal category|internal categories]] in $S$, we define an __anafunctor__ $F: C\to D$ to consist of a span $C\leftarrow E \to D$ of internal functors such that:

1. $E\to C$ is fully-faithful, in the internal sense that the following is a pullback square:
$$\array{E_1 & \to & C_1 \\ \downarrow && \downarrow \\ E_0\times E_0& \to & C_0\times C_0}$$

1. $E_0\to C_0$ is a cover.

By the remarks above, if $S=Set$ and "cover" means "surjection" (or equivalently, "regular epi"), then we recover the above-defined external notion of anafunctor.

In [HGT I][] the following additional axiom was assumed on the class of covers,

* every equivalence relation involving a cover has a quotient, which is a cover.

This is used in the section on descent and its relation to (2-)bundles.

#Homotopy-theoretic interpretation#

Observe that the surjective-on-objects equivalences are precisely the [[model category|acyclic fibrations]] for the [[folk model structure]] on [[Cat]].  Therefore, anafunctors can be identified with the "one-step generalized morphisms" in $Cat$ whose first leg is not just a weak equivalence but an acyclic fibration.

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


## References

* [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/) (first explicit formulation of anafunctors)

* [Higher gauge theory I: 2-Bundles][HGT I] (first explicit formulation of internal anafunctors)

* [Local Transition of Transport, Anafunctors and Descent of n-Functors](http://golem.ph.utexas.edu/category/2006/12/local_transition_of_transport.html) (first explicit formulation of $n$-anafunctors)

* [Model structures for homotopy of internal categories][EKV 2004]


[EKV 2004]: http://www.tac.mta.ca/tac/volumes/15/3/15-03abs.html
[HGT I]: http://arxiv.org/abs/math.CT/0410328
