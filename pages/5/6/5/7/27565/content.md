* table of contents
{:toc}

## Idea

A _parameterized monad_ or _indexed monad_ is the notion of [[monad]] that arises from an [[two-variable adjunction|adjunction with a parameter]]. Recall that if $F:S\times C\to D$ is a functor such that for every $s\in S$, the functor $F(s,-):C\to D$ has a right adjoint $G_s:D\to C$, then there is a canonical way to make $G$ into a [[bifunctor]] $G:S^{op}\times D\to C$. 

## Definition

Let $S$ and $C$ be categories.

A _parameterized monad_ $T$ comprises:

* a functor $T:S^{op}\times S\times C\to C$;

* a unit $a\to T(s,s,a)$ morphism in $C$, [[extranatural]] in $a$ and $s$;

* a multiplication $T(s_1,s_2,T(s_2,s_3,a))\to T(s_1,s_3,a)$, [[extranatural]] in $a$ and $s_1,s_2,s_3$;

all satisfying analogues of the monad laws. 

If $C$ has products then the parameterized monad might also be equipped with a strength, which is an extranatural family

$$a \times T(s_1,s_2,b)\to T(s_1,s_2,a\times b)$$ 

satisfying analogues of the strength laws.

Finally for modelling programming languages, one might require $C$ to be a [[cartesian closed category]], but often a weaker requirement is that the "Kleisli exponentials" exist, which means the [[hom-objects]] of the form $C(a,T(s_1,s_2,b))$. 

## Examples

### Parameterized state:

Let $S=C=\mathbf{Set}$, the [[category of sets]].
Then the parameterized [[state monad]] is given by 

$$ T(s_1,s_2,a)=(s_2\times a)^{s_1}$$

### Parameterized continuations:

Let $C=\mathbf{Set}$, and let $S=C^{op}$.
Then the parameterized [[continuation monad]] is given by 

$$ T(r_1,r_2,a)=[[a,r_2],r_1]$$

writing $[a,b]$ for the internal hom. 

## Connection with enriched categories

Let $C$ be a category with products. Let $D$ be [[enriched]] in $C$ with [[copowers]]. 
The definition of copower is that for any $d \in D$, the enriched hom-functor $D(d,-):D\to C$ has a left adjoint, $(-\bullet d):C\to D$. This is an enriched adjunction with a parameter. 

Let $S$ be a subcategory of $D$. We can use this adjunction with parameter to define an $S$-parameterized strong monad on $C$:

$$T(s_1,s_2,c)=D(s_1,c\bullet s_2)$$

(which looks like an enriched version of the parameterized state monad). 

In fact, every parameterized strong monad is of this form. 

+-- {: .num_theorem #VsEnriched}
###### Theorem

Let $C$ be a category with products, and let $S$ be a category. The following data are equivalent:

* A strong $S$-parameterized monad on $C$ with Kleisli exponentials;

* A category $D$ enriched in $C$ with copowers, having $S$ as a subcategory such that every object $d$ of $D$ is of the form $d=c\bullet s$ for $c$ in $C$ and $s$ in $S$. 
=--

The proof from top to bottom constructs $D$ as the "parameterized [[Kleisli category]]" of $T$. 

## Related concepts

* [[graded monad]]



## References

The definitions were first spelt out in 

* [[Robert Atkey]], Parameterised Notions of Computation. Journal of functional programming, 2009. [preprint at Strathclyde](https://strathprints.strath.ac.uk/34572/). 

The idea goes back further, for example,

* [[Philip Wadler]]. Monads and composable continuations. Lisp and Symbolic Computation, 7(1):39–55, 1994.

A connection to [[graded monads]] is given in 

* [[Dominic Orchard]], [[Philip Wadler]] and [[Harley Eades III]]. Unifying graded and parameterised monads. MSFP 2020. arxiv:[2001.10274](https://arxiv.org/abs/2001.10274). 

A treatment of both [[graded monads]] and parameterized monads is given in

* Soichiro Fujii, _A 2-Categorical Study of Graded and Indexed Monads_, ([arXiv:1904.08083](https://arxiv.org/abs/1904.08083))

The connection to enriched categories is discussed in Section 9 of

* [[Rasmus Møgelberg]] and [[Sam Staton]], Linear Usage of State, Logical Methods in Computer Science 2014. arxiv:[1403.1477](https://arxiv.org/abs/1403.1477). 