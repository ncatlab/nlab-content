
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _regular 2-category_ is the analog in [[2-category theory]] of the notion of _[[regular category]]_ in [[category theory]].

## Definition

+-- {: .num_defn}
###### Definition

A [[2-category]] $K$ is called **regular**  if

1. It is finitely complete (has all [[finite limit|finite]] [[2-limits]] );

1. [[eso morphism|esos]] are stable under [[2-pullback]];

1. Every [[2-congruence]] which is a kernel can be completed to an 
   exact [[2-fork]].

=--

+-- {: .num_remark}
###### Remark

In particular, the last condition implies that every 2-congruence which is a kernel has a [[quotient]].

=--

## Examples

* [[nLab:Cat|Cat]] is regular.

* A [[1-category]] is regular as a 2-category iff it is [[regular category|regular]] as a 1-category, since the esos in a 1-category are precisely the [[strong epimorphism|strong epis]].

* Every finitely complete] [[(0,1)-category]] (that is, every [[meet-semilattice]]) is regular.

## Properties

### Factorizations

In [[StreetCBS]] the last condition is replaced by

* Every morphism $f$ factors as $f\cong m e$ where $m$ is [[ff morphism|ff]] and $e$ is eso.

We now show that this follows from our definition.  First we need:

+--{: .num_lemma}
###### Lemma

