
> This is about [[rigs]] whose multiplication is [[idempotent]]. For rigs whose addition is idempotent, see [[additively idempotent rig]]. 

> This article is about Boolean rigs as defined by [[Toby Bartels]]. For other notions of "Boolean rig" or "Boolean semiring", see [[Boolean semiring]]. 

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **multiplicatively idempotent rig** or **Boolean rig** is a [[rig]] in which multiplication is [[idempotent]]; that is, a rig in which $x^2 = x$ always holds.

**Note:** These structures are called *idempotent rigs* by [[John Baez]], see e.g. [Baez 2022](#Bartels22). However, the term "[[idempotent rig]]" can also refer to [[additively idempotent rigs]], and now is a disambiguation page on the nLab. 

**Note:** These structures are called *Boolean rigs* by [[Toby Bartels]], see e.g. [Bartels 2020](#Bartels20). The name originated from the fact that a [[Boolean ring]] is defined in the literature as a [[ring]] for which multiplication is idempotent ([Bartels 2020](#Bartels20), [Rogers 2024](#Rogers24)). However, the terms "[[Boolean rig]]" has multiple meanings representing some generalization of [[Boolean rings]], and now redirects to the disambiguation page [[Boolean semiring]] on the nLab. 

## Properties

Every multiplicatively idempotent rig is an [[idempotent monoid]] [[object]] in [[CMon]], the category of [[commutative monoids]] and [[monoid homomorphisms]]. 


## Examples

The main examples are probably [[distributive lattices]].  In this case, the join operation called $\vee$ above will match the original join/addition operation called $+$ above.

Of course, a [[Boolean ring]] is a multiplicatively idempotent rig, since any ring is a rig.  However, since it\'s also a distributive lattice, a Boolean ring is actually a Boolean rig in two different ways.

Similarly, a [[Boolean rig (Guzmán)|Boolean rig]] as defined by Fernando Guzmán is a multiplicatively idempotent by definition. 

### Smallest multiplicatively idempotent rigs

Let’s see what are the smallest multiplicatively idempotent rigs.

- The only multiplicatively idempotent rig of cardinal $1$ is the zero ring $0$.

There are exactly two multiplicatively idempotent rigs of cardinal $2$. In such a multiplicatively idempotent rig, we necessarily have $0 \neq 1$, because $0=1$ would imply that $x=1 \cdot x=0 \cdot x=0$ for every $x$ and then the multiplicatively idempotent rig would be the zero ring $0$. The two elements of the multiplicatively idempotent rigs are thus $0$ and $1$. From the axioms of a rig, we have $0+0=0$, $1+0=0+1=1$, $0 \cdot 0=0$, $1 \cdot 0=0 \cdot 1=0$ and $1 \cdot 1=1$. We then have two possibilities for $1+1$, either $0$ or $1$. The two possibilities give a multiplicatively idempotent rig.  

* One of the two multiplicatively idempotent rigs of cardinal $2$ is $\mathbb{Z}/2\mathbb{Z}$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[exclusive disjunction]] and $\cdot$ as the [[conjunction]]).
* One of the two multiplicatively idempotent rigs of cardinal $2$ is $\mathbb{B}=\{0,1\}$ where $1+1=1$ ($0$ can be interpreted as "False", $1$ as "True", $+$ as the [[disjunction]] and $\cdot$ as the [[conjunction]]).

In either case, the multiplication is commutative and distributive over addition. 

One can construct a non-commutative multiplicatively idempotent rig of cardinal $9$ ([Rogers 2024](#Rogers24)). 

## Related concepts

* [[Boolean algebra]]
* [[Boolean ring]]
* [[01-bounded semilattice]]
* [[idempotent monoid]]
* [[Boolean semiring (Guzmán)]]
* [[additively idempotent rig]]

## References

The term *multiplcatively idempotent rig* appears in:

* {#Rogers24} [[Morgan Rogers]], *From free idempotent monoids to free multiplicatively idempotent rigs* &lbrack;[arXiv:2408.17440](https://arxiv.org/abs/2408.17440)&rbrack;

The term *idempotent rig* appears in:

* {#Baez22} [[John Baez]], *Free Idempotent Rigs and Monoids*, Azimuth Blog, 21 December 2022. &lbrack;[web](https://johncarlosbaez.wordpress.com/2022/12/21/free-idempotent-rigs-and-monoids/)&rbrack;

The term *Boolean rig* was used by [[Toby Bartels]] in this current article on the nLab, before it was renamed to *multiplcatively idempotent rig*:

* {#Bartels20} [[Toby Bartels]], *Boolean rig*, 5th revision of the nLab article "[[multiplicatively idempotent rig]]", August 15, 2020. &lbrack;[nLab](https://ncatlab.org/nlab/revision/multiplicatively+idempotent+rig/5)&rbrack;

The term *Boolean rig* was also used in this Category Theory Zulip discussion:

* {#Vienney22} [[J-B Vienney]], *Are Boolean rigs commutative?*, Category theory Zulip, ([web](https://categorytheory.zulipchat.com/#narrow/channel/266967-deprecated.3A-mathematics/topic/Are.20boolean.20rigs.20commutative.3F))

[[!redirects multiplicatively idempotent rig]]
[[!redirects multiplicatively idempotent rigs]]
[[!redirects multiplicatively idempotent rig]]
[[!redirects multiplicatively idempotent rigs]]

[[!redirects multiplicatively idempotent semiring]]
[[!redirects multiplicatively idempotent semirings]]
[[!redirects multiplicatively idempotent semiring]]
[[!redirects multiplicatively idempotent semirings]]

[[!redirects Boolean semiring (Bartels)]]
[[!redirects Boolean semirings (Bartels)]]
[[!redirects boolean semiring (Bartels)]]
[[!redirects boolean semirings (Bartels)]]

[[!redirects Boolean rig (Bartels)]]
[[!redirects Boolean rigs (Bartels)]]
[[!redirects boolean rig (Bartels)]]
[[!redirects boolean rigs (Bartels)]]

