
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##  Idea


The _associative operad_ $Assoc$ is the [[operad]] whose [[algebras over an operad|algebras]] are [[monoid|monoids]]; i.e. objects equipped with an [[associative]] and [[unital]] binary operation.

One might also consider the non-unital version, whose algebras are objects equipped with a binary operation but not with a [[unit]]. 

## Definition

### As a $Vect$-operad

The _associative operad_, denoted $Assoc$ or $Ass$, is often taken to be the [[Vect]]-[[operad]] whose [[algebra over an operad|algebras]] are precisely [[associative unital algebras]].

### As a $Set$-operad

As a [[Set]]-enriched [[planar operad]], $Assoc$ is the operad that has precisely one single $n$-ary operation for each $n$.  Accordingly, $Assoc$ in this sense is the [[terminal object]] in the [[category]] of [[planar operads]].

(Here the unique 0-ary operation is the [[unit]]. Hence the non-unital version of $Assoc$ has a single operation in each positive arity and none in arity 0.)

As a [[Set]]-enriched [[symmetric operad]] $Assoc$ has (the set underlying) the [[symmetric group]] $\Sigma_n$ in each degree, with the [[action]] being the action of $\Sigma_n$ on itself by multiplication from one side.

Similarly, as a _planar_ [[dendroidal set]], $Assoc$ is the [[presheaf]] that assigns the singleton to every [[planar tree]] (hence also the [[terminal object]] in the category of dendroidal sets).

But, by the above, as an [[symmetric operad|symmetric]] [[dendroidal set]], $Assoc$ is not the terminal object.

## Properties

### Resolution

The relative [[Boardman-Vogt resolution]] $W([0,1],I_* \to Assoc)$ of $Assoc$ in [[Top]] is [[Jim Stasheff]]'s version of the [[A-∞ operad]] whose [[algebra over an operad|algebras]] are [[A-∞ algebras]].

### Relation to planar operads

A [[planar operad]] may be identified with a [[symmetric operad]] that is equiped with a map to the associative operad. See at _[[planar operad]]_ for details.

## Related concepts

* **associative operad**

* [[commutative operad]]

* [[Lie operad]]

## References

In the context of [[higher algebra]] of [[(infinity,1)-operads]], the associative operad is discussed in section 4.1.1 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects Assoc]]
