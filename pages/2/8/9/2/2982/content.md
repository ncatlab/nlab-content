
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

## Terminology

There are many terms used for the associative operad. These include:

* **As**, in [Aguiar & Livernet 2005](#AL05) for the symmetric associative operad and in [Lodey & Vallette 2012](#LV12), [Chenavier, Cordero & Giraudo 2018](#CCG18) for the non-symmetric associative operad. 

* **Ass**, in [Lodey & Vallette 2012](#LV12) for the symmetric associative operad.

* **Assoc**, in [Lurie 2017](#Lurie17). 

**Note:** *Due to confusion with the English language obscenity, the nLab now discourages the usage of the term "Ass" on the nLab itself to refer to the associative operad, instead preferring the alternate terms listed. If you encounter uses of this sort elsewhere on the nLab, please replace them if possible.* 

## Definition

### As a $Vect$-operad

The _associative operad_ $Assoc$ is often taken to be the [[Vect]]-[[operad]] whose [[algebra over an operad|algebras]] are precisely [[associative unital algebras]].

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

* {#AL05} [[Marcelo Aguiar]], [[Muriel Livernet]] *The associative operad and the weak order on the symmetric groups* &lbrack;[arXiv:math/0511698](https://arxiv.org/abs/math/0511698)&rbrack;

* {#LV12} [[Jean-Louis Loday]], [[Bruno Vallette]], *Algebraic Operads*, Grundlehren der mathematischen Wissenschaften, Springer-Verlag Berlin Heidelberg 2012 &lbrack;[doi:10.1007/978-3-642-30362-3](https://doi.org/10.1007/978-3-642-30362-3), [version 0.99 pdf](https://www.math.univ-paris13.fr/~vallette/Operads.pdf)&rbrack;

* {#CCG18} [[Cyrille Chenavier]], [[Christophe Cordero]] and [[Samuele Giraudo]], *Generalizations of the associative operad and convergent rewrite systems*, Higher-Dimensional Rewriting and Algebra, EasyChair Preprint no. 143, 2018 &lbrack;[doi:10.29007/mfnh](https://doi.org/10.29007/mfnh), [arXiv:1808.06181](https://arxiv.org/abs/1808.06181)&rbrack;

In the context of [[higher algebra]] of [[(infinity,1)-operads]], the associative operad is discussed in section 4.1.1 of 

* {#Lurie17} [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects associative operad]]
[[!redirects associative operads]]

[[!redirects symmetric associative operad]]
[[!redirects symmetric associative operads]]

[[!redirects non-symmetric associative operad]]
[[!redirects non-symmetric associative operads]]

[[!redirects Assoc]]
[[!redirects As]]