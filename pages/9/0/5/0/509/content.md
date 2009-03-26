In a [[category]] $C$ with a [[terminal object]], a **pointed object** is an [[object]] $X$ equipped with a [[global element]] $1\to X$, often called its _basepoint_.

A pointed object is distinguished from an [[inhabited set|inhabited]] one in that the chosen point is _structure_ rather than a property.  In particular, a morphism of pointed objects is a morphism in the original category which preserves the points.  In other words, the category of pointed objects in $C$ is the [[under category|co-slice category]] $1/C$ under the terminal object.

There is an obvious [[forgetful functor]] from $1/C$ to $C$.  If $C$ has finite coproducts, this functor has a left [[adjunction|adjoint]] which takes an object $X$ to the coproduct $1\sqcup X$, equipped with its obvious point.  This is often written $X_+$ and called "$X$ with a disjoint basepoint adjoined."


## Examples ##

* Pointed [[topological space|topological spaces]] and [[simplicial set|simplicial sets]] are important in [[homotopy theory]], where they are often called **based**.

* Pointed $n$-[[n-category|categories]] figure prominently in the [[delooping hypothesis]]; see also [[k-tuply monoidal n-category]].  In particular, a fancy name for a pointed set is a _0-tuply monoidal 0-category_.


## Zero objects and pointed categories ##

The category of pointed objects in any category $C$ with a terminal object always has a [[zero object]], i.e. with an object which is both a [[terminal object|terminal]] and [[initial object|initial]]: this is the point itself regarded as a pointed object in the unique way.  A category with a zero object is sometimes called a [[pointed category]] (not to be confused with a pointed object in [[Cat]]).

Conversely, if $C$ has a zero object, then every object is automatically pointed in a unique way, so that $C$ is equivalent to its category of pointed objects.


## Closed and monoidal structure ##

If $C$ is a [[closed monoidal category]] with finite limits and $X$ and $Y$ are pointed objects in $C$, we can consider their pointed internal-hom (the "object of basepoint-preserving maps"), defined as the pullback
$$
\array{ [X,Y]_* & \rightarrow & 1\\
  \downarrow && \downarrow\\
  [X,Y] & \rightarrow & [1,Y]}
$$
Here the map $[X,Y]\to [1,Y]$ is induced from the point $1\to X$, and the map $1\to [1,Y]$ is [[adjunct]] to $1\otimes 1 \to 1 \to Y$.  We give $[X,Y]_*$ the basepoint induced by the map $1\to [X,Y]$ whose adjunct is $1\otimes X \to 1 \to Y$.  If $C$ also has finite colimits, this pointed-hom has a left adjoint called the [[smash product]], defined to be the pushout
$$
\array{(X\otimes 1) \sqcup (1\otimes Y) & \rightarrow & 1\\
  \downarrow && \downarrow\\
  X\otimes Y & \rightarrow & X\wedge Y}
$$
with the obvious basepoint.  These constructions make $1/C$ itself a closed monoidal category, which is symmetric if $C$ is.  The unit is $I_+$, where $I$ is the unit for the monoidal structure on $C$.

If $C$ is [[monoidal category|monoidal]] but not closed, the same definition of the smash product makes $1/C$ monoidal as long as the tensor product of $C$ preserves finite colimits in each variable separately.  If not, the smash product can fail to be associative; for instance, the smash product on the ordinary category [[Top]] (without any [[nice category of spaces|niceness conditions]] imposed) is not associative.

This construction is almost always applied only when $C$ is [[cartesian monoidal category|cartesian]] monoidal, but this restriction is not necessary.

Moreover, if $C$ is a [[monoidal model category]] with cofibrant unit, then $1/C$ is also a monoidal model category, and the adjunction $1/C \rightleftarrows C$ is [[Quillen adjunction|Quillen]].


#Kernels and cokernels#

For a morphism $f : A \to B$ into an object $B$ equipped with a point $pt \stackrel{pt_B}{\to} B$, its _kernel_ $ker_{pt_B}(f)$ is the pullback

$$
  \array{
     ker_{pt_B}(f) &\to& A
     \\
     \downarrow && \downarrow^f
     \\
     pt
     &\stackrel{pt_B}{\to}&
     B
  }
  \,.
$$

The kernel is itself naturally a pointed object if $A$ is and if $f$ is a morphism of pointed objects.

Similarly, the _cokernel_ of such a morphism is the pushout

$$
  \array{
     A &\stackrel{f}{\to}& B
     \\
     \downarrow && \downarrow
     \\
     pt
     &\stackrel{pt_{coker(f)}}{\to}&
     coker(f)
  }
  \,,
$$
which is always naturally pointed as indicated. 

The notion of kernel in a category with zero morphism is obtained from this in the special case that all objects are assumed to be pointed, so that we are in a [[pointed category]] with zero-morphism $0 : A \to B$ given by 
$A \to pt \stackrel{pt_B}{\to} B$.
