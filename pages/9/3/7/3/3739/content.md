
# Proper subsets
* table of contents
{: toc}

## Idea

A [[subset]] $A$ of a [[set]] $S$ is __proper__ if it is not the [[improper subset]] of $S$ ($S$ as a subset of itself).  We may also say (in the context of [[concrete sets]]) that $S$ is a proper [[superset]] of $A$ or that $S$ properly [[containment|contains]] $A$.

## Definition

### In material set theory

In [[material set theory]], we may state that $A$ is proper in any of these equivalent ways:

1.  $A$ is not equal (as a subset) to $S$;
2.  There exists an element $x$ of $S$ such that $x \notin A$;
3.  Given any way of expressing $A$ as the [[intersection]] of a [[family of subsets]] of $S$, this family is [[inhabited set|inhabited]]. 

Actually, these three definitions are equivalent only if we accept the principle of [[excluded middle]]; in [[constructive mathematics]], we usually prefer (3).  (For example, consider the notion of [[proper filter]] on a set $X$, thought of as a subset of the [[power set]] of $X$.)  However, (3) is not [[predicative mathematics|predicative]]; see [[positive element]] for discussion of this in the dual context.  Also, (2) may be strengthened using an [[inequality relation]] other than the [[denial inequality]].

### In structural set theory

In [[structural set theory]], subsets are represented by [[injections]], and so we may state that the injection $m:A \hookrightarrow S$ is proper in any of these equivalent ways:

1.  The [[injection]] $m:A \hookrightarrow S$ is not an [[bijection]];
2.  There exists an element $x$ of $S$ such that for all elements $y \in A$, $m(x) \neq y$;
3.  Given any way of expressing $m:A \hookrightarrow S$ as the [[intersection]] of a [[family]] of [[injections]] into $S$, this family is [[inhabited set|inhabited]]. 

Similarly as the case in [[material set theory]], these three definitions are equivalent only if we accept the principle of [[excluded middle]]. 

### More generally

In any category $C$, subsets become [[subobjects]] and are thus represented by the [[monomorphisms]] in $C$. Then a **proper subobject** is defined in any of the following ways:

1.  The [[monomorphism]] $m:A \hookrightarrow S$ is not an [[isomorphism]];
2.  If $C$ is a [[well-pointed category]] with [[terminal object]] $1$, then there exists a global element $x:1 \to S$ such that for all global elements $y:1 \to A$, $m \circ x \neq y$;
2.  If the [[subobject preorder]] of every object in $C$ is a [[preorder|pre]]-[[inflattice]], then given any way of expressing $m:A \hookrightarrow S$ as the [[intersection]] of a [[family]] of [[monomorphisms]] into $S$, this family is [[inhabited set|inhabited]]. 

## See also

* [[subset]], [[proper subset]], [[improper subset]]

* [[subobject]], [[proper subobject]], [[improper subobject]]

* [[filter]], [[proper filter]], [[improper filter]]

[[!redirects proper subset]]
[[!redirects proper subsets]]
[[!redirects proper superset]]
[[!redirects proper superset]]
[[!redirects proper containment]]

[[!redirects proper subobject]]
[[!redirects proper subobjects]]