
# Bicategory of maps
* table of contents
{: toc}

## Definition

If $K$ is a [[bicategory]], then a [[morphism]] $f \colon a \to b$ is called a **map** if it has a [[right adjoint]] $f^* \colon b \to a$.

The bicategory $Map K$ is the [[locally full sub-2-category]] of $K$ determined by the maps.


## Examples

In the bicategory [[Rel]] of [[sets]] and [[relations]], a relation is a map if and only if it is the [[graph of a function]].  Consequently, $Map Rel$ is equivalent to [[Set]].

Similarly, if $C$ is a category with finite [[limits]], then there is a bicategory $Span C$ of [[spans]] in $C$.  The bicategory $Map Span C$ is equivalent to $C$.


## Properties

If $K$ is a [[cartesian bicategory]], then $Map K$ has finite $2$-products.

If every map in $K$ is [[comonadic morphism|comonadic]] and $Map K$ has a terminal object, then $Map K$ is equivalent to a $1$-category.

$Map K$ is a [[regular category]] if and only if $K$ is a unitary tabular [[allegory]], equivalently a [[bicategory of relations]] in which every [[coreflexive morphism]] [[split idempotent|splits]].  In that case $Rel Map K \simeq K$.


## References

* Carboni, Walters, _Cartesian bicategories I_, JPAA 49, 1987.
{: #CW87 }

* Lack, Walters, Wood, _Bicategories of spans as cartesian bicategories_, TAC 24(1), 2010.
{: #LWW10 }
