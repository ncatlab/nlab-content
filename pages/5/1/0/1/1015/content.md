A **set theory** is a theory of [[set]]s.

**Na&#239;ve set theory** is the basic algebra of the [[subset]]s of any given set $U$, together with a few levels of [[power set]]s, say up to $\mathcal{P}\mathcal{P}\mathcal{P}U$ and possibly no further.  Often students see this first for the set of [[real number]]s as $U$ (although in fact one could start with the set of [[natural number]]s and go one level further for an equivalent theory).  One could also use [[function set]]s instead of power sets as the basic set-forming operation (especially for a [[predicative mathematics|predicative]] theory).

Once you start thinking very much about the nature of sets in general (rather than merely *using* na&#239;ve set theory), it quickly becomes clear that one must be careful about how one can and cannot form sets.  Georg Cantor is credited with being the first to think about sets this deeply; although he did not propose a system of general rules for valid set-making operations, he recognised that some sets were 'inconsistent'.  Gottlob Frege\'s set theory was found (by Bertrand Russell) to be logically trivial because he was too careless in this regard.

There are two ways to go about doing a more careful **axiomatic set theory**.  The more ambitious is to develop set theory as [[foundations]] for all of mathematics.  This is what Frege proposed (although he failed through inconsistency); Ernst Zermelo is credited with the first consistent foundational set-theory.  A variation of Zermelo\'s system (developed by Fraenkel and Skolem and called Zermelo--Fraenkel set theory or ZFC) is the orthodox foundations today, although it needs to be supplemented by [[Grothendieck universe]]s (or something along those lines) to handle modern [[category theory]].

ZFC is a form of **material set theory** (the term used by [[Steve Awodey]]) in which everything is a [[pure set]], including the elements of sets themselves, and any two sets may be meaningfully compared to ask if they are [[equal]] or if one is a member of the other.  As a slight variation (still material set theory), one may accept ur-elements (or atoms), but it is still meaningful to ask whether any ur-element or set is an element of a given set.

Another approach to set-theoretic foundations is **structural set theory** (the term used by [[Mike Shulman]]), which looks more like [[type theory]].  Here, the elements of sets have no structure (and in particular are not themselves sets), and elements of different sets cannot be compared by default.  Among category theorists, it\'s popular to specify elementary properties of [[Set|the category of sets]]; the orthodoxy here (to the extent that there is one) is probably Bill Lawvere\'s [[ETCS]].  It is weaker than ZFC and must be supplemented to handle some esoteric parts of modern mathematics, although it suffices for most everyday uses.

Both pure set theory and structural set theory are **foundational set theories**; it is also possible to make a **definitional set theory**, in which one defines sets in terms of some more primitive concept.  Lawvere also proposed a foundation based on [[Cat|the category of categories]]; then a set may be defined as a [[discrete category]].  In [[constructive mathematics]], a foundation based on [[type theory]] is popular, with types interpreted as _[[tobybartels:preset|presets]]_ (sets without [[equality]]); then a set may be defined as a preset equipped with an [[equivalence relation]] (the term [[setoid]] is also used for such a gadget).  In [[computer science]], a foundation based on the [[lambda-calculus]]s is sometimes seen; in these terms, the concept of _[[list]]_ is more natural than set, with the difference being that sets have a coarser notion of equality.

Category theory can provide a common [[model theory]] to compare all of these notions.  Although only structural set theories like ETCS treat the elementary properties of the category $Set$ of sets as fundamental, one can ask for any set theory what properties $Set$ satisfies and compare them in those terms.  At the very least, $Set$ should be a [[pretopos]].

# Remarks #

* There is also [[algebraic set theory]], in which a material set theory (such as ZFC) is interpreted in the [[internal logic]] of some [[ambient category]], often called a "category of classes."


[[!redirects material set theory]]
[[!redirects structural set theory]]
