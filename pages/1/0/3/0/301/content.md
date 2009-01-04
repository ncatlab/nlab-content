Classically, a __truth value__ is either $\top$ (True) or $\bot$ (False). (In [[constructive mathematics]], this is not so simple, although it still holds that any truth value that is not true is false.)

More generally, a __truth value__ in a [[topos]] $T$ is a morphism $1 \to \Omega$ (where $1$ is the [[terminal object]] and $\Omega$ is the [[subobject classifier]]) in $T$.  By definition of $\Omega$, this is equivalent to an (equivalence class of) monomorphisms $U\hookrightarrow 1$.  In a [[two-valued topos]], it is again true that every truth value is either $\top$ or $\bottom$, while in a [[Boolean topos]] this is true in the [[internal logic]].

Truth values form a [[poset]] by declaring that $p$ precedes $q$ iff the [[conditional]] $p \to q$ is true.  In a topos $T$, $p$ precedes $q$ if the corresponding subobject $P\hookrightarrow 1$ is contained in $Q\hookrightarrow 1$.  Classically (or in a two-valued topos), one can write this poset as $\{\bot \to \top\}$.

The poset of truth values is a [[Heyting algebra]]. Classically (or in a [[Boolean topos]]), this poset is even a [[Boolean algebra]]. It is also a [[complete poset]]; in fact, it can be characterised as the [[initial object|initial]] complete poset. As a complete Heyting algebra, it is a [[frame]], corresponding to the one-point [[locale]].

A truth value may be interpreted as a [[0-poset]] or as a [[(-1)-groupoid]]. It is also the best interpretation of the term '[[(-1)-category]]', although this doesn\'t fit all the patterns of the [[periodic table]].
