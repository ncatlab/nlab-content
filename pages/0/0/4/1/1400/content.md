An **anabicategory** is a particular notion of _weak [[2-category]]_ appropriate in the absence of the [[axiom of choice]] (including in many [[internal category|internal]] contexts).  It is derived from the notion of [[bicategory]] by replacing the [[composition functor]]s $\circ: B(y,z) \times B(x,y) \to B(x,z)$ with [[anafunctor]]s (and therefore the [[associator]]s and [[unitor]]s with [[ananatural transformation]]s).

+-- {.query}
[[Zoran Škoda]]: I understand that there is a version of $Cat$ using anafunctors, but it is not clear to me 
what are the axioms for a variant of 2-category which this example belongs to. I do not understand what you mean by replacing hom-functor with anafunctor in that definition: I mean which definition of bicategory is phrased in terms of hom-functors; standard definition talks associators and so on...Please be more explicit. 

[[Mike Shulman|Mike]]: Is this version clearer?

_Toby_:  Or look at the complete definition in the reference that I just added.
=--

If [[Cat]] is defined as consisting of ([[small category|small]]) [[category|categories]], anafunctors, and [[ananatural transformation]]s (as is most appropriate in the absence of choice), then $Cat$ is more naturally an anabicategory rather than any stricter notion.

+--{: .query}
[[Mike Shulman|Mike]]: Is that only because of the non-canonicity of pullbacks in $Set$?  If our version of $Set$ has canonical chosen pullbacks, do we get an ordinary bicategory?

_Toby_:  H\'m ... as I recall, you get an ordinary bicategory using canonical pullbacks and general anafunctors, but if you move to *saturated* anafunctors, then you still only get an anabicategory.  I should check this and then rewrite (here and at [[Cat]]) to say it correctly.  (Of course, if you really use anafunctors, then you should only *want* an anabicategory.)
=--

# Explicit definition #

An anabicategory $\mathcal{C}$ consists of a set $\mathcal{C}_0$ of objects, a set $\mathcal{C}_1$ of 1-cells, which are relations $\mathcal{C}_0 \times \mathcal{C}_0$, and a set $\mathcal{C}_2$ of 2-cells, which are relations $\mathcal{C}_1 \times \mathcal{C}_1$. On these sets are defined several relations; for each relation $R$ if we have $R(x, y)$ $y$ is said to be a _value_ of $R$ at $x$. Some pairs $x, y$ with $R(x, y)$ are also said to be $specified values$; generally if $R$ has some value at $x$, at least one such value will be specified.
1. There are _source_ and _target_ relations $\mathcal{C}_1 \times \mathcal{C}_0$ and $\mathcal{C}_2 \times \mathcal{C}_1$, and every 1- or 2- cell $f$ has some specified value for its source and target.
1. There are _2-source_ and _2-target_ relations $\mathcal{C}_2 \times \mathcal{C}_0$, and every 2- cell $f$ has some specified value for its 2-source and 2-target.
1. There are _identity_ relations $\mathcal{C}_0 \times \mathcal{C}_1$ and $\mathcal{C}_1 \times \mathcal{C}_2$, and every object or 1-cell has some specified value for its identity.
1. There is a _composition_ relation $(\mathcal{C}_1 \times \mathcal{C}_1) \times \mathcal{C}_1$; whenever $f_1$ and $f_2$ are such that some specified value of the target at $f_1$ is also a specified value of the source at $f_2$, there is some specified value of the composite of $f_1$ and $f_2$.
1. There is a _1-composition_ relation $(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$; whenever $f_1$ and $f_2$ are such that some specified value of the 2-target at $f_1$ is also a specified value of the 2-source at $f_2$, there is some specified value of the composite of $f_1$ and $f_2$.
1. There is a _2-composition_ relation $(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$; whenever $f_1$ and $f_2$ are such that some specified value of the target at $f_1$ is also a specified value of the source at $f_2$, there is some specified value of the composite of $f_1$ and $f_2$.

The relations satisfy the following conditions:
1. For any 2-cell $f$, and any values $x$ and $y$ of its source and target (respectively), the set of values of the target of $x$, the target of $y$, and the 2-target of $f$ are all equal, and likewise for sources/2-sources. If $x$ or $y$ is a specified value, each specified value of its source is a specified value of the 2-source, and likewise for targets/2-targets.
1. Any value of the source of a value $x$ of one of the identity relations is also a value of the target of $x$, and vice versa. (However, we do not require the sets of specified values to match.) For any specified value $y$ of one of the identities on $x$, $x$ should be a specified value of the source and target on $y$.
1. If $h$ is a value of the composition $f \circ g$, the set of target values of $f$ is equal to the set of target values of $h$, and the set of source values of $g$ is equal to the set of source values of $h$. If $h$ is a specified value of the composition, any specified target value of $f$ is a specified target value of $h$, and any specified source value of $g$ is a specified source value of $h$. (In general the converses may fail.)
1. If $h$ is a value of the 2-composition $f \circ g$, the set of target values of $f$ is equal to the set of target values of $h$, and the set of source values of $g$ is equal to the set of source values of $h$. If $h$ is a specified value of the 2-composition, any specified target value of $f$ is a specified target value of $h$, and any specified source value of $g$ is a specified source value of $h$.
1. If $h$ is a value of the 1-composition $f \circ g$, each value of the source of $h$ is a value of the composition of some source value of $f$ and some source value of $g$, and each such composition value is a value of the source of $h$. For any specified source values of $f$ and $g$, each specified value of their composition is a specified source value of $h$. The same results hold with source replaced by target.

There are also conditions defining equivalence relations on $\mathcal{C}_0$ and $\mathcal{C}_1$. (The equivalence relation for $\mathcal{C}_2$ is simply equality.) All the relations defined above are required to be invariant under the appropriate equivalence relations (note, however, that their specified values do not need to be invariant). So in particular, the identity relation $\mathcal{C}_1\times \mathcal{C}_2$ and the 1- and 2- composition relations $(\mathcal{C}_2 \times \mathcal{C}_2) \times \mathcal{C}_2$ are functional: any two values of the identity on some 1-cell $x$, or any two values of one of the compositions on some 2-cells $f$ and $g$, must be equal (as elements of $\mathcal{C}_2$.
* A 2-cell $f$ is said to be an _isomorphism_ (between any of its source-values and any of its target-values) if there are some 2-cell $g$ and 1-cell $x$ such that the 2-composition of $f$ and $g$ is the identity value of $x$. We say that $g$ is an _inverse_ of $f$.
* Two 1-cells $f$ and $g$ are _isomorphic_ if there is a 2-cell isomorphism $h$ with $f$ as a source value and $g$ as a target value (or equivalently, vice versa). This is the chosen equivalence relation for $\mathcal{C}_1$.
* ETC. (The isomorphism for $\mathcal{C}_0$ is of course natural equivalence.)

# Reference #

*  [[Michael Makkai]]; Avoiding the axiom of choice in general category theory; section 3 (which is part 4 [here](http://www.math.mcgill.ca/makkai/anafun/)).