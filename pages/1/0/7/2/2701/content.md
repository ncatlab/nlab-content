
# MacNeille completion
* tic
{: toc}

## Idea

The MacNeille or Dedekind--MacNeille (*not* 'Mac Neille') [[completion]] of a [[lattice]] (or even [[poset]]) $L$ is the [[universal construction|universal]] [[complete lattice]] containing $L$. In [[Pos]], the MacNeille completion of an object is its [[injective hull]].


## Definition

A **MacNeille completion** of $L$ is any [[complete lattice]] $C$ containing $L$ as a [[subobject|sublattice]], with $L$ both join-dense and meet-dense in $C$ (that is, each element of $C$ is both a [[join]] of elements of $L$ and a [[meet]] of elements of $L$), and such that if $C'$ is another such lattice then there is a unique isomorphism from $C$ to $C'$ fixing $L$.  In particular, this allows us to speak of [[the]] MacNeille completion of $L$.

A MacNeille completion may be constructed as follows.  Let $P(L)$ be the [[power set|set of all subsets]] of $L$, ordered by inclusion. For any $X \in P(L)$ let

* $X^{\Delta} = \{\alpha \in L \mid \forall x \in X . \alpha \geq x \}$

* $X^{\nabla} = \{\alpha \in L \mid \forall x \in X . \alpha \leq x \}$

These form a [[Galois connection]] on $P(L)$; the condition $\phi(X) = (X^{\Delta})^{\nabla}$ defines a [[Moore closure|closure]] operation $\phi$ on $P(L)$. The lattice $C$ of all $\phi$-closed subsets of $L$ is complete. For any $x \in L$ the set $i(x) = (\{x\}^{\Delta})^{\nabla}$ is the [[principal ideal]] generated by $x$. Then $i$ is an isomorphic embedding of $L$ into the complete lattice $C$ that preserves all least upper bounds (joins) and greatest lower bounds (meets) existing in $L$.


## Examples

When applied to the ordered set of [[rational number]]s, the construction described above gives the completion of the set of rational numbers by Dedekind sections, *including* the empty sections.  Thus we get, not the [[real line]] $\mathbb{R} = {]{-\infty},\infty[}$, but the [[extended real line]] $\overline{\mathbb{R}} = [-\infty,\infty]$.  In [[constructive mathematics]], we may get additional finite elements, since the Dedekind sections are not required to be located; if we then drop $\pm\infty$, we get the (bounded) [[MacNeille real numbers]].


## Related pages

* The MacNeille completion can be [[categorification|categorified]] to the category of self-dual (saturated) objects in the [[Isbell envelope]]; see [this MO question and answers](https://mathoverflow.net/q/59291/).

## References

* [MacNeille completions and canonical extensions](http://www.math.nmsu.edu/mgehrke/gehharven.pdf)
* [Encyclopedia of Mathematics](http://eom.springer.de/c/c024070.htm)
* Section 21H of [[The Joy of Cats]] ([web](http://katmat.math.uni-bremen.de/acc/acc.pdf))


[[!redirects MacNeille completion]]
[[!redirects MacNeille completions]]
[[!redirects Mac Neille completion]]
[[!redirects Mac Neille completions]]
[[!redirects Dedekind-MacNeille completion]]
[[!redirects Dedekind-MacNeille completions]]
[[!redirects Dedekind–MacNeille completion]]
[[!redirects Dedekind–MacNeille completions]]
[[!redirects Dedekind--MacNeille completion]]
[[!redirects Dedekind--MacNeille completions]]