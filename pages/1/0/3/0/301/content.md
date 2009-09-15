<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


Classically, a __truth value__ is either $\top$ (True) or $\bot$ (False). (In [[constructive mathematics]], this is not so simple, although it still holds that any truth value that is not true is false.)

More generally, a __truth value__ in a [[topos]] $T$ is a morphism $1 \to \Omega$ (where $1$ is the [[terminal object]] and $\Omega$ is the [[subobject classifier]]) in $T$.  By definition of $\Omega$, this is equivalent to an (equivalence class of) monomorphisms $U\hookrightarrow 1$.  In a [[two-valued topos]], it is again true that every truth value is either $\top$ or $\bottom$, while in a [[Boolean topos]] this is true in the [[internal logic]].

Truth values form a [[partial order|poset]] by declaring that $p$ precedes $q$ iff the [[conditional]] $p \to q$ is true.  In a topos $T$, $p$ precedes $q$ if the corresponding subobject $P\hookrightarrow 1$ is contained in $Q\hookrightarrow 1$.  Classically (or in a two-valued topos), one can write this poset as $\{\bot \to \top\}$.

The poset of truth values is a [[Heyting algebra]]. Classically (or internal to a Boolean topos), this poset is even a [[Boolean algebra]]. It is also a [[complete lattice]]; in fact, it can be characterised as the [[initial object|initial]] complete lattice. As a complete Heyting algebra, it is a [[frame]], corresponding to the one-point [[locale]].

When the set of truth values is equipped with the [[specialization topology]], the result is [[Sierpinski space]].

A truth value may be interpreted as a $0$-[[0-poset|poset]] or as a $(-1)$-[[(-1)-groupoid|groupoid]]. It is also the best interpretation of the term '$(-1)$-[[(-1)-category|category]]', although this doesn\'t fit all the patterns of the [[periodic table]].

# Discussion

From [[(-1)-groupoid]]: 

+--{.query}
  _[[Urs Schreiber|Urs]]:_ Can't this be motivated more systematically?

  _[[Mike Shulman|Mike]]:_ There's a funny weirdness that happens at the bottom with the relationship between sets and posets.  I don't completely understand it, nor do I know any reason why "we should expect" the $0$-category of $(-1)$-groupoids to be a $(0,1)$-category, since the 1-category of 0-groupoids (sets) is not a $(1,2)$-category (except trivially).  On the other hand, the 1-category of $(0,1)$-categories is a $(1,2)$-category, so maybe the point is that every $(-1)$-groupoid is actually a $(-1,0)$-category?

I don't really understand why we have separate pages for $(-1)$-groupoids and $(-1)$-categories; has anyone ever come up with a way in which they are different?

_Toby_: There are separate pages [[truth value]], [[(-1)-groupoid]], [[(-1)-category]] and (eventually) [[0-poset]]. Partly it\'s that [[(-1)-category]] was written first, although it\'s the worst name. But I think that it will be good, given the nature of this wiki, to have pages organised more by term than subject (I will write a bit about this on the Caf&#233;). But this means that the pages will have different purposes.

As [[truth value]] is the most mundane and ordinary name for the concept, that page will have the most content. There we should discuss what a truth value is in a topos or other sort of category, or what it is to a constructivist or other sort of alternative mathematician; there we should discuss how truth values form a poset, and what structures and properties this poset has; there we should talk about what categories and groupoids enriched over this poset (with either of the two obvious monoidal structures) are.

At [[(-1)-category]], which exists only because we like $n$-categories so much and so wonder what an $(-1)$-category is, we explain why the concept is a little fishy but the best way to define it is as a truth value. And there we show how this fits the patterns of the periodic table to the extent that it does, and also poitn out those cases where it doesn\'t.

At [[(-1)-groupoid]], which again exists because that\'s our special thing, we explain why a $(-1)$-groupoid is a truth value, and how that fits the patterns of the periodic table.

At [[0-poset]], we\'ll do exactly the same thing, only thinking about $n$-posets rather than $n$-groupoids.

(If this were Wikipedia, we would not organise things this way. I\'ll discuss that at the Caf&#233;.)

In particular, I think that general facts about internalising the concept to categories other than $\Set$ work best at [[truth value]], while they would really fit in here only if we wanted to explain how that reproduces (or, conceivably, turns out to be different from) a general method for internalising the concept of $n$-groupoid. (Probably we will eventually want to talk about that, but as far as I know there\'s nothing to say about it now.)

By the way, here is the answer to Mike\'s question about what "we should expect": the $\infty$-category of $(n,r)$-categories is an $(n+1,r+1)$-category (which I should discuss on [[(n,r)-category]] but have not); accordinly, the $\infty$-category of $n$-groupoids is an $(n,1)$-category. In particular, the $\infty$-category of $(-1)$-groupoids is a $(0,1)$-category.
=--

[[!redirects truth values]]