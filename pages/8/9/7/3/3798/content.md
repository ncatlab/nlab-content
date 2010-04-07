# Contents
* tic
{: toc}

## Idea

A **vertical transformation** is an analogue of a [[natural transformation]] which goes between [[double functors]] of [[double categories]], and whose components are vertical arrows and squares.  There is a dual notion of **horizontal transformation.


## Definition

If $C$ and $D$ are strict double categories regarded as [[internal categories]] in $Cat$ and $F,G\colon C\to D$ are double functors regarded as internal functors in $Cat$, then a transformation between them is simply an internal natural transformation in $Cat$.  Whether this is a vertical or horizontal transformation depends on how we identify double categories with internal categories in $Cat$ (there being two ways).

More explicitly, a vertical transformation $\alpha\colon F\to G$ consists of

* For every object $c\in C$, a vertical arrow
  $$ \array{ F c \\ \downarrow ^{\alpha_c} \\ G c}$$
  in $D$, which are natural with respect to vertical composition of vertical arrows in $C$.

* For every horizontal arrow $p\colon c_1 \to c_2$ in $C$, a square
  $$\array{F c_1 & \overset{F p}{\to} & F c_2\\
    ^{\alpha_{c_1}}\downarrow & \Downarrow^{\alpha_p}& \downarrow^{\alpha_{c_2}}\\
    G c_1& \underset{G p}{\to} & G c_2}$$
  in $D$, which are natural with respect to vertical composition of squares in $C$.

* For each $c\in C$, if $1_c\colon c\to c$ is its horizontal identity, then the square $\alpha_{1_c}$ is equal to $1_{\alpha_c}$, the identity square on the arrow $\alpha_c$.

* For $p\colon c_1\to c_2$ and $q\colon c_2\to c_3$, the horizontal composite of $\alpha_p$ and $\alpha_q$ is equal to $\alpha_{q p}$.

The notion of horizontal transformation is dual.


## The double category of double functors

Another characterization of transformations between double categories comes from observing that the 1-category $DblCat$ is [[cartesian closed category|cartesian closed]], and so any two double categories have an exponential $D^C$.  The objects of $D^C$ are double functors, its vertical arrows are vertical transformations, and its horizontal arrows are horizontal transformations.  Its squares are a sort of "square modification" relating a pair of vertical and a pair of horizontal transformations.

## Generalizations

It is easy to modify the explicit definition to handle the cases when $C$ and $D$ are weak in one direction or the other, and/or when $F$ and $G$ are pseudo functors in one direction or the other, by composing with appropriate coherence constraints.  In this way, we obtain many [[2-categories]] of double categories.

It is also easy to define *vertical* transformations between double functors which are *horizontally* lax or colax, and dually.  In fact, given double categories $C,D,C',D'$, lax functors $F\colon C\to D$ and $F'\colon C'\to D'$, and colax functors $G\colon C\to C'$ and $G'\colon D\to D'$, we can define a vertical transformation having the shape
$$\array{C & \overset{F}{\to} & D \\
  ^G\downarrow & \Downarrow& \downarrow^{G'}\\
  C'& \underset{F'}{\to} & D'}$$
despite the fact that the composites $G' \circ F $and $F'\circ G$ do not exist as double functors of any sort.  Such transformations are the squares of a large double category $Dbl$ whose objects are double categories, whose horizontal arrows are lax functors, and whose vertical arrows are colax functors.  This, in turn, is a special case of a construction which works for algebras over any [[2-monad]].

Finally, we can also define vertical transformations between functors of (horizontally) [[virtual double categories]].



[[!redirects horizontal transformation]]
[[!redirects vertical transformations]]
[[!redirects horizontal transformations]]
