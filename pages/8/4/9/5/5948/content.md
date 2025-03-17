
# Categories of factorizations
* table of contents
{: toc}

## History

In his monograph on (co-)extensions of monoids, Leech introduced a construction that had also been used for other purposes by MacLane, see [[twisted arrow category]].  A short time later Charles Wells distributed a preprint which made the short trip from monoids to small categories with a fixed set of objects.  This introduced the constructions below but then the subject lay fallow until work by [[Baues]] and Wirshing introduced what is now usually called [[Baues-Wirsching cohomology]].  Compare also [[factorization category]].


## Definition

The following constructions were used by Baues and Wirsching and we will more or less adapt their terminology and notation.

Given a small category $I$, one defines a __category of factorizations__ $FI$ as follows. The objects of $FI$ are the morphisms of $I$. A morphism from $x:i\to j$ to $y : k\to l$ is a commutative square of the form (note the direction of arrows!)
$$\array{
i & \stackrel{v}\longleftarrow & k\\
{x}^{\mathllap{}}\downarrow&&\downarrow{y}^{\mathrlap{}}\\
j &\stackrel{u}\longrightarrow & l
}$$
In other words, it is a pair $(u,v)$ which factorizes $y = u\circ x \circ v$. The composition is defined in the obvious way: $(u',v')\circ (u,v) := (u'\circ u, v\circ v')$. For a morphism $f$ in $I$, one usually denotes $D(f)$ by $D_f$ and uses the abbreviation $D_i = D_{id_i}$ for every object $i$ in $I$. Other conventions include
$u_* = D(u,Id) : D_x\to D_{u x}$ and $v^* = D(Id, v) : D_x\to D_{x v}$. 


## Natural systems

A __natural system__ on $I$ is a functor $D : FI\to Ab$.

The evident notion of a non-Abelian natural system does not behave that well. A lax version (introduced by Wells) handles that case.

Simple examples of natural systems are provided from the consideration of the sequence of functors

$$
FI \stackrel{(i\overset{x}\to j)\mapsto (i,j)}\longrightarrow
I^{op}\times I \stackrel{(i,j)\mapsto j}\longrightarrow I
$$
which implies that any functor $I\to Ab$ and, more generally, any functor $I^{op}\times I\to Ab$ provides (after precomposing with the canonical functor from $FI$) a natural system on $I$.

Natural systems on $I$ are the coefficients of a __Baues-Wirsching cohomology__ of small categories. Namely, the Baues-Wirsching cochain complex $C^*(I,D)$ has 

$$
C^n(I,D) = \prod D_{x_1\cdots x_n}
$$

where the product is over all $i_n\stackrel{x_n}\longrightarrow \ldots \stackrel{x_1}\longrightarrow i_0$.


## References 

(A more extensive list may be found at the entry on [[Baues-Wirsching cohomology]].)
  

* [[H.-J. Baues]], _[[Algebraic Homotopy]]_, Cambridge studies in advanced mathematics  __15__, Camb, Univ. Press 1989.

* [[H.-J. Baues]], G. Wirsching, _Cohomology of small categories_, J. Pure Appl. Alg. __38__ (1985), 187-211.

* T. Pirashvili, _On the center and Baues-Wirsching cohomology_, Georgian Math. J. __16__ (2009) 1, 131-144

* [[C. Wells]], _Extension theories for categories (preliminary report)_ (1979), [available here](
http://www.cwru.edu/artsci/math/wells/pub/pdf/catext.pdf).


[[!redirects category of factorizations]]
[[!redirects category of factorisations]]
[[!redirects categories of factorizations]]
[[!redirects categories of factorisations]]
[[!redirects natural system]]
[[!redirects natural systems]]
