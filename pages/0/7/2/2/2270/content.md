The concept of internal relation is an [[internalization]] of the concept of a [[relation]] from [[Set]] to more general [[categories]] and it is often called just a __relation__ in the category $C$.

If $C$ is a [[regular category]], then its category of internal binary relations is an [[allegory]]. The objects of an allegory may, but do not need to be, internal relations in some ambient category. 


## Definitions

Let $C$ be a category.  An __internal binary relation__ from an object $X$ to an object $Y$ is an object $R$ and a pair of maps $d_0: R \to X$ and $d_1: R \to Y$ that are _jointly monic_, that is such that, given any object $G$ and morphism $e, e': G \to R$, if $d_0 \circ e = d_0 \circ e'$ and $d_1 \circ e = d_1 \circ e'$, then it must be that $e = e'$.

Now suppose that $C$ has binary [[products]].  Then we can simply the definition; an internal binary relation from $X$ to $Y$ is simply a [[subobject]] $r: R\hookrightarrow X\times Y$. The $d_0$ and $d_1$ above may be recovered as the [[composites]]
$$ d_0 = p_X\circ r : R\hookrightarrow X\times Y\to X,\quad d_1 = p_Y\circ r : T\hookrightarrow X\times Y\to Y ,$$
called the _projections_ of the relation $R$.

A relation from $X$ to $X$ is also said to be an __internal binary relation on $X$__.

As with [[relations]] in general, we can extend from binary to arbitrary internal relations by generalising from the pair $(X,Y)$ to an arbitrary family of objects.  If this family has a [[product]] in $C$, then the internal relation is simply a subobject of that product; in general, the internal relation is given by a jointly monic family of morphisms.


## Kinds of internal relations

The various kinds of relations described at [[relation]] can often be interpreted internally.

For example, an internal relation $R$ on $X$ is said to be __[[reflexive relation|reflexive]]__ if it contains the [[diagonal subobject]] $X\hookrightarrow X\times X$ of $X$; this can even be stated if $X \times X$ does not exist in the category.

An internal [[equivalence relation]] is often called a [[congruence]].