## Idea

A **monoidal adjunction** is an [[adjunction]] between [[monoidal categories]] which respects the monoidal structure.

## Definition

Actually, since there are several types of [[monoidal functors]] (lax, colax, and strong) there are several types of "adjunctions between monoidal categories which respect the monoidal structure."  Namely, we could have:

* An adjunction in the [[2-category]] $MonCat$ of monoidal categories and strong monoidal functors.  In this case both the left and right adjoint are strong.  We call this a **strong monoidal adjunction**.

* An adjunction in the 2-category $MonCat_\ell$ of monoidal categories and lax monoidal functors.  In this case the right adjoint is lax, while the left adjoint is necessarily strong (by [[doctrinal adjunction]]).  This version, which is one of the most frequently occurring, is often called simply a **monoidal adjunction**.

* The dual: an adjunction in the 2-category $MonCat_c$ of monoidal categories and colax monoidal functors, in which case the left adjoint is colax and the right adjoint is strong.  One might call this an **opmonoidal adjunction**.

* A mixed situation, in which the left adjoint is colax, the right adjoint is lax, and the lax and colax structure maps are [[mates]] under the adjunction.  This is a [[conjunction]] in the [[double category]] of monoidal categories and lax and colax monoidal functors, so we may call it a **monoidal conjunction** or a **lax/colax monoidal adjunction**.  By [[doctrinal adjunction]], given any adjunction between monoidal categories, if the right adjoint is lax monoidal, then the left adjoint automatically acquires a colax monoidal structure making the adjunction into a monoidal conjunction, and dually.

[[!redirects monoidal adjunctions]]
[[!redirects opmonoidal adjunction]]
[[!redirects opmonoidal adjunctions]]
[[!redirects comonoidal adjunction]]
[[!redirects comonoidal adjunctions]]
[[!redirects monoidal conjunction]]
[[!redirects monoidal conjunctions]]

