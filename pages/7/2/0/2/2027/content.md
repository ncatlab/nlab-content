
#Contents#
* table of contents
{:toc}

## Definition

A unital [[ring]] $R$ is an __integral domain__ (or simply domain) if it is nontrivial and has no non-zero [[zero divisors]] (i.e., $1 \ne 0$ and $a b = 0$ implies $a = 0$ or $b = 0$). For example, the ring of [[integers]], any [[skewfield]], the ring of global sections of the structure sheaf of any [[integral scheme]], an [[Ore extension]] of any other integral domain.

In [[constructive mathematics]], one wants to phrase the condition as $a b \neq 0$ whenever $a \neq 0$ and $b \neq 0$, where $\neq$ is a tight [[apartness relation]] relative to which the ring operations are strongly extensional.  (Of course, if the underlying set of the ring has [[decidable equality]] ---as is true of $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{Z}/n$, [[finite fields]], etc--- then this is trivial.)

The [[trivial ring]] is [[too simple to be simple|too simple]] to be an integral domain.  You can see this by phrasing the definition without [[bias]] as: any product of (finitely many) nonzero elements of $R$ (which includes the empty product $1$) must be nonzero.

Another equivalent definition is: an integral domain is any [[subring]] of a [[skewfield]].  Specifically, any integral domain $R$ is a subring of its [[field of fractions]].

Some authors require an integral domain to be [[commutative ring|commutative]], even when they do not require this of rings in general.  Then they are subrings of [[fields]].

In principle, one could just as easily consider a [[rig]] or [[semiring]] $R$.  In that case, however, a [[zero divisor]] is not what the name literally implies: the definition is that multiplication by a nonzero element (on either side) is injective.  Furthermore, we should add the additional requirement that addition in $R$ is cancellable (that is, addition by any element is injective), to make the analogue of the previous paragraph correct.  Since 'integral domain' is too specific and 'integral ring' is not standard (and means something else in the phrase 'integral ring extension'), it\'s not clear exactly what these should be called; perhaps _integral cancellable rig/semiring_ is sufficiently unambiguous.

An integral domain $R$ is an __[[Ore domain]]__ if the set of all nonzero elements is an [[Ore set]] in $R$. In that case the Ore localized ring is called the _[[Ore quotient ring]]_ of $R$.


## Related concepts

* [[Dedekind domain]]


[[!redirects integral domain]]
[[!redirects integral domains]]

[[!redirects integral cancellable rig]]
[[!redirects integral cancellable rigs]]
[[!redirects integral cancellable semiring]]
[[!redirects integral cancellable semirings]]