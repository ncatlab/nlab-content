In [[logic]], the **context** of an assertion (or judgement) consists of all of the assumptions that are made when that assertion to claimed be valid (regardless of whether it is in fact valid).

Generally, contexts will be though of as relative to some underlying logical theory.  This underlying theory will contain most of the assumptions of what constitutes validity; the context of an assertion in this theory will then include only those extra assumptions that may be used by that assertion.

For example, in the theory of a [[group]], it is understood that there is a group $G$, that $G$ has various elements, that two elements of $G$ may be equal, that the product of two elements of $G$ is an element of $G$, and that various axioms are satisfied (which we will not list here).  However, the assertion that $a$ and $b$ commute in $G$ still does not make sense without the additional context that $a$ and $b$ are elements of $G$.  Even in that context, this assertion, while at least meaningful, is not valid.  However, if we add to the context the assumption that $(a b)^2 = a^2 b^2$, then the assertion is valid.  Written symbolically,
$$ \vdash a b = b a$$
is meaningless;
$$ a: G, b: G \vdash a b = b a$$
is meaningful but invalid; and
$$ a: G, b: G, (a b)^2 = a^2 b^2 \vdash a b = b a$$
is valid.

In a sufficiently rich logical language, contexts are unnecessary, which is why contexts are not usually explained in accounts of logic for ordinary reasoning (including in ordinary mathematics).  For example, the two meaningful assertions above may be rewritten thus:
$$ \vdash (\forall a: G): (\forall b: G): a b = b a$$
and
$$ \vdash (\forall a: G): (\forall b: G): (a b)^2 = a^2 b^2 \Rightarrow a b = b a$$
Here the context on the left side is the **empty context**, consisting of no assumptions whatsoever (beyond those underlying the base theory).  However, the previous versions of these assertions work in weaker logics.  In fact, these assertions make sense (and the valid one may be proved) in the [[internal logic]] of a group object in a [[cartesian monoidal category|cartesian]] [[multicategory]].  Accordingly, they can be interpreted (and the valid one is true) as statements about any group object in any cartesian multicategory, exactly as they do for groups (which are group objects in the cartesian multicategory of sets).