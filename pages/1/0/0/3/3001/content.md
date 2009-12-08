In [[algebraic topology]] one defines and uses [[functor]]s from some category of [[topological space]]s to some category of algebraic objects to help solving some existence of uniqueness problems for spaces or maps. 

There are 4 basic problems of algebaric topology for the existence of maps: extension problem, retraction problem, lifting problem and section problem.

Regarding that these problems make sense in any category we will talk about objects and morphisms and not spaces and maps. 

**Extension problem.** Given morphisms $i:A\to X$, $f:A\to Y$ find the extension of $f$ onto $X$, i.e. a morphism $\tilde{f}:X\to Y$ such that $i\circ\tilde{f}=f$. Notice that if $i:A\hookrightarrow X$ is a subobject, then $i\circ\tilde{f}$ is the restriction $\tilde{f}|A$, and the condition is $\tilde{f}|_A = f$. 

**Retraction problem.** Let $f:A\to Y$ be a morphism. Find $r:Y\to A$ such that $r\circ f = id_A$.

The [[retraction]] problem is a special case of the extension problem for $A=X$ and $i=id_A$. Conversely, the general extension problem may be reduced to a retraction problem:

**Proposition. (Reducing an extension to a retraction.)** If the pushout $Y\coprod_A X$ exists (for $i$, $f$ as above) then the extensions $\tilde{f}$ of $f$ along $i$ are in 1-1 correspondence with the retractions of $i_*(f) : Y\to Y\coprod_A X$. 

**Lifting problem.**
Given morphisms $p:E\to B$ and $g:Z\to B$, a **lifting**  of a map $g$ is a morphism $\tilde{g}:Z\to E$ such that
$p\circ\tilde{g}=g$.

**Section problem.** For any $p:E\to B$ find a section $s: B\to E$, i.e. a morphism $s$ such that $p\circ s = id_B$. 

The section problem is a special case of a lifting problem where $g = id_E : E\to E$. Then the lifting is the section: $\tilde{g} = s$.  A converse is true in the sense

**Proposition. (Reducing a lifting to a section.)** If the pullback $Z\times_B E$ exists then the general liftings for of $G$ along $p$ as above are in a bijection to the section of $g^*(p)=Z\times_B p : Z\times_B E\to Z$. 





