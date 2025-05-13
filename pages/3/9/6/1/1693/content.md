
# Boolean rigs
* table of contents
{: toc}

## Idea

As a [[Boolean ring]] is a [[ring]] in which multiplication is [[idempotent]], so a Boolean rig is a [[rig]] in which multiplication is idempotent; that is, a rig in which $x^2 = x$ always holds.

While many further properties follow from the idempotence of multiplication in a ring, most of these require subtraction (or at least cancellation of addition), so these will not necessarily hold for a Boolean rig. As such, it might be proper to add some of them as axioms for a Boolean rig.

## Properties

Even without subtraction, we may define the Boolean join operation $x \vee y \coloneqq x + x y + y$; however, it also seems to have no nice properties without additional axioms.  In a *commutative* Boolean rig, however, we can prove that multiplication distributes over join, meaning that multiplication and join together form another rig structure.  But we cannot prove that this rig is also Boolean, or that join is a [[semilattice]] operation; in fact, if the Boolean rig is a [[distributive lattice]], then the "join" operation defined above is the same as the addition operation. 

## Examples

The main examples are probably [[distributive lattices]].  In this case, the join operation called $\vee$ above will match the original join/addition operation called $+$ above.

Of course, a [[Boolean ring]] is a Boolean rig, since any ring is a rig.  However, since it\'s also a distributive lattice, a Boolean ring is actually a Boolean rig in two different ways.

Let see what are the smallest commutative boolean rigs.

- The only boolean rig of cardinal $1$ is the zero ring $0$.

There are exactly two boolean rings of cardinal $2$. In such a boolean ring, we necessarily have $0 \neq 1$, because $0=1$ would imply that $x=1.x=0.x=0$ for every $x$ and then the boolean ring would be the zero ring $0$. The two elements of the boolean rings are thus $0$ and $1$. From the axioms of a rig, we have $0+0=0$, $1+0=0+1=1$, $0.0=0$, $1.0=0.1=0$ and $1.1=1$. We then have two possibilities for $1+1$, either $0$ or $1$. The two possibilities give a boolean rig. The multiplications being commutative, one has only to check the distributivity $(a+b).c = a.c +b.c$. 

- One of the two boolean rigs of cardinal $2$ is $\mathbb{Z}/2\mathbb{Z}$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[exclusive disjunction]] and $.$ as the [[conjunction]]).
- One of the two boolean rigs of cardinal $2$ is $\mathbb{B}=\{0,1\}$ where $1+1=1$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[disjunction]] and $.$ as the [[conjunction]]).

## Related concepts

* [[Boolean algebra]]
* [[Boolean ring]]
* [[01-bounded semilattice]]

## References

There seem to be none.  The 'Boolean semirings' in the literature (by which I mean, what Google found for me that wasn\'t cloaked) are something much more complicated than what we\'re looking at here.

[[!redirects Boolean rig]]
[[!redirects Boolean rigs]]
[[!redirects boolean rig]]
[[!redirects boolean rigs]]

[[!redirects Boolean semiring]]
[[!redirects Boolean semirings]]
[[!redirects boolean semiring]]
[[!redirects boolean semirings]]
