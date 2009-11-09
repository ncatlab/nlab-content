#Idea# 

In as far as the notion of [[functor]] generalizes that of [[function]]
and that of [[profunctor]] generalizes that of [[relation]], the
notion of _graph_ of a (pro)functor generalizes that of [[graph of a function]].

Just as the [[graph of a function]] $f : X \to Y$, 
or more generally that of a [[relation]] $R \subset X \times Y$
for $X,Y \in Set = 0 Cat$
is nothing but the [[category of elements]] of the corresponding 
characteristic function $\chi_R : X \times Y \to (-1)Cat = \{0,1\}$, so the graph
of a functor $F\colon C \to D$, or more generally that of a [[profunctor]]
$\chi : C^{op} \times D \to 0 Cat = Set$, is nothing but its [[category of elements]].

Generally, the graph of a functor 
$f : C \to D$ between $(n,r)$-[[(n,r)-category|categories]]
is the 
[[Grothendieck construction]] of the corresponding correspondence:
the fibration classified by the correspondence, 
i.e. the [[comma object]]

$$
  \array{
    Graph(f) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    C^{op} \times D &\stackrel{\chi_f}{\to}& (n-1,r-1)Cat
  }
$$

whenever this makes sense. For instance in the context of 
$(\infty,1)$-[[Higher Topos Theory|category theory]] the graph
may be taken to be the fibration classified by $\chi_f : C \times D^{op} \to (\infty,0)$
as described at  [[universal fibration of (∞,1)-categories]].


# Definition #

For $0 \leq n \leq \infty$ let $(n-1) Cat$ and $n Cat$ be a realization of the 
notions of $n$-category of $(n-1)$-categories and of the $(n+1)$-category of $n$-categories,
respectively,
such that standard constructions of [[category theory]] work,
in particular a version of the [[Yoneda lemma]].
See [[higher category theory]]. 

Then with $C,D \in n Cat$ let $f : C \to D$ be a ($n$-)[[functor]].

By the general logic of [[distributor]]s this defines an $n$-correspondence

$$
  \chi_f : C^{op} \times D \stackrel{f^{op} \times Id}{\to} D^{op} 
     \times D \stackrel{Func(-,-)}{\to} (n-1) Cat
$$

The **graph** of $f$ is the fibration $Graph(f) \to C^{op} \times D$ classified
by $\chi_f$.

+--{: .query}
[[Mike Shulman]]: It's not obvious to me that this is the best thing to call the graph of a functor; there are lots of other graphy things one can construct from a functor that all reduce to the usual notion of the graph of a function.  To start with, there is of course also the induced opfibration oven $C\times D^{op}$, would you call that the "opgraph"?  But actually, the two-sided fibration $D \leftarrow P \to C$ (an opfibration over $C$ and a fibration over $D$) looks to me more like a graph.  And then there is of course the *other* profunctor induced by $f$, which gives a fibration over $C\times D^{op}$, an opfibration over $C^{op}\times D$, and a two-sided fibration from $C$ to $D$.
=--


# Examples #

## Graphs of 0-functors ##

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

## Graphs of 1-functors ##

For $f : C \to D$ an ordinary [[functor]], with corresponding [[profunctor]]
$\chi_f : C^{op} \times D \to Set$, the category $Graph(f)$ is the 
[[category of elements]] $\int \chi_f$ of $\chi_f$.

If we regard $C$ and $D$ as [[2-category|2-categories]] under the embedding
$1Cat \hookrightarrow 2Cat$ then the profunctor $\chi_f$ corresponding to 
$f$ is of the form $\chi_f : C^{op} \times D \to Cat$
and in this context $Graph(f) \to C^{op} \times D$ is the 
[[Grothendieck construction]] on $\chi_f$.


#Related concepts#

Closely related is the notion of [[cograph of a functor]].
