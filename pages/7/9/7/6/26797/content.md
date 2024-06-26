
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A rectangular [[matrix]] whose entries are in a [[field]], or more generally, in a [[unital ring]], is a __matrix in row echelon form__ if it satisfies the following criteria:

1. all rows whose all entries are $0$ are the consecutive bottom rows;

1. the leftmost nonzero entry ("leading entry") in each row is to the right from each column in which there is a nonzero entry in some row above.

The second condition is equivalent to saying that all the entries in the same column and below the leading entry of any row are zeros.

A matrix in row echelon form is in __reduced row echelon form__ if in addition 

* the leading entries of all nonzero rows equal $1$
* all the other entries in the column of any leading entry of some row are equal to zero (both below and above).

The second condition does not mean that all the entries are $0$ or $1$, as some entries are not leading entries of any row in general (if the matrix is both quadratic and nonsingular then the only possibility is the unit matrix).

#### Terminological remarks

The word *echelon* is a French military term originating from Latin *scala*, *scalae* f. for "ladder".

Being in row echelon form is a property of a matrix, while the terminology suggests that it can be changed (as forms do); this points to useful procedures which involve steps changing matrices (typically row operations) some of which have as an intermediate aim to change ("reduce") a matrix to a matrix in row echelon form. Thus two matrices are related by such an admissible procedure where the latter is in a row echelon form.

Distinguish the notion of a row echelon form from the notion of an [[upper triangular matrix]]: the latter notion is traditionally used for quadratic matrices only and it does not need to be in row echelon form -- as long as the nonzero entries are on or above the diagonal no other ordering conditions are needed to be satisfied; in particular an upper triangular matrix may have zero rows which are not at the bottom.

## Properties

Every matrix over a field (or more generally over a skewfield) can be changed by row operations or, equivalently, by a sequence of multiplications by [[elementary matrices]] from the left.

category: algebra

[[!redirects row echelon matrix]]
[[!redirects row echelon matrices]]
