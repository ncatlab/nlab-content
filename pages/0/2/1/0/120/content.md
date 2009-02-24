In general two objects are considered _equivalent_ if they may be replaced by one another in all contexts under consideration, in particular whenever one is not doing anything [[evil]].

The general theory of equivalence is discussed at [[equivalence relation]], but the real question is the correct definition of equivalence in various situations.

# In higher category theory #

In [[higher category theory]] an **equivalence** often means a morphism which is invertible in a maximally weak sense (that is, up to all higher equivalences).  Two objects are **equivalent** if there is an equivalence between them.  For example:

* In a 1-category, an equivalence is just an [[isomorphism]].

* In a (possibly weak) 2-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cell isomorphisms $f g \cong 1_y$ and $g f \cong 1_x$.  In the 2-category $Cat$ this reduces to the above notion.

* In a (possibly weak) 3-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-2-categories.  In the (weak) 3-category $Bicat$ of [[bicategory|bicategories]], pseudofunctors, pseudonatural transformations, and modifications, such equivalences are often called _biequivalences_, and that term is sometimes also used for an equivalence in any 3-category.

* In an $\infty$-category, an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-$\infty$-categories.  This "definition" is recursive with no base case, so it requires a little work to make rigorous.

# In homotopy theory #

We need [[homotopy equivalence]] and [[weak homotopy equivalence]].