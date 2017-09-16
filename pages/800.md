A functor $F : C \to D$ between categories is said to be an **[[equivalence]]** if there is a functor $G : D \to C$ that is a weak inverse for it, meaning that $F G$ is [[natural isomorphism|naturally isomorphic]] to the identity functor $1_C$, and $G F$ is naturally isomorphic to $1_D$.  Sometimes an _equivalence_ means a pair of functors $F$ and $G$ together with natural isomorphisms $F ; G\cong 1_C$ and $F \circ G \cong 1_D$.  Any such equivalence can be improved to an **adjoint equivalence** in which these natural isomorphisms satisfy the [[adjoint functor|triangle identities]].  Two categories $C$ and $D$ are said to be **equivalent** if there is an equivalence between them.

This definition is correct if the [[axiom of choice]] holds; otherwise, you should use weak equivalences or equivalences of anafunctors; see the discussion below.

#Weak equivalences and strong equivalences#

If $F$ is an equivalence of categories, then it is full, faithful, and essentially surjective.  The converse is true assuming a sufficiently strong [[axiom of choice]].  This is not just a question of foundations, since the axiom of choice usually fails in [[internalization|internal contexts]].  In the absence of enough choice, a functor which is full, faithful, and essentially surjective is sometimes called a **weak equivalence**.

However, in contexts without choice it is usually better to use [[anafunctor|anafunctors]] than ordinary functors.  If by $Cat$ we mean the bicategory of categories, anafunctors, and natural transformations, then even without choice, an (ana)functor between categories is an equivalence in $Cat$ (that is, it has a weak inverse anafunctor) iff it is essentially surjective on objects, full, and faithful.  However, its weak inverse may not be a functor, so it need not be an equivalence in the 2-category $StrCat$ of categories, strict (non-ana) functors, and natural transformations.  In the presence of choice, $Cat$ and $StrCat$ are equivalent 2-categories, but without it they are different.  We can regard $Cat$ as obtained from $StrCat$ by "formally inverting" the weak equivalences; see [[weak equivalence]].

Likewise, one expects that in any $(n+1)$-category of $n$-categories, every equivalence will be essentially $k$-[[k-surjective functor|surjective]] for all $0\le k\le n+1$; this is the $n$-version of "full, faithful, and essentially surjective."  The converse should be true assuming both that

* either we have an axiom of choice or we use anafunctors, _and_

* the notion of functor is sufficiently weak.

For example, assuming choice, a strict 2-functor between 2-categories is an equivalence in $Bicat$ if and only if it is essentially surjective on objects (up to equivalence), locally essentially surjective (up to isomorphism), and locally full and faithful. However, its weak inverse may not be a _strict_ 2-functor, so it need not be an equivalence in the 3-category $Str2Cat$ of 2-categories and strict 2-functors.  Again, using [[homotopy theory]], we can recover $Bicat$ from $Str2Cat$ by formally inverting all such weak equivalences.  Analogous facts are expected to be true for higher structures as well.


#Property and structure#

In general, a good rule of thumb is that it is okay to consider either

* a functor with the _property_ of being an equivalence (weak or strong), or

* a pair of functors with the _structure_ of being an _adjoint_ equivalence (that is, a pair of natural isomorphisms $F G \cong 1$ and $1\cong G F$ satisfying the triangle identities),

whereas considering

* a pair of functors with the _structure_ of being a _non-adjoint_ equivalence (that is, merely a pair of natural isomorphisms $F G \cong 1$ and $1\cong G F$).

is fraught with peril.  For instance, the 2-category that is a free-living adjoint equivalence is equivalent to the terminal 2-category, whereas the free-living non-adjoint equivalence is not. Including adjoint equivalences is also the only way to make a higher-categorical structure completely _algebraic_.

+--{+ .query}
[[Zoran Skoda]]: I do not understand the clause
"the 2-category that is a free-living adjoint equivalence is equivalent to the terminal 2-category" at all. 
I have no idea what is a free-living adjoint equivalence, and how a 2-category can be an example of such an equivalence. Or you want to make some sort of 2-cat out of adjoint equivalences ? Please English...

_Toby_:  It means a $2$-category with objects $C$ and $D$, morphisms $f: C \to D$, $g: D \to C$, iso-$2$-cells $\iota: \id_C \to f ; g$ and $\epsilon: g ; f \to id_D$, such that the triangle identities are satisfied, and everything else that is needed to make a $2$-category (the required composites and such).  In other words, it\'s the free $2$-category on the data in an adjoint equivalence.
=--