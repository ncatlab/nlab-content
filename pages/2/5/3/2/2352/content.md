
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#

* automatic table of contents goes here
{:toc}

## Idea

In as far as the notion of [[functor]] generalizes that of [[function]] and that of [[profunctor]] generalizes that of [[relation]], the notion of _graph_ of a (pro)functor generalizes that of [[graph of a function]].

Just as the [[graph of a function]] $f : X \to Y$, 
or more generally that of a [[relation]] $R \subset X \times Y$ for $X,Y \in Set = 0 Cat$ is nothing but the [[category of elements]] of the corresponding characteristic function $\chi_R : X \times Y \to (-1)Cat = \{0,1\}$, so the graph
of a functor $F\colon C \to D$, or more generally that of a [[profunctor]] $H : C^{op} \times D \to 0 Cat = Set$, is nothing but its [[category of elements]], a.k.a. [[Grothendieck construction]].

However, there are a number of different ways to construct such a category of elements, depending on the variance of morphisms in $C$ and $D$ that we include in it.  A one-variable functor $C\to Set$ has two categories of elements, one with a projection to $C$ (which is a [[discrete opfibration]]) and one with a projection to $C^{op}$ (which is a [[discrete fibration]]).  Similarly, a two-variable functor such as $H : C^{op}\times D\to Set$ has *four* categories of elements; thus a profunctor has four different "graphs".  In addition, there are two ways to make a functor into a profunctor, so a functor actually has *eight* graphs.

These can be unified by instead choosing a canonical notion of "graph of a profunctor", and recognising that, using the fact that [[Prof]] is a [[compact closed 2-category]], we can "shift around" the defining factors in a profunctor to produce different graphs.

## Definition

### Graphs of a profunctor

Let $H \colon C^{op} \times D \to Set$ be a [[profunctor]]. Using the convention in that article, we say that $H$ is a profunctor $H \colon D &#8696; C$.

We obtain the following four **graphs** by shifting around factors:

* The [[category of elements]] of the profunctor $D &#8696; C$, which comes equipped with a projection to $D \times C$ that is a [[two-sided discrete fibration]] contravariant over $C$ and covariant over $D$. This is the *canonical* graph associated to the profunctor $H$.

* The category of elements of the induced profunctor $C^{op} \times D &#8696; 1$, using the [[compact closed 2-category]] structure on [[Prof]]. This comes equipped with a projection to $C^{op} \times D$ that is a [[discrete opfibration]]. It is also the [[comma category]] $(* \downarrow H)$:

  $$
  \array{
    Graph(H) &\to& {*}
    \\
    \downarrow & \swArrow & \downarrow
    \\
    C^{op} \times D &\stackrel{H}{\to}& Set
  }
  $$

* The category of elements of the induced profunctor $1 &#8696; D^{op} \times C$. This graph comes with a projection to $C \times D^{op}$ that is a [[discrete fibration]]; it is the opposite of the previous category.

* The category of elements of the induced profunctor $C^{op} &#8696; D^{op}$. This graphs comes with a projection to $C^{op} \times D^{op}$ that is a [[two-sided discrete fibration]], covariant over $C^{op}$ and contravariant over $D^{op}$; it is the opposite of the first graph.

If the profunctor is the [[hom profunctor]] of a category $C$, then the first graph is the [[arrow category]] of $C$ and the second graph is the [[twisted arrow category]] of $C$.

### Graphs of a functor

Let $F:C\to D$ be a functor, and let $F^\bullet \colon C^{op} \times D \to Set$ and $F_\bullet \colon D^{op} \times C \to Set$ be the corresponding representable [[profunctors]]:

$$F^\bullet(c,d) = D(F c, d) \qquad F_\bullet(d,c) = D(d,Fc).$$

We may regard $F^\bullet$ as a profunctor $D &#8696; C$, and $F_\bullet$ as a profunctor $C &#8696; D$. Each of these yield four distinct graphs (with one "canonical" graph), so $F$ has 8 resulting distinct graphs (with two "canonical" graphs).

## For higher categories

### In general

For $n \leq \infty$, let $(n-1) Cat$ and $n Cat$ be a realization of the 
notions of $n$-category of $(n-1)$-categories and of the $(n+1)$-category of $n$-categories,
respectively,
such that standard constructions of [[category theory]] work,
in particular a version of the [[Yoneda lemma]].
See [[higher category theory]]. 

Then with $C,D \in n Cat$ let $f : C \to D$ be a ($n$-)[[functor]].  By the general logic of [[profunctors]] this defines $n$-profunctors

$$
   F^\bullet : C^{op} \times D \stackrel{F^{op} \times Id}{\to} D^{op} 
     \times D \stackrel{D(-,-)}{\to} (n-1) Cat
$$

$$
   F_\bullet : C \times D^{op} \stackrel{F \times Id}{\to} D^{op} 
     \times D \stackrel{D(-,-)}{\to} (n-1) Cat
$$

We can then consider analogues of all eight kinds of graphs.  For instance, the second kind of graph of $F$ is the fibration $Graph(f) \to C^{op} \times D$ classified by $F^\bullet$.

### For $(\infty,1)$-categories

In the context of 
$(\infty,1)$-[[Higher Topos Theory|category theory]], this graph may be taken to be the fibration classified by $\chi_f : C \times D^{op} \to (\infty,0)$ as described at  [[universal fibration of (∞,1)-categories]].

### For (0,0)-categories (sets)

To reproduce the ordinary notion of [[graph of a function]] let $(n,r) = (0,0)$.
then $(n,r)$-categories $X,Y$ are just sets and a functor $f : X \to Y$ is
just a function between sets. Moreover, the category of $(n-1,r) = (-1,0)$-categories
is the set $\{0,1\}$ of truth values, as described at [[(-1)-category]].
The [[profunctor]] corresponding to $f : X \to Y$ is therefore the 
characteristic function

$$
  \chi_f : X \times Y \to \{0,1\}
$$

that maps

$$
  \chi_f(x,y) = 
    \left\lbrace
      \array{
        1 & if f(x) = y
        \\
        0 & otherwise
      }
    \right.
    \,.
$$

(Notice that in this case $X^{op} = X$.)

The [[2-pullback]] of ${*} = {1} \to \{0,1\}$ along $\chi_f$ is 
just the ordinary [[pullback]]

$$
\array{
  Graph(f) &\to& {*}
  \\
  \downarrow && \downarrow
  \\
  X \times Y
  &\stackrel{\chi_f}{\to}&
  \{0,1\}
}
$$

which identifies $Graph(f) \hookrightarrow X \times Y$ with the subset of pairs $(x,y)$
for which $f(x) = y$. This is the ordinary notion of [[graph of a function]].


## Related concepts

* **graph of a functor**, [[cograph of a functor]]
* [[cograph of a profunctor]]
* [[tabulator]]

[[!redirects graphs of a functor]]
[[!redirects graphs of functors]]
[[!redirects graph of a profunctor]]
[[!redirects graphs of a profunctor]]
[[!redirects graphs of profunctors]]
[[!redirects graph of a distributor]]
[[!redirects graphs of a distributor]]
[[!redirects graphs of distributors]]