**(Street's Lemma)**  Let $K$ be a finitely complete 2-category where esos are stable under pullback, let $e:A\to B$ be eso, and let $n:B\to C$ be a map.
1. If the induced morphism $ker(e) \to ker(n e)$ is ff, then $n$ is faithful.
1. If $ker(e) \to ker(n e)$ is an equivalence, then $n$ is ff.

=--
+--{: .proof}
###### Proof

First note that $ker(e)\to ker(n e)$ being ff means that if $a_1,a_2: Y \rightrightarrows A$ and $\delta_1,\delta_2 : e a_1 \;\rightrightarrows\; e a_2$ are such that $n \delta_1 = n \delta_2$, then $\delta_1=\delta_2$.  Likewise, $ker(e)\to ker(n e)$ being an equivalence means that given any $\alpha: n e a_1 \to n e a_2$, there exists a unique $\delta: e a_1 \to e a_2$ such that $n \delta = \alpha$.

We first show that $n$ is faithful under the first hypothesis.  Suppose we have $b_1,b_2:X \rightrightarrows B$ and $\beta_1,\beta_2:b_1\to b_2$ with $n \beta_1 = n \beta_2$.  Take the pullback
$$\array{&Y & \overset{r}{\to} & X \\
  (a_1,a_2) & \downarrow && \downarrow & (b_1,b_2)\\
  &  A\times A & \overset{e\times e}{\to} & B\times B}$$
Then we have two 2-cells
$$\beta_1 r, \beta_2 r: b_1 r \;\rightrightarrows\; b_2 r$$
such that the composites
$$n e a_1 \cong n b_1 r \overset{n \beta_1 r = n \beta_2 r}{\to}
n b_2 r \cong n e a_2$$
are equal.  By the hypothesis, $n \beta_1 r = n \beta_2 r$ implies $\beta_1 r = \beta_2 r$.  But $r$ is eso, since it is a pullback of the eso $e\times e$, so this implies $\beta_1=\beta_2$.  Thus, $n$ is faithful.

Now suppose the (stronger) second hypothesis, and form the pair of pullbacks:
$$\array{(n e / n e) & \overset{g}{\to} & n / n & \to & C^{\mathbf{2}}\\
  \downarrow && \downarrow && \downarrow \\
  A\times A & \overset{e\times e}{\to} & B\times B & \overset{n\times
n}{\to} & C\times C}$$
Then $g$, being a pullback of $e\times e$, is eso.  We also have a commutative square
$$\array{(e/e) & \to & (n e / n e)\\ \downarrow && \downarrow g \\
  B^{\mathbf{2}} & \to & (n/n).}$$
By assumption, $(e/e) \to (n e / n e)$ is an equivalence.  Since we have shown that $n$ is faithful, the bottom map $B^{\mathbf{2}} \to (n/n)$ is ff, so since the eso $g$ factors through it, it must be an equivalence as well.  But this says precisely that $n$ is ff.

=--


+--{: .num_theorem #StreetDefn}
###### Theorem

A 2-category is regular if and only if
1. it has finite limits,
1. esos are stable under pullback,
1. every morphism $f$ factors as $f\cong m e$ where $m$ is ff and $e$ is eso, and
1. every eso is the quotient of its kernel.

=--

+--{: .proof}
###### Proof

First suppose $K$ is regular; we must show the last two conditions.  Let $f:A\to B$ be any morphism.  By assumption, the kernel $ker(f)$ can be completed to an exact 2-fork $ker(f) \rightrightarrows A \overset{e}{\to} C$.  Since $e$ is the quotient of the 2-congruence $ker(f)$, it is eso, and since $f$ comes with an action by $ker(f)$, we have an induced map $m:C\to B$ with $f\cong m e$.  But since the 2-fork is exact, we also have $ker(f)\simeq ker(e)$, so by Street's Lemma, $m$ is ff.

Now suppose that in the previous paragraph $f$ were already eso.  Then since it factors through the ff $m$, $m$ must be an equivalence; thus $f$ is equivalent to $e$ and hence is a quotient of its kernel.

Now suppose $K$ satisfies the conditions in the lemma.  Let $f:A\to B$ be any morphism; we must show that $ker(f)$ can be completed to an exact 2-fork.  Factor $f = m e$ where $m$ is ff and $e$ is eso.  Since $m$ is ff, we have $ker(f)\simeq ker(e)$.  But every eso is the quotient of its kernel, so the fork $ker(f) \rightrightarrows A \overset{e} \to C$ is exact.

=--

In [[StreetCBS]] it is claimed that the final condition in Theorem \ref{StreetDefn} follows from the other three, but there is a flaw in the proof.


### Subobjects 

In a regular 2-category $K$, we call a ff $m:A\to X$ with codomain $X$ a **subobject** of $X$.  We write $Sub(X)$ for the [[nLab:preorder|preorder]] of subobjects of $X$, as a full sub-2-category of the [[slice 2-category]] $K/X$.  Since $K$ is finitely complete and pullbacks preserve ffs, we have pullback functors $f^*:Sub(Y)\to Sub(X)$ for any $f:X\to Y$.

If $g \cong m e$ where $m$ is ff and $e$ is eso, we call $m$ the **image** of $g$.  Taking images defines a left adjoint $\exists_f:Sub(X)\to Sub(Y)$ to $f^*$ in any regular 2-category, and the [[nLab:Beck-Chevalley condition|Beck-Chevalley condition]] is satisfied for any pullback square, because esos are stable under pullback.


### Preservation

It is easy to check that if $K$ is regular, so are:

* its [[nLab:opposite 2-category|2-cell dual]] $K^{co}$ (by the remarks about opposite [[2-congruence]]s).
* the (2,1)-category $gpd(K)$ of [[groupoidal object]]s in $K$.
* the (1,2)-category $pos(K)$ of [[posetal object]]s in $K$.
* the 1-category $disc(K)$ of [[discrete object]]s in $K$.
* and more generally the $n$-category $trunc_n(K)$ of $n$-[[truncated object|truncated objects]] in $K$.

The [[slice 2-category]] $K/X$ does not, in general, inherit regularity, but we have:

+--{: .num_theorem}
###### Theorem

If $K$ is regular, so are the [[fibrational slice]]s $Opf(X)$ and $Fib(X)$.

=--

### Regular completion

See at _[[2-congruence]]_ the section _[Regularity](http://ncatlab.org/nlab/show/2-congruence#Regularity)_.

## Related concepts

* [[regular category]]

* [[regular completion]]

## References

The above definitions and observations are originally due to

* [[Michael Shulman]], _[[michaelshulman:regular 2-category]]_


[[!redirects regular 2-categories]]

[[!redirects regular (2,1)-category]]
[[!redirects regular (2,1)-categories]]