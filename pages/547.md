A [[category]] $C$ is **well-powered** if every object has a [[small category|small]] [[partial order|poset]] of [[subobject]]s.

Assuming that by 'subobject' we mean (an equivalence class of) [[monomorphism|monomorphisms]], this means that for every object $X$, the (generally large) [[preorder]] of monomorphisms with codomain $X$ is equivalent to a small poset.  Variations exist that use notions of subobject other than monomorphisms.

If $C^{op}$ is well-powered, we say that $C$ is **well-copowered** (although "cowell-powered" is also common).

# Relation to local smallness #

A well-powered category with binary [[product|products]] is always [[locally small category|locally small]], since morphisms $f: A \to B$ can be identified with particular subobjects of $A \times B$ (their [[graph]]s).

Conversely, any locally small category with a [[subobject classifier]] must obviously be well-powered.  In particular, a [[topos]] is locally small if and only if it is well-powered.