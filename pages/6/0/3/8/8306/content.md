
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### For abelian groups

+-- {: .num_defn #BilinearOnAbelianGroups}
###### Definition

For $A$, $B$ and $C$ [[abelian groups]] and $A \times B$ the [[cartesian product]] group, a **bilinear map** 

$$
  f : A \times B \to C
$$

from $A$ and $B$ to $C$ is a [[function]] of the underlying [[sets]] (that is, a [[binary function]] from $A$ and $B$ to $C$) which is a [[linear map]] -- that is a [[group homomorphism]] -- in each argument separately. 

=--

+-- {: .num_remark}
###### Remark

In terms of [[elements]] this means that 
a bilinear map $f : A \times B \to C$ is a function of sets that satisfies for all elements $a_1, a_2 \in A$ and $b_1, b_2 \in B$ the two relations

$$
  f(a_1 + a_2, b_1) = f(a_1,b_1) + f(a_2, b_1)
$$

and

$$
  f(a_1, b_1 + b_2) = f(a_1, b_1) + f(a_1, b_2)
  \,.
$$

Notice that this is _not_ a group homomorphism out of the [[direct product]] group.
The product group $A \times B$ is the group whose elements are pairs $(a,b)$ with $a \in A$ and $b \in B$, and whose group operation is 

$$
  (a_1, b_1) + (a_2, b_2) = (a_1 + a_2 \;,\; b_1 + b_2)
  \,.
$$

A _[[group homomorphism]]_

$$
  \phi : A \times B \to C
$$

hence satisfies

$$
  \phi( a_1+a_2, b_1 + b_2 ) = \phi(a_1,b_1) + \phi(a_2, b_2)
$$

and hence in particular

$$
  \phi( a_1+a_2, b_1  ) = \phi(a_1,b_1) + \phi(a_2, 0)
$$

$$
  \phi( a_1, b_1 + b_2 ) = \phi(a_1,b_1) + \phi(0, b_2)
$$

which is (in general) different from the behaviour of a bilinear map.

=--

The definition of [[tensor product of abelian groups]] is precisely such that the following is an equivalent definition of bilinear map:

+-- {: .num_defn}
###### Definition

For $A, B, C \in Ab$ a function of sets $f : A \times B \to C$ 
is a **bilinear map** from $A$ and $B$ to $C$ precisely if it factors through the [[tensor product of abelian groups]] $A \otimes B$ as

$$
  f : A \times B \to A \otimes B \to C
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The analogous definition for more than two arguments yields __multilinear maps__. There is a [[multicategory]] of abelian groups and multilinear maps between them; the bilinear maps are the [[binary morphisms]], and the multilinear maps are the [[multimorphisms]]. 

=--


### For modules

More generally :

+-- {: .num_defn}
###### Definition

For $R$ a [[ring]] (or [[rig]]) and $A, B, C \in R$[[Mod]] being [[modules]] (say on the left, but on the right works similarly) over $R$, a **bilinear map** from $A$ and $B$ to $C$ is a function of the underlying sets

$$
  f : A \times B \to C
$$

which is a bilinear map of the underlying [[abelian groups]] as in def. \ref{BilinearOnAbelianGroups} and in addition such that for all $r \in R$ we have

$$
  f(r a, b) = r f(a,b)
$$

and

$$
  f(a, r b) = r f(a,b)
  \,.
$$

=--

As before, if $R$ is [[commutative ring|commutative]] then this is equivalent to $f$ factoring through the [[tensor product of modules]]

$$
 f : A \times B \to A \otimes_R B \to C
  \,.
$$

__Multilinear maps__ are again a generalisation.


### For $\infty$-modules
 {#ForInfinityModules}

([Lurie, section 4.3.4](#Lurie))

See at _[[tensor product of ∞-modules]]_


## Classification

A __[[bilinear form]]__ is a bilinear map $f\colon A, B \to K$ whose target is the [[ground ring]] $K$; more generally, a __[[multilinear form]]__ is multilinear map whose target is $K$.

A bilinear map $f\colon A, A \to K$ whose two sources are the same is __[[symmetric bilinear map|symmetric]]__ if $f(a, b) = f(b, a)$ always; more generally, a multilinear map whose sources are all the same is __[[symmetric multilinear map|symmetric]]__ if $f(a_1, a_2, \ldots, a_n) = f(a_{\sigma(1)}, a_{\sigma(2)}, \ldots, a_{\sigma(n)})$ for each [[permutation]] $\sigma$ in the [[symmetric group]] $S_n$.  (It\'s enough to check the $n-1$ generators of $S_n$ that transpose two adjacent arguments.)  In particular, this defines symmetric [[symmetric bilinear form|bilinear]] and [[symmetric multilinear form|multilinear]] forms.

A bilinear map $f\colon A, A \to K$ whose two sources are the same is __[[antisymmetric bilinear map|antisymmetric]]__ if $f(a, b) = -f(b, a)$ always; more generally, a multilinear map whose sources are all the same is __[[antisymmetric multilinear map|antisymmetric]]__ if $f(a_1, a_2, \ldots, a_n) = (-1)^\sigma f(a_{\sigma(1)}, a_{\sigma(2)}, \ldots, a_{\sigma(n)})$ for each [[permutation]] $\sigma$ in the [[symmetric group]] $S_n$, where $(-1)^\sigma$ is $1$ or $-1$ according as $\sigma$ is an even or odd permutation.  (It\'s enough to check the $n-1$ generators of $S_n$ that transpose two adjacent arguments, which are each odd and so each introduce a factor of $-1$.)  In particular, this defines antisymmetric [[antisymmetric bilinear form|bilinear]] and [[antisymmetric multilinear form|multilinear]] forms.

A bilinear map $f\colon A, A \to K$ whose two sources are the same is __[[alternating bilinear map|alternating]]__ if $f(a, a) = 0$ always; more generally, a multilinear map whose sources are all the same is __[[alternating multilinear map|alternating]]__ if $f(a_1, a_2, \ldots, a_n) = 0$ whenever there exists a nontrivial [[permutation]] $\sigma$ in the [[symmetric group]] $S_n$ such that $(a_1, a_2, \ldots, a_n) = (a_{\sigma(1)}, a_{\sigma(2)}, \ldots, a_{\sigma(n)})$, in other words whenever there exist indexes $i \ne j$ such that $a_i = a_j$.  (It\'s enough to say that $f(a_1, a_2, \ldots, a_n) = 0$ whenever two adjacent arguments are equal, although this is not as trivial as the analogous statements in the previous two paragraphs.)  In particular, this defines alternating [[alternating bilinear form|bilinear]] and [[alternating multilinear form|multilinear]] forms.

In many cases, antisymmetric and alternating maps are equivalent:

+-- {: .num_prop #alternationImpliesAntisymmetry}
###### Proposition

An alternating bilinear (or even multilinear) map must be antisymmetric.
=--

+-- {: .proof}
###### Proof

If $f$ is an alternating bilinear map, then $f(a + b, a + b) = f(a, a) + f(a, b) + f(b, a) + f(b, b) = 0 + f(a, b) + f(b, a) + 0$, so $f(a, b) + f(b, a) = f(a + b, a + b) = 0$, so $f(a, b) = -f(b, a)$; that is, $f$ is antisymmetric.  The general multilinear case is similar.  (Note that linearity is essential to this proof.)
=--

+-- {: .num_prop #antisymmetryImpliesAlternation}
###### Proposition

If the ground ring is a [[field]] whose characteristic is not $2$, or more generally if $1/2$ exists in the ground ring, or more generally if $2$ is cancellable in the target of the map in question, then an antisymmetric bilinear (or even multilinear) map must be alternating.
=--

+-- {: .proof}
###### Proof

If $f$ is an antisymmetric bilinear map, then $f(a, a) = -f(a, a)$, so $2 f(a, a) = f(a, a) + f(a, a) = f(a, a) - f(a, a) = 0$, so $f(a, a) = 0$ (by dividing by $2$, multiplying by $1/2$, or cancelling $2$, as applicable).  The general multilinear case is similar.  (Note that linearity is irrelevant to this proof.)
=--

The argument that the simplified description of alternation is correct is along the same lines as Proposition \ref{alternationImpliesAntisymmetry} above:

+-- {: .num_prop #transpositionsSufficeForAlternation}
###### Proposition

If a trilinear map is alternating in the first two arguments and in the last two arguments, or more generally if a multilinear map is alternating in every pair of adjacent arguments (or indeed in any set of transpositions that generate the entire symmetric group), then the map is alternating overall.
=--

+-- {: .proof}
###### Proof

If $f$ is a trilinear map that alternates in each adjacent pair of arguments, then $f(a + b, a + b, a) = f(a, a, a) + f(a, b, a) + f(b, a, a) + f(b, b, a) = 0 + f(a, b, a) + 0 + 0$, so $f(a, b, a) = f(a + b, a + b, a) = 0$; that is, $f$ is alternating in the remaining pair of arguments.  The general multilinear case is similar.  (Again, linearity is essential to this proof.)
=--


## Related concepts

* [[binary function]], **bilinear map**, **multilinear map**

* [[binary morphism]], [[multimorphism]]

* [[bifunctor]], [[Quillen bifunctor]]


## References

In the context of [[higher algebra]]/[[(∞,1)-category theory]] [[bilinear maps in an (∞,1)-category]] are discussed in section 4.3.4 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

[[!redirects bilinear]]
[[!redirects bilinear map]]
[[!redirects bilinear maps]]
[[!redirects bilinear mapping]]
[[!redirects bilinear mappings]]
[[!redirects bilinear function]]
[[!redirects bilinear functions]]

[[!redirects bilinear operator]]
[[!redirects bilinear operators]]

[[!redirects multilinear map]]
[[!redirects multilinear maps]]
[[!redirects multilinear mapping]]
[[!redirects multilinear mappings]]
[[!redirects multilinear function]]
[[!redirects multilinear functions]]

[[!redirects bilinear map in an (∞,1)-category]]
[[!redirects bilinear maps in an (∞,1)-category]]
[[!redirects bilinear map in an (infinity,1)-category]]
[[!redirects bilinear maps in an (infinity,1)-category]]
