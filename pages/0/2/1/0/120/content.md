#Equivalences of categories#

A functor $F : C \to D$ between categories is said to be an **equivalence** if there is a functor $G : D \to C$ that is a [[weak inverse]] for it, meaning that $F G$ is [[natural isomorphism|naturally isomorphic]] to the identity functor $1_C$, and $G F$ is naturally isomorphic to $1_D$.  Sometimes an _equivalence_ means a pair of functors $F$ and $G$ together with natural isomorphisms $F G\cong 1_C$ and $F G \cong 1_D$.  Any such equivalence can be improved to an **adjoint equivalence** in which these natural isomorphisms satisfy the [[adjunction|triangle identities]].  Two categories $C$ and $D$ are said to be **equivalent** if there is an equivalence between them.

If $F$ is an equivalence, then it is full, faithful, and essentially surjective.  The converse is true assuming a sufficiently strong [[axiom of choice]].  This is not just a question of foundations, since the axiom of choice usually fails in [[internalization|internal contexts]]; one solution is to use [[anafunctor|anafunctors]].  In the absence of enough choice, a functor which is full, faithful, and essentially surjective is sometimes called a **weak equivalence**.

#Equivalences in higher category theory#

More generally, in [[higher category theory]] an **equivalence** often means a morphism which is invertible in a maximally weak sense (that is, up to all higher equivalences).  Two objects are **equivalent** if there is an equivalence between them.  For example:

* In a 1-category, an equivalence is just an [[isomorphism]].
* In a (possibly weak) 2-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cell isomorphisms $f g \cong 1_y$ and $g f \cong 1_x$.  In the 2-category $Cat$ this reduces to the above notion.
* In a (possibly weak) 3-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-2-categories.  In the (weak) 3-category $Bicat$ of [[bicategory|bicategories]], pseudofunctors, pseudonatural transformations, and modifications, such equivalences are often called _biequivalences_, and that term is sometimes also used for an equivalence in any 3-category.
* In an $\infty$-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-$\infty$-categories.  This "definition" is recursive with no base case, so it requires a little work to make rigorous.

One expects that in any $(n+1)$-category of $n$-categories, every equivalence will be essentially $k$-[[k-surjectivity|surjective]] for all $0\le k\le n+1$; this is the $n$-version of "full, faithful, and essentially surjective."  The converse should be true assuming _both_

1. a sufficiently strong axiom of choice, and
1. sufficient weakness of the morphisms.

For example, assuming choice, a strict 2-functor between 2-categories is an equivalence in $Bicat$ if and only if it is essentially surjective on objects (up to equivalence), locally essentially surjective (up to isomorphism), and locally full and faithful. However, its weak inverse may not be a _strict_ 2-functor, so it need not be an equivalence in the 3-category $Str2Cat$ of 2-categories and strict 2-functors.  But using [[homotopy theory|model categories]], $Bicat$ can be recovered from $Str2Cat$ together with the class of all such weak equivalences.
