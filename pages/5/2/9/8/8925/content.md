
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The **[[core]]** of a [[category]] $A$ is the maximal [[subcategory]] of $A$ that is a [[groupoid]], consisting of all its [[objects]] and all [[isomorphisms]] between them.  The core is not a [[functor]] on the [[2-category]] [[Cat]], but it is a functor on the [[(2,1)-category]] $Cat_g$ of categories, functors, and [[natural isomorphisms]].  In fact, it is a [[coreflective subcategory|coreflection]] of $Cat_g$ into [[Gpd]].

In general, for any [[2-category]] $K$ we write $K_g$ for its "homwise core:" the sub-2-category determined by all the objects and morphisms but only the iso [[2-morphisms]].  Of course, $K_g$ is a [[(2,1)-category]].  Then $gpd(K)$ is a full [[sub-2-category]] of $K_g$, and we can ask whether it is coreflective.  In a [[regular 2-category]], however, it turns out that there is a stronger and more useful notion which implies this coreflectivity.

## Definition

### Core

+--{: .num_defn}
###### Definition
A **core** of an object $A$ in a [[regular 2-category]] is a [[morphism]] $J\to A$ which is [[eso morphism|eso]], [[pseudomonic functor|pseudomonic]], and where $J$ is groupoidal.

=--

### Enough groupoids 

We say that a regular 2-category has **enough groupoids** if every object admits an eso from a groupoidal one.  Thus, a (2,1)-exact 2-category has cores if and only if it has enough groupoids.

Likewise, we say that a regular 2-category has **enough discretes** if every object admits an eso from a discrete one.  Clearly this is a stronger condition.  Note, though, that if $K$ has enough groupoids, then $pos(K)$ has enough discretes, since the core of any posetal object is discrete.

Having enough discretes, or at least enough groupoids, is a very familiar aspect of 2-categories such as $Cat$.  It also turns out to make the [[2-internal logic|internal logic]] noticeably easier to work with.  However, in a sense none of the really "new" 2-categories have enough groupoids or discretes.

* The 2-exact 2-categories having enough discretes are precisely the categories of internal categories and anafunctors in 1-exact 1-categories; see [[exact completion of a 2-category]].  Likewise, any 2-exact 2-categories having enough groupoids consists of certain internal categories in a (2,1)-category.

* Basically the only [[Grothendieck 2-toposes]] having enough discretes are the 2-categories of stacks on [[2-site|1-sites]], and the only ones having enough groupoids are the 2-categories of stacks on (2,1)-sites.  The "honestly 2-dimensional" case of stacks on 2-sites (almost?) never have enough of either.


## Properties

### General

+--{: .num_lemma}
###### Lemma
In a regular 2-category $K$, any core $J\to A$ is a coreflection of
$A$ from $K_g$ into $gpd(K)$.
=--
+--{: .proof}
###### Proof

We must show that for any groupoidal $G$, the functor
$$gpd(K)(G,J)=K_g(G,J)\to K_g(G,A)$$
is an equivalence.  Since $J\to A$ is pseudomonic in $K$, it is ff in $K_g$, so this functor is full and faithful; thus it remains to show it is eso.  Given any map $G\to A$, take the pullback
$$\array{P & \to & J\\ \downarrow && \downarrow \\ G & \to & A}$$
and let $P_1\;\rightrightarrows\; P$ be the kernel of $P\to G$.  Since the composite $P\to A$ descends to $G$, it comes equipped with an action by this kernel.  However, since $G$ is groupoidal, $P_1\;\rightrightarrows\; P$ is a [[n-congruence|(2,1)-congruence]], so the 2-cell defining the action must be an isomorphism.  Therefore, it must factor uniquely through the pseudomonic $J\to A$, so $P\to J$ has an action as well; thus it descends to a map $G\to J$, as desired.

=--

In particular, cores in a regular 2-category are unique up to unique
equivalence.  We write $J(A)$ for the core of $A$, when it exists.

