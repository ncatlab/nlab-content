
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

The generalization of the notion of _[[coherent category]]_ from [[category theory]] to [[2-category theory]]. 

## Definition 

+-- {: .num_defn}
###### Definition

A [[2-category]] is called **coherent** if
1. it has finite [[2-limits]],
1. finite jointly-[[eso]] families are stable under [[2-pullback]], and
1. every finitary [[2-polycongruence]] which is a kernel can be completed to an exact [[2-polyfork]].

=--

Here a family $\{f_i:A_i \to B\}$ is said to be **jointly-eso** if whenever $m:C\to B$ is ff and every $f_i$ factors through $m$ (up to isomorphism), then $m$ is an equivalence.

Likewise, we have **infinitary coherent** 2-categories in which "finite" in the second two conditions is replaced by "small."


## Examples 

* [[Cat]] is coherent.

* A [[1-category]] is coherent as a 2-category iff it is [[coherent category|coherent]] as a 1-category.

* A [[(0,1)-category]] (= [[poset]]) is coherent iff it is a [[distributive lattice|distributive lattice]], and infinitary-coherent iff it is a [[frame]].


## Properties

### Factorizations 

The following are proven just like their unary analogues in a [[regular 2-category]].

+--{: .num_lemma}
###### Lemma
**(Street's Lemma)** In a finitely complete 2-category where finite jointly-eso families are stable under pullback, if $\{e_i:A_i \to B\}$ is finite and jointly-eso and $n:B\to C$ is such that the induced functor $\ker(e_i) \to ker(n e_i)$ is an equivalence, then $n$ is ff.
=--

+--{: .num_theorem}
###### Theorem
A 2-category is coherent if and only if
1. it has finite limits,
1. finite jointly-eso families are stable under pullback,
1. every finite family $\{f_i\}$ factors as $f_i = m e_i$ where $m$ is ff and $\{e_i\}$ is jointly-eso, and
1. every jointly-eso family is the quotient of its kernel.
=--

Of course, there are infinitary versions.  In particular, we conclude that in a coherent (resp. infinitary-coherent) 2-category, the posets $Sub(X)$ have finite (resp. small) unions that are preserved by pullback.


### Colimits 

+--{: .num_lemma}
###### Lemma
A coherent 2-category has a strict [[initial object]]; that is an initial object $0$ such that any morphism $X\to 0$ is an equivalence.
=--
+--{: .proof}
###### Proof
The empty 2-congruence is the kernel of the empty family (over any object), so it must have a quotient $0$, which is clearly an initial object.  The empty family over $0$ is jointly-eso, so for any $X\to 0$ the empty family over $X$ is also jointly-eso; but this clearly makes $X$ initial as well.
=--

Two [[nLab:ff morphism|ffs]] $m:A\to X$ and $n:B\to X$ are said to be **disjoint** if the _comma objects_ $(m/n)$ and $(n/m)$ are initial objects.  If initial objects are strict, then this implies that the pullback $A\times_X B$ is also initial, but it is strictly stronger already in $Pos$.

+--{: .num_lemma #DisjointUnion}
###### Lemma
In a coherent 2-category, if $A\to X$ and $B\to X$ are disjoint subobjects, then their union $A\cup B$ in $Sub(X)$ is also their coproduct $A+B$.
=--
+--{: .proof}
###### Proof
If $A$ and $B$ are disjoint subobjects of $X$, then the kernel of $\{A\to X, B\to X\}$ is the disjoint union of $ker(A)$ and $ker(B)$.  Therefore, a quotient of it (which is a union of $A$ and $B$ in $Sub(X)$) will be  a coproduct of $A$ and $B$.
=--

A coproduct $A+B$ in a 2-category is **disjoint** if $A$ and $B$ are disjoint subobjects of $A+B$.  We say a coherent 2-category is **positive** if any two objects have a disjoint coproduct.  By Lemma \ref{DisjointUnion}, this is equivalent to saying that any two objects can be embedded as disjoint subobjects of some other object.  Disjoint coproducts in a coherent 2-category are automatically stable under pullback, so a positive coherent 2-category is necessarily [[extensive 2-category|extensive]].  Conversely, we have:

+--{: .num_lemma}
###### Lemma
A regular and extensive 2-category is coherent (and positive).
=--
+--{: .proof}

In the presence of finite coproducts, a family $\{e_i:A_i\to B\}$ is jointly-eso iff $\coprod_i A_i \to B$ is eso; thus regularity and universal coproducts imply that finite jointly-eso families are stable under pullback.  And assuming extensivity, any 2-polycongruence $\{C_{i j}\} \rightrightarrows \{C_i\}$ gives rise to an ordinary 2-congruence $\coprod_{i j} C_{i j} \rightrightarrows \coprod_i C_i$.  Likewise, 2-polyforks $\{C_{i j}\} \rightrightarrows \{C_i\} \to X$ correspond to 2-forks $\coprod_{i j} C_{i j} \rightrightarrows \coprod_i C_i \to X$, and the property of being a kernel or a quotient is preserved; thus regularity implies coherency.

=--


### Preservation

If $K$ is coherent, then easily so are $K^{co}$, $disc(K)$, $gpd(K)$, $pos(K)$, and $Sub(1)$.  Moreover, we have:

+--{: .num_theorem}
###### Theorem
If $K$ is a coherent 2-category, so are the [[fibrational slice]]s $Opf(X)$ and $Fib(X)$ for any $X\in K$.
=--

## References

This is due to 

* [[Michael Shulman]], _[[michaelshulman:coherent 2-category]]_

based on

* [[Ross Street]], _[[StreetCBS]]_

[[!redirects coherent 2-categories]]
