
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A canonical or Sweedler [[coring]] is an algebraic structure that is roughly the [[duality|formal dual]] of the [[Čech nerve]] of a [[cover]]: it is used to describe [[descent]] in algebraic contexts.

See also [[monadic descent]].

## Definition

### In components

Let $f : R \hookrightarrow S$ be the extension of associative unital $k$-[[associative algebra|algebra]]s (where $k$ is a commutative unital [[ring]]). 

The corresponding __canonical coring__ or __Sweedler coring__ is the $S$-[[coring]] 

$$
  C = S\otimes_R S
$$ 

with coproduct 

$$
  \Delta : C\to C\otimes_S C \cong S\otimes_R S\otimes_R S
$$ 

given by the bilinear extension of the formula 

$$
  \Delta: s_1\otimes s_2 \mapsto s_1\otimes 1 \otimes s_2
$$ 

and counit 

$$
  \epsilon : C\to S,\,\,\,\,\,\,\,
 \epsilon: s_1 \otimes s_2 \mapsto s_1 s_2
 \,.
$$  

The element $1\otimes 1$ is a [[grouplike element]] in the Sweedler's coring. 

### Geometric interpretation {#GeomInterpretationOfCoring}

We give a dual geometric interpretation of the Sweedler coring. 

Suppose a context of spaces and function algebras on spaces that satisfies the basic axioms of [[geometric function theory]], in that the algebra of functions $C(Y_1 \times_X Y_2)$ on a [[fiber product]] 

$$
  \array{
    Y_1 \times_X Y_2 &\to& Y_2
    \\
    \downarrow && \downarrow
    \\
    Y_1 &\to& X
  }
$$

is the [[tensor product]] of the functions on the factors:

$$
  C(Y_1 \times_X Y_2) = C(Y_1) \otimes_{C(X)} C(Y_2)
  \,.
$$

Then let $\pi : Y \to X$ be a morphism of spaces and set

$$
  R := C(X)
$$

and

$$
  S = C(Y)
$$

and

$$
  (R \hookrightarrow S) := \pi^* : C(X) \to C(Y)
  \,.
$$

The morphism $\pi$ induces its augmented [[Čech nerve]]

$$
  \left(
     \cdots
     \stackrel{\to}{\stackrel{\to}{\stackrel{\to}{\to}}}
     Y \times_X Y \times_X Y
     \stackrel{\to}{\stackrel{\to}{\to}}
     Y \times_X Y \stackrel{\to}{\to}
     Y
     \stackrel{\pi}{\to}
     X
  \right)
  \,.
$$

Taking function algebras of this yields, by the above, 

$$
  \left(
     \cdots
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}}}
     S \otimes_R S \otimes_R S
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}}
     S \otimes_R S 
     \stackrel{\leftarrow}{\leftarrow}
     S
     \stackrel{\pi^*}{\leftarrow}
     R
  \right)
  \,.
$$

Writing again $C = S \otimes_R S$ for the Sweedler coring, this is 

$$
  \left(
     \cdots
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}}}
     C \otimes_S C
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}}
     C 
     \stackrel{\leftarrow}{\leftarrow}
     S
     \stackrel{\pi^*}{\leftarrow}
     R
  \right)
  \,.
$$

## Properties

### Relation to ring extensions

Various properties of canonical coring correspond to adequate properties of the ring extension. For example, [[coseparable coring|coseparable]] canonical corings correspond to [[split extension]]s (the $k$-algebra extension $R\to S$ is split if there is an $R$-bimodule map $h: S\to R$ with $h(1_S) = 1_R$).

In the case of the trivial ring extension $R\to R$ the coproduct of the canonical coring is the canonical isomorphism 
$R\to R\otimes_R R$ and the counit is the identity $R\to R$. Thus, every right $R$-module is a comodule over the canonical coring. Such a canonical coring is called a __trivial coring__. This example puts the rings (or associative unital algebras) and their categories of modules as a special case of corings and their categories of comodules. In view of the next paragraph, this is a generalization of a coring of a cover for the case of a trivial (identity) cover.

