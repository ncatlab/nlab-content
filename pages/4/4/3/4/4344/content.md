
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A C\*-category can be thought of as a [[horizontal categorification]] of a C\*-[[C-star-algebra|algebra]]. Equivalently,  a C\*-algebra $A$ is thought of as a pointed one-object C\*-category $\mathbf{B}A$ (the [[delooping]] of $A$).  Accordingly, a more systematic name for C\*-categories would be __C\*-[[algebroids]]__.


## Definition

+-- {: .num_defn}
###### Definition

A (unital) __C\*-category__ is a \*-[[star-category|category]] [[enriched category|enriched]] in the category [[Ban]] of [[Banach spaces]] such that: 

1. Every arrow $a \in Hom(x,y)$ satisfies the C\*-identity ${\|a^* a\|} = {\|a\|}^2$.

2. Composition satisfies ${\|{b a}\|} \leq {\|b\|} {\|a\|}$ for all composable pairs of arrows $a$ and $b$. (That is, we give $Ban$ the [[projective tensor product]].)
 
3. For every arrow $a \in Hom(x,y)$ there exists an arrow $b \in Hom(x,x)$ such that $a^\ast a = b^ \ast b$.
=--

+-- {: .num_remark}
###### Remark

Condition (3) above is equivalent to requiring that every arrow of the form $x^* x$ is positive in the sense of C\*-algebras. Unlike C\*-algebras, this does not follow automatically, as can be seen by considering the category with two objects $x,y$ with all morphism sets a copy of $\mathbb{C}$ and with involution defined on $a \in Hom(x,y)$ by $a^* = \overline{a}$ if $x=y$ and $a^* = -\overline{a}$ otherwise.  
=--

+-- {: .num_remark}
###### Remark
A __C\*-category__ can be defined analogously to unital C\*-categories, using enriched [[nonunital categories]] instead of (unital) [[enriched categories]].
=--


## Examples

+-- {: .num_example}
###### Example

The $C^\ast$-[[representation category]] of a weak [[Hopf C-star-algebra|Hopf]] $C^\ast$-algebra (see there for details) is naturally a [[rigid monoidal category|rigid monoidal]] $C^\ast$-category.
=--

+-- {: .num_example}
###### Example

The category $Hilb$ of Hilbert spaces and bounded linear maps is a C\*-category. 
=--

## Representation Theory

C\*-algebras can be represented as algebras of bounded linear operators on some choice of Hilbert space, using the [[Gelfand-Naimark-Segal construction|G.N.S. construction]]. C\*-categories have an analogue of the G.N.S. construction that allows them to represented on the category $Hilb$ of [[Hilbert space|Hilbert spaces]] and bounded linear maps. 

+-- {: .num_theorem}
###### Theorem

For any (small) C\*-category $\mathcal{C}$ there exists a faithful \*-functor $\rho \colon \mathcal{C} \to Hilb$.
=--

## Related concepts

* [[GNS construction]]

* [[star-category]], [[dagger-category]]

* [[W-star category]]

* [[unitary fusion category]]

* [[spaceoid]]

* [[KK-theory]]

## References

With emphasis on the special case of [[W-star category|$W^\ast$-categories]]:

* {#GhezLinaRoberts85} P. Ghez, R. Lima, [[John E. Roberts]], Prop. 1.9 in: *$W^\ast$-categories*,  Pacific J. Math. **120** 1 (1985) 79-109 &lbrack;[euclid:pjm/1102703884](https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-120/issue-1/Wast-categories/pjm/1102703884.full)&rbrack;



[[!redirects C-star-category]]
[[!redirects C-star-categories]]
[[!redirects C*-category]]
[[!redirects C*-categories]]
[[!redirects C-star category]]
[[!redirects C-star categories]]

[[!redirects C-star-algebroid]]
[[!redirects C-star-algebroids]]
[[!redirects C*-algebroid]]
[[!redirects C*-algebroids]]
[[!redirects C-star algebroid]]
[[!redirects C-star algebroids]]