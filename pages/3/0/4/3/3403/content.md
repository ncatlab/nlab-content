__$Semi Lat$__ is the [[category]] whose [[objects]] are [[semilattices]] and whose [[morphisms]] are semilattice [[homomorphisms]], that is [[functions]] which preserve finitary [[joins]] (equivalently, binary joins and the [[bottom element]]).

We mention joins above as if the objects are join-semilattices; one can just as well consider them meet-semilattices and say that the homomorphisms preserve finitary [[meets]] (including the [[top element]]).  For $Semi Lat$ in itself, this is purely a difference in notational convention.  However, this choice corresponds to using either of two [[inclusion functor]]s representing $Semi Lat$ as a [[subcategory]] of [[Pos]].

There is a forgetful functor from $Semi Lat$ to $Set$, and its left adjoint sends any [[set]] $X$ to the __[[free object|free]] semilattice__ on that set: namely, the __finite [[powerset]]__ $\mathcal{P}_{fin}(X)$ of $X$, i.e. the set of [[finite set|finite]] subsets of $X$, thought of as a join-semilattice.  (Note that this exists even in [[predicative mathematics]], as long as we are allowed to define sets by [[recursion]] over [[natural numbers]], although you have to construct it by general nonsense instead of as a subset of the full powerset.  For purposes of [[constructive mathematics]], by 'finite' we mean [[K-finite set|Kuratowski finite]].)

$Semi Lat$ is given by a finitary [[variety of algebras]], or equivalently by a [[Lawvere theory]], so has all the usual properties of such categories. 


category: category

[[!redirects SemiLat]]
[[!redirects Semi Lat]]
[[!redirects SLat]]
[[!redirects S Lat]]

[[!redirects free semilattice]]
[[!redirects free meet semilattice]]
[[!redirects free meet-semilattice]]
[[!redirects free join semilattice]]
[[!redirects free join-semilattice]]
[[!redirects finite powerset]]
[[!redirects finite power set]]
