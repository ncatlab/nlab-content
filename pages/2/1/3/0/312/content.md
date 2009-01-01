In category theory, a subobject of an object $c$ of a category $C$ is an isomorphism class of monos $i: a \to c$ into $c$. 

The notion of subobject figures prominently in topos theory and in other approaches to set theory based on categories. Stylistically, it is not an exact translation of the usual notion of "subset" in traditional set theory; in ordinary set theory, the notion of subset is defined in terms of a global elementhood relation between sets, which one doesn't have in categorical set theory (and which one wouldn't necessarily want: it's "[[evil|evil]]" in the sense of not being invariant with respect to isomorphism). 

* Categorically, the traditional notion of subset gives a way of picking out a canonical representative or "normal form" among all the monos in an isomorphism class. As we intimated, there is no intrinsic way of defining such representatives in the theory of toposes: such would have to be considered an extra structure on a topos. Mathematically, there is no particular gain in having such structure around; at best it enables a traditional mode of discourse in which subsets are concrete maps, and to this end it can function as a psychological convenience. 

Equivalently, monos into a particular object $c$ are preordered by the relation 

$$(i: a \to c) \leq (j: b \to c)$$ 

if and only if there exists $k: b \to c$ such that $i = j k$. (There is at most one such $k$ since $j$ is monic, and such $k$ is monic since $i$ is monic.) A subobject of $c$ may be defined as an element of the posetal reflection of the preorder, but as the inclusion and reflection 

$$i: Posets \to Preorders \qquad r: Preorders \to Posets$$ 

form an adjoint equivalence $r \dashv i$, there is no compelling categorical need to prefer posets to preorders, and no compelling reason for a bias toward subobjects over monos, except for the convenience of being able to say "equal" in place of "canonically isomorphic". 