### Descent in terms of coring comodules
 {#DescentIntermsOfCoringModules}

Given a morphism $f : R \to S$ with corresponding Sweedler coring $(C = S \otimes_R S,\Delta,\epsilon)$ as above, the category of [[descent]] data $\mathrm{Desc}(S/R)$ for the categories of right modules along $k$-algebra extension $R\to S$  is precisely the category of right $C$-[[comodule]]s.

In other words, the objects of $\mathrm{Desc}(S/R)$ are the pairs $(N,\alpha)$ where $N$ is a right $S$-[[module]], and $\alpha: N\to N\otimes_R S$ is a right $S$-module morphism and if we write $\alpha(m) = \sum_i m_i \otimes s_i$ then

* $\sum_i \alpha(m_i)\otimes s_i = \sum_i m_i\otimes 1\otimes s_i$,

* $\sum_i m_i s_i = m$.


#### In terms of (co)monadic descent {#ComonadicDescent}

This [[coring]]-formulation of [[descent]] may be understood as special case of [[comonadic descent]] (see also the discussion at [[Bénabou-Roubaud theorem]]). See e.g. ([Hess 10, section 2](#Hess10)) for a review. We spell this out in a bit more detail:

The [[bifibration]] in question is 

$p :$ [[Mod]] $\to$ [[CRing]]

that sends an object in the category [[Mod]] of [[module]]s to the ring that it is a module over.

A descent datum for a morphism $f : R \to S$ with respect to this bifibration is a (co)algebra object over the co[[monad]] $f_* f^*$ induced by this morphism. We have that

* the morphism $f_*$ sends an $R$-module $N$ to the $S$-module $N \otimes_R S$;

* the morphism $f^*$ sends an $S$-module $P$ to the $R$-module $P \otimes_S S_R$, where $S_R$ is $S$ regarded as a left $S$- and a right $R$-module. So $P \otimes_S S_R$ is just the $S$-module $P$ with only the right $R$-action remembered.

Accordingly, the comonad with underlying functor $f_* f^*$ sends an $S$-module $P$ to the $S$-module $P \otimes_S S \otimes_R S = P \otimes_S C$.

A (co)algebra object for this comonad is hence a co-action morphism 

$$
  P \to P \otimes_S C
$$

compatible with the monad action. This is precisely a comodule over the Sweedler coring, as defined above.



#### Geometric interpretation {#GeomInterpretationOfDescent}

Descent for Sweedler corings is a special case of [[monadic descent|comonadic descent]]. We describe this in detail and relate it by duality to the geometrically more intuitive [monadic descent for codomain fibrations](http://ncatlab.org/nlab/show/monadic+descent#ForCodomainFibs).

Assuming again a suitable geometric context as above, we may identify a [[module]] over $R = C(X)$ with (the collection of [[section]]s of) a [[vector bundle]] (or rather a suitable generalization of that: a  [[coherent sheaf]]) over $X$. Similarly for $Y$. So we write

$$
  Vec(X) := R Mod
$$

and

$$
  Vec(Y) := S Mod
$$

for the corresponding [[category|categories]] of [[module]]s. The assignment of such categories to spaces

$$
  Vec : Z \mapsto Vec(Z)
$$

extends to a contravariant [[pseudofunctor]]

$$
  Vec : Spaces^{op} \to Cat
$$

by assigning to a morphism $f : Y \to X$ of spaces the corresponding [[functor]]

$$
  Vec(X) \simeq C(X) Mod \stackrel{- \otimes_{f} C(Y)}{\to} C(Y) Mod \simeq Vec(Y)
  \,.
$$

This way $Vec$ becomes a [[stack|prestack]] of categories on our category of spaces. 

If this prestack satisfies [[descent]] along suitable [[cover]]s, it is a [[stack]].

Geometrically this is the case if for each morphism $\pi : Y\to X$ that is regarded as a [[cover]], the category $Desc(Y,Vec)$ whose objects are tuples consisting of

* an [[object]] $a \in Vec(Y)$

* an [[isomorphism]] $g : \pi_1^* a \to \pi_2^* a$

* such that 

  $$  
    \array{
       && \pi_2^* a
       \\
       & {}^{\mathllap{\pi_{12}^* g}}\nearrow && \searrow^{\mathrlap{\pi_{23}^* g}}
       \\
       \pi_1^* a &&\stackrel{\pi_{13}^*}{\to}&& \pi_3^*
    }
  $$

  commutes.

Morphism are defined similarly (see [[stack]] and [[descent]] for details).

To get the geometric pucture that underlies, by duality, the above comodule definition of descent, we need to reformulate this just a little bit more:

every ordinary [[vector bundle]] $E \to X$ (of finite rank) is the [[associated bundle]] $E \simeq P \times_{O(n)} V$ of an [[orthogonal group|O(n)]]-[[principal bundle]] $P \to X$, and as such its [[section]]s may be identified with $O(n)$-equivariant functions $P \to V \simeq \mathbb{R}^n$ on the total space of $P$. 

Using this we may think of the $C(X)$-module of sections of $E$ as a submodule of the $C(X)$-module of all functions on $P$

$$
  \Gamma(E) \subset C(P)
  \,.
$$

We now reformulate the geometric descent for [[vector bundle]]s in terms of geometric descent for their underlying [[principal bundle]]s, and then take functions on everything in sight to obtain the comodule definition of descent that we want to describe:

A descent datum (transition function) for a [[principal bundle]] $Q \to Y$ may be thought of as the the morphism $g$ in the double [[pullback]] diagram

$$
  \array{
    &&Y\times_X Y \times_Y Q &\to& Q
    \\
    &&\downarrow && \downarrow
    \\
    &{}^{\mathllap{g}}\swarrow&Y \times_X Y &\to& Y
    \\
    &&\downarrow && \downarrow^{\mathrlap{\pi}}
    \\
    Q &\to& Y &\stackrel{\pi}{\to}& X
  }
  \,.
$$

Because here $Y \times_X Y \times_Y Q$ is the space whose points consist of a point in a double overlap of the cover and a point in the fiber of $Q$ over that with respect to one patch, and the morphism identifies this with a point in the fiber of $Q$ regarded as sitting over the other patch. Analogously, there is a cocycle condition on $g$ on triple overlaps.

Now, blindly applying our functor that takes functions of spaces to the above diagram yields the double [[pushout]] diagram

$$
  \array{
    &&C(Y\times_X Y \times_Y Q) &\leftarrow& C(Q)
    \\
    &&\uparrow && \uparrow
    \\
    &{}^{\mathllap{g}^*}\nearrow&C(Y \times_X Y) &\leftarrow& C(Y)
    \\
    &&\uparrow && \uparrow^{\mathrlap{\pi^*}}
    \\
    C(Q) &\leftarrow& C(Y) &\stackrel{\pi^*}{\leftarrow}& C(X)
  }
  \,.
$$

We may restrict to $N := \Gamma(E) \subset C(Q)$ as just discussed and switch to the notation from above to get

$$
  \array{
    &&N \otimes_{S} C &\leftarrow& N
    \\
    &&\uparrow && \uparrow
    \\
    &{}^{\mathllap{g}^*}\nearrow& C &\leftarrow& S
    \\
    &&\uparrow && \uparrow^{\mathrlap{\pi^*}}
    \\
    N &\leftarrow& S &\stackrel{\pi^*}{\leftarrow}& R
  }
  \,.
$$

The morphism

$$
  \alpha := g^* : N \to N \otimes_S C
$$

obtained this way is the co-action morphism from the above algebraic definition. 

The further cocycle condition on $g$ similarly translates into the condition that $\alpha$ really satisfies the [[comodule]] property.


### Relation to generalized cohomology and Adams spectral sequence
 {#RelationToGeneralizedCohomology}

Applied to [[E-infinity rings]] the Sweedler coring construction
yields the [[Hopf algebroids]] of dual [[Steenrod algebras]]
and appears in the [[Adams spectral sequence]].


## Related concepts

* [[Amitsur complex]], [[Hopf algebroid]]

* [[descent]]

  * [[cover]]

  * [[cohomological descent]]

  * [[monadic descent]], 

    * **Sweedler coring**

    * [[monadic descent]], [[higher monadic descent]]

    * [[descent in noncommutative algebraic geometry]]

* [[sheaf]], [[(2,1)-sheaf]], [[2-sheaf]] [[(∞,1)-sheaf]]

## References

Sweedler corings are named after [[Moss Sweedler]].

A textbook account is in

*  [[Tomasz Brzezinski]], [[Robert Wisbauer]], section 29 of _Corings and Comodules_, Cambridge University Press, London Math. Soc. LN 309 (2003), ([errata pdf](http://www.math.uni-duesseldorf.de/~wisbauer/corinerr.pdf))

Section 29 there discusses the relation to the [[Amitsur complex]] and the [[descent theorem]].

* MO: [how-is-a-descent-datum-the-same-as-a-comodule-structure](http://mathoverflow.net/questions/150547/how-is-a-descent-datum-the-same-as-a-comodule-structure)

Discussion in the context of ([[higher monadic descent|higher]]) [[monadic descent]] is around example 2.24 of 

* [[Kathryn Hess]], section 6 of _A general framework for homotopic descent and codescent_ ([arXiv:1001.1556](http://arxiv.org/abs/1001.1556))
 {#Hess10}

[[!redirects Sweedler corings]]
[[!redirects Sweedler's coring]]
[[!redirects Sweedler's corings]]

[[!redirects canonical coring]]
[[!redirects canonical corings]]
[[!redirects canonical co-ring]]
[[!redirects canonical co-rings]]
