
#Contents#
* table of contents
{:toc}

## Definition

### By the cancellative property

A unital [[ring]] $R$ is an __integral domain__ (or simply domain) if it is nontrivial and the multiplicative submonoid $R \backslash \{0\}$ is a [[cancellative monoid]] (i.e., $1 \neq 0$ and left and right multiplication by $c$ is injective if $c \neq 0$, which may be combined as left and right multiplication by $c$ is injective if and only if $c \neq 0$) 

Some authors require an integral domain to be [[commutative ring|commutative]], even when they do not require this of rings in general.  Commutative integral domains are precisely subrings of [[fields]].

### By zero divisors

A unital [[ring]] $R$ is an __integral domain__ (or simply domain) if it is nontrivial and has no non-zero [[zero divisors]] (i.e., $1 \ne 0$ and $a b = 0$ implies $a = 0$ or $b = 0$). 

In this definition, the [[trivial ring]] is [[too simple to be simple|too simple]] to be an integral domain. You can see this by phrasing this definition without [[bias]] as: any product of (finitely many) nonzero elements of $R$ (which includes the empty product $1$) must be nonzero.

### In constructive mathematics

in constructive mathematics, there are different inequivalent ways to define an integral domain

#### Discrete integral domains

+-- {: .num_defn #discrete}
###### Definition

If we replace "left and right multiplication by $c$ is injective iff $c$ is nonzero" in the above definition by "left and right multiplication by $c$ is injective [[xor]] $c$ is zero" (which is equivalent in [[classical logic]] but stronger in [[constructive logic]]), then we obtain the notion of **discrete integral domain**.  This condition implies that $0 \neq 1$.
=--

Such an integral domain $D$ is 'discrete' in that it decomposes as a coproduct $D = \{0\} \sqcup D^\times$ (where $D^\times$ is the submomoid of $D$ that is cancellative). An advantage is that this is a [[coherent logic|coherent theory]] and hence also a [[geometric theory]].  A disadvantage is that this axiom is not satisfied (constructively) by the ring of [[real numbers]] (however these are defined), although it is satisfied by the ring of [[integers]] and the ring of [[rational number|rationals]].

#### Heyting integral domains

+-- {: .num_defn #heyting}
###### Definition

If we interpret 'nonzero' as a reference to a [[tight apartness relation]] $\#$, thus defining the apartness relation $\#$ by $x#y$ if left and right multiplication by $x - y$ is injective, then we obtain the notion of **Heyting integral domain**. (As shown [here](/nlab/show/local+ring#internal), the ring operations become [[strong extensionality|strongly extensional]] functions). It follows that every element apart from $0$ is not a zero divisor. 
=--

This is how 'practising' constructive analysts of the Bishop school usually define the simple word 'integral domain'. 

An advantage is that the (located Dedekind) [[real numbers]] form a Heyting integral domain. A disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories.

Of course, if the underlying set of the ring has [[decidable equality]] ---as is true of $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{Z}/n$, [[finite fields]], etc--- then a Heyting integral domain is a discrete integral domain.

## Properties

An integral domain $R$ is an __[[Ore domain]]__ if the set of all nonzero elements is an [[Ore set]] in $R$. In that case the Ore localized ring is called the _[[Ore quotient ring]]_ of $R$.

## Examples

For example, the ring of [[integers]], any [[skewfield]], the ring of global sections of the structure sheaf of any [[integral scheme]], an [[Ore extension]] of any other integral domain.

## Generalizations

In principle, one could just as easily consider a [[rig]] or [[semiring]] $R$.  In that case, however, only the definition involving the cancellative property extends to rigs and semirings. Furthermore, we should add the additional requirement that addition in $R$ is cancellable (that is, addition by any element is injective), to make the analogue of the previous paragraph correct.  Since 'integral domain' is too specific and 'integral ring' is not standard (and means something else in the phrase 'integral ring extension'), it\'s not clear exactly what these should be called; perhaps _integral cancellable rig/semiring_ is sufficiently unambiguous. 

## Related concepts

* [[Dedekind domain]]

* [[field]], [[field of fractions]]

* [[integral monoid]]

[[!redirects integral domain]]
[[!redirects integral domains]]

[[!redirects integral cancellable rig]]
[[!redirects integral cancellable rigs]]
[[!redirects integral cancellable semiring]]
[[!redirects integral cancellable semirings]]

[[!redirects discrete integral domain]]
[[!redirects discrete integral domains]]

[[!redirects Heyting integral domain]]
[[!redirects Heyting integral domains]]
[[!redirects heyting integral domain]]
[[!redirects heyting integral domains]]