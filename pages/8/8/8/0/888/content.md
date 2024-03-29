
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Euclidean relations
* table of contents
{: toc}

## Definitions

A (binary) [[relation]] $\sim$ on an [[abstract set]] $A$ is __left euclidean__ if every two elements both related to a third are also related to each other:
$$ x, y, z: A,\; x \sim z,\; y \sim z \;\vdash\; x \sim y .$$
A relation $\sim$ is __right euclidean__ if this works in the other order:
$$ x, y, z: A,\; x \sim y,\; x \sim z \;\vdash\; y \sim z .$$
One could also say __euclidean__ and __co-euclidean__ or __op-euclidean__, or similarly.


## Relationship to other kinds of relations

An [[equivalence relation]] is a relation that is both [[reflexive relation|reflexive]] and euclidean in either direction (in which case it\'s euclidean in both directions).  Defining equivalence relations this way (rather than using transitivity and symmetry) is analogous to defining a [[group]] using (one-sided) division instead of multiplication and inverse; both are special cases of an analogous definition of [[groupoid]].  One can also define an equivalence relation as a relation that is both [[entire relation|entire]] and left euclidean (or the reverse); this is analogous to defining a group using division and furthermore merely stating that some element exists rather than that there is an identity element.  (Perhaps more familiarly, one can define a [[subgroup]] of a given group as a subset that is closed under division and has at least one element.)

A _[[circular relation]]_ satisfies
$$ x, y, z: A,\; x \sim y,\; y \sim z \;\vdash\; z \sim x .$$
This is analogous to taking the reciprocal of the product in a group(oid).  Again, a reflexive circular relation is an equivalence relation.


## History

The above (reflexive and euclidean) is the earliest definition of equivalence, dating back (at least) to [[Euclid]]\'s Common Notion 1 (hence the name).  In Heath\'s translation,

>Things \[geometric figures\] which are equal to \[have the same magnitude as\] the same thing are also equal to one another.

It is not clear, however, if Euclid appreciated the distinction between this and transitivity; he may have taken it for granted that equality of magnitude is symmetric, which destroys the distinction.  (One can similarly argue whether Common Notion 4 expresses reflexivity or whether it merely means that [[congruence]] entails [[equality]] of magnitude, with the equivalence-relation nature of congruence again going unstated.  See [this discussion](http://aleph0.clarku.edu/~djoyce/java/elements/bookI/cn.html).)


[[!redirects euclidean relation]]
[[!redirects euclidean relations]]
[[!redirects Euclidean relation]]
[[!redirects Euclidean relations]]

[[!redirects coeuclidean relation]]
[[!redirects coeuclidean relations]]
[[!redirects co-euclidean relation]]
[[!redirects co-euclidean relations]]
[[!redirects coEuclidean relation]]
[[!redirects coEuclidean relations]]
[[!redirects co-Euclidean relation]]
[[!redirects co-Euclidean relations]]
[[!redirects opeuclidean relation]]
[[!redirects opeuclidean relations]]
[[!redirects op-euclidean relation]]
[[!redirects op-euclidean relations]]
[[!redirects opEuclidean relation]]
[[!redirects opEuclidean relations]]
[[!redirects op-Euclidean relation]]
[[!redirects op-Euclidean relations]]

[[!redirects left euclidean relation]]
[[!redirects left euclidean relations]]
[[!redirects left Euclidean relation]]
[[!redirects left Euclidean relations]]
[[!redirects right euclidean relation]]
[[!redirects right euclidean relations]]
[[!redirects right Euclidean relation]]
[[!redirects right Euclidean relations]]
