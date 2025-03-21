+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Adjoint strings

* table of contents
{: toc}

## Definition

In [[category theory]],
an **adjoint string of length $n$**, **adjoint chain of length $n$**, **adjoint sequence of length $n$**, or an **adjoint $n$-tuple**, is a sequence of $(n-1)$ [[adjunctions]] between $n$ [[functors]] (or more generally [[morphisms]] in a [[2-category]]):

$$f_1 \dashv f_2 \dashv \cdots \dashv f_n $$

## Special cases

* An adjoint $2$-tuple is just an ordinary [[adjunction]].
* An adjoint $3$-tuple is an [[adjoint triple]].
* An adjoint $4$-tuple is an [[adjoint quadruple]].

## Examples

1. There is an adjoint $5$-tuple between $[Set^{op}, Set]$ and $Set$. Indeed, given a [[locally small category]] $B$, and the [[Yoneda embedding]], $y: B \to [B^{op}, Set]$, then $y$ being the rightmost functor of an adjoint $5$-tuple entails that $B$ is equivalent to [[Set]]; see [Rosebrugh-Wood](#RWSets).

1. For any category $C$, there is a functor $ids: C\to Ar(C)$ from $C$ to its [[arrow category]] that assigns the identity morphism of each object.  This functor always has both a left and a right adjoint which assign the codomain and domain of an arrow respectively; thus we have an adjoint triple $cod \dashv ids \dashv dom$.  If $C$ has an initial object $0$, then $cod$ has a further left adjoint $I$ assigning to each object $x$ the morphism $0\to x$; and dually if $C$ has a terminal object $1$ then $dom$ has a further right adjoint $T$ assigning to $x$ the morphism $x\to 1$.  Thus if $C$ has an initial and terminal object, we have an adjoint $5$-tuple.

1. Continuing from the last example, if $C$ is moreover a [[pointed category]] with [[pullbacks]] and [[pushouts]], then $I$ has a further left adjoint that constructs the [[cokernel]] of a morphism $x\to y$, i.e. the pushout of $y \leftarrow x \to 0$; and $T$ has a further right adjoint that constructs the [[kernel]] of a morphism $x \to y$, namely the pullback of $x\to y \leftarrow 0$.  Thus we have an adjoint $7$-tuple.  In fact, the existence of such an adjoint $7$-tuple characterizes pointed categories among categories with finite limits and colimits.

1. The previous two examples apply also to [[derivators]], and the extension of the analogous adjoint $5$-tuple to a $7$-tuple again characterizes the [[pointed derivators]].  Moreover, the [[stable derivators]] are characterized by the extension of this $7$-tuple to a doubly-infinite adjoint string with period 6 ([GrothShul17](#GrothShul17)).

1. Let $[n]$ denote the [[totally ordered]] $(n+1)$-element set, regarded as a category. For each positive integer $n$, we have $n+1$ order-preserving injections from $[n-1]$ to $[n]$, and $n$ order-preserving surjections from $[n]$ to $[n-1]$. Regarded as functors, these injections and surjections interleave to form an adjoint chain of length $2n + 1$.  These categories, functors, and adjunctions form the [[simplex category]] [[simplex category#As2Categories|regarded as a locally posetal 2-category]]; see below.

1. Let $C$ be a category with a [[terminal object]] but no [[initial object]]. Then there are functors
  $$
    \array{
      \delta_i \colon [n+1,C] \to [n,C] & 0\leq i \leq n; 
      \\
      \sigma_i\colon [n,C] \to [n+1,C] &  0\leq i \leq n
    }
  $$
such that
  $$
    \delta_0 \dashv \sigma_0 \dashv \cdots \dashv \delta_n \dashv \sigma_n
  $$
is a maximal string of adjoint functors (all but $\sigma_n$ are obtained by applying $[-, C]$ to the simplex category example, and $\sigma_n$ exploits the presence of the terminal object of $C$). 

1. Generalizing the simplex category example: if $P$ is a [[lax idempotent monad]] with unit $u: 1 \to P$ and multiplication $m: P P \to P$ (so that $m \dashv u P$), then there is an adjoint string 
$$P^{n-1} m \dashv P^{n-1} u P \dashv P^{n-2}m P \dashv \ldots \dashv m P^{n-1} \dashv u P^n$$ 
of length $2 n + 1$, back and forth between $P^{n+1}$ and $P^n$. The example of $[n]$ and $[n+1]$ above is based on the fact that the [[simplex category]] $\Delta$, regarded as a locally posetal [[bicategory]], is the [[walking structure|walking]] lax idempotent monoid. 

1. Given an [[ambidextrous adjunction]] (and in particular a [[self-adjoint functor]]), $F \dashv G$ and $G \dashv F$, we of course get an infinite adjoint string 
$$\ldots \dashv F \dashv G \dashv F \dashv \ldots$$ 
of period 2. 

## References

A study of adjoint strings, in particular showing that cyclic chains of any length, and adjoint chains of any length exist, may be found in:

* {#Booth72} [[Peter I. Booth]], *Sequences of adjoint functors*, Archiv der Mathematik **23** (1972)  489-493 &lbrack;[doi:10.1007/BF01304920](https://doi.org/10.1007/BF01304920)&rbrack;

See also:

* {#Hoffmann80} [[Rudolf-E. Hoffmann]], _Sequences of adjoints for Ens-valued functors_, manuscripta mathematica **32** (1980) &lbrack;[EuDML;154724](https://eudml.org/doc/154724)&rbrack;

Characterizing the [[category of sets]] as that whose [[Yoneda embedding]] extends to the [[left adjoint|left]] to an [[adjoint quintuple]] of [[adjoint functors]]:

* {#RWSets} [[Robert Rosebrugh]], [[Richard J. Wood]], *An adjoint characterization of the category of sets*. PAMS **122** 2 (1994) 409-413 &lbrack;[jstor:2161031](https://www.jstor.org/stable/2161031)&rbrack;


On [[adjoint quadruples]] with a [[fully faithful functor|fully faithful]] [[right adjoint]]:

* [[Bob Rosebrugh]], [[Richard J. Wood]], *Distributive Adjoint Strings*, Theory and Applications of Categories, **1** 6 (1995) 119-145 &lbrack;[tac:1-06](http://www.tac.mta.ca/tac/volumes/1995/n6/1-06abs.html)&rbrack;

See also: 

* {#GrothShul17} [[Moritz Groth]], [[Mike Shulman]], _Generalized stability for abstract homotopy theories_, [arXiv:1704.08084](https://arxiv.org/abs/1704.08084).

On adjoint strings between a [[topos]] and [[Set]] and specifically on *completely connected* toposes ([[locally connected toposes]] with a further [[left adjoint]] to the left adjoint to the [[inverse image]] functor):

* [[Ryuya Hora]]: _Grothendieck topos with a left adjoint to a left adjoint to a left adjoint to the global sections functor_ &lbrack;[arXiv:2503.04317](https://arxiv.org/abs/2503.04317)&rbrack;

[[!redirects adjoint string]]
[[!redirects adjoint strings]]
[[!redirects adjoint chain]]
[[!redirects adjoint chains]]
[[!redirects adjoint sequence]]
[[!redirects adjoint sequences]]
[[!redirects adjoint n-tuple]]
[[!redirects adjoint n-tuples]]
[[!redirects distributive adjoint string]]
[[!redirects distributive adjoint strings]]

[[!redirects adjoint quintuple]]
[[!redirects adjoint quintuples]]

