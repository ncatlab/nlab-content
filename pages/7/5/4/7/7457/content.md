
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

The generalization of the notion of _[[extensive category]]_ from [[category theory]] to [[2-category theory]].

## Definition

A [[2-coproduct]] $A+B$ in a [[2-category]] is said to be **disjoint** if we have [[comma squares]]
$$\array{
  A^{\mathbf{2}} & \to & A & \quad &
  B^{\mathbf{2}} & \to & B & \quad &
  0 & \to & A & \quad &
  0 & \to & B \\
  \downarrow & \Downarrow & \downarrow & \quad &
  \downarrow & \Downarrow & \downarrow & \quad &
  \downarrow & \Downarrow & \downarrow & \quad &
  \downarrow & \Downarrow & \downarrow & \quad\\
  A & \to & A+B & \quad &
  B & \to & A+B & \quad &
  B & \to & A+B & \quad &
  A & \to & A+B & \quad}
$$
The first two say that $A\to A+B$ and $B\to A+B$ are [[ff morphism|ff]] and the second two say that they are disjoint subobjects of $A+B$.

A coproduct $A+B$ is said to be **universal** if for any morphism $Z\to A+B$, the pullbacks
$$\array{X & \to & Z & \leftarrow & Y\\
  \downarrow & & \downarrow & & \downarrow\\
  A & \to & A+B & \leftarrow & B}$$
exist and exhibit $Z$ as a coproduct $X+Y$.

Finally, we say a 2-category is **extensive** if it has finite coproducts which are disjoint and universal.  If it also has finite limits we say it is **lextensive**, and if it is also [[coherent 2-category|coherent]] we call it **positive**.  (Note that disjoint coproducts in a coherent 2-category are always universal.)

An extensive 2-category does satisfy 2-categorical versions of the additional characterizations of an [[nLab:extensive category|extensive 1-category]], but unlike in the 1-categorical case, these alternate conditions do not seem to suffice to characterize extensivity.  In particular, though, a 1-category is extensive as a 1-category iff it is so as a homwise-discrete 2-category.

## Properties

### Preservation 

If $K$ is extensive, so is $K^{co}$, obviously.  Less obvious is:

+--{: .num_lemma}
###### Lemma
If $K$ is extensive, so are $gpd(K)$, $pos(K)$, and $disc(K)$.  In other words, if $K$ is extensive, so is its $(n+1)$-category $trunc_n(K)$ of $n$-[[truncated object|truncated objects]] for $0\le n$.
=--
+--{: .proof}
###### Proof
Since the three given categories are closed in $K$ under limits and strict initial objects, it suffices to show they are closed under coproducts.  First suppose given two morphisms $f,g:Z\to A_1+A_2$.  Then $f$ decomposes $Z=X_1+X_2$, and $g$ decomposes $Z=Y_1+Y_2$.  Then the inclusions $X_i \to Z = Y_1+Y_2$ also decompose each $X_i=X_{i 1} + X_{i 2}$.  Now if there exists a 2-cell $f\to g$, it induces a map from each $X_{i j}$ to the comma object of $A_1$ and $A_2$.  Since coproducts are disjoint and initials are strict, this implies that $X_{12}=X_{21}=0$.  Therefore, we have a decomposition $Z=X_{11}+X_{22}$ so that $f=f_1+f_2$ and $g=g_1+g_2$, where $f_i:X_{i i} \to A_i$ and $g_i:X_{i i} \to A_i$.

Now, by universality of the coproduct $X_{11}+X_{22}$, it follows that 2-cells $f\to g$ are determined uniquely by pairs of 2-cells $f_1\to g_1$ and $f_2\to g_2$.  Therefore, if $A_1$ and $A_2$ are groupoidal, any 2-cells $f_1\to g_1$ and $f_2\to g_2$ are invertible, and thus so is any 2-cell $f\to g$; so $A_1+A_2$ is groupoidal.  And if $A_1$ and $A_2$ are posetal, any parallel 2-cells $f_1 \;\rightrightarrows\; g_1$ and $f_2 \;\rightrightarrows\; g_2$ are equal, and thus so are any $f \;\rightrightarrows\; g$; so $A_1+A_2$ is posetal.  And of course the discrete case follows by combining these.
=--

However, the (0,1)-category (= poset) $Sub(1)$ of (-1)-truncated objects (= subterminal objects) does _not_ inherit extensivity, and in fact posets are almost never extensive: the only disjoint coproduct is $0+0$.

We also have:

+--{: .num_lemma}
###### Lemma
If $K$ is extensive, so are the [[fibrational slice]]s $Opf(X)$ and $Fib(X)$ for any $X\in K$.
=--


## References

This is due to 

* [[Mike Shulman]], _[[michaelshulman:extensive 2-category]]_

[[!redirects extensive 2-categories]]