+--{: .num_lemma}
###### Lemma
An object $A$ of a (2,1)-exact 2-category has a core if and only if
there is an eso $C\to A$ where $C$ is groupoidal.
=--

+--{: .proof}
###### Proof

"Only if" is clear, so suppose that $p:C\to A$ is eso and $C$ is groupoidal.  Let $C_1 = C\times_A C$ be the pullback.  Then $C_1$ is also groupoidal and is a (2,1)-congruence on $C$, so by exactness it is the kernel of some eso $q:C\to J$.  There is an evident induced map $m:J\to A$; we claim that this is a core of $A$.

Evidently $m:J\to A$ is eso, since the eso $C\to A$ factors through it.  And since $C_1$ is a (2,1)-congruence, the classification of [[n-congruence|congruences]] implies that $J$ is groupoidal; thus it remains to show that $m$ is pseudomonic.

First suppose given $f,g: X\;\rightrightarrows\; J$.  Pulling back $q$ along $f$ and $g$ gives esos $P_1\to X$ and $P_2\to X$, whose pullback $P = P_1\times_X P_2$ comes with an eso $r:P \to T$ and two morphisms $h,k:P \to C$ with $q h \cong f r$ and $q k \cong g r$.  Then any pair of 2-cells $\alpha,\beta: f\to g$ induce maps $P\;\rightrightarrows\; C_1$, since $C_1$ is the kernel $(q/q)$.  But if $m\alpha = m\beta$, then these two maps must be equal, since $C_1$ is also the kernel $(p/p)$.  Therefore, $\alpha r=\beta r$, and since $r$ is eso, $\alpha=\beta$; thus $m$ is faithful.

On the other hand, again given $f,g: X\;\rightrightarrows\; J$, any isomorphism $\alpha: m f\cong m g$ induces a map $P\to C_1$ and therefore a 2-cell $\beta: f r\to g r$ with $m\beta = \alpha r$.  To show that $\beta$ descends to a 2-cell $f\to g$, we must verify that it is an action 2-cell for the actions of $P\;\rightrightarrows\; J$ on $f r$ and $g r$.  But $m\beta$ is an action 2-cell, since $m\beta = \alpha r$, and we now know that $m$ is faithful, so it reflects the axiom for an action 2-cell.  Therefore, $m$ is full-on-isomorphisms, and hence pseudomonic.
=--


### Subobjects 

We also remark that cores, when they exist, "capture all the information about [[subobjects]]."

+--{: .num_prop}
###### Proposition
If $K$ is a regular 2-category and $A$ is an object having a core $j:J\to A$, then $j^*:Sub(A)\to Sub(J)$ is an equivalence.
=--
+--{: .proof}
###### Proof
It is a general fact in a regular 2-category that for any eso $f:X\to Y$, $f^*:Sub(Y)\to Sub(X)$ is full (and faithful, which of course is automatic for a functor between posets).  For if $f^*U \le f^*V$, then we have a square
$$\array{f^*U & \to & f^*V & \to & V\\
  \downarrow &&&& \downarrow\\
  U & & \to & & Y}$$
in which $f^*U \to U$ is eso and $V\to Y$ is ff, hence we have $U\to V$ over $Y$.

Thus, in our case, $j^*$ is full and faithful since $j$ is eso, so it suffices to show that for any ff $U\to J$ we have $j^* \exists_j U \le U$ in $Sub(J)$.  But we have a commutative square
$$\array{U & \to & \exists_j U\\
  \downarrow && \downarrow\\
  J & \to & X}$$
where the vertical arrows are ff and the bottom arrow $J\to X$ is faithful and pseudomonic, from which it follows that $U\to \exists_j U$ is also faithful and pseudomonic.  Since $U\to \exists_j U$  is eso by definition, $U$ is a core of $\exists_j U$, and since $j^*\exists_j U$ is a groupoid mapping to $\exists_j U$, it factors through $U$, as desired.
=--

## Related concepts

* [[core]]

* [[decategorification]]

## References

The material on this page is taken from

* [[Mike Shulman]], _[[michaelshulman:core]]_

[[!redirects cores in a 2-category]]