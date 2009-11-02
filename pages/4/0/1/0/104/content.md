A **homological resolution of a quotient** is a special case of a more general **homological resolution** of an object in a category in which (co)[[chain complex]]es make sense. Typically, one is interested in resolutions of non-free objects by free ones. The ur examples are the Koszul or Koszul--Tate resolutions of an $A$-[[module]] by free $A$-modules or of an $A$-algebra by free $A$-algebras. 

For example, let $A$ be a commutative [[augmented algebra]] over a field $k$ and $I$ an ideal in $A$. Resolve $A/I$ by a free $A$-algebra $R$ with a [[derivation]] differential so that $H(R) = A/I$ is concentrated in degree $0$ and all other homology vanishes. Iff $I$ is a [[regular ideal]], the [[Koszul complex]] will do; if $I$ is not regular, continue the process forming the [[Koszul-Tate resolution]], the algebraic analog of a [[Moore-Postnikov system]], which was indeed Tate's inspiration.

If the original object is itself [[graded object|graded]] or differential graded, the resolution will be bigraded by resolution degree and _internal degree_.

By **homological resolution of a quotient**, one means a _weak quotient_ or _homotopy quotient_ in some $\infty$-categorical [[homotopy theory]] context which is equivalent to a category of (co)chain complexes. This means: a homological resolution of a quotient is a (co)chain complex $C^\bullet$ of abelian groups whose _(co)homology_ $H^\bullet(C^\bullet)$ in some degree, usually in degree 0, is the desired quotient, $H^0(C) = desired quotient$. 
Depending on the situation one may want to demand that the (co)homology in all other degrees vanish, in which case $C^\bullet$ would be [[homotopy theory|weakly equivalent]] to the desired quotient.

+-- {: .query}
_The term 'resolution' is usually reserved for the case in which (co)homology in all other **resolution** degrees vanishes.
(Jim)_
=--

In general, i.e. not restricted to the context of  (co)chain complexes, weak or homotopy quotients are a common theme throughout [[homotopy theory]] and [[higher category theory]]. It underlies for instance the idea of regarding [[Lie groupoid]]s as orbifolds (see [Orbifolds as Groupoids](http://arxiv.org/abs/math.DG/0203100)) and the idea of [[stack|stacky quotients]]. The point of all these weak quotients is usually that the weak quotient in general exists only in a category of [[dichotomy between nice objects and nice categories|nicer objects]] than the true quotient: if a Lie group $G$ acts non-freely on a [[manifold]] $X$, the action groupoid $X//G$ exists as a [[Lie groupoid]], an [[internal category|internal groupoid]] in manifolds, whereas the "true" quotient $X/G$ cannot be equipped with the structure of a manifold anymore.


[[!redirects Homological resolution]]
[[!redirects weak quotient]]
[[!redirects homotopy quotient]]