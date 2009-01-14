In a [[category]] with a [[terminal object]], a **pointed object** is an [[object]] $X$ equipped with a [[global element]] $1\to X$.

A pointed object is distinguished from an [[inhabited set|inhabited]] one in that the chosen point is _structure_ rather than a property.  In particular, a morphism of pointed objects is a morphism in the original category which preserves the points.  In other words, the category of pointed objects in $C$ is the [[co-slice category]] $1/C$ under the terminal object.

## Remarks ##

* A category of pointed objects is always a category with a [[zero object]], i.e. with an object which is both a [[terminal object|terminal]] and [[initial object|initial]]: this is the point itself regarded as a pointed object in the unique way. A category with zero object is called a [[pointed category]].

## Examples ##

* Pointed [[topological space|topological spaces]] and [[simplicial set|simplicial sets]] are important in [[homotopy theory]], where they are often called **based**.

* Pointed $n$-[[n-category|categories]] figure prominently in the [[delooping hypothesis]]; see also [[k-tuply monoidal n-category]].

* In a category with a [[zero object]], every object is automatically pointed in a unique way.

## Remarks ##

* If $C$ is a [[monoidal category]] (usually [[cartesian monoidal category|cartesian]]), there is a [[smash product]] of pointed objects which is usually the "correct" notion of product to consider.

* If $C$ is a non-cartesian monoidal category, occasionally one may instead want a "pointed object" to be one equipped with a map $I\to X$, where $I$ is the unit of the monoidal structure.


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
