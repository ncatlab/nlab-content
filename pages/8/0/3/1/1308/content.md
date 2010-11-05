+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# The Eckmann--Hilton argument
* table of contents
{: toc}

## Statement

In its usual form, the _Eckmann--Hilton argument_ shows that a [[monoid object|monoid]] or [[group object]] [[internalization|in]] the category of [[monoids]] or [[Grp|groups]] is [[abelian group|commutative]]. In other terms, if a set is equipped with two monoid structures, such that one is a homomorphism for the other, then the two structures coincide and the resulting monoid is commutative.

An even more general version is this:  If a set is equipped with two binary operations with [[identity elements]], as long as they commute with each other in the sense that one is (with respect to the other) a homomorphism of sets with binary operations, then everything else follows:
1.  the other is also a homomorphism with respect to the first;
1.  each also preserves the other\'s identity;
1.  the identities are the same;
1.  the operations are the same;
1.  the operation is commutative;
1.  the operation is associative.

If we [[internalisation|internalise]] the monoid version, then the Eckmann--Hilton argument shows that

+-- {: .un_prop }
###### Proposition

Let $C$ be a [[2-category]] and $x \in C$ an [[object]]. Write $Id_x$ for the [[identity]] [[morphism]] of $X$ and $End(Id_x)$ for the set of [[endomorphism|endo]]-[[2-morphism]]s on $X$. Then:

* [[horizontal composition]] and [[vertical composition]] define the same [[monoid]] structure on $End(Id_x)$;

* this is an [[abelian monoid]].

=--

+-- {: .proof}
###### Proof

The [[pasting diagram]]-proof is depicted for instance <a href="http://cheng.staff.shef.ac.uk/degeneracy/eggclock.pdf">here</a>.

The basic equation that we have (that one operation $*$ is a homomorphism with respect to another operation $\circ$) is
$$ (a \circ b) * (c \circ d) = (a * c) \circ (b * d) .$$
We prove the above list of results in order:

1.  Simply read the basic equation backwards to see that $\circ$ is a homomorphism with respect to $*$.

1.  Now if $1_*$ is the identity of $*$ and $1_\circ$ is the identity of $\circ$, we have
$$ 1_\star \circ 1_\star = (1_\star \circ 1_\star) * 1_\star = (1_\star \circ 1_\star) * (1_\star \circ 1_\circ) = (1_\star * 1_\star) \circ (1_\star * 1_\circ) = 1_\star \circ 1_\circ = 1_\star .$$
A similar argument proves the other half.

1.  Then
$$ 1_\star = 1_\star * 1_\star = (1_\star \circ 1_\circ) * (1_\circ \circ 1_\star) = (1_\star * 1_\circ) \circ (1_\circ * 1_\star) = 1_\circ \circ 1_\circ = 1_\circ ,$$
so the identities are the same; we will now write this identity simply as $1$.

1.  Now
$$ a * b = (a \circ 1) * (1 \circ b) = (a * 1) \circ (1 * b) = a \circ b ,$$
so the operations are the same; we will write them both with concatenation.

1.  Then
$$ a b = (1 a) (b 1) = (1 b) (a 1) = b a ,$$
so this operation is commutative.

1.  Finally,
$$ (a b) c = (a b) (1 c) = (a 1) (b c) = a (b c) ,$$
so the operation is associative.

Note that if you start with the slick monoid-in-$Mon$ approach, then only (4&5) need to be shown; the others are part of the hypothesis.  This classic form of the Eckmann--Hilton argument may be combined into a single calculation:
$$ a * b = (a \circ 1) * (1 \circ b) = (a * 1) \circ (1 * b) = a \circ b = (1 * a) \circ (b * 1) = (1 * b) \circ (a * 1) = b * a ,$$
where the desired results involve the first, middle, and last expressions.

=--

## Corollaries

A $2$-[[k-tuply monoidal n-category|tuply monoidal]] $0$-[[0-category|category]], if defined as a [[pointed object|pointed]] [[k-tuply connected n-category|simply connected]] [[bicategory]], is also the same as an abelian monoid.

A $2$-tuply monoidal $1$-[[1-category|category]], if defined as a pointed simply connected [[tricategory]], is the same as a [[braided monoidal category]].

Every [[homotopy group]] $\pi_n$ for $n \geq 2$ is [[abelian group|abelian]].



## References


* [[The Catsters]]

  _Eckmann-Hilton 1_ ([video](http://www.youtube.com/watch?v=Rjdo-RWQVIY))
  
  _Eckmann-Hilton 2_ ([video](http://www.youtube.com/watch?v=wnRqo7UHa-k))

For higher analogues see 

within the discussion of commutative algebraic monads

* [[Nikolai Durov]], _New approach to Arakelov geometry_ , ([arXiv:0704.2030](http://arxiv.org/abs/0704.2030))

*  [[Michael Batanin]], _The Eckmann-Hilton argument and higher operads_ ,  Adv. Math.  217  (2008),  no. 1, 334--385; ([arXiv:math.CT/0207281](http://arxiv.org/abs/math/0207281))


[[!redirects Eckmann-Hilton argument]]
[[!redirects Eckmann-Hilton arguments]]
[[!redirects Eckmann–Hilton argument]]
[[!redirects Eckmann–Hilton arguments]]
[[!redirects Eckmann--Hilton argument]]
[[!redirects Eckmann--Hilton arguments]]
